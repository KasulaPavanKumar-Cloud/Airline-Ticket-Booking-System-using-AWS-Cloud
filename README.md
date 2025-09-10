# ✈️ Serverless Airline Booking System

A **serverless airline ticket booking system** built on AWS where users can:
✅ Search available flights
✅ Book tickets
✅ Receive confirmation via **Email (SES)** and **SMS (SNS)**
✅ Access via a **custom domain + SSL (Route 53 + CloudFront)**

---

## 📌 Architecture

```mermaid
flowchart TD
  User[User] -->|Search/Book| CloudFront
  CloudFront --> S3[S3 (Frontend Website)]
  CloudFront --> APIGW[API Gateway]
  APIGW --> Lambda[Lambda Functions]
  Lambda --> DDB1[(DynamoDB Flights Table)]
  Lambda --> DDB2[(DynamoDB Bookings Table)]
  Lambda --> SES[Amazon SES (Email)]
  Lambda --> SNS[Amazon SNS (SMS)]
```

---

## ⚙️ Tech Stack

* **Frontend**: HTML, CSS, JavaScript (Hosted on S3 + CloudFront)
* **Backend**: AWS Lambda + API Gateway
* **Database**: DynamoDB (Flights & Bookings)
* **Notifications**: SES (Email), SNS (SMS)
* **Domain & Security**: Route 53, ACM, CloudFront (Custom Domain + SSL)

---

## 🚀 Features

* Flight search by **Source, Destination, Date**
* Ticket booking with **unique Booking ID**
* **Email/SMS notifications** after successful booking
* **Secure domain access** ([https://pa1all.space](https://pa1all.space))

---

## 📚 Learnings & Challenges

* Configuring **custom domains and SSL certificates** in Route 53 & ACM
* Handling DynamoDB **conditional updates** for seat availability
* Debugging IAM permission issues with Lambda
* Received **valuable guidance from mentor/sir** to fix configuration and policy errors

---

## 🛠️ Setup Instructions

1. Clone the repo:

   ```bash
   git clone https://github.com/pavankumarkasula73/Airline-Booking-System.git
   ```
2. Deploy backend with Lambda + API Gateway.
3. Set up DynamoDB tables (`Flights`, `Bookings`).
4. Configure SES (verify sender/recipient email).
5. Add your domain in Route 53 and connect via CloudFront + ACM.
6. Update frontend (`index.html`) with your API URL.

---

## 📸 Screenshots
<img width="1572" height="1018" alt="image" src="https://github.com/user-attachments/assets/9bb551c8-0e1d-4dba-aa06-62ce7015e0f0" />
<img width="1491" height="654" alt="image" src="https://github.com/user-attachments/assets/a0f09323-cd79-4e59-88bd-356dc7725b30" />


---

## 📌 Status

✅ Working and hosted at: **[https://pa1all.space](https://pa1all.space)**
