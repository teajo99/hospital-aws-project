#  Hospital Portal – AWS Cloud Architecture Project

A scalable hospital web system built on AWS demonstrating cloud fundamentals including compute, auto scaling, load balancing, monitoring, and NoSQL database design.

---

##  Project Overview

This project simulates a **hospital patient management system** deployed on AWS. It is designed to handle variable traffic (500K+ users conceptually) using cloud-native services for scalability, reliability, and monitoring.

The system automatically scales based on demand, routes traffic efficiently, and stores patient data securely in a managed NoSQL database.

---

## Architecture Components

- **Compute Layer:** Amazon EC2
- **Auto Scaling:** EC2 Auto Scaling Group
- **Load Balancing:** Application Load Balancer (ALB)
- **Database:** Amazon DynamoDB
- **Monitoring:** Amazon CloudWatch
- **Storage (EC2 root volume):** EBS gp3

---

##  AWS Services Used

- :contentReference[oaicite:0]{index=0} – Hosts the hospital web application  
- :contentReference[oaicite:1]{index=1} – Automatically scales instances based on CPU load  
- :contentReference[oaicite:2]{index=2} – Distributes traffic across multiple EC2 instances  
- :contentReference[oaicite:3]{index=3} – Stores patient records and hospital data  
- :contentReference[oaicite:4]{index=4} – Monitors CPU, network, and system performance  

---

## Key Features

- Auto-scaling EC2 instances based on CPU utilization
- Load-balanced traffic across multiple availability zones
- Real-time monitoring using CloudWatch metrics and alarms
- Serverless-style database using DynamoDB
- Manual data entry for hospital patient records
- Fault-tolerant and highly available architecture

---

## Sample Data (DynamoDB)

### Patients Table
| PatientID | Name       | Age | Condition |
|-----------|------------|-----|----------|
| 1         | Fatimo Y   | 21  | Fever    |
| 2         | Tomson P   | 76  | Cold     |
| 3         | Racheal    | 19  | Headache |

---

## System Flow

User → ALB → EC2 → DynamoDB
↓
CloudWatch
↓
Auto Scaling



---

##  What I Learned

- How cloud auto scaling reacts to CPU demand
- How load balancers distribute traffic across instances
- How DynamoDB stores structured hospital data without servers
- How CloudWatch monitors system health and triggers alerts
- How EC2 integrates with IAM roles and AWS services

---

##  Project Goal

To build a real-world cloud architecture simulating a hospital system that is:
- Scalable
- Highly available
- Monitored in real-time
- Secure and distributed

---

## Future Improvements

- Add backend API (Node.js / Python Flask)
- Add authentication system for patients and doctors
- Add frontend dashboard UI
- Connect real-time health data streams
- Add encryption for DynamoDB

---

##  Author

Built as a hands-on AWS cloud engineering learning project.

---

##  Status

✔ Completed – Core cloud architecture deployed and tested
