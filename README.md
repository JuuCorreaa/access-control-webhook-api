# 🚪 Access Control Integration API (Webhook)

Production-ready API for real-time access control integration via webhook.

> Example integration with access control devices (e.g. Intelbras).

---

## 🚀 Objective

Allow physical events (people entering/leaving) to be captured and processed in real time within a system.

---

## ⚙️ Technologies

- Node.js
- Express
- PostgreSQL
- Docker
- REST API
- Webhooks

---

## 🔄 How it works

1. Access control device sends an event  
2. API receives the webhook  
3. Payload is validated  
4. Event is processed  
5. Data is stored  
6. System updates presence/access  

---

## 📡 Example payload

```json
{
  "device_id": "turnstile_01",
  "user_id": "123",
  "event": "access_granted",
  "timestamp": "2026-04-22T10:00:00Z"
}
📌 Main route
POST /webhook/access

Receives access control events.

🔐 Security
Token-based authentication
Payload validation
Protection against invalid requests
🔄 Event Flow

Device → Webhook → API → Processing → Database → Application

Device sends access event
API receives webhook
Payload is validated
Event is processed
Data is stored
System updates user access/presence
⚡ Real-world scenario

This API simulates real-world integration between physical access control hardware and digital systems, commonly used in:

Schools
Companies
Events
Smart buildings
🧠 Technical highlights
Real-time event processing
Scalable architecture
Clean code structure (controller, service, repository)
Ready for integration with multiple devices
🛠️ Run locally
git clone https://github.com/seu-usuario/access-control-webhook-api.git
cd access-control-webhook-api
npm install
npm run dev
📁 Project structure
src/
  controllers/
  services/
  routes/
  database/
  middlewares/
