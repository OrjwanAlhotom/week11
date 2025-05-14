Week11 Progress Plan 

---

Full Assignment Requirements

1. GitHub Content
README.md includes:

Brief explanation of the project goal

Detailed summary of all steps taken

Tools/services used (Terraform, Ansible, EC2, S3, MongoDB Atlas, IAM)

Challenges encountered and how they were solved

Cleanup steps (terraform destroy, revoking IAM credentials)
All Terraform configuration files stored in terraform/
Ansible playbook placed inside ansible/roles/backend/
screenshots/ folder includes:
pm2-backend.png
mongodb-cluster.png
media-upload-success.png
s3-frontend.png




---

Success Criteria
Frontend is deployed and accessible via S3 static website
Backend is deployed on EC2 and managed via PM2 using Ansible
MongoDB Atlas is successfully connected
Media uploads are correctly stored in the S3 media bucket
All four screenshots captured and documented

![Architecture Diagram](Diagram/diagram.png)
## Screenshots

### PM2 Backend
![PM2 Backend](screenshots/pm2-backend.jpeg)

### MongoDB Cluster
![MongoDB Cluster](screenshots/mongodb-cluster.jpeg)

### Media Upload Success
![Media Upload](screenshots/media-upload.jpeg)

### S3 Frontend Hosting
![S3 Frontend](screenshots/s3-fronted.jpeg)

### Upload Success (Extra)
![Upload Success](screenshots/upload-success.jpeg)
---

Completed Tasks

Terraform:
terraform init
terraform plan
terraform apply
Created IAM user and applied correct IAM policies
S3 buckets for frontend and media successfully created

Security group configured for ports 22, 80, and 5000

EC2 instance successfully created and connected with correct Key Pair


Backend Setup:
 MongoDB connection string added in .env

Ansible playbook successfully provisioned backend instance
PM2 started and is managing index.js


Frontend:
Frontend tested locally using Vite
Frontend built and deployed to S3 bucket


Screenshots:
pm2-backend.png
mongodb-cluster.png
media-upload-success.png
s3-frontend.png



---

Challenges Faced:

Node.js was not installed globally at first – fixed by using Ansible provisioning.

Missing Key Pair during Terraform EC2 provisioning – solved by creating and referencing a valid key.

MongoDB was not connected initially – resolved by correcting the connection string in the .env file.

Vite build errors due to dependency mismatch – fixed using npm install --legacy-peer-deps

AWS credentials were mistakenly pushed – removed and keys revoked immediately.



---

Final Assessment:

✅ All requirements have been completed 100% and the assignment is ready for submission.
