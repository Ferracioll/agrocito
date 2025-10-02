# AGROCITRO - Sistema de Gestão Agrícola

## SOBRE O PROJETO

Este é o Projeto Agrocitro, um sistema de gestão focado na agricultura de citros e outros alimentos. Nosso objetivo é simplificar a vida do produtor rural através do armazenamento e gerenciamento digital de informações vitais, como:

* **Registro de Plantio:** Armazenamento de dados sobre a variedade, quantidade, data e localização das mudas de laranja e outros alimentos.
* **Agendamento de Irrigação:** Permite agendar irrigações com base em dados do plantio (supondo que no futuro sejam baseados em monitoramento do solo/previsões meteorológicas).
* **Registro de Colheita:** Os agricultores podem registrar dados como data, quantidade colhida e qualidade do produto.

## INSTRUÇÕES DE CONFIGURAÇÃO E EXECUÇÃO

### 1. Pré-requisitos

Para rodar este projeto, você precisa ter:

* **Node.js** e **npm**.
* **Servidor MySQL** instalado e rodando(O serviço do MySQL deve estar ativo, por exemplo, no painel do XAMPP ou WAMP, antes de seguir para a etapa 4).

### 2. Instalação de Dependências

Acesse a pasta do projeto pelo terminal e instale as dependências necessárias, incluindo o `dotenv` para variáveis de ambiente e o `nodemon` para desenvolvimento:

```bash

# Inicializa o projeto Node.js (se ainda não o fez)
npm init 

# Instala as dependências principais (Express, MySQL2, dotenv)
npm install express mysql2 dotenv

# Instala o Nodemon (recomendado para desenvolvimento)
npm install nodemon --save-dev
```


### 3. Banco de Dados

Instrução: Importe o arquivo SQL (.sql isolado) para o seu servidor MySQL. Certifique-se de que o nome do banco de dados criado corresponda ao valor definido em DB_DATABASE no arquivo .env.

Crie um arquivo na raiz, chamado *.env*, na raiz do projeto e com as seguintes credenciais de conexão:
  ```bash
DB_HOST=localhost
DB_USER=seu_usuario_mysql
DB_PASSWORD=sua_senha_mysql
DB_DATABASE=nome_do_seu_banco_agrocitro
API_PORT=3000
```

### 4. Inicialização do Servidor

Execute esse comando somente após o MySql estar ativo
```bash
npm run dev
```
Ou 
```bash
npm start
```

### 5. Acesso ao FrontEnd

Para acessar o FRONTEND é necessario abrir o arquivo *index.html*(Ou use a extensão Live Server)

OBSERVAÇÕES:

  - É necessario observar se o nome das suas variaveis do banco de dados se relaciona com as descritas no seu codigo - mais precisamente no Javascript.
  - Reinício do Servidor: O comando npm run dev reinicia o servidor automaticamente após mudanças no código. Se estiver usando npm start, é necessário fechar (Ctrl+C) e abrir de novo a cada alteração.

  INTEGRANTES:

  - Pedro Henrique Ferracioli Marques
  - Eric Fernando Ferreira Rodrigues
  - Matheus Garcia de Oliveira
  - Maria Isabella Silva Machado
