## Interview Framework

### Understand the Problem

**Clarify Requirements: Ask for detailed requirements and constraints**
- What are the primary features and functionalities?
- What is the core functionality of the system?
- Are there specific performance or scalability requirements?
- What are the expected user loads and data sizes?
- What are the key user interactions and use cases?

**Establish Scope: Define what is in-scope and out-of-scope for the design**
- Are there any specific boundaries or constraints?
- What are the non-functional requirements (e.g., latency, availability)?

**Identify Stakeholders: Determine who will use the system and their needs**
- Who are the primary users?
- What are their key pain points?

**Dos:**
- Listen carefully to the requirements.
- Ask clarifying questions to ensure you understand the problem completely.
- Confirm assumptions and constraints with the interviewer.

**Don’ts:**
- Don’t assume requirements; always ask for clarification.
- Avoid jumping to solutions without understanding the problem.

### Calculate Numbers / Metrics

**Estimate Traffic: Determine the expected load and traffic patterns**
- How many users will be using the system concurrently?
- What are the expected request rates?

**Define Storage Needs: Calculate data storage requirements**
- How much data will be generated?
- What are the data retention policies?

**Plan for Scalability: Estimate future growth and scalability needs**
- How will the system scale with increased load?
- What are the anticipated peak loads?

**Dos:**
- Use realistic and practical numbers based on the requirements.
- Consider both current and future metrics.

**Don’ts:**
- Don’t overlook the potential for future growth.
- Avoid using arbitrary numbers; base estimates on requirements.

### Propose High-Level Design

**Outline System Components: Identify the major components of the system and their interactions**
- Load balancers
- Web servers
- Application servers
- Databases
- Caching systems
- Message queues

**Define Data Flow: Illustrate how data moves through the system**
- Create a high-level architecture diagram.

**Choose Technologies: Select appropriate technologies and frameworks**
- What technologies are best suited for the components?
- Are there any specific constraints or preferences?

**Dos:**
- Create a clear and simple high-level architecture diagram.
- Ensure that all major components are included and interact as expected.

**Don’ts:**
- Don’t omit key components or interactions.
- Avoid overly complex diagrams; keep it understandable.

### Design Deep Dive

**Component Design: Dive deeper into each component of the system**
- Database schema and queries
- API design and endpoints
- Caching strategies
- Load balancing and fault tolerance

**Discuss Trade-offs: Analyze the trade-offs involved in design decisions**
- What are the trade-offs of different database designs?
- How does the choice of caching strategy impact performance?

**Address Non-Functional Requirements: Ensure that the design meets performance, scalability, and reliability requirements**
- How will you handle scaling and failover?
- What are the security implications?

**Dos:**
- Provide detailed explanations for each component and design choice.
- Discuss potential challenges and how to address them.

**Don’ts:**
- Don’t ignore potential edge cases or failure scenarios.
- Avoid being overly technical; focus on clarity.

### Wrap Up

**Summarize Design: Recap the high-level design and key decisions**
- High-level architecture
- Key components and their interactions
- Main trade-offs and rationale

**Discuss Future Enhancements: Mention any potential future improvements or extensions**
- What are some potential features for future versions?
- How can the system be evolved over time?

**Address Feedback: Be open to feedback and questions from the interviewer**
- Are there any aspects of the design you would like to change based on feedback?
- How would you handle specific scenarios or challenges?

**Dos:**
- Summarize the design clearly and concisely.
- Be open to feedback and willing to iterate on the design.

**Don’ts:**
- Don’t rush through the wrap-up; take the time to summarize effectively.
- Avoid being defensive about design choices; focus on constructive discussion.
