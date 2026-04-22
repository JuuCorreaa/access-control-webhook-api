# 🚪 Access Control Integration API (Webhook)

API backend desenvolvida para integrar dispositivos de controle de acesso (catracas, biometria, etc) com sistemas web, recebendo eventos em tempo real via webhook.

> Exemplo de integração com dispositivos de mercado como Intelbras.

---

## 🚀 Objetivo

Permitir que eventos físicos (entrada/saída de pessoas) sejam capturados e processados em tempo real dentro de uma aplicação.

---

## ⚙️ Tecnologias utilizadas

- Node.js
- Express
- PostgreSQL
- Docker
- Webhooks
- REST API

---

## 🔄 Como funciona

1. O dispositivo de controle de acesso envia um evento via webhook
2. A API recebe esse evento
3. Os dados são processados
4. O sistema registra presença/acesso
5. Logs são armazenados para auditoria

---

## 📡 Exemplo de evento recebido

```json
{
  "device_id": "catraca_01",
  "user_id": "123",
  "event": "access_granted",
  "timestamp": "2026-04-22T10:00:00Z"
}
```

---

## 📌 Rotas principais

### POST /webhook/access

Recebe eventos de dispositivos de controle de acesso.

---

## 🔐 Segurança

- Autenticação via token
- Validação de payload
- Proteção contra requisições inválidas

---

## 🧠 Destaques técnicos

- Processamento de eventos em tempo real
- Arquitetura preparada para alta escala
- Separação de camadas (controller, service, repository)
- Estrutura pronta para integração com múltiplos dispositivos

---

## 🛠️ Como rodar o projeto

```bash
# Clonar repositório
git clone https://github.com/seu-usuario/access-control-webhook-api.git

# Instalar dependências
npm install

# Rodar servidor
npm run dev
```

---

## 📁 Estrutura do projeto

```
src/
  controllers/
  services/
  routes/
  database/
  middlewares/
```

---

## 📄 Observações

Este projeto é uma versão demonstrativa para fins de portfólio, com dados simulados e sem conexão com ambientes produtivos.

---

## 👨‍💻 Autor

Desenvolvido como projeto de integração entre hardware e software para sistemas de gestão.
