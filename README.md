# AI Research Assistant

An advanced AI-powered research and study platform that enables users to interact with documents, research papers, URLs, and images through a conversational interface. The platform combines document intelligence, adaptive learning, research analytics, and secure AI-powered workflows using Google Gemini and Supabase.

---

## 🚀 Overview

AI Research Assistant is a full-stack AI-powered platform designed to streamline research, learning, and document analysis. Users can upload documents, analyze websites, compare research papers, generate adaptive study schedules, interact with AI through a ChatGPT-style interface, and gain insights through analytics dashboards.

The platform leverages Google Gemini models for document understanding, vision analysis, translation, quiz generation, and conversational AI while maintaining enterprise-grade security using Supabase.

---

## ✨ Key Features

### 💬 Conversational AI Chat

* ChatGPT-style interface with streaming responses
* Persistent conversation history
* Pin, star, and categorize conversations
* PDF export of chat sessions
* Color-coded tags (Research, Interview, Exam)

### 📄 Document Intelligence

* Upload PDF, DOC, and DOCX files (up to 30 MB)
* AI-powered document summarization
* Research paper analysis
* Context-aware document Q&A
* Academic insight generation

### 📚 Multi-Document Comparison

* Compare multiple research papers
* Extract algorithms and methodologies
* Analyze metrics and experimental results
* Generate structured comparison reports

### 🌐 URL Research & Safety Analysis

* Phishing and malware risk assessment
* URL safety confidence scoring
* Website content extraction
* SSRF protection
* Multi-user-agent scraping strategy

### 🧠 Adaptive Study Scheduler

* AI-generated study plans
* Quiz-based progression system
* Performance-driven learning paths
* Monthly calendar visualization
* Automated study recommendations

### 🖼️ Vision Analysis

* Image upload and processing
* Visual question answering
* Diagram and chart interpretation
* AI-assisted image understanding

### 🌍 Translation & Voice Features

* Multi-language translation
* Speech-to-text conversion
* Text-to-speech synthesis
* Support for multiple languages

### 📊 Analytics Dashboard

* Research activity tracking
* Learning streak visualization
* Feedback analytics
* Study progress monitoring
* Interactive charts and reports

### 🎯 Domain Mode

* Restricts AI responses to uploaded documents
* Citation-grounded answers
* Reduced hallucinations
* Source-aware retrieval

### 🔄 Continuous Improvement Loop

* User feedback collection
* AI prompt refinement
* Response quality enhancement
* Adaptive learning system

### 🤝 Chat Sharing

* Secure token-based conversation sharing
* Conversation cloning and import
* Independent chat duplication

---

## 🏗️ System Architecture

```text
User Interface (React + TypeScript)
                │
                ▼
        Supabase Backend
                │
    ┌───────────┼───────────┐
    ▼           ▼           ▼
 Authentication Storage  Edge Functions
    │                       │
    ▼                       ▼
 PostgreSQL Database   Google Gemini AI
```

---

## 🛠️ Tech Stack

### Frontend

* React 18
* TypeScript
* Vite
* Tailwind CSS
* shadcn/ui
* Radix UI
* Framer Motion
* Recharts
* jsPDF
* React Hook Form
* Zod

### Backend

* Supabase

  * PostgreSQL
  * Authentication
  * Storage
  * Edge Functions (Deno)

### AI & Machine Learning

* Google Gemini 2.5 Pro
* Google Gemini 2.5 Flash
* Gemini Vision Models

### Development Tools

* ESLint
* TypeScript Strict Mode
* Git & GitHub

---

## 🔒 Security Features

### Authentication Security

* Email verification
* Google OAuth
* Apple OAuth
* Bcrypt password hashing
* HIBP password breach detection
* JWT session management

### Application Security

* Row-Level Security (RLS)
* SSRF protection
* Error sanitization
* Server-side API key storage
* Private document storage
* Signed URL access control

### Database Security

* User-specific data isolation
* Protected authentication schema
* Secure storage buckets
* Permission-controlled access

---

## 📁 Database Design

### Core Tables

| Table         | Purpose                    |
| ------------- | -------------------------- |
| profiles      | User profile information   |
| conversations | Chat sessions              |
| messages      | Conversation messages      |
| documents     | Uploaded document metadata |
| feedback      | User feedback records      |
| schedulers    | Study schedules            |
| subscriptions | Subscription management    |
| shared_chats  | Shared conversation tokens |

### Storage Buckets

#### Private Bucket

* documents

#### Public Bucket

* avatars

---

## 📄 Document Processing Pipeline

### PDF/DOC Processing

1. User uploads document
2. File stored in Supabase Storage
3. File converted to Base64
4. Gemini extracts structured text
5. Metadata saved in PostgreSQL
6. Document linked to conversation
7. AI chat initialized with extracted context

### Features

* Supports files up to 30 MB
* Chunked processing
* AI-powered extraction
* Automatic summarization
* Context-aware retrieval

---

## 🌐 URL Research Pipeline

### Safety Analysis

The system evaluates URLs using:

* Suspicious TLD detection
* IP-address detection
* Excessive subdomain detection
* Homograph attack detection
* HTTPS validation

### Content Extraction

1. URL validation
2. SSRF protection checks
3. Multi-user-agent fetching
4. HTML cleaning
5. Content extraction
6. AI summarization

---

## 🎓 Adaptive Study Scheduler Workflow

1. User defines learning objectives
2. AI generates study roadmap
3. Daily learning modules created
4. Quiz generated for each module
5. Progress evaluated automatically
6. Future content unlocked based on performance
7. Progress displayed in analytics dashboard

---

## 📊 Analytics Features

* Research streak tracking
* Study hour monitoring
* User feedback analytics
* Learning progress visualization
* Interactive charts and reports

---

## 🔄 Chat Sharing Mechanism

### Token Generation

The platform generates cryptographically secure random tokens using the browser's Web Crypto API.

### Workflow

1. User selects "Share Chat"
2. Secure token generated
3. Token stored in shared chat table
4. Recipient imports using token
5. Conversation duplicated
6. New independent copy created

### Security Benefits

* High-entropy random tokens
* No personal information exposure
* Server-side validation
* Original chat remains private

---

## 🚀 Project Highlights

* Full-stack AI-powered research ecosystem
* Real-time conversational AI
* Advanced document intelligence
* Secure multi-tenant architecture
* Adaptive AI learning workflows
* Enterprise-grade security controls
* Modern glassmorphism UI
* Scalable cloud-native deployment

---

## 👨‍💻 Developer Responsibilities

* Frontend Development
* Backend Development
* Database Architecture
* Security Implementation
* AI Integration
* Prompt Engineering
* UI/UX Design
* Deployment & Maintenance

---

## 📌 Resume Description

Developed a full-stack AI-powered research and study platform that enables users to chat with PDFs and URLs, compare research papers, generate adaptive study schedules with AI-created quizzes, and analyze images using Google Gemini. Implemented secure authentication, document intelligence, analytics dashboards, multi-language support, and real-time conversational AI using React, TypeScript, Supabase, and Gemini APIs.

### Technologies Used

React • TypeScript • Tailwind CSS • Supabase • PostgreSQL • Google Gemini • Framer Motion • Recharts • jsPDF • React Hook Form • Zod • Vite

---

## Future Enhancements

* Vector database integration
* Research citation generation
* Collaborative workspaces
* Knowledge graph visualization
* Mobile application support
* Advanced RAG pipelines
* Fine-tuned AI models

---

## License

This project is intended for educational, research, and productivity purposes.
