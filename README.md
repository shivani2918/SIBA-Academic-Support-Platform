# SIBA Digital Academic Support Platform (SDASP)

## Project Abstract
The SIBA Digital Academic Support Platform (SDASP) is an AI-based academic assistance system created to modernize academic support at Sukkur IBA University. Traditional support systems face limitations due to lack of physical presence, time constraints, and the absence of centralized knowledge storage. To solve this, SDASP utilizes a hybrid method combining Artificial Intelligence (AI) with human moderation. 

## Authors
* Shiwani Golani
* Tisha Dara
* Darshan Chelani


## Core Features
* **Multi-Format Query Support:** The platform allows queries to be submitted via text, voice, and file uploads.
* **Centralized Knowledge Base:** Validated academic solutions are stored for reuse, enabling easy retrieval and minimizing redundancy.
* **Gamification System:** The system uses points, badges, and engagement mechanisms to motivate user participation.

## User Roles
* **Student:** Submits academic queries and tracks their responses.
* **Moderator:** Reviews, edits, and validates AI-generated responses.
* **Administrator:** Manages system operations, oversees usage, and monitors analytics.

## Technical Stack
* **Frontend:** React.js is used for responsive and user-friendly web interfaces.
* **Backend:** Node.js with Express.js handles server-side logic and API routing.
* **Database:** MongoDB Atlas (Cloud) is used for flexible, scalable data storage.
* **Deployment:** The frontend is hosted on Vercel, and the backend is deployed on Railway for optimal performance.

## System Architecture Layering
The system uses a multi-layered, modular architecture to ensure scalability:
* **Presentation Layer:** Provides the interface for students, moderators, and admins.
* **Application Layer:** Handles business logic, JWT authentication, and query processing.
* **Middleware Layer:** Manages communication with external AI APIs and notification services.
* **Data Access Layer:** Handles database operations and query handlers.
* **Database Layer:** Securely stores all system data, users, and logs.

## AI Workflow & Dual-Model Validation
The backend triggers concurrent requests to OpenAI GPT-4o and Google Gemini 1.5 Pro using a Chain-of-Thought (CoT) prompting strategy. This allows the system to cross-reference AI outputs and reduce hallucination rates before human moderation. 

The knowledge base utilizes Vector Embeddings (MongoDB Atlas Vector Search) to perform semantic similarity checks and retrieve verified academic answers via a RAG framework.

## Security Protocols
* **Authentication:** JSON Web Tokens (JWT) with RSA-256 secure login and role-based access control.
* Data transmission is secured via HTTPS, and the human-in-the-loop validation strictly prevents inaccurate AI-generated responses from reaching the end users.