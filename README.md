# 🌐 Personal Blogging Platform on AWS 

Welcome to my **end-to-end DevOps Portfolio Project** a production-grade **personal blog platform** powered by **Hugo** and hosted on **AWS**. 
This project is designed to demonstrate real-world skills in **Cloud Infrastructure, CI/CD, Security, Monitoring**, and even **Chaos Engineering**; going far beyond tutorials and certificates.

---

## 📌 Live Demo
👉 [https://my-blog-domain.com](https://my-blog-domain.com)

---

## 🏗️ Project Architecture

![image](https://github.com/user-attachments/assets/2a80e80a-f967-4fda-82d4-e15414590a92)


---

## 🚀 Key Features

✅ **Hugo** Static Site Generator  
✅ **AWS S3** Static Website Hosting  
✅ **AWS CloudFront** for global CDN & HTTPS  
✅ **AWS Route53** for Custom Domain  
✅ **AWS ACM** for SSL/TLS Certificate  
✅ **CloudFormation** for complete Infrastructure-as-Code  
✅ **GitHub Actions** for automated CI/CD Pipeline  
✅ **AWS Secrets Manager** for secure credential management  
✅ **AWS CloudWatch** for logs and metrics  
✅ **Chaos Engineering** using AWS FIS *(Fault Injection Simulator)*  

---

## 🔧 Tech Stack

| Layer             | Tool/Service                  |
|------------------|-----------------------------|
| Blog Framework    | [Hugo](https://gohugo.io)    |
| Cloud Provider    | AWS                         |
| Hosting          | S3 + CloudFront + Route 53   |
| CI/CD            | GitHub Actions               |
| Infrastructure   | AWS CloudFormation (YAML)    |
| Secrets Mgmt     | AWS Secrets Manager          |
| Monitoring       | AWS CloudWatch               |
| Chaos Testing    | AWS FIS (Fault Injection)    |

---

## ⚙️ Deployment — CI/CD Workflow (GitHub Actions)

- **Trigger:** On `push` to `main` branch
- **Steps:**
  1. Checkout Code
  2. Install Hugo
  3. Build Site (`hugo`)
  4. Deploy to AWS S3 using `s3-sync`
  5. Invalidate CloudFront Cache (optional)
  
See [`.github/workflows/deploy.yml`](./.github/workflows/deploy.yml) for details.

---

## 🔒 Security Highlights

- **S3 Bucket Policies** — private access blocked; served only via CloudFront  
- **IAM Roles** — fine-grained permissions for GitHub Actions  
- **AWS Secrets Manager** — no hardcoded secrets or AWS keys  
- **HTTPS enforced** via ACM + CloudFront  
- **Container Scanning** (if Dockerized Hugo used) with Trivy *(optional)*  

---

## 📈 Monitoring & Logging

- **CloudWatch Metrics & Logs:**  
  - S3 access logs  
  - CloudFront request metrics  
  - Error rates & latency  

- Optional: Export CloudFront metrics to **Grafana dashboards** (coming soon).

---

## ⚡ Chaos Engineering (AWS FIS)

Simulated failures to test resilience:
- Inject S3 latency
- Throttle CloudFront origin requests
- Simulate regional outage
*(See `chaos/fis-experiment-template.yaml` for details)*

---

## 📂 Project Structure

![image](https://github.com/user-attachments/assets/72637b0f-be29-4325-9270-90ca2b4eda8b)


---

## 📝 Future Enhancements

- [ ] Automatic CloudFront Cache Invalidation  
- [ ] Multi-environment Support (Dev, Staging, Prod)  
- [ ] Terraform version of infra  
- [ ] Grafana + Prometheus monitoring stack  

---

## 🙌 Acknowledgements

- [Hugo](https://gohugo.io)  
- [AWS Free Tier](https://aws.amazon.com/free/)  
- [GitHub Actions](https://github.com/features/actions)  

---

## 👤 Author

**Sujoy Roy**  
🔗 [LinkedIn](https://www.linkedin.com/in/sujoys/)  
🌐 [Sujoy's Personal Blog](https://sujoyshub.github.io)  

---

## 🏆 Why This Project?

> "Because running production-grade systems, with real monitoring, security, infrastructure-as-code, and failure simulations; beats any online tutorial or certification. This is *real DevOps practice*."

---





