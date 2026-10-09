# Golang HTTP Service & DevOps Environment

Serviço em Golang utilizando o framework **Gin Gonic** e **Docker / Docker Compose** para aplicar conceitos e ferramentas da cultura DevOps. O projeto foca em conteinerização, isolamento de ambiente e automação de processos de entrega de software.

> 🇺🇸 **English Version Available:** Service in Golang using Gin Gonic framework and Docker/Docker Compose to apply DevOps Culture concepts and tools. You can check [ENGLISH-README.md](./ENGLISH-README.md) for instructions in English.

---

## 📌 Informações Gerais

- **Título:** HTTP Server em Golang/Gin Gonic
- **Versão:** 1.0.0
- **Host Local:** `http://localhost:80`
- **Tecnologias:** Go (Golang), Gin Gonic, Docker, Docker Compose, Linux, Git

---

## 🚀 Status do Projeto & Roadmap

- [x] **Fase 1: Aplicação & Conteinerização**
  - Servidor HTTP e rotas em Go com Gin Gonic.
  - Conteinerização da aplicação via `Dockerfile`.
  - Orquestração de ambiente local com `docker-compose` na porta 80.
  - Retorno de payload JSON com dados da requisição e horário do servidor.
- [ ] **Fase 2: Observabilidade & Métricas**
  - Integração de middleware para exposição de métricas do Prometheus (`/metrics`).
  - Coleta de métricas e exibição via dashboards no Grafana.
- [ ] **Fase 3: Automação & Provisionamento**
  - Criação de playbooks do **Ansible** para automação de setup e deploy no host.

---

## 💻 Pré-requisitos

Antes de iniciar, certifique-se de ter as seguintes ferramentas instaladas no seu ambiente:

* [Go](https://go.dev/doc/install) *(v1.20+)* — Linguagem de programação para execução e compilação local (opcional se utilizar apenas Docker).
* [Docker](https://docs.docker.com/get-started/get-docker/) & [Docker Compose](https://docs.docker.com/compose/) — Necessários para a execução e orquestração do container em ambiente isolado.

---

## ⚙️ Instalação e Execução

Siga os passos abaixo para subir a aplicação localmente:

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/GuilhermeAlmeidadaLuz/golang-devops-lab.git
   ```

2. Acesse o diretório do projeto:

    ```bash
    cd golang-devops-lab
    ```

3. Suba os containers com Docker Compose:

    ```bash
    docker compose up --build
    # O comando faz o build da imagem, resolve as dependências e inicia o servidor HTTP exposto na porta 80.
    ```

## 🧪 Testando a Aplicação
Com os containers ativos, você pode validar o funcionamento do endpoint das seguintes formas:

1. Via cURL (Terminal)
    ```bash
    curl http://localhost:80/projeto-korp
    ```
2. Via Navegador
    Acesse a URL: http://localhost:80/projeto-korp

📝 Resultado Esperado
```JSON
    {
      "nome": "Projeto Korp",
      "horario": "2026-10-09T16:36:10Z"
    }
```
