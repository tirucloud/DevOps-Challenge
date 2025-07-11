# 🚀 DevOps, Kubernetes, Terraform & Docker – 40 Interview Questions

### 1. You encounter a lock error when running `terraform apply`. What might resolve it?
A) Delete the `.terraform` directory
B) Run `terraform force-unlock` with the lock ID
C) Reinitialize with `terraform init`
D) Use the `-lock=false` flag

### 2. What does the `terraform refresh` command do?
A) Updates state file to match real-world resources
B) Resets the Terraform configuration
C) Deletes unused resources
D) Updates the provider plugin

### 3. What happens if a resource is removed from the Terraform configuration?
A) Ignored during apply
B) Deleted during apply
C) Error during plan
D) Prompts for confirmation

### 4. Which backend is commonly used to store Terraform state in AWS?
A) AWS DynamoDB
B) Amazon RDS
C) Amazon S3
D) AWS Lambda

### 5. How do you prevent sensitive data from being logged in state files?
A) Use `sensitive` argument
B) Encrypt manually
C) Use KMS
D) Use `.tfvars`

### 6. Which Terraform command is used to apply changes?
A) terraform init
B) terraform plan
C) terraform apply
D) terraform validate

### 7. How do you define a reusable module in Terraform?
A) .module file
B) Directory + module block
C) Custom provider
D) terraform block

### 8. Which provider config syntax is correct?
A) provider "aws" { region = "us-west-2" }
B) aws_provider {}
C) provider aws {}
D) aws {}

### 9. What does `terraform plan` do?
A) Applies changes
B) Validates syntax
C) Shows pending changes
D) Removes state

### 10. Which file should be `.gitignore`d?
A) main.tf
B) terraform.tfstate
C) variables.tf
D) outputs.tf

### 11. What is `terraform validate` for?
A) Apply config
B) Update provider
C) Check syntax
D) Clean state

### 12. How to upgrade providers?
A) terraform update
B) terraform refresh
C) terraform upgrade
D) terraform init -upgrade

### 13. Manage dev/prod environments?
A) Hardcode values
B) Workspaces or var files
C) Single `main.tf`
D) Local backend

### 14. How can you ensure that a pod is scheduled on a specific node?
A) Use a Node Selector
B) Use an Affinity Rule
C) Set a Node Label and use Node Affinity
D) All of the above

### 15. Which command can you use to debug a running Kubernetes pod?
A) kubectl logs
B) kubectl exec
C) kubectl describe pod
D) All of the above

### 16. You notice a pod in the `CrashLoopBackOff` state. What should you check first?
A) Logs of the failed pod
B) Node status
C) Kubernetes API server logs
D) Network policies

### 17. You need to securely inject sensitive data into a Kubernetes pod. What should you use?
A) ConfigMap
B) Secret
C) Environment Variables
D) Persistent Volume

### 18. What is the primary purpose of a Kubernetes Ingress?
A) Handle internal pod communication
B) Provide external HTTP and HTTPS routing to services
C) Allocate persistent storage
D) Monitor pod health

### 19. Which Kubernetes object maintains a specific number of pod replicas?
A) Deployment
B) StatefulSet
C) DaemonSet
D) ReplicaSet

### 20. What is the default restart policy for Kubernetes pods created by a Deployment?
A) Never
B) OnFailure
C) Always
D) Manual

### 21. How can you manually scale a deployment to 5 replicas?
A) kubectl scale replicas=5
B) kubectl edit deployment
C) kubectl scale deployment <name> --replicas=5
D) kubectl set replicas=5

### 22. What is the use of a ConfigMap in Kubernetes?
A) Securely store secrets
B) Expose services externally
C) Store non-sensitive configuration data
D) Schedule pods

### 23. What does `kubectl get all` return?
A) Only running pods
B) All Kubernetes resources in the cluster
C) All resources in the current namespace
D) All node logs

### 24. How do you create a Kubernetes resource from a YAML file?
A) kubectl install -f file.yaml
B) kubectl start -f file.yaml
C) kubectl apply -f file.yaml
D) kubectl deploy -f file.yaml

### 25. You want to run a container in the background and expose a port. Which command should you use?
A) docker run -it
B) docker run -d -p
C) docker exec -p
D) docker-compose up -d

### 26. How can you reduce the size of a Docker image during the build process?
A) Use a lightweight base image
B) Use multiple RUN commands
C) Include dev dependencies
D) Use ADD instead of COPY

### 27. You need a specific library version in a container. What do you do?
A) Specify in Docker Compose
B) Include in FROM directive
C) Use config at runtime
D) Multistage build

### 28. Which Docker command shows all containers?
A) docker ps
B) docker ps -a
C) docker container list
D) docker inspect

### 29. Container can't reach external API. What should you check first?
A) Container DNS config
B) CMD in Dockerfile
C) CPU allocation
D) Image version

### 30. What does `docker build` do?
A) Pull image
B) Create volume
C) Build from Dockerfile
D) Install Docker

### 31. What is the default Docker network driver?
A) Host
B) None
C) Bridge
D) Overlay

### 32. ENTRYPOINT vs CMD difference?
A) CMD > ENTRYPOINT
B) ENTRYPOINT = command, CMD = args
C) CMD runs first
D) No difference

### 33. Remove all stopped containers?
A) stop --all
B) rm $(docker ps -a -q)
C) clean
D) kill -a

### 34. Purpose of `.dockerignore`?
A) Ignore errors
B) Exclude from startup
C) Exclude from build context
D) Disable features

### 35. What type of Kubernetes service exposes an app to the internet?
A) ClusterIP
B) NodePort
C) LoadBalancer
D) ExternalName

### 36. What is a ClusterIP service?
A) Internet access
B) Internal-only
C) Node-pod link
D) DNS

### 37. What is a NodePort service?
A) High port on Node
B) Internal only
C) Used with Ingress
D) Expose pod on port 80

### 38. What does CoreDNS do?
A) Monitors network
B) DNS for pods/services
C) Node balancer
D) Manages ingress

### 39. What is ExternalName service type?
A) Internal traffic
B) DNS alias to external
C) Load balances pods
D) Host port

### 40. Which component handles Ingress routing?
A) kube-proxy
B) Ingress Controller
C) CoreDNS
D) etcd


---

## ✅ Answer Key

1. B
2. A
3. B
4. C
5. A
6. C
7. B
8. A
9. C
10. B
11. C
12. D
13. B
14. D
15. D
16. A
17. B
18. B
19. D
20. C
21. C
22. C
23. C
24. C
25. B
26. A
27. B
28. B
29. A
30. C
31. C
32. B
33. B
34. C
35. C
36. B
37. A
38. B
39. B
40. B
