Login & Signup Website with AWS ALB
📌 Project Overview

This project demonstrates hosting simple Login and Signup web pages on two EC2 instances using an AWS Application Load Balancer (ALB) with path-based routing.
Requests to /login/ and /signup/ are routed to different target groups, each linked to an EC2 instance.

🚀 Project Architecture

EC2 Instances

Instance 1 → Hosts Login Page (/login/)

Instance 2 → Hosts Signup Page (/signup/)

Target Groups

Target Group 1 → Mapped to Instance 1 (Login)

Target Group 2 → Mapped to Instance 2 (Signup)

Application Load Balancer

Listener: Port 80

Rules:

/login/* → Target Group 1

/signup/* → Target Group 2

🛠️ Steps Performed

Created HTML pages using nano:

nano /var/www/html/login/index.html

nano /var/www/html/signup/index.html

Launched two EC2 instances (Amazon Linux 2 / Ubuntu with Apache or Nginx).

Created Target Groups in ALB:

Target1 → Instance1

Target2 → Instance2

Configured Application Load Balancer (ALB):

Listener on port 80

Rules:

/login/* → Target1

/signup/* → Target2

Testing:

http://<ALB-DNS>/login/ → Displays Login Page

http://<ALB-DNS>/signup/ → Displays Signup Page

📂 Project Structure
/var/www/html/
 ├── login/
 │    └── index.html   # Login page
 └── signup/
      └── index.html   # Signup page

🎯 Outcome

This project demonstrates how to use AWS ALB with path-based routing to host multiple applications (Login and Signup) behind a single DNS endpoint.
