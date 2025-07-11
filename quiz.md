
# 🚀 DevOps, Kubernetes, Terraform & Docker – 40 Interview Questions with Answers

Sharpen your skills with these categorized multiple-choice questions. Each question comes with the correct answer and a short explanation.

---

## 🛠 Terraform

### 1. You encounter a lock error when running `terraform apply`. What might resolve it?
A) Delete the `.terraform` directory  
B) Run `terraform force-unlock` with the lock ID  
C) Reinitialize with `terraform init`  
D) Use the `-lock=false` flag  
**✅ Correct Answer: B** – Releases a stuck lock in the state file.

### 2. What does the `terraform refresh` command do?
A) Updates state file to match real-world resources  
B) Resets the Terraform configuration  
C) Deletes unused resources  
D) Updates the provider plugin  
**✅ Correct Answer: A** – Ensures Terraform reflects actual infrastructure.

### 3. What happens if a resource is removed from the Terraform configuration?
A) Ignored during apply  
B) Deleted during apply  
C) Error during plan  
D) Prompts for confirmation  
**✅ Correct Answer: B**

### 4. Which backend is commonly used to store Terraform state in AWS?
A) AWS DynamoDB  
B) Amazon RDS  
C) Amazon S3  
D) AWS Lambda  
**✅ Correct Answer: C**

### 5. How do you prevent sensitive data from being logged in state files?
A) Use `sensitive` argument  
B) Encrypt manually  
C) Use KMS  
D) Use `.tfvars`  
**✅ Correct Answer: A**

### 6. Which Terraform command is used to apply changes?
A) terraform init  
B) terraform plan  
C) terraform apply  
D) terraform validate  
**✅ Correct Answer: C**

### 7. How do you define a reusable module in Terraform?
A) `.module` file  
B) Directory + module block  
C) Custom provider  
D) terraform block  
**✅ Correct Answer: B**

### 8. Which provider config syntax is correct?
A) `provider "aws" { region = "us-west-2" }`  
B) `aws_provider {}`  
C) `provider aws {}`  
D) `aws {}`  
**✅ Correct Answer: A**

### 9. What does `terraform plan` do?
A) Applies changes  
B) Validates syntax  
C) Shows pending changes  
D) Removes state  
**✅ Correct Answer: C**

### 10. Which file should be `.gitignore`d?
A) main.tf  
B) terraform.tfstate  
C) variables.tf  
D) outputs.tf  
**✅ Correct Answer: B**

### 11. What is `terraform validate` for?
A) Apply config  
B) Update provider  
C) Check syntax  
D) Clean state  
**✅ Correct Answer: C**

### 12. How to upgrade providers?
A) terraform update  
B) terraform refresh  
C) terraform upgrade  
D) terraform init -upgrade  
**✅ Correct Answer: D**

### 13. Manage dev/prod environments?
A) Hardcode values  
B) Workspaces or var files  
C) Single `main.tf`  
D) Local backend  
**✅ Correct Answer: B**

---

## ☸️ Kubernetes

### 14. Pod on specific node?
A) Node Selector  
B) Affinity Rule  
C) Node Label + Affinity  
D) All  
**✅ Correct Answer: D**

### 15. Debug a pod?
A) logs  
B) exec  
C) describe  
D) All  
**✅ Correct Answer: D**

### 16. Pod in `CrashLoopBackOff`, check?
A) Logs  
B) Node  
C) API server  
D) Network  
**✅ Correct Answer: A**

### 17. Secure data in pod?
A) ConfigMap  
B) Secret  
C) Env vars  
D) PV  
**✅ Correct Answer: B**

### 18. Purpose of Ingress?
A) Pod-to-pod  
B) External HTTP/HTTPS  
C) Persistent storage  
D) Health check  
**✅ Correct Answer: B**

### 19. Maintain pod replicas?
A) Deployment  
B) StatefulSet  
C) DaemonSet  
D) ReplicaSet  
**✅ Correct Answer: D**

### 20. Default pod restart policy?
A) Never  
B) OnFailure  
C) Always  
D) Manual  
**✅ Correct Answer: C**

### 21. Scale deployment to 5?
A) scale replicas=5  
B) edit deployment  
C) scale deployment --replicas=5  
D) set replicas=5  
**✅ Correct Answer: C**

### 22. Use of ConfigMap?
A) Secrets  
B) External access  
C) Config storage  
D) Scheduling  
**✅ Correct Answer: C**

### 23. `kubectl get all` shows?
A) Pods only  
B) All cluster resources  
C) All in namespace  
D) Node logs  
**✅ Correct Answer: C**

### 24. Apply YAML config?
A) install -f  
B) start -f  
C) apply -f  
D) deploy -f  
**✅ Correct Answer: C**

---

## 🐳 Docker

### 25. Run in background and expose port?
A) `run -it`  
B) `run -d -p`  
C) `exec -p`  
D) `compose up -d`  
**✅ Correct Answer: B**

### 26. Reduce image size?
A) Lightweight base image  
B) Many RUNs  
C) Add dev deps  
D) Use ADD  
**✅ Correct Answer: A**

### 27. Lock base version?
A) Compose file  
B) FROM version  
C) Runtime config  
D) Multistage  
**✅ Correct Answer: B**

### 28. Show all containers?
A) ps  
B) ps -a  
C) container list  
D) inspect  
**✅ Correct Answer: B**

### 29. Container can't reach API?
A) DNS config  
B) CMD  
C) CPU  
D) Image  
**✅ Correct Answer: A**

### 30. `docker build` does what?
A) Pull image  
B) Create volume  
C) Build image from Dockerfile  
D) Install Docker  
**✅ Correct Answer: C**

### 31. Default network driver?
A) Host  
B) None  
C) Bridge  
D) Overlay  
**✅ Correct Answer: C**

### 32. ENTRYPOINT vs CMD?
A) CMD > ENTRYPOINT  
B) ENTRYPOINT = command, CMD = args  
C) CMD runs first  
D) Same  
**✅ Correct Answer: B**

### 33. Remove stopped containers?
A) stop --all  
B) rm $(docker ps -a -q)  
C) clean  
D) kill -a  
**✅ Correct Answer: B**

### 34. Purpose of `.dockerignore`?
A) Ignore errors  
B) Skip files on run  
C) Exclude from build context  
D) Disable features  
**✅ Correct Answer: C**

---

## 🌐 Kubernetes Networking

### 35. Internet-access service?
A) ClusterIP  
B) NodePort  
C) LoadBalancer  
D) ExternalName  
**✅ Correct Answer: C**

### 36. ClusterIP service?
A) Internet access  
B) Internal-only  
C) Node pod link  
D) DNS  
**✅ Correct Answer: B**

### 37. NodePort service?
A) High port on Node  
B) Internal only  
C) For Ingress  
D) Pod port 80  
**✅ Correct Answer: A**

### 38. CoreDNS does what?
A) Monitor policies  
B) DNS for pods/services  
C) Node balancing  
D) Ingress rules  
**✅ Correct Answer: B**

### 39. ExternalName service?
A) Internal traffic  
B) DNS alias to external  
C) Pod LB  
D) Host port  
**✅ Correct Answer: B**

### 40. Ingress traffic controller?
A) kube-proxy  
B) Ingress Controller  
C) CoreDNS  
D) etcd  
**✅ Correct Answer: B**
