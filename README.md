## MCP para envio de e-mail

Ambiente Docker para automação de envio de e-mails com n8n, PostgreSQL e pgAdmin, integrável ao ecossistema MCP para disparos de e-mail.

### Stack

- n8n
- PostgreSQL
- pgAdmin
- MCP (Send Email)

### Requisitos

- Docker e Docker Compose

### Primeiros passos

1. Copie `.env-example` para `.env`.

2. Suba os serviços

```bash
docker compose up -d
```

3. Verifique

```bash
docker compose ps
```

### Acesso aos serviços

- n8n: http://localhost:<porta_n8n>
- pgAdmin: http://localhost:<porta_pgadmin>
- PostgreSQL: localhost:<porta_postgres>

Portas e credenciais em `docker-compose.yml` e `.env`.

### Persistência

- `data/n8n/`
- `data/postgres/`
- `data/pgadmin/`

### Uso via MCP no Cursor

- Configure um servidor MCP de envio de e-mail.
- Dispare a ferramenta com os parâmetros necessários.

### Estrutura

```text
mcp_envio-de-email/
  data/
    n8n/
    pgadmin/
    postgres/
  docker-compose.yml
  .env-example
  LICENSE
```

### Licença

Veja `LICENSE`.

### Autor

Robson Rodrigues
