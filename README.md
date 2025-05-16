# NodeBB com Docker

Este projeto configura o **NodeBB** com **Redis** e **MongoDB** usando Docker e Docker Compose para facilitar o desenvolvimento e a implantação.

---

## 🚩 Pré-requisitos

- [Docker](https://docs.docker.com/get-docker/) (versão 20+ recomendada)
- [Docker Compose](https://docs.docker.com/compose/install/)
- Bash Shell (Linux/macOS ou Git Bash no Windows)

---

## 🚀 Como iniciar

1. Clone este repositório:

```bash
git clone https://github.com/byBiel/nodebb-docker
cd nodebb-docker 
```
2. Configure as variáveis de ambiente:
Copie o arquivo .env.example para .env e ajuste os valores conforme sua necessidade:

```bash
cp .env.example .env
```

3. Suba os containers:

```bash
docker-compose up -d
```


## ⚙️ Configuração Inicial do Fórum NodeBB

Após subir os containers e acessar o fórum pela primeira vez, siga estes passos para configurar o NodeBB:

1. Acesse o fórum no navegador:


[http://localhost:4567](http://localhost:4567)


2. Crie o usuário administrador:

- Preencha nome, email e senha para o usuário admin do fórum.

3. Configure o banco de dados MongoDB:

| Campo           | Valor            |
|-----------------|------------------|
| Host            | `mongodb`        |
| Porta           | `27017`          |
| Nome do banco   | `nodebb`         |
| Usuário         | (definido no `.env`) |
| Senha           | (definida no `.env`) |

> O hostname `mongodb` funciona pois o Docker Compose cria uma rede interna.

4. Configure o Redis para cache e sessões:

| Campo | Valor       |
|-------|-------------|
| Host  | `redis`     |
| Porta | `6379`      |

5. Finalize a configuração e aguarde o NodeBB preparar o banco.

6. Faça login com o usuário administrador criado e configure o fórum pelo painel administrativo.
