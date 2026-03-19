# trustlens-ai





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
                       