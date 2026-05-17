Architecture Diagram
![image alt](https://github.com/teajo99/hospital-aws-project/blob/9c2318bf0e383dc1543c81738b50ca998144698d/scalable-hospital-system-aws/Architecture%20Diagram.png)

#  Hospital Portal – AWS Cloud Architecture Project

A scalable hospital web application built on AWS demonstrating real-world cloud engineering concepts including compute, auto scaling, load balancing, monitoring, and database integration.

---

##  Project Overview

This project simulates a hospital patient portal designed to handle high traffic using AWS cloud services. The system is fully scalable, monitored, and designed with high availability principles.

The application is deployed using EC2 instances that automatically scale based on demand and are distributed via a load balancer. Patient data is stored in a managed NoSQL database.

---

##  AWS Architecture

User → Application Load Balancer → EC2 Instances → index.html
↓
DynamoDB
↓
CloudWatch
↓
Auto Scaling Group


---

##  AWS Services Used

- :contentReference[oaicite:0]{index=0} – Hosts the hospital web application  
- :contentReference[oaicite:1]{index=1} – Automatically scales EC2 instances based on CPU usage  
- :contentReference[oaicite:2]{index=2} – Distributes traffic across multiple EC2 instances  
- :contentReference[oaicite:3]{index=3} – Stores patient records and hospital data  
- :contentReference[oaicite:4]{index=4} – Monitors CPU usage, system health, and triggers alarms  

---

## Project Files

- `index.html` → Simple hospital portal frontend UI  
- `user-data.sh` → EC2 bootstrap script that installs and configures web server automatically  
- `README.md` → Project documentation  

---

##  Deployment Flow

1. EC2 instance launches using a Launch Template  
2. `user-data.sh` automatically installs and configures web server  
3. Application Load Balancer distributes traffic across instances  
4. Auto Scaling Group adjusts capacity based on CPU load  
5. CloudWatch monitors system performance and triggers alarms  
6. DynamoDB stores patient data securely  

---

##  Sample DynamoDB Data

### Patients Table

| PatientID | Name       | Age | Condition |
|----------|------------|-----|----------|
| 1        | Fatimo Y   | 21  | Fever    |
| 2        | Tomson P   | 76  | Cold     |
| 3        | Racheal    | 19  | Headache |

---

##  Key Features

- Auto-scaling infrastructure based on demand
- Load-balanced traffic across multiple availability zones
- Real-time monitoring using CloudWatch
- Serverless NoSQL database (DynamoDB)
- Automated EC2 setup using user-data script
- Simple hospital UI (HTML-based)

---

##  What I Learned

- Designing scalable AWS architectures
- Configuring EC2 Auto Scaling Groups
- Using Application Load Balancers effectively
- Working with DynamoDB as a NoSQL database
- Monitoring infrastructure using CloudWatch
- Automating EC2 setup using user-data scripts

---

##  Project Goal

To build a real-world cloud architecture simulating a hospital system that is:
- Highly available
- Auto scalable
- Monitored in real time
- Cloud-native and serverless where possible

---

##  Future Improvements

- Add backend API (Node.js / Python Flask)
- Add authentication system for users and doctors
- Replace static HTML with dynamic frontend (React)
- Add encryption for DynamoDB tables
- Implement CI/CD pipeline

---

##  Author

Built as a hands-on AWS cloud engineering project to demonstrate real-world infrastructure skills.

---

##  Status

✔ Completed – Fully functional AWS cloud architecture deployed and tested
