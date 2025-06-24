# AirBnB Clone Project

## Project Overview
A full-stack clone of the Airbnb platform that allows users to browse, view, and book property listings.

## Project Goals
- Master collaborative team workflows using GitHub.
- Deepen understanding of backend architecture and database design principles.
- Implement advanced security measures for API development.
- Gain proficiency in designing and managing CI/CD pipelines for efficient deployment.
- Strengthen ability to document and plan complex software projects effectively.
- Develop an understanding of integrating different technologies in a unified ecosystem.

## Technology Stack

- **Frontend**: HTML, CSS, JavaScript (React)
- **Backend**: Django, GraphQL
- **Database**: PostgreSQL
- **Version Control**: Git, GitHub
- **Design Tools**: Figma
- **Deployment/Infrastructure**: Docker

### It's purpose in the project

- **Django**: A high-level Python web framework used for developing the backend and APIs.
- **GraphQL**: A query language for APIs, used to optimize data retrieval for frontend clients.
- **MySQL**: A relational database used for storing user, property, booking, and payment information.
- **Docker**: A tool to containerize the app and ensure environment consistency across all systems.

# Frontend

## UI/UX Design Planning

### Design Goals
- Create an intuitive booking flow
- Maintain visual consistency
- Ensure fast loading times
- Prioritize mobile responsiveness

### Key Features
- Property search and filtering
- Detailed property viewing
- Secure checkout process
- User authentication

### Primary Pages

| Page           | Description     |    
|----------------|-----------------|
|Property Listing View        | Grid display of available properties with filters |
| Listing Detailed View          |Complete property details with images and booking form |
| Simple Checkout View          |Streamlined payment and booking confirmation|

### Importance of a user-friendly design
- Enhances User Experience
- Reduces Booking Errors
- Improves Accessibility
- Boosts Conversion Rates
- Builds Trust and Credibility

## Figma Design Specifications

### Color Styles

- **Primary:** `#FF5A5F`
- **Secondary:** `#008489`
- **Background:** `#FFFFFF`
- **Text:** `#222222`
- **Secondary Text:** `#717171`

### Typography

- **Primary Font:** Circular, Medium (500), 16px
- **Headings:** Circular, Bold (700), 24px–32px
- **Secondary Text:** Circular, Book (400), 14px

### Importance of identifying design properties of a mock up design
- Ensures Design Consistency
- Supports Responsive Design
- Facilitates Developer Handoff
- Improves Usability
- Speeds Up Iteration and Feedback

## Project Roles and Responsibilities

| Role             | Responsibilities                                                 |
|------------------|------------------------------------------------------------------|
| Project Manager  | Manages timeline, communication, and deliverables                |
| Frontend Devs    | Build responsive UI with React, manage state                     |
| Backend Devs     | Create REST APIs, manage DB logic, integrate with frontend       |
| Designers        | Design UI in Figma, maintain visual consistency                  |
| QA/Testers       | Write test cases, test features, report bugs                     |
| DevOps Engineers | Manage hosting, deployment, CI/CD pipelines                      |
| Product Owner    | Define features, prioritize tasks, represent user needs          |
| Scrum Master     | Facilitate standups, manage agile boards, remove blockers        |

## UI Component Patterns

### Navbar
- Logo
- Search bar
- User navigation
- Responsive hamburger menu

### Property Card
- Property image
- Location, price, rating
- Favorite button
- Responsive layout

### Footer
- Site links
- Company info
- Social media icons
- Copyright

## Backend

## Team Roles

- **Backend Developer**: Implements the application logic, builds REST/GraphQL APIs, integrates database operations, and ensures secure endpoints.
- **Database Administrator (DBA)**: Designs, manages, and optimizes the MySQL database schema, ensures data integrity and backups.
- **DevOps Engineer**: Sets up Docker containers and GitHub Actions for CI/CD workflows, manages deployment pipelines.
- **Security Specialist**: Ensures all security measures are implemented, including encryption, access control, and vulnerability monitoring.
- **Project Manager**: Coordinates timelines, assigns tasks, and tracks project milestones for successful and timely delivery.

## Database Design

#### Entities and Relationships

- **Users**
  - `id`, `name`, `email`, `password`, `role`
  - A user can book multiple properties and post reviews.

- **Properties**
  - `id`, `owner_id`, `location`, `price`, `description`
  - A property is listed by a user and can have multiple bookings.

- **Bookings**
  - `id`, `user_id`, `property_id`, `check_in`, `check_out`
  - A booking belongs to one user and one property.

- **Reviews**
  - `id`, `user_id`, `property_id`, `rating`, `comment`
  - A user can post multiple reviews for properties they've booked.

- **Payments**
  - `id`, `booking_id`, `amount`, `payment_method`, `status`
  - Each payment is linked to a specific booking.
 
## Feature Breakdown

- **User Management:** Enables user registration, login, role assignment, and secure session management.
- **Property Management:** Allows property owners to list, update, and delete their rental properties.
- **Booking System:** Users can book available properties by selecting dates and making payments.
- **Review System:** After a booking, users can leave feedback to help others make informed choices.
- **Payment Gateway Integration:** Supports secure transactions and payment tracking.
- **Admin Panel:** Admin users can monitor system activity, manage users, and flag/report suspicious listings.

## API Security

#### Security Measures

- **Authentication:** Ensures only registered users can access protected endpoints.
- **Authorization:** Grants different access levels to users based on roles (e.g., admin vs. regular user).
- **Rate Limiting:** Prevents abuse by limiting the number of requests a user can make in a certain time.
- **Input Validation:** Protects against injection attacks by sanitizing input.
- **HTTPS:** Ensures secure communication over the network.

### Why security is crucial?
- Protects user data and prevents unauthorized access.
- Ensures secure financial transactions.
- Maintains platform trust and integrity.

## CI/CD Pipeline

CI/CD stands for Continuous Integration and Continuous Deployment. It is a method of automating software delivery, from code commits to deployment.

### Tools Used:
- **GitHub Actions**: Automates testing, building, and deploying the app on every commit.
- **Docker**: Ensures the app runs in the same environment across development, staging, and production.
