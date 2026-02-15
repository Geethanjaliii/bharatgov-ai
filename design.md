# System Design – BharatGov AI

## 1. Architecture Overview

The system follows a serverless, scalable cloud-native architecture using AWS services.

User → Frontend → API Gateway → AWS Lambda →  
Vector Database (Embeddings) + Amazon Bedrock (LLM) → Response

---

## 2. Core Components

### 2.1 Frontend
- Web or mobile interface
- Language selection
- Chat-based interaction

### 2.2 API Gateway
- Receives user requests
- Routes to backend services

### 2.3 AWS Lambda
- Handles business logic
- Processes user inputs
- Calls RAG pipeline

### 2.4 Vector Database
- Stores embeddings of government scheme documents
- Enables semantic search

### 2.5 Amazon Bedrock
- Large Language Model
- Generates contextual and multilingual responses

### 2.6 S3 Storage
- Stores scheme documents
- Stores static assets

---

## 3. RAG Workflow

1. User submits query.
2. Query converted into embeddings.
3. Similar documents retrieved from vector database.
4. Retrieved context passed to LLM.
5. LLM generates grounded response.
6. Response translated to user-selected language.

---

## 4. Scalability

- Serverless Lambda auto-scales.
- API Gateway handles high request load.
- Stateless architecture ensures horizontal scaling.
- Can integrate CDN for performance.

---

## 5. Security

- IAM-based access control.
- HTTPS encrypted communication.
- No sensitive data permanently stored.
- Role-based admin access.

---

## 6. Future Enhancements

- Voice bot integration.
- WhatsApp chatbot integration.
- Offline SMS-based query system.
- Integration with DigiLocker or Aadhaar APIs (with compliance).
