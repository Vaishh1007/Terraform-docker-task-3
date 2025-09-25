# 🚀 Task 3: Infrastructure as Code (IaC) with Terraform

## 📌 Objective
Provision a **local Docker container** using **Terraform** to understand Infrastructure as Code (IaC).

---

## 🛠 Tools Used
- **Terraform**
- **Docker**

---

## 📂 Files
- `main.tf` → Terraform config
- `README.md` → Documentation
- `.gitignore` → Ignore state/lock files
- `screenshots/` → Screenshots of execution

---

## ⚙️ Steps to Run

### 1. Install Dependencies
```bash
terraform -v
docker -v
```
### 2. Initialize Terraform
```bash
terraform init
```
### 3. Preview Plan
```bash
terraform plan
```
### 4. Apply Config
```bash
terraform apply -auto-approve
```
👉 Visit: http://localhost:8080 → You should see the Nginx welcome page.

### 5. Verify
```bash
docker ps
terraform state list
```
### 6. Destroy Infra
```bash
terraform destroy -auto-approve
```
---
### 📸 Screenshots to Capture
1. terraform-init.png → Output of terraform init
2. terraform-plan.png → Output of terraform plan
3. terraform-apply.png → Output of terraform apply
4. docker-ps.png → Show running container (docker ps)
5. nginx-browser.png → Browser screenshot of http://localhost:8080
6. terraform-destroy.png → Output of terraform destroy
---
### ❓ Interview Questions
---
#### Q1. What is IaC?
Managing infrastructure via code, ensuring consistency and automation.

#### Q2. How does Terraform work?

It compares .tf config with infra state → generates plan → applies changes via providers.

#### Q3. What is Terraform state file?

A .tfstate file storing infra state.

#### Q4. Difference between apply and plan?

plan = preview changes, apply = execute changes.

#### Q5. What are Terraform providers?

Plugins to interact with external APIs (AWS, Docker, etc.).

#### Q6. Resource dependency?

Terraform builds infra in order (e.g., image before container).

#### Q7. Handle secrets?

Use .tfvars, environment variables, Vault/SSM.

#### Q8. Benefits of Terraform?

Consistency, automation, reproducibility, collaboration, versioning.


---
### ✅ Outcome

Learned IaC basics

Provisioned Docker container with Terraform

Verified deployment via CLI & browser

Destroyed infra safely


---

## 5️⃣ Verification Checklist
After `terraform apply`, check:
- `docker ps` → container `nginx_server` is running  
- Browser → [http://localhost:8080](http://localhost:8080) shows Nginx  
- `terraform state list` → shows image + container  

---
