# HeroPay
---
## Project Description
---

Expense reimbursement system hosted on an S3 bucket and ran on an EC2. The aim is to allow a single website (SPA) to allow employees to create reimbursement requests and allow managers to accept or reject them. This information is persisted in an RDS instance to help keep track of previous requests and track various statistics of each employee.

---

## Technologies Used
---

- JavaScript
- HTML
- CSS
- JWT
- PostgreSQL
- Java 8
- Javalin
- Hibernate
- Mockito
- JUnit 5
- Maven

---

## Features
---

- SPA website using DOM manipulation through JavaScript
- RESTful API server
- JWT generationi and validation enforcing REST logins
- Hosted fully remotely using the AWS technologies

---

## Getting Started
---

```
#Create a local git repository using git clone
git clone git@github.com:DementedTiger/HeroPay.git
cd HeroPay
# Start working on the project

# If HTTP is preferred incase an ssh key is not setup
git clone https://github.com/DementedTiger/HeroPay.git
cd HeroPay
```
---
## Usage

Essential requirements
- Jave JDK 8
- Maven
- An RDS system or installed on a local machine

For remote capabilities:
- A running EC2 instance to host the app
- A running RDS instance to host the database
- An S3 bucket using static website hosting

Steps to get it running:
1. Package the application using Maven with `mvn clean package` within the file folder in a cli
3. Copy the jar package into an EC2 instance
4. Run it using either a Jenkins pipeline (not covered here) or `nohup java -jar <jar-file-name> &>`
5. Place the HTML, CSS and Scripts into the S3 bucket and ensure public access
6. Change the security group of the EC2 to allow access from the RDS instance
7. Assign a role to the EC2 to allow access by the S3 bucket (more details [here](https://aws.amazon.com/premiumsupport/knowledge-center/ec2-instance-access-s3-bucket/)
8. Make sure the RDS instance DB has the SQL scripts ran that generate the required tables
9. Populate the tables with user logins needed to access the website
10. Complete.
