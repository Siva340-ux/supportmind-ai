# System Architecture

## High-Level Architecture

                 React Frontend

                        |

                        |

                 Spring Boot API

                        |

                        |

                   Spring AI

                /            \

               /              \

        Tool Calling         RAG

           |                  |

           |                  |

         MySQL            ChromaDB

              \           /

               \         /

                Gemini/Ollama

---

## Responsibilities

### React Frontend

- Customer Dashboard
- Order Management
- Ticket Management
- AI Chat Interface

---

### Spring Boot

- Business Logic
- REST APIs
- Authentication
- Data Validation
- Integration with Spring AI

---

### MySQL

Stores:

- Users
- Customers
- Orders
- Refunds
- Support Tickets
- Chat Sessions

---

### ChromaDB

Stores:

- Refund Policies
- Shipping Policies
- FAQs
- Support Documentation

---

### Spring AI

Responsibilities:

- LLM Communication
- Embedding Generation
- Retrieval
- Tool Calling
- Memory Handling
- Agentic Workflows
