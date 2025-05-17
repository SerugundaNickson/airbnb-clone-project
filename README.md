# airbnb-clone-project

## Overview

This project is part of the ALX Software Engineering program. The goal is to build a simplified clone of the AirBnB web application using core backend and frontend technologies. It will help reinforce our understanding of object-oriented programming, web development, and deployment.

## Project Goals

- Create a command interpreter to manage AirBnB objects (users, places, etc.)
- Persist data using JSON serialization
- Implement the backend logic for storing and retrieving data
- Build out basic frontend templates
- Integrate both backend and frontend to simulate the AirBnB experience

## Tech Stack

- **Python** – Core logic and backend
- **Flask** – Web framework (for web interface in later stages)
- **JSON** – Data storage format
- **HTML/CSS** – Frontend structure and design
- **Git & GitHub** – Version control and collaboration

## Status

Project is currently in its setup stage.

## Team Roles

###  Business Analyst (BA)
- **Responsibilities**:
  - Understands the customer's business processes.
  - Translates business needs into technical requirements.
  - Bridges the gap between stakeholders and the development team.
- **Role in Project**:
  - Ensures that the development aligns with business objectives by analyzing workflows and stakeholder feedback.

###  Product Owner (PO)
- **Responsibilities**:
  - Holds responsibility for the product vision and evolution.
  - Ensures the final product meets customer requirements.
  - Manages the product backlog.
- **Role in Project**:
  - Acts as the decision-maker, balancing business needs and market trends to define the product strategy.

###  Project Manager (PM)
- **Responsibilities**:
  - Ensures timely and budget-compliant delivery of the product.
  - Manages and motivates the software development team.
- **Role in Project**:
  - Oversees task distribution, work planning, and maintains transparency throughout the development process.

###  UI/UX Designer
- **Responsibilities**:
  - Designs user interfaces and user experiences.
  - Ensures the product is user-friendly and meets design standards.
- **Role in Project**:
  - Translates requirements into interactive designs that enhance user satisfaction.

###  Software Architect
- **Responsibilities**:
  - Defines the overall structure of the software system.
  - Ensures scalability, performance, and security.
- **Role in Project**:
  - Provides technical guidance and makes high-level design choices.

###  Software Developer
- **Responsibilities**:
  - Writes and maintains the codebase.
  - Implements features and fixes bugs.
- **Role in Project**:
  - Develops the application according to specifications and ensures functionality.

###  Quality Assurance (QA) Engineer
- **Responsibilities**:
  - Develops and executes test plans.
  - Identifies and documents bugs.
- **Role in Project**:
  - Ensures the product meets quality standards and functions as intended.

###  Test Automation Engineer
- **Responsibilities**:
  - Creates automated tests to streamline the testing process.
  - Maintains test scripts and frameworks.
- **Role in Project**:
  - Enhances testing efficiency and coverage through automation.

###  DevOps Engineer
- **Responsibilities**:
  - Manages deployment pipelines and infrastructure.
  - Ensures continuous integration and delivery.
- **Role in Project**:
  - Facilitates smooth deployment processes and system reliability.

## Technology Stack

This project uses a range of technologies to implement the backend, database, API, and future frontend functionality.

###  Python
- **Purpose**: The core programming language used to build the application logic and handle backend operations.

###  Django
- **Purpose**: A high-level Python web framework used to build RESTful APIs, handle routing, and structure backend services.

###  PostgreSQL
- **Purpose**: A powerful, open-source relational database system used for storing and managing structured application data.

###  GraphQL
- **Purpose**: A flexible query language for APIs, allowing the client to request exactly the data it needs — enhancing performance and reducing over-fetching.

###  Pytest
- **Purpose**: A testing framework used to write and run unit tests, ensuring that the application functions correctly and remains stable over time.

###  Git & GitHub
- **Purpose**: Version control tools used to track code changes, collaborate with others, and manage source code in the cloud.

###  Docker (Optional in later stages)
- **Purpose**: Used to containerize the application for consistent development, testing, and deployment environments.

###  RESTful APIs
- **Purpose**: Used to structure how the backend communicates with the frontend or other services, following HTTP standards.

## Database Design

The database schema for the AirBnB Clone project includes key entities that represent the core functionalities of the platform. Each entity contains important fields and has defined relationships with others.

###  Users
Represents the people using the platform (guests and hosts).
- `id`: Unique identifier
- `name`: Full name of the user
- `email`: Email address (must be unique)
- `password_hash`: Hashed password for authentication
- `is_host`: Boolean flag to indicate if the user is a host

###  Properties
Represents accommodations listed by hosts.
- `id`: Unique identifier
- `user_id`: Foreign key linking to the host (Users table)
- `title`: Name or title of the property
- `description`: Detailed description
- `location`: Address or general location

###  Bookings
Represents reservations made by users.
- `id`: Unique identifier
- `user_id`: Foreign key for the guest (Users table)
- `property_id`: Foreign key for the booked property
- `check_in`: Date of check-in
- `check_out`: Date of check-out

###  Reviews
Allows users to leave feedback after a stay.
- `id`: Unique identifier
- `user_id`: Foreign key of the reviewer
- `property_id`: Foreign key of the reviewed property
- `rating`: Numerical rating (e.g., 1 to 5)
- `comment`: Textual review

###  Payments
Tracks financial transactions for bookings.
- `id`: Unique identifier
- `booking_id`: Foreign key for the related booking
- `amount`: Total amount paid
- `payment_method`: e.g., Credit Card, PayPal
- `payment_status`: e.g., Paid, Pending, Failed

---

###  Entity Relationships

- A **User** can be a **host** (owns multiple properties) or a **guest** (books properties).
- A **Property** belongs to one **User** (host).
- A **Booking** is made by a **User** and is linked to one **Property**.
- A **Review** is written by a **User** about a **Property** after a booking.
- A **Payment** is associated with one **Booking**.

## Feature Breakdown

The Airbnb Clone project includes several core features that replicate the functionalities of the original Airbnb platform. Each feature is designed to deliver a complete and interactive user experience.

### User Management
Allows users to sign up, log in, and manage their profiles. This feature supports user authentication and role distinction between guests and hosts.

### Property Management
Enables hosts to list, edit, and delete property listings. Hosts can provide details such as descriptions, locations, pricing, and photos for potential guests.

### Booking System
Allows users to view available properties and make reservations. This system manages booking dates, availability, and prevents conflicts in scheduling.

### Payment Processing
Handles secure payment transactions for bookings. This feature supports multiple payment methods and keeps track of the payment status for each transaction.

### Review and Rating System
Enables guests to leave reviews and ratings for properties after their stay. It helps maintain trust in the platform and provides feedback for both hosts and future guests.

### Search and Filtering
Provides users with the ability to search for properties using filters such as location, price, availability, and amenities. This enhances usability and helps users find suitable accommodations quickly.

### Admin Panel (Optional - Advanced)
Offers administrative controls to monitor users, properties, and bookings. This feature is useful for moderating content and maintaining platform integrity.




