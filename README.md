# 🚗 Mini API de Carros

**Autor:** Jonathan Rodrigues

## 📘 Visão Geral

Este projeto é uma aplicação web simples desenvolvida em PHP que oferece uma API para gerenciamento de carros, permitindo operações de criação, leitura, atualização e exclusão (CRUD). A aplicação também inclui uma interface front-end para interação com a API.

## 🚀 Funcionalidades

- **API RESTful** para gerenciamento de carros:
  - Criar, listar, atualizar e deletar registros de carros.
- **Interface Web** para interação com a API:
  - Formulário para adicionar novos carros.
  - Listagem de carros existentes.
  - Opções para editar e remover carros.
- **Persistência de dados** utilizando MySQL.

## 🛠️ Requisitos

- PHP 7.4 ou superior
- Composer
- MySQL
- Docker e Docker Compose (opcional, para ambiente containerizado)

## 📦 Instalação

### 1. Clonar o repositório

```bash
git clone https://github.com/jonathanrodrigues12/mini-api-carro.git
cd mini-api-carro
```

### 2. Configurar o ambiente

#### Opção 1: Utilizando Docker

- Certifique-se de que o Docker e o Docker Compose estão instalados em sua máquina.
- Execute o seguinte comando para iniciar os containers:

```bash
docker-compose up -d
```

- O serviço estará disponível em `http://localhost:8080`.

#### Opção 2: Ambiente local

- Configure um servidor web (Apache, Nginx, etc.) apontando para o diretório do projeto.
- Crie um banco de dados MySQL chamado `SLICEIT`.
- Importe o arquivo `script.sql` localizado na raiz do projeto para o banco de dados.
- Atualize as configurações de conexão com o banco de dados no arquivo `classes/conexao.php`.

### 3. Instalar dependências PHP

Se estiver utilizando o Composer, execute:

```bash
composer install
```

## 🧪 Uso

- Acesse a interface web em `http://localhost:8080` (ou conforme configurado).
- Utilize os formulários disponíveis para adicionar, editar ou remover carros.
- A API também pode ser acessada diretamente via endpoints HTTP:

  - `GET /api.php?acao=listar` - Lista todos os carros.
  - `POST /api.php?acao=criar` - Cria um novo carro.
  - `PUT /api.php?acao=atualizar&id={id}` - Atualiza um carro existente.
  - `DELETE /api.php?acao=deletar&id={id}` - Remove um carro.

## 📝 Observações

- Certifique-se de que as extensões necessárias do PHP estão habilitadas (por exemplo, `pdo_mysql`).
- As credenciais do banco de dados e outras configurações podem ser ajustadas conforme necessário nos arquivos de configuração.

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests com melhorias e correções.

## 📄 Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).
