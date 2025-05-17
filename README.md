```
README.md
```

```
# Aplicação de Cliente-Servidor TCP para Cálculo de Expressões Matemáticas

## Linguagem Utilizada

Esta aplicação foi desenvolvida em **Python**. Python é uma linguagem de programação de alto nível, interpretada e de fácil aprendizado, amplamente utilizada para desenvolvimento de aplicações de rede, automação, ciência de dados, entre outros.

## Modelo de Comunicação Adotado

O modelo de comunicação utilizado é o **modelo Cliente-Servidor** utilizando sockets TCP/IP.

- **Servidor TCP**: Escuta conexões em um endereço IP e porta específicos, aceita conexões de clientes e processa as solicitações recebidas.
- **Cliente TCP**: Conecta-se ao servidor usando o endereço IP e porta especificados, envia mensagens (comandos ou expressões matemáticas) e recebe respostas do servidor.

Essa comunicação é orientada a conexão, garantindo a entrega confiável dos dados entre cliente e servidor.

## Como Executar e Testar a Aplicação

### Pré-requisitos

- Python 3 instalado na máquina.
- Acesso ao terminal ou prompt de comando.

### Passos para Executar

1. **Salvar o código**

   Salve o código Python fornecido anteriormente em um arquivo chamado, por exemplo, `socket_calc.py`.

2. **Abrir dois terminais**

   Abra duas janelas de terminal ou prompt de comando: uma será usada para executar o servidor, outra para o cliente.

3. **Iniciar o Servidor**

   Na primeira janela de terminal, navegue até o diretório onde está o arquivo `socket_calc.py` e execute:

   ```bash
   python socket_calc.py
```

   ou em sistemas onde o Python 3 é chamado com ```
python3
```

:

```
python3 socket_calc.py
```

   Quando solicitado, digite ```
s
```

 para iniciar o servidor.

1. **Iniciar o Cliente**

   Na segunda janela de terminal, navegue para o mesmo diretório e execute:

   ```
   python socket_calc.py
   
   ```

   ou

   ```
   python3 socket_calc.py
   
   ```

   Quando solicitado, digite ```
   c
   ```

    para iniciar o cliente.
2. **Usar a Aplicação**

   No terminal do cliente, digite comandos para se comunicar com o servidor:
   - Para realizar um cálculo, use o comando ```
     calcular
     ```

      seguido da expressão matemática. Exemplo:

     ```
     calcular 5 + 3 * (2 - 1)
     
     ```
   - Para enviar mensagens simples ao servidor:

     ```
     Olá, servidor!
     
     ```
   - Para encerrar o cliente, digite:

     ```
     sair
     
     ```
3. **Visualizar Resposta**

   Na janela do cliente, a resposta do servidor será exibida logo após o envio da mensagem.

   No terminal do servidor, você verá logs indicando as conexões e mensagens recebidas.

### Observações

- O servidor deve estar sempre ativo antes que o cliente tente se conectar.
- A aplicação realiza a validação básica das expressões matemáticas para evitar execuções inseguras.
- Atualmente, a aplicação suporta operações aritméticas básicas: adição, subtração, multiplicação e divisão, incluindo o uso de parênteses e números decimais.

---

Com esses passos, é possível executar e testar a aplicação cliente-servidor para cálculo de expressões matemáticas via TCP.

```
```
# Aplicação de Cliente-Servidor TCP para Cálculo de Expressões Matemáticas

## Linguagem Utilizada

Esta aplicação foi desenvolvida em **Python**. Python é uma linguagem de programação de alto nível, interpretada e de fácil aprendizado, amplamente utilizada para desenvolvimento de aplicações de rede, automação, ciência de dados, entre outros.

## Modelo de Comunicação Adotado

O modelo de comunicação utilizado é o **modelo Cliente-Servidor** utilizando sockets TCP/IP.

- **Servidor TCP**: Escuta conexões em um endereço IP e porta específicos, aceita conexões de clientes e processa as solicitações recebidas.
- **Cliente TCP**: Conecta-se ao servidor usando o endereço IP e porta especificados, envia mensagens (comandos ou expressões matemáticas) e recebe respostas do servidor.

Essa comunicação é orientada a conexão, garantindo a entrega confiável dos dados entre cliente e servidor.

## Como Executar e Testar a Aplicação

### Pré-requisitos

- Python 3 instalado na máquina.
- Acesso ao terminal ou prompt de comando.

### Passos para Executar

1. **Salvar o código**

   Salve o código Python fornecido anteriormente em um arquivo chamado, por exemplo, `socket_calc.py`.

2. **Abrir dois terminais**

   Abra duas janelas de terminal ou prompt de comando: uma será usada para executar o servidor, outra para o cliente.

3. **Iniciar o Servidor**

   Na primeira janela de terminal, navegue até o diretório onde está o arquivo `socket_calc.py` e execute:

   ```bash
   python socket_calc.py
ou em sistemas onde o Python 3 é chamado com python3:

festança
Correr
Copiar código
python3 socket_calc.py
Quando solicitado, digite spara iniciar o servidor.

Iniciar o Cliente

Na segunda janela do terminal, navegue para o mesmo diretório e execute:

festança
Correr
Copiar código
python socket_calc.py
ou

festança
Correr
Copiar código
python3 socket_calc.py
Quando solicitado, digite cpara iniciar o cliente.

Usar o aplicativo

No terminal do cliente, digite comandos para se comunicar com o servidor:

Para realizar um cálculo, use o comando calcularseguido da expressão matemática. Exemplo:

Correr
Copiar código
calcular 5 + 3 * (2 - 1)
Para enviar mensagens simples ao servidor:

Correr
Copiar código
Olá, servidor!
Para encerrar o cliente, digite:

Correr
Copiar código
sair
Visualizar Resposta

Na janela do cliente, a resposta do servidor será exibida logo após o envio da mensagem.

No terminal do servidor, você verá logs decrescentes nas conexões e mensagens recebidas.

Observações
O servidor deve estar sempre ativo antes que o cliente tente se conectar.
A aplicação realiza a validação básica das expressões matemáticas para evitar execuções inseguras.
Atualmente, o aplicativo suporta operações aritméticas básicas: adição, subtração, multiplicação e divisão, incluindo o uso de parênteses e números decimais.
Com esses passos, é possível executar e testar um aplicativo cliente-servidor para cálculo de expressões matemáticas via TCP.
