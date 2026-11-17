# ATM Simulator System

A desktop-based ATM simulation application built using **Java Swing** and **MySQL**. The application provides a graphical interface for account registration, login, and common ATM transactions.

## Features

- **Account registration:** Multi-step form for entering personal, additional, and account details.
- **Login:** Sign in using a card number and PIN.
- **Deposit:** Record deposits against an account.
- **Cash withdrawal:** Withdraw a specified amount.
- **Fast cash:** Select a preset withdrawal amount.
- **Balance enquiry:** Calculate and display the account balance from transaction records.
- **Mini statement:** View recorded deposits and withdrawals.
- **PIN change:** Update the account PIN.

## Technology Stack

- **Language:** Java
- **GUI:** Java Swing / AWT
- **Database:** MySQL
- **Database connectivity:** JDBC (MySQL Connector/J)
- **IDE/project format:** Apache Ant / NetBeans project structure
- **Additional library:** JCalendar (date chooser)

## Project Structure

```text
ATM-Simulator-System/
├── src/
│   └── ASimulatorSystem/
│       ├── Login.java
│       ├── Signup.java
│       ├── Signup2.java
│       ├── Signup3.java
│       ├── Transactions.java
│       ├── Deposit.java
│       ├── Withdrawl.java
│       ├── FastCash.java
│       ├── BalanceEquiry.java
│       ├── MiniStatement.java
│       ├── Pin.java
│       ├── Conn.java
│       └── icons/
├── nbproject/
├── build.xml
└── README.md
```

The `build/` directory contains generated build output and is not required as source code.

## Prerequisites

Install/configure the following before running the application:

1. JDK (the supplied NetBeans project is configured for Java 8 source/target compatibility).
2. MySQL Server.
3. MySQL Connector/J.
4. JCalendar library (`jcalendar-tz-1.3.3-4.jar`).
5. NetBeans IDE with Ant project support, or a compatible Java IDE.

## Database Configuration

The connection is configured in `src/ASimulatorSystem/Conn.java`.

The current source uses:

- Database: `bankmanagementsystem`
- MySQL username: `root`
- MySQL password: currently hard-coded in the source

Before running the application:

1. Start MySQL Server.
2. Create the database named `bankmanagementsystem`.
3. Create the tables expected by the application: `signup`, `signup2`, `signup3`, `login`, and `bank`.
4. Update the JDBC URL, username, and password in `Conn.java` to match your local MySQL configuration.
5. Ensure the MySQL Connector/J driver is included in the project classpath.

### Database connection safety

Do not commit real database passwords or other credentials. For a public repository, replace hard-coded credentials with configuration supplied locally (for example, environment variables or a local, untracked configuration file). If a password has already been pushed publicly, change it.

## Running the Project

### Using NetBeans

1. Open NetBeans.
2. Select **File → Open Project**.
3. Select the folder containing `build.xml` and `nbproject`.
4. Add MySQL Connector/J and JCalendar to the project's libraries/classpath if they are not already configured.
5. Configure the MySQL database as described above.
6. Set the correct main class in the project run configuration if required.
7. Build and run the project.

The supplied project configuration contains a machine-specific JCalendar JAR path. Update it to the location of the JAR on your computer before building.

## Learning Outcomes

This project provides practical exposure to:

- Building desktop GUI applications with Java Swing.
- Connecting a Java application to MySQL using JDBC.
- Performing database operations for account and transaction records.
- Implementing event-driven interaction through Swing action listeners.
- Organising a multi-screen Java application.
