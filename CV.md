# Bojan Srdic - CV Reference

> This file is used as context for AI prompts when generating or updating CVs.
> Last updated: 2026-02-18

---

## Personal Info

- **Name**: Bojan Srdic
- **Title**: Software Engineer
- **Location**: Novi Sad, Serbia
- **Phone**: +381 655440460
- **Email**: srdicbb@gmail.com
- **GitHub**: github.com/BojanSrdic
- **LinkedIn**: linkedin.com/in/bojan-srdic-515477190/
- **Languages**: English (B2 intermediate), German (A2 elementary)

---

## About Me

Experienced software engineer dedicated to software improvement, in search of high quality solutions. Committed to continuous improvement, prioritize conceptual understanding over being overly dependent on specific technologies. In search for a dynamic work environment and an organization that nurtures a culture of learning.

---

## Technical Skills

### Primary Stack
- **Backend**: C#, .NET Core/.NET 5/.NET 6, .NET Framework
- **Frontend**: Angular, React, TypeScript, JavaScript
- **Mobile**: React Native
- **Databases**: MS SQL Server
- **ORM/Data Access**: Entity Framework, ADO.NET, Dapper

### Secondary / Tools
- **Messaging**: RabbitMQ, MQTT Broker
- **Containers**: Docker
- **Version Control**: Git
- **Testing**: Cypress, Cucumber
- **Real-time**: SignalR
- **Scripting**: Python
- **CI/CD**: Azure DevOps

### Embedded / IoT
- **Hardware**: ESP32, PMS5003 sensors, SCD41 sensors
- **Protocols**: MQTT, CAN communication, Automotive Ethernet
- **Low-level**: Linux kernel drivers, FPGA, character drivers

---

## Work Experience

### Tiac d.o.o., Novi Sad | Feb 2024 - Present
**Software Engineer**

Working as a Full-Stack Developer for FIS, developing a risk assessment solution using .NET (C#), MSSQL and Angular. Also mentoring interns on ESG-focused initiatives and leading the development of IoT projects involving real-time data monitoring and processing.

### VegaIT d.o.o., Novi Sad | Oct 2021 - Jan 2024
**Software Engineer**

Worked on commercial projects for international clients from Israel, the UK and the Netherlands. Primary technologies: .NET, ADO.NET, Entity Framework, Dapper, MS SQL Server, Cypress, Docker, TypeScript, React, RabbitMQ, Git.

### RT-RK d.o.o., Novi Sad | Dec 2020 - May 2021
**Automotive Embedded Engineer**

Realization of Linux drivers for automotive Ethernet transceiver (Linux Kernel, Automotive Ethernet, Character Driver). Logical design of computer systems (FPGA) - Data transfer between two development systems EasyPIC V7 and Arduino UNO achieved using CAN communication.

---

## Relevant Projects

### Risk Assessment Application for Financial Institutions
**Client**: FIS | **Stack**: .NET Core, Angular, MS SQL Server, SignalR, Cypress

- Large-scale risk assessment platform for economic trend analysis, market scenario modeling, and complex market data processing
- Migrating legacy desktop application to modern web-based architecture while preserving original ORM layer and core business logic
- Reverse-engineering and debugging legacy code, mapping non-standard desktop workflows to new REST endpoints
- Designed and implemented backend modules following clean REST principles
- Handled concurrency through custom LOCK mechanisms
- Supported multi-tenant architecture powered by AutoFac and SignalR for real-time communication
- Frontend: RxJS (Observables and Subjects), custom Control Value Accessors, interceptors, form controls, custom form validation logic, resolvers and route guards

### ESG - IoT Data Processing & Real-Time Monitoring Platform
**Stack**: .NET Core, Python, MQTT Broker, SignalR, Cron Jobs, MS SQL Server

- Initiated and led internal ESG R&D project, originally developed as part of internship program (served as technical mentor)
- Responsible for overall system architecture, technology decisions and technical coordination
- Backend in .NET Core, Python used for sensor simulation during early development
- Designed and implemented hardware solution using ESP32 microcontrollers with PMS5003 (particulate matter) and SCD41 (CO2) sensors
- Implemented public-private key cryptography for authenticating and encrypting sensor data
- Integrated MQTT for device-to-platform communication
- Created cron jobs for large-scale data processing
- Implemented SignalR for real-time data visualization
- Used Lavaable AI for React-based frontend prototyping
- Project matured from mentorship assignment into scalable prototype planned for further development

### Israeli Travel Agency
**Stack**: .NET Framework, ADO.NET, Angular, MS SQL Server, Cypress, Docker, TypeScript

- Accommodation booking platform similar to Booking.com (flights, hotels, tours)
- Backend development and SQL database management
- Refactored poorly written services, integrated with new external providers
- Proposed breaking 14-year-old monolith into microservices using .NET Core
- Proposed transitioning from ADO.NET to Dapper
- Navigated complex integration issues with external providers (including Trivago integration)
- Introduced automation testing using Cypress and Cucumber with Azure pipeline for daily tests
- Established end-to-end test coverage for core functionalities
- Introduced Pull Requests to improve development workflow

### Crypto Exchange (Internal Project)
**Stack**: .NET Core, Entity Framework, MS SQL Server, Docker, RabbitMQ

- Internal Vega project for deep understanding of cutting-edge technologies
- Microservices architecture with RabbitMQ queues, Docker, JWT Authentication, API Gateway
- Integration with external providers (CoinMarketCap API)
- Simulated real-time data processing
- Goal: deploy and simulate high user/transaction load for performance evaluation

### Linux Drivers for Automotive Ethernet Transceiver
**Role**: C Developer

- Developed Linux drivers for automotive Ethernet
- Configured drivers for auto-negotiation at 100Mbit/s and 1Gbit/s
- Supported master and slave modes
- Optimized driver performance and addressed compatibility issues
- Integrated industry standard advancements

---

## Education

- **Master of Science** - Faculty of Technical Sciences, University of Novi Sad - Applied Computer and Informatics (2021 - Present)
- **Bachelor of Science** - Faculty of Technical Sciences, University of Novi Sad - Energy, Electrical and Telecommunications

---

## Publications

- **"Realization of resonant pressure sensor"** - Co-author, published in cooperation with prof. Dr. Ljiljana Zivanov at International Software Systems Engineering Conference (ISSE) 2021

---

## Key Achievements & Differentiators

- Proposed and began migration of 14-year-old monolith to microservices architecture
- Introduced PR workflow and automated testing culture to a team that had neither
- Architected an IoT platform from scratch (hardware selection, crypto, MQTT, real-time visualization)
- Mentored interns who built a functional ESG prototype
- Unique background spanning embedded systems (Linux drivers, FPGA) to modern web development
- Published academic research while working in industry

---

## Skills In Progress (Learning Roadmap)

> See senior-dev-roadmap.md for full details

Currently focusing on:
- Design patterns (formal knowledge)
- System design and distributed systems
- AI/LLM ecosystem (RAG, vector databases, MCP)
- Kubernetes and cloud services
- Security fundamentals (OWASP Top 10)

---

## Notes for CV Generation

When generating a new CV from this data:
1. Tailor the "About Me" section to the target role
2. Reorder skills based on job requirements
3. Highlight relevant projects first
4. Include newly learned skills from the roadmap as they are completed
5. Keep it to 2 pages maximum for standard applications
6. The IoT + full-stack combination is a unique selling point - emphasize when relevant
7. Embedded background shows depth of understanding - use for senior/architect roles
