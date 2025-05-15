# Cliente👱🏻‍♂️---Servidor💻
# Aplicação de Cliente-Servidor TCP para Cálculo de Expressões Matemáticas
----------------------------------------------------------------------------------------------------------------
Grupo : Marcos ,João Marcos , Jaime Werick , Tedy Monteiro 
----------------------------------------------------------------------------------------------------------------

import socket
import re

# Configurações do Servidor
HOST = '127.0.0.1'
PORT = 12345

def calcular(expressao):
    try:
        expressao = expressao.replace(" ", "")
        if not re.match(r'^[\d\+\-\*/\(\)\.]+$', expressao):
            raise ValueError("Expressão inválida: Caracteres não permitidos.")
        resultado = eval(expressao)
        return resultado
    except ZeroDivisionError:
        raise ValueError("Erro: Divisão por zero.")
    except Exception as e:
        raise ValueError(f"Expressão inválida: {e}")

def iniciar_servidor():
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
        s.bind((HOST, PORT))
        s.listen()
        print(f"Servidor ouvindo em {HOST}:{PORT}")

        while True:
            conn, addr = s.accept()
            with conn:
                print(f"Conectado por {addr}")
                while True:
                    try:
                        data = conn.recv(1024)
                        if not data:
                            print("Cliente desconectado.")
                            break
                        mensagem = data.decode('utf-8')
                        print(f"Recebido de {addr}: {mensagem}")

                        # Processa a mensagem
                        msg_lower = mensagem.strip().lower()
                        if msg_lower.startswith("calcular "):
                            expressao = mensagem[len("calcular "):].strip()  # Extrai a expressão
                            try:
                                resultado = calcular(expressao)
                                resposta = f"Resultado: {resultado}".encode('utf-8')
                            except ValueError as e:
                                resposta = f"Erro: {e}".encode('utf-8')
                        else:
                            resposta = f"Mensagem recebida: {mensagem}".encode('utf-8')

                        # Envia a resposta de volta para o cliente
                        conn.sendall(resposta)
                    except ConnectionResetError:
                        print(f"Conexão com {addr} foi resetada.")
                        break
                    except Exception as e:
                        print(f"Erro ao lidar com a conexão: {e}")
                        break

def iniciar_cliente():
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
        s.connect((HOST, PORT))
        print(f"Conectado ao servidor em {HOST}:{PORT}")

        while True:
            mensagem = input("Digite sua mensagem (ou 'calcular <expressão>', ou 'sair'): ")
            if mensagem.lower() == 'sair':
                break
            s.sendall(mensagem.encode('utf-8'))
            data = s.recv(1024)
            resposta = data.decode('utf-8')
            print(f"Recebido do servidor: {resposta}")

if __name__ == "__main__":
    while True:
        escolha = input("Deseja iniciar o servidor (s) ou o cliente (c)? ").lower()
        if escolha == 's':
            iniciar_servidor()
            break
        elif escolha == 'c':
            iniciar_cliente()
            break
        else:
            print("Opção inválida. Por favor, digite 's' ou 'c'.")
