# AWS-S3-Bucket-Permission-Policy-Management-Public-Private-Deny-Rules-
 Bucket Permission &amp; Policy Management (Public, Private, Deny Rules)

## 📌 Project Overview
This project demonstrates real-world Amazon S3 permission and security management using
bucket policies and object-level permissions. Different folders in a single S3 bucket
are configured with specific allow and deny rules to control access.

This project is designed for AWS learning, interviews, and resume use.

---

## 🎯 Project Objectives
- Understand S3 bucket policies
- Implement public and private object access
- Restrict delete, upload, and read operations
- Apply security best practices in AWS S3

---

## 🏗️ Bucket Structure
s3-permission-demo-bucket
│
├── images/
│ ├── public-image.jpg (Public Read)
│ └── private-image.jpg (Private)
│
├── mydata/ (Delete Denied)
├── videos/ (Upload Denied)
└── myfiles/ (Read Denied)


---

## 🔧 AWS Services Used
- Amazon S3
- IAM
- Bucket Policy

---

## 🪜 Step-by-Step Implementation

### 1️⃣ Create S3 Bucket
- Create an S3 bucket
- Disable “Block all public access”
- Enable ACLs

---

### 2️⃣ Images Folder (Public & Private)
- Upload two images
- Make one image public using object permissions
- Keep the second image private

✅ Public image opens in browser  
❌ Private image shows Access Denied

---

### 3️⃣ mydata Folder – Delete Denied
**Bucket Policy**
```json
{
  "Effect": "Deny",
  "Principal": "*",
  "Action": "s3:DeleteObject",
  "Resource": "arn:aws:s3:::s3-permission-demo-*/mydata/*"
}
✔ Upload allowed
❌ Delete denied

4️⃣ videos Folder – Upload Denied
Bucket Policy

{
  "Effect": "Deny",
  "Principal": "*",
  "Action": "s3:PutObject",
  "Resource": "arn:aws:s3:::s3-permission-demo-*/videos/*"
}
❌ Upload denied

5️⃣ myfiles Folder – Read Denied
Bucket Policy

{
  "Effect": "Deny",
  "Principal": "*",
  "Action": "s3:GetObject",
  "Resource": "arn:aws:s3:::s3-permission-demo-*/myfiles/*"
}
❌ Browser URL access denied

🧪 Testing Summary
Folder	Permission Tested	Result
images	Public Read	✅ Allowed
images	Private Read	❌ Denied
mydata	Delete	❌ Denied
videos	Upload	❌ Denied
myfiles	Read	❌ Denied
📁 Repository Structure
aws-s3-permission-management-project/
│
├── README.md
├── policies/
│   ├── delete-deny-mydata.json
│   ├── upload-deny-videos.json
│   └── read-deny-myfiles.json
│
└── screenshots/
📌 Resume Description
AWS S3 Permission Management Project
Implemented secure Amazon S3 bucket policies to control public and private access,
restrict delete, upload, and read operations for sensitive data following AWS best practices.

✅ Author
Om Suryawanshi


