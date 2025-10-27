# requirement-analysis
Repository for exploring and documenting requirement analysis in software development.

## What is Requirement Analysis?

Requirement Analysis is the process of identifying, documenting, and managing the needs and expectations of stakeholders for a software system. It serves as the foundation of the **Software Development Life Cycle (SDLC)**, ensuring that the final product aligns with user requirements and business goals.

During this phase, developers, analysts, and stakeholders work together to:
- Understand what the users need from the system.
- Define functional and non-functional requirements.
- Detect ambiguities, conflicts, or inconsistencies in the requirements.
- Prioritize requirements based on importance and feasibility.

### Importance of Requirement Analysis
Requirement Analysis is crucial because it:
1. **Prevents Miscommunication:** Clearly defines what is to be built, reducing misunderstandings between clients and developers.  
2. **Saves Time and Cost:** Identifying issues early avoids costly changes in later stages of development.  
3. **Improves Quality:** Ensures that the system meets user expectations and performs as intended.  
4. **Provides a Clear Roadmap:** Acts as a reference for design, development, and testing teams throughout the SDLC.  

In summary, Requirement Analysis transforms vague ideas into clear, actionable requirements — forming the blueprint for successful software projects.

## Why is Requirement Analysis Important?

Requirement Analysis plays a crucial role in ensuring the success of any software project. It acts as the bridge between the client’s expectations and the developer’s implementation, reducing the risk of project failure. Below are some key reasons why this phase is essential in the Software Development Life Cycle (SDLC):

### 1. Prevents Project Failure
Many software projects fail because the requirements were not clearly understood or properly documented. Requirement Analysis ensures all stakeholders share a common understanding of the project goals, preventing costly misunderstandings and scope creep.

### 2. Saves Time and Resources
By identifying potential challenges, constraints, and priorities early in the process, teams can plan efficiently. Detecting issues during analysis is far less expensive than fixing them during coding or testing.

### 3. Enhances Product Quality
Thorough requirement analysis leads to well-defined specifications, which guide developers and testers toward building a system that meets user expectations and business needs. This results in a higher-quality, user-focused product.

### 4. Supports Effective Communication
Requirement Analysis serves as a communication channel between clients, users, and developers. It ensures that everyone involved in the project understands what will be delivered, when, and how.

### 5. Provides a Clear Project Roadmap
The process creates detailed documentation that becomes the foundation for design, development, and testing activities. It provides a clear roadmap, ensuring all future phases of the SDLC are aligned with the defined requirements.

## Key Activities in Requirement Analysis

Requirement Analysis involves a series of structured activities that ensure all system requirements are properly understood, defined, and verified. These activities help transform user needs into clear, actionable requirements for the development team.

Below are the five key activities in Requirement Analysis:

- ### **1. Requirement Gathering**
  This is the initial step where information is collected from stakeholders, users, and clients to understand their needs and expectations. Techniques such as interviews, questionnaires, and observation are commonly used to gather this data.

- ### **2. Requirement Elicitation**
  Elicitation involves discovering and refining requirements through collaboration and discussion. The goal is to uncover hidden needs, clarify assumptions, and resolve conflicts between stakeholder expectations.

- ### **3. Requirement Documentation**
  In this phase, all gathered and elicited requirements are formally recorded. The documentation typically includes functional and non-functional requirements, use cases, and user stories. This serves as a reference for all future development activities.

- ### **4. Requirement Analysis and Modeling**
  This activity focuses on analyzing, prioritizing, and organizing requirements. It also involves modeling the requirements using diagrams such as Data Flow Diagrams (DFDs), UML models, or Entity-Relationship Diagrams (ERDs) to visualize the system structure and behavior.

- ### **5. Requirement Validation**
  Validation ensures that the documented requirements are complete, consistent, and aligned with user needs and business goals. Reviews, walkthroughs, and prototyping are often used to confirm that the requirements are correct and feasible.

Together, these activities ensure that the software development team has a clear, validated understanding of what needs to be built — reducing risks and increasing the likelihood of project success.

## Types of Requirements

In software development, requirements are broadly divided into **Functional** and **Non-functional Requirements**.  
Functional requirements describe **what** the system should do, while non-functional requirements describe **how well** the system performs those functions.  

Using the **Hotel Booking Management System** (like Airbnb, Booking.com, or OYO) as a case study, we can clearly identify both types.

---

### **1. Functional Requirements**

Functional requirements specify the system’s **core operations and interactions** that allow users to complete specific tasks.  
They define what actions the system must perform for both customers and hotel managers.

**Examples for a Hotel Booking Management System:**

- **User Registration and Authentication:**  
  Customers and hotel managers can sign up, log in, and manage their profiles securely.

- **Hotel Management:**  
  Hotel owners can add, update, or remove property details such as room type, pricing, location, and availability via the **Hotel Management Service**.

- **Search Functionality:**  
  Customers can search hotels based on filters like price range, city, and amenities.  
  The **Search Service** retrieves results from **Elasticsearch** for fast and accurate queries.

- **Booking Process:**  
  Users can select rooms, choose check-in/check-out dates, and make reservations.  
  The **Booking Service** handles this flow and interacts with the **Payment Gateway** for transactions.

- **Payment Processing:**  
  Integration with third-party payment systems (e.g., Stripe, PayPal) ensures secure, real-time payment confirmation.

- **View Bookings:**  
  Users can view their booking history and current reservations.  
  The **View Booking Service** accesses data stored in **Redis** (for recent data) and **Cassandra** (for archived data).

- **Notifications:**  
  The system automatically sends notifications for booking confirmations, updates, or promotional offers via **Kafka Messaging Queues**.

**Purpose:**  
Functional requirements define the **specific features and actions** the system must perform to meet user needs.

---

### **2. Non-functional Requirements**

Non-functional requirements focus on **system quality, performance, and reliability**.  
They describe how well the system executes its functions and ensures a smooth experience for millions of users.

**Examples for a Hotel Booking Management System:**

- **Performance:**  
  The system should respond to user actions within **2–3 seconds**, even under high load.  
  ➤ Achieved through **Redis caching** and **Content Delivery Networks (CDNs)**.

- **Scalability:**  
  The architecture should support thousands of hotels and millions of customers simultaneously.  
  ➤ Implemented using **microservices** and **load balancers** to distribute traffic.

- **Availability:**  
  The system must maintain **99.9% uptime** with minimal service interruptions.  
  ➤ Managed by **replicated databases** and **failover strategies**.

- **Security:**  
  All sensitive data (like passwords and payments) must be **encrypted** and **protected with authentication layers**.

- **Reliability:**  
  The system should function consistently across distributed environments.  
  ➤ Supported by **Kafka queues** and **Cassandra** for durable message delivery and data persistence.

- **Maintainability:**  
  The modular microservice design allows developers to update or fix one service without impacting others.

- **Usability:**  
  The user interface (web and mobile) must be intuitive, responsive, and accessible.

- **Data Analytics:**  
  Data streams through **Apache Streaming** into **Hadoop** for advanced analytics like customer segmentation and business insights.

**Purpose:**  
Non-functional requirements define the **quality benchmarks** that ensure the system is efficient, secure, and scalable.

---

### **Summary**

| Requirement Type | Description | Example |
|------------------|-------------|----------|
| **Functional** | Defines what the system does | User login, hotel listing, search, booking, payments |
| **Non-Functional** | Defines how the system performs | Scalability, speed, security, reliability |

---

Together, these requirements ensure that the **Hotel Booking Management System** delivers a seamless experience — balancing functionality, performance, and user satisfaction across all services.


## Use Case Diagrams

A **Use Case Diagram** is a visual representation of how different users (actors) interact with a system. It helps identify the main functionalities (use cases) that the system must provide and the relationships between users and those functions.

Use Case Diagrams are an essential part of **Requirement Analysis** because they:
- Provide a **clear overview** of system interactions from the user’s perspective.
- Help developers and stakeholders **understand system functionality** without technical details.
- Serve as a **communication tool** between business analysts, developers, and clients.
- Aid in identifying **functional requirements** during the analysis phase.

---

### **Booking Management System – Use Case Diagram**

Below is the use case diagram for the **Booking Management System**, illustrating the main actors and use cases.

**Actors:**
- **Customer** – books, modifies, or cancels a reservation.
- **Admin** – manages bookings and generates reports.
- **Payment System** – handles payment processing.

**Use Cases:**
- Search Available Rooms
- Create Booking
- Modify Booking
- Cancel Booking
- Make Payment
- Generate Reports
- Send Confirmation

---

### **Use Case Diagram:**

![Booking Management System Use Case Diagram](alx-booking-uc.png //link:https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&dark=auto#G1M5pzXggJC633bRNI44gh0HyYsCMuzQAJ)
*Figure: Use Case Diagram for Booking Management System*

## Acceptance Criteria

**Acceptance Criteria** are the predefined conditions or requirements that a software feature must meet to be accepted by the stakeholders, client, or end user.  
They define **“what must be true”** for a feature to be considered complete, functional, and aligned with the user’s expectations.

---

### **Importance of Acceptance Criteria**

Acceptance Criteria play a critical role in the **Requirement Analysis** and **Software Development Life Cycle (SDLC)** because they:

1. **Clarify Expectations:**  
   They ensure that developers, testers, and stakeholders have a shared understanding of what the feature should do and how it should behave.

2. **Define Done:**  
   They help determine when a feature is complete and ready for release, preventing scope creep and incomplete functionality.

3. **Guide Testing:**  
   They serve as a foundation for test case creation — helping quality assurance (QA) teams verify that the feature works as intended.

4. **Improve Communication:**  
   They provide a clear, measurable way to confirm that business requirements are met, improving collaboration between technical and non-technical teams.

---

### **Example – Checkout Feature (Booking Management System)**

Below is an example of **Acceptance Criteria** for the **Checkout Feature** in the *Booking Management System*.

**Feature:** Checkout and Payment Processing

**User Story:**  
> As a customer, I want to complete my booking and make a secure payment so that I can confirm my reservation.

**Acceptance Criteria:**
1. The system must display a summary of the booking details (date, price, and room type) before payment.  
2. The customer must be able to select a payment method (credit card, debit card, or digital wallet).  
3. Payment must be processed securely using the integrated payment gateway.  
4. The system must generate a booking confirmation message upon successful payment.  
5. The customer must receive a confirmation email or SMS containing booking details and payment receipt.  
6. If the payment fails, the system must notify the user and allow them to retry or cancel the checkout process.  

---

**In Summary:**  
Acceptance Criteria ensure that each feature in the system is **clear, testable, and verifiable**, reducing ambiguity and ensuring high-quality software delivery that aligns with user expectations.
