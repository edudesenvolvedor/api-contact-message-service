# Microserviço API Contact Message Service

## Descrição

Este microserviço é responsável por gerenciar as mensagens de contato recebidas de diversos websites. Ele fornece uma interface para receber, armazenar e potencialmente processar as informações de contato enviadas pelos usuários através dos formulários de contato dos sites.

## Funcionalidades Principais

* **Recebimento de Mensagens:** Endpoint para receber mensagens de contato de diferentes websites.
* **Validação de Dados:** Validação básica dos campos da mensagem de contato (e.g., nome, email, mensagem).
* **Armazenamento de Mensagens:** Persistência das mensagens de contato em um banco de dados.
* **Identificação da Origem:** Mecanismo para identificar de qual website a mensagem foi enviada.
* **Possíveis Extensões:**
    * Integração com sistemas de notificação (e.g., envio de e-mails para administradores).
    * Implementação de filtros de spam.
    * Análise das mensagens de contato.

## Tecnologias Utilizadas

* NodeJs
* NextJs
* Sqlite
* Docker

## Configuração e Execução

Siga as instruções abaixo para configurar e executar o microserviço em seu ambiente local.

### Pré-requisitos

* NodeJs v20.18

### Passos para Execução

1.  **Clonar o Repositório:**
    ```bash
    git clone [https://github.com/dolthub/dolt](https://github.com/dolthub/dolt)
    cd contact-message-service
    ```

2.  **Configurar as Variáveis de Ambiente:**
    * Crie um arquivo `.env` na raiz do projeto (se aplicável).
    * Defina as variáveis de ambiente necessárias para a conexão com o banco de dados, configurações de API, etc.
        ```
        DATABASE_URL=...
        API_KEY=...
        # Outras variáveis conforme necessário
        ```

3.  **Instalar as Dependências:**
    * Se estiver usando Python:
        ```bash
        pip install -r requirements.txt
        ```
    * Se estiver usando Node.js:
        ```bash
        npm install
        # ou
        yarn install
        ```
    * [Adicionar instruções para outras linguagens/frameworks]

4.  **Configurar o Banco de Dados:**
    * Crie o banco de dados conforme especificado na configuração.
    * Execute as migrações necessárias para criar as tabelas (se aplicável).
        ```bash
        # Exemplo para Flask/SQLAlchemy
        flask db upgrade
        ```

5.  **Executar o Microserviço:**
    * Se estiver usando Python/Flask:
        ```bash
        python app.py
        ```
    * Se estiver usando Node.js/Express.js:
        ```bash
        npm run dev # ou npm start
        # ou
        yarn dev # ou yarn start
        ```
    * [Adicionar instruções para outras linguagens/frameworks]

6.  **Executar com Docker (Opcional):**
    * Certifique-se de ter o Docker e o Docker Compose instalados.
    * Construa a imagem Docker:
        ```bash
        docker build -t contact-message-service .
        ```
    * Execute o container Docker:
        ```bash
        docker run -p [porta_local]:[porta_do_container] contact-message-service
        ```
    * Ou utilize o Docker Compose (se configurado):
        ```bash
        docker-compose up -d
        ```
