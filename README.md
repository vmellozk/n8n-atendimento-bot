# 🤖 Chatbot com n8n + Docker

Este projeto é uma automação de chatbot desenvolvida com [n8n](https://n8n.io), usando uma stack leve com Docker. A automação permite capturar dados via Webhook, armazená-los em planilhas do Google, realizar operações com IA (Groq + ferramentas auxiliares), e fazer requisições HTTP com base nas respostas da IA.

---

## 📦 Tecnologias utilizadas

- [n8n](https://n8n.io) - Plataforma de automação low-code  
- Docker e Docker Compose  
- Google Sheets API  
- Groq Chat Model (Open Source LLM)  
- Webhooks  
- HTTP Request  
- AI Agent + Tools (Memory, Calculator, Wikipedia)

---

## 🧠 Funcionalidade do Workflow

O fluxo faz o seguinte:

1. Recebe dados via `Webhook`
2. Avalia condição com `If`
3. Edita campos (normaliza ou estrutura os dados)
4. Armazena os dados em uma planilha do Google Sheets
5. Usa um modelo de IA para gerar resposta (via Groq Chat)
6. Envia os dados para uma API externa com `HTTP Request`
7. Finaliza com uma operação nula (para controle de fim do fluxo)

---

## 🐳 Rodando o projeto com Docker

### 1. Clone este repositório

```bash
git clone https://github.com/seu-usuario/chatbot-n8n-docker.git
cd chatbot-n8n-docker
```

### 2. Crie a estrutura de pastas

```bash
mkdir n8n_data
```

### 3. Suba o ambiente

```bash
docker compose up -d
```

### 4. Acesse a interface Web do n8n

```text
http://localhost:{porta-que-usou}
(ou coloca o domínio correto para produção)
```

## 🧾 Banco de Dados

Para esse projeto simples de chatbot, não é necessário banco de dados externo, pois o próprio n8n salva os dados do workflow e da memória em disco.

Se futuramente quiser:

- Registrar estatísticas (vendas, faturamento, produto mais vendido)
- Criar painéis

... então um banco de dados (como PostgreSQL ou SQLite) pode ser incluído facilmente.

---

## 🚀 Possíveis expansões

- Conectar com APIs de pedidos (ex: Anota AI, Consumer, etc.)
- Enviar mensagens automáticas por WhatsApp ou Telegram
- Imprimir pedidos diretamente via comando remoto
- Armazenar interações com clientes
- Criar dashboards com ferramentas externas (Grafana, Metabase)

---

## 💡 Observações

- Você pode exportar seus fluxos do n8n Cloud e importar nesta instância local.
- Ideal para rodar em VPS ou servidor com Docker.
- Pode ser usado para cada cliente em um container separado.

---

## 📄 Licença

Este projeto é livre para uso pessoal e comercial.  
Sem licença específica por enquanto.

---

Caso tenha dúvidas ou queira colaborar, fique à vontade para abrir issues ou pull requests!
