
# TrustLens AI

AI-powered trust evaluation system for inbound communication (LinkedIn, email, etc.)

## Architecture
- API Gateway (Spring Cloud Gateway)
- Analysis Service (LLM + Rule Engine)
- Enrichment Service

## Tech Stack
- Java (Spring Boot, WebFlux)
- Docker
- Kafka (planned)
- OpenAI (planned)

## How to Run
1. cd gateway-service
2. mvn clean package
3. docker build -t gateway .
4. docker run -p 8080:8080 gateway

## Current Status
✅ Gateway completed  
🚧 Analysis service in progress



                API Gateway (Spring Boot / Spring Cloud Gateway)
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
 Message Service      Analysis Service      User Service
        │                     │
        │             ┌───────┼────────┬────────┐
        │             │       │        │        │
        │        Parser   Signal   LLM Client  Enrichment
        │             │       │        │        │
        │             └───────┴────────┴────────┘
                              │
                       Scoring Engine
                              │
                       Response Generator
                       