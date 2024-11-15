## Bank of Success Pvt LTD - Banking Module

### Project Overview
The **Bank of Success Pvt LTD** banking module is a Java-based application simulating core banking functionalities, designed to manage **Savings** and **Current** account types with distinct attributes and behaviors. This project leverages **Object-Oriented Programming (OOP)** principles, **SOLID principles**, and **JDBC** to enable data persistence, ensuring code clarity, maintainability, and integration with relational databases.

### Key Features
1. **Account Types**:
   - **Savings Account**: Includes personal attributes like date of birth, gender, and phone number.
   - **Current Account**: Includes business-related attributes like company name, website, and registration number.

2. **Common Account Attributes**:
   - **Account Information**: Unique account number, account holder's name, pin number, and balance.
   - **Account Privileges**: Enum values (PREMIUM, GOLD, SILVER) defining different privilege levels.
   - **Account Status**: Tracks if the account is active or inactive, with activation and closure dates.

3. **Database Persistence**:
   - Uses **JDBC** to connect to a MySQL database, enabling account information to be stored, retrieved, and managed in **MySQL Workbench**.
   - Provides a relational structure to store and query account details efficiently.

### Technical Concepts
- **Object-Oriented Programming (OOP)**:
  - **Encapsulation**: Each account type encapsulates its own attributes and methods, which are not directly accessible outside their respective classes.
  - **Inheritance**: Common attributes and behaviors are defined in a base `Account` class, which is inherited by `SavingsAccount` and `CurrentAccount` subclasses.
  - **Polymorphism**: Common methods in the base `Account` class can be overridden by subclasses to provide specific implementations where needed.

- **Java Enums**: The `Privilege` enum defines specific levels for accounts, improving readability and ensuring type safety.

- **JDBC and MySQL Integration**: The project uses **JDBC** to interface with a MySQL database, ensuring reliable data storage and retrieval.

- **Exception Handling**: Includes robust exception handling to manage errors such as invalid account actions, unauthorized access, and database connection issues.

### Application of SOLID Principles
1. **Single Responsibility Principle (SRP)**: Each class has a single responsibility, such as account-specific attributes, business logic, or data access.
  
2. **Open/Closed Principle (OCP)**: The project is open for extension but closed for modification, allowing new account types or functionalities without altering existing code.

3. **Liskov Substitution Principle (LSP)**: Subclasses like `SavingsAccount` and `CurrentAccount` can be used interchangeably with the `Account` class without impacting program correctness.

4. **Interface Segregation Principle (ISP)**: Interfaces separate actions, making each interface focused on specific functionalities, like deposit/withdrawal or account status.

5. **Dependency Inversion Principle (DIP)**: The project relies on abstractions rather than concrete classes, enhancing flexibility and testability.

### Technologies and Tools
- **Java**: Core language for implementing the banking module.
- **JDBC**: Used for database connectivity and data manipulation.
- **MySQL Workbench**: Manages account data in a relational database.
- **JUnit** (if applied): Unit testing each class and method.
- **Eclipse IDE**: Development environment for building and debugging.
