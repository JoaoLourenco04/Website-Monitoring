# Website Monitoring System

A full-stack web application designed to monitor website availability and performance in real time.

The system automatically performs health checks on registered websites, tracks their HTTP status and response times, stores monitoring history, and provides a visual dashboard with performance metrics and charts.

This project was independently developed during my Full-Stack Development internship at TSS Ciberseguridad.

---

## Features

- Add, edit and remove websites
- Automatic scheduled website monitoring
- Manual website health checks
- Online, Offline and Unknown status detection
- HTTP status code tracking
- Response time monitoring
- Monitoring history
- Performance charts with different time intervals
- Dashboard with monitoring statistics and recent checks
- Automatic email alerts when a website becomes unavailable
- Daily monitoring summary emails
- Application settings
- Dark mode

---

## Tech Stack

### Backend

- Java 21
- Spring Boot
- Spring Data JPA
- Hibernate
- JavaMail
- Gradle

### Frontend

- React
- JavaScript
- HTML5
- CSS3
- Recharts
- Vite

### Database

- MySQL

### Tools

- Git
- GitHub
- Postman

---

## Project Structure

```text
WebsiteMonitoring/
│
├── src/                         # Spring Boot backend
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   └── test/
│
├── WebsiteMonitoringFrontend/   # React frontend
│   ├── src/
│   ├── public/
│   └── package.json
│
├── gradle/
├── build.gradle
├── settings.gradle
├── gradlew
├── gradlew.bat
└── README.md
```

---

## Requirements

Before running the project, make sure you have the following installed:

- **Java JDK 21**
- **MySQL**
- **Node.js**
- **npm**
- **Git**

You can verify the installations using:

```bash
java -version
node -v
npm -v
git --version
```

The Java version should be **Java 21**.

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/JoaoLourenco04/Website-Monitoring.git
```

Then navigate to the project directory:

```bash
cd Website-Monitoring
```

---

## Database Setup

The application uses **MySQL** for data persistence.

Create a MySQL database for the application:

```sql
CREATE DATABASE website_monitoring;
```

Then configure your database connection in:

```text
src/main/resources/application.properties
```

Example configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/website_monitoring
spring.datasource.username=YOUR_MYSQL_USERNAME
spring.datasource.password=YOUR_MYSQL_PASSWORD
```

Replace the username and password with your local MySQL credentials.

> Do not commit real passwords or credentials to the repository.

---

## Running the Backend

The backend is built with **Java 21, Spring Boot and Gradle**.

### Windows

From the root directory:

```bash
gradlew.bat bootRun
```

### macOS / Linux

```bash
./gradlew bootRun
```

Alternatively, the application can be started from an IDE such as IntelliJ IDEA by running the Spring Boot main application class.

Once started, the backend will be available locally through the port configured by Spring Boot.

---

## Running the Frontend

Open another terminal and navigate to the frontend directory:

```bash
cd WebsiteMonitoringFrontend
```

Install the required dependencies:

```bash
npm install
```

Start the Vite development server:

```bash
npm run dev
```

Vite will display the local URL in the terminal, usually:

```text
http://localhost:5173
```

Open this address in your browser to access the application.

---

## Email Configuration

The application supports email notifications for website downtime and daily monitoring summaries.

If email functionality is enabled, configure the SMTP credentials through environment variables or your local application configuration.

Example:

```properties
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=${MAIL_USERNAME}
spring.mail.password=${MAIL_PASSWORD}
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true
```

Set the required environment variables locally:

```text
MAIL_USERNAME=your-email@example.com
MAIL_PASSWORD=your-app-password
```

> Never publish your real email password, Gmail App Password, database password, API keys or other credentials on GitHub.

---

## How It Works

The backend periodically checks each registered website and records information such as its availability, HTTP status code and response time.

Each health check is stored in the database, allowing the application to maintain a monitoring history and generate performance statistics.

The React frontend consumes the REST API and provides a dashboard where users can view the current status of their websites, analyse historical data and manage the websites being monitored.

When a website changes from **Online to Offline**, the system can automatically send an email notification. The application can also generate and send a daily monitoring summary.

---

## Main Technologies

`Java 21` `Spring Boot` `React` `MySQL` `Hibernate` `Spring Data JPA` `REST API` `Recharts` `Gradle` `Vite`

---

## Project Context

This application was developed as an individual project during my **Full-Stack Development internship at TSS Ciberseguridad**.

The project allowed me to work across the complete development process, including:

- Backend development
- Database persistence
- REST API design
- Frontend development
- Frontend-backend integration
- Automated scheduled tasks
- Email notifications
- Testing
- Debugging

---

## Author

**João Lourenço**

LinkedIn: [João Lourenço](https://www.linkedin.com/in/joão-lourenço-41762b254/)

GitHub: [JoaoLourenco04](https://github.com/JoaoLourenco04)
