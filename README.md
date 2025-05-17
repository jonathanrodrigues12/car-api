## 📦 Setup do Ambiente (Docker)

Para executar o projeto localmente com Docker, siga os passos abaixo:

### 1. Suba os containers com Docker Compose
Certifique-se de ter o Docker e o Docker Compose instalados:
```bash
docker-compose up -d
```

### 2. Importe o script SQL
Utilize o arquivo [`script.sql`](script.sql) para popular o banco de dados `SLICEIT`, que é criado automaticamente no container `mysql-container`.

> 🔐 A senha do usuário `root` pode ser encontrada no próprio arquivo [`docker-compose.yaml`](docker-compose.yaml).

### 3. Configure a conexão com o banco
Atualize a variável `host` na classe [`conexao.php`](classes/conexao.php) para apontar corretamente para o container MySQL.

---

## 📋 Requisitos do Projeto

O projeto está dividido em **duas etapas principais**, avaliando seus conhecimentos em **PHP (Back-End)** e **HTML/CSS/JavaScript (Front-End)**.

---

## 🚀 Como Iniciar

1. Faça um **fork** deste repositório.
2. Clone o fork na sua máquina:
   ```bash
   git clone https://github.com/<seu-usuario>/estadao-dev-test.git
   ```
3. Crie uma branch com seu nome:
   ```bash
   git checkout -b jonathan-rodrigues
   ```
4. Ao finalizar, envie um **Pull Request** com sua solução.

---

## 🔧 Etapa 1 - Back-End (PHP)

Desenvolver uma **mini API RESTful** para manipular registros de **Carros**.

### Requisitos

- Utilizar arquivos (`.txt`, `.json`) como banco de dados.
- A entidade **Carro** deve conter os campos: `id`, `marca`, `modelo` e `ano`.

### Endpoints sugeridos

| Método | Rota             | Descrição                          |
|--------|------------------|------------------------------------|
| GET    | `/carros`        | Retorna todos os carros            |
| POST   | `/carros`        | Cria um novo carro                 |
| GET    | `/carros/{id}`   | Retorna um carro específico        |
| PUT    | `/carros/{id}`   | Atualiza um carro existente        |
| DELETE | `/carros/{id}`   | Remove um carro existente          |

---

## 💻 Etapa 2 - Front-End (SPA)

Criar uma aplicação **SPA (Single Page Application)** com as seguintes funcionalidades:

### Funcionalidades obrigatórias

- Listar carros cadastrados
- Criar um novo carro
- Editar um carro existente
- Excluir um carro

> **Requisitos adicionais:**
> - A aplicação deve ser responsiva
> - Todas as interações devem ocorrer via **AJAX**, sem recarregar a página
> - O campo `marca` no formulário deve ser um elemento `<select>`

---

## 🐳 Ambiente via Docker

Um ambiente Docker já está pré-configurado neste projeto. Após iniciar os containers, acesse:

```
http://localhost:8080
```

> **Comando para subir apenas o serviço do NGINX (frontend):**
```bash
docker-compose up -d nginx
```

---

## 📝 Observações Finais

- ✅ O projeto **deve rodar via Docker** para ser avaliado.
- 🔧 Alterações no `docker-compose.yaml` são permitidas, desde que o ambiente continue funcional sem configurações manuais adicionais.
- 📁 Você pode reestruturar os arquivos livremente.
- 🧰 É permitido utilizar frameworks no front-end e back-end, desde que o código seja limpo e bem organizado.
- ⚙️ Ferramentas de automação como **Gulp** ou **Grunt** podem ser utilizadas, com instruções claras de uso.
- 🌟 Serão considerados diferenciais:
  - Uso de **JavaScript puro**
  - **Programação orientada a objetos**
  - Aplicação de **design patterns**
  - Presença de **testes automatizados**

---
