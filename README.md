# ✈️ Airline Ticket Booking System (AWS Cloud Project)

## 📌 Overview
This project is a **cloud-based Airline Ticket Booking System** built on AWS.  
It allows users to search for flights, book tickets, and receive automatic confirmation emails.

## 🛠️ AWS Services Used
- **Amazon S3** → Hosts the static website (frontend)  
- **Amazon API Gateway** → Exposes REST APIs for frontend-backend communication  
- **AWS Lambda (Python)** → Serverless backend for booking & search functionality  
- **Amazon DynamoDB** → NoSQL database for storing flights & bookings  
- **Amazon SES** → Sends email confirmations after booking  

## 🚀 Features
- Search for available flights (From, To, Date)  
- Book a ticket with name & email  
- Automatic **booking confirmation email** (SES)  
- Updates **available seats** in DynamoDB  
- Scalable, serverless, and cost-efficient architecture  


## 📸 Architecture
![Architecture Diagram](<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/d6734a03-93ae-41d0-bd66-18ed32de9325" />
)

## 🧠 Learnings
- Learned AWS **S3 hosting**, **API Gateway + Lambda integration**, and **DynamoDB schema design**  
- Understood how to fix **CORS issues** by enabling headers in API Gateway & Lambda  
- Learned **SES sandbox restrictions** (only verified emails work in testing)  
- Strengthened debugging skills using **CloudWatch logs** & API Gateway execution logs  

## 🚧 Challenges
- At first, the **confirmation email was not delivered** after booking.  
  - My guide suggested two checks:  
    1. Try hosting frontend on **EC2** to test if the issue was with S3.  
    2. Verify the **API Gateway invoke URL** in the frontend code.  
  - This helped me identify the problem and fix it step by step.  


👨‍💻 Developed by **K. Pavan Kumar**  
