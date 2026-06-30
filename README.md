# 🍽️ AI Hotel Restaurant Assistant

An AI-powered restaurant chatbot built with **n8n** that allows customers to order food through **Telegram** using both **text and voice messages**.

The assistant verifies menu availability, stores orders in Google Sheets, generates invoices, tracks orders, and even replies with realistic AI-generated voice responses.

---

## 🚀 Features

- 🤖 AI-powered restaurant assistant
- 💬 Telegram chatbot
- 🎙️ Voice message support
- 📝 Speech-to-Text using AssemblyAI
- 🔊 AI Text-to-Speech using Groq
- 📋 Dynamic Menu from Google Sheets
- 📦 Order Management
- 💳 Invoice Generation
- 📊 Google Sheets as Database
- 🧠 Conversation Memory
- 📌 Order Tracking
- ❌ Item Availability Validation
- 📄 FAQ Support

---

## 🛠 Tech Stack

- n8n
- Telegram Bot API
- Google Sheets
- OpenRouter AI
- Groq API
- AssemblyAI
- HTTP Request Nodes
- AI Agent
- Buffer Memory

---

## 📂 Workflow

```
Telegram
     │
     ▼
Telegram Trigger
     │
     ▼
Switch (Voice/Text)
     │
     ├──────────────┐
     │              │
     ▼              ▼
Voice            Text
     │              │
AssemblyAI         │
Speech-to-Text     │
     │              │
     └──────┬───────┘
            ▼
      AI Restaurant Agent
            │
     ┌──────┼─────────────┐
     │      │             │
     ▼      ▼             ▼
 Menu   Orders Sheet   FAQ Sheet
            │
            ▼
      Generate Response
            │
      ┌─────┴─────────┐
      │               │
      ▼               ▼
Telegram Text     Groq TTS
                      │
                      ▼
              Telegram Voice Reply
```

---

## 📋 Functionalities

### 🍔 Food Ordering

- Takes customer details
- Collects order
- Verifies menu availability
- Calculates bill
- Stores order

---

### 📖 Menu

- Show complete menu
- Search menu items
- Check availability
- Display prices

---

### 📦 Order Tracking

Search using:

- Order ID
- Email Address

Returns:

- Customer Name
- Item
- Quantity
- Amount
- Status
- Date

---

### 🧾 Invoice

Automatically generates:

- Customer Details
- Ordered Items
- Quantity
- Total Amount
- GST
- Service Charges

---

### 🎤 Voice Support

Customer can simply send:

- Voice Message

Workflow automatically:

Voice ➜ Speech-to-Text ➜ AI ➜ Text-to-Speech ➜ Voice Reply

---

## 🗂 Google Sheets

### Menu Sheet

| Item | Price | Availability | Category |

### Orders Sheet

| Order ID | Name | Email | Item | Quantity | Amount | Status | Date |

### FAQ Sheet

Restaurant FAQs

---

## AI Services

### OpenRouter

- Restaurant Assistant
- Order Management
- Memory

### AssemblyAI

- Voice Transcription

### Groq

- AI Voice Generation

---

## Installation

1. Clone the repository

```bash
git clone https://github.com/Sanskar-Parab/telegram-ai-restaurant-assistant.git
```

2. Import the workflow into n8n

3. Configure credentials

- Telegram Bot
- Google Sheets
- OpenRouter
- AssemblyAI
- Groq

4. Start the workflow

---

## Future Improvements

- Online Payment Integration
- WhatsApp Support
- Razorpay Integration
- Admin Dashboard
- Customer Analytics
- Multi-language Support
- Table Reservation
- Live Kitchen Status
- Email Invoice
- Loyalty Program

---


## Author

**Sanskar Parab**

If you like this project, consider giving it a ⭐ on GitHub.
