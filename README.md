# Kimberly-Sales-Agent

An AI-powered WhatsApp sales automation agent built with **n8n**, **Google Gemini**, **WhatsApp Cloud API**, **Google Sheets**, and **ElevenLabs**.

Kimberly Sales Agent automates customer conversations, product recommendations, delivery calculations, payment processing, payment verification, and order registration—allowing businesses to sell products directly through WhatsApp without manual intervention.

---

## 🚀 Features

### AI Sales Assistant
- Intelligent customer conversations
- Product recommendations
- Sales qualification
- Product information retrieval
- Order processing

### WhatsApp Automation
- Receive WhatsApp messages
- Automated customer responses
- Text and voice support
- Real-time engagement

### Voice AI
- Speech-to-Text transcription
- Text-to-Speech responses
- Voice note conversations

### Product Management
- Product database integration
- Dynamic price retrieval
- Inventory-aware responses

### Delivery Calculation
- Delivery fee lookup
- Location-based shipping estimates
- Automated cost calculations

### Payment Processing
- Payment link generation
- Payment verification
- Payment status validation

### Order Management
- Customer registration
- Automated order recording
- Sales tracking
- CRM-style data collection

### Memory & Context
- Conversation memory
- Context-aware responses
- Multi-step customer interactions

---

## 🏗️ System Architecture

```text
Customer (WhatsApp)
        │
        ▼
WhatsApp Trigger
        │
        ▼
Message Type Router
        │
 ┌──────┴──────┐
 │             │
 ▼             ▼
Text        Voice Note
 │             │
 │      Speech-to-Text
 │             │
 └──────┬──────┘
        ▼
   AI Sales Agent
        │
        ▼
 Product Database
        │
        ▼
Delivery Calculator
        │
        ▼
 Payment Generator
        │
        ▼
Payment Verification
        │
        ▼
 Order Registration
        │
        ▼
 WhatsApp Response
```

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|------------|
| Automation | n8n |
| AI Model | Google Gemini |
| Voice AI | ElevenLabs |
| Messaging | WhatsApp Cloud API |
| Database | Google Sheets |
| Memory | n8n Memory Buffer |
| Payments | Payment Workflow |
| Hosting | Railway / Render / VPS |

---

## 📋 Workflow Overview

### Product Inquiry

1. Customer sends a message.
2. AI identifies customer intent.
3. Product information is retrieved.
4. AI provides recommendations.

### Order Processing

1. Customer selects product(s).
2. AI calculates total amount.
3. Delivery fee is determined.
4. Payment link is generated.
5. Payment is verified.
6. Order is registered automatically.

### Voice Message Handling

1. Voice note received.
2. Audio downloaded.
3. Speech converted to text.
4. AI processes request.
5. Response generated.
6. Voice reply sent back.

---

## 📊 Database Structure

### Products

| Field |
|---------|
| Product Name |
| Category |
| Price |
| Description |
| Stock Status |

### Delivery Fees

| Field |
|---------|
| Location |
| Delivery Cost |
| Region |

### Orders

| Field |
|---------|
| Customer Name |
| Email |
| Product |
| Payment Reference |
| Payment Status |
| Delivery Address |
| Delivery Fee |
| Total Amount |

---

## 🔒 Business Rules

The AI Agent:

- Retrieves all prices from the database.
- Retrieves all delivery fees from the database.
- Verifies payment before order confirmation.
- Prevents order registration before payment validation.
- Uses real business data only.
- Maintains conversation context throughout the sales process.

---

## ⚙️ Deployment

### Local Setup

```bash
npm install n8n -g
n8n start
```

### Docker

```bash
docker run -it --rm \
-p 5678:5678 \
-v ~/.n8n:/home/node/.n8n \
docker.n8n.io/n8nio/n8n
```

### Recommended Hosting

- Railway
- Render
- Hostinger VPS
- AWS EC2

---

## 📈 Future Enhancements

- Supabase integration
- RAG-powered product search
- Customer segmentation
- Analytics dashboard
- Inventory management
- CRM integration
- Multi-agent architecture
- Automated upselling

---

## 🎯 Project Goal

To build a fully automated AI sales representative capable of handling customer inquiries, processing orders, verifying payments, and managing sales operations directly through WhatsApp.

---

## 👨‍💻 Author

**Raphael Okorie**

AI Automation Engineer • Agent Engineer • n8n Specialist

---

## 📄 License

MIT License

Feel free to use, modify, and build upon this project.
