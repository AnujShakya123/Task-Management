                                                               Task Management system:-


Introduction:-The Task Management System allows users to perform various operations on tasks, including creation, retrieval, updating, and deletion.
It employs token generation to authorize task updates, ensuring that only authorized users can modify tasks.

                                                                 System Setup:-

This section describes the setup procedure for the Task Management System project, including installing and configuring the necessary tools and applications.

Tools and Applications
Before starting the setup, ensure that you have the following tools and applications installed:

1)IntelliJ IDEA Community Edition 2023.1.1: A Java Integrated Development Environment (IDE) for Java programming.

2)MySQL Server 8.0: A relational database management system utilized for storing application data.

3)Postman: A platform for API development collaboration, used for API testing and debugging.

Installation Steps
Follow these steps to install the required tools and applications:

1)IntelliJ IDEA Community Edition 2023.1.1:
->Download the installer from the official website of IntelliJ IDEA Community Edition 2023.1.1.
->Run the installer and complete the installation process by following the on-screen instructions.

2)MySQL Server 8.0:
->Download the MySQL Server 8.0 installer from the official website.
->Run the installer and proceed with the installation steps provided by the wizard.
->During installation, set up the root user password and configure other options as required.

3)Postman:
->Download and install Postman from its official website.
->Follow the installation instructions specific to your operating system.

Configuration
After installing the necessary tools and applications, proceed with configuring them for use in the project:

1)IntelliJ IDEA:
->Launch IntelliJ IDEA.
->Configure the Java Development Kit (JDK) if it's not automatically detected. Navigate to File > Project Structure > Project > Project SDK, and choose the installed JDK.
->Set up project dependencies and libraries as needed.

2)MySQL Server 8.0:
->Start the MySQL Server service.
->Connect to the MySQL Server using a MySQL client such as MySQL Workbench or MySQL Command Line.
->Create a new database for the Task Management System project.
->Configure database users and permissions according to requirements.

3)Postman:
->Launch Postman.
->If applicable, set up environment variables for API testing.
->Configure request collections and environments for testing the Task Management System APIs.


                                                  Running the System:-

1.)Creating Spring Boot Project:-
->Visit the Spring Initializr website.
->Select Maven Project, Java language, and Spring Boot version 3.2.3.
->Provide a Group, Artifact, and Description for your project.
->Choose the following dependencies:
       Lombok
       Spring Data JPA
       Spring Web
       MySQL Driver
       Spring Boot DevTools


2.)Project Structure:-
Create packages (or directories) in IntelliJ IDEA with the following structure:

->entities:
    Role.java
    Task.java
    User.java

->controllers:
    TaskController.java
    UserController.java

->repositories:
    TaskRepo.java
    UserRepo.java

->services:
   TaskService.java
   UserService.java

->implementations:
   TaskServiceImpl.java
   UserServiceImpl.java

->exceptions:
   GlobalExceptionHandler.java
   ResourceNotFoundException.java
   ResourceNotFoundExceptionForStatus.java

->constants:
  ApiResponse.java
  AppConstants.java
  TaskResponse.java

->authentications:
  AuthController.java
  CustomUserDetailsService.java
  JwtAuthenticationEntryPoint.java
  JwtAuthenticationFilter.java
  JwtConfig.java
  JwtHelper.java
  JwtRequest.java
  JwtResponse.java
  SecurityConfig.java


3.)Database Configuration:-
In your application.properties file, add the following configurations to connect to your MySQL database:
                                                    
spring.datasource.url=jdbc:mysql://localhost:3306/task_management
spring.datasource.username=root
spring.datasource.password=Anuj@8645
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

Explanantion:-

->Entities: Serve as the representation of the application's data model.
->Controllers: Manage incoming HTTP requests and route them to the suitable services.
->Repositories: Act as an interface for retrieving data from the database.
->Services: Execute the business logic and communicate with repositories.
->Implementations: Realize the functionalities defined in service interfaces.
->Exceptions: Manage custom exceptions and furnish relevant responses.
->Constants: Set forth fixed values utilized across the application.
->Authentications: Enforce JWT-based authentication and establish security configurations.




Screenshots of running application are :-

->After code we will be provide the screeshot of running the application 

![Alt text](<Screenshot (12)-1.png>)

->By using the postman application we can check the apis :-

![Alt text](<Screenshot (13).png>)
![Alt text](<Screenshot (14).png>)
![Alt text](<Screenshot (15).png>)