# Website Monitoring System

A full-stack web application designed to monitor website availability and performance in real time.

The system automatically performs health checks on registered websites, tracks their HTTP status and response times, stores monitoring history, and provides a visual dashboard with performance metrics and charts.

This project was independently developed during my Full-Stack Development internship at TSS Ciberseguridad.

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

## How It Works

The backend periodically checks each registered website and records information such as its availability, HTTP status code and response time.

Each health check is stored in the database, allowing the application to maintain a monitoring history and generate performance statistics.

The React frontend consumes the REST API and provides a dashboard where users can view the current status of their websites, analyse historical data and manage the websites being monitored.

When a website changes from Online to Offline, the system can automatically send an email notification. The application can also generate and send a daily monitoring summary.

## Main Technologies

`Java` `Spring Boot` `React` `MySQL` `Hibernate` `Spring Data JPA` `REST API` `Recharts`

## Project Context

This application was developed as an individual project during my Full-Stack Development internship at TSS Ciberseguridad.

The project allowed me to work across the complete development process, including backend development, database persistence, REST API design, frontend development, frontend-backend integration, automated tasks, email notifications, testing and debugging.

## Author

**João Lourenço**

LinkedIn: [João Lourenço](https://www.linkedin.com/in/joão-lourenço-41762b254/)
