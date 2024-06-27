# System Architecture Diagram
The following diagram illustrates the architecture of the EventEase MVP, showing the end-to-end data flow through the system. Each component is clearly labeled to provide a comprehensive understanding of how data
moves from the client side to the server side and back.

# Diagram Description:

## Client Side:
Web Browser / Mobile App: Users interact with the application through a web browser or a mobile app. The frontend is built using HTML, CSS, and JavaScript.
### Frontend:
Blazor Components: These are used to create a dynamic and interactive user interface. The frontend interacts with the backend through API calls.
### API Gateway:
ASP.NET Core Web API: This serves as the intermediary between the frontend and the backend, handling HTTP requests and responses. It ensures secure communication and proper routing of data.
## Backend:
### Business Logic Layer:
Contains the core application logic, processing requests from the API gateway and interacting with the database. It includes services for event management, user management, vendor coordination, and RSVP tracking.
### Data Access Layer:
Manages interactions with the database using Entity Framework Core. It handles CRUD operations and ensures data integrity and security.
### Database:
SQL Server: The relational database stores all application data, including user information, events, vendors, and RSVPs. It provides robust ACID compliance and complex query capabilities.
### Cloud Platform:
Azure: Hosts the application, providing high availability, scalability, and security. Azure services like App Services, Azure SQL Database, and Azure Storage are utilized.
### DevOps:
CI/CD Pipeline: GitHub Actions automate the build, test, and deployment process. Each merge into the main branch triggers the CI/CD pipeline, ensuring continuous integration and delivery.

# Data Flow:
## User Interaction:
The user interacts with the frontend through the web browser or mobile app.
## API Request:
The frontend sends an HTTP request to the ASP.NET Core Web API.
## Business Logic Processing:
The API gateway forwards the request to the business logic layer, which processes the request.
## Database Interaction:
The business logic layer interacts with the data access layer to perform CRUD operations on the SQL Server database.
## API Response:
The data access layer returns the processed data to the business logic layer, which then sends the response back to the frontend through the API gateway.
## User Interface Update:
The frontend updates the user interface based on the data received from the backend
