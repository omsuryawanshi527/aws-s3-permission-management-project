# AWS-S3-Bucket-Permission-Policy-Management-Public-Private-Deny-Rules-
 Bucket Permission &amp; Policy Management (Public, Private, Deny Rules)

📌 Project Overview

This project demonstrates how to manage and control access permissions in an Amazon S3 bucket using bucket policies and object-level permissions.
Different folders and files are configured with Public, Private, and Deny access rules to understand real-world S3 security behavior.

🏗️ Project Architecture (Design)

AWS S3 Bucket

Multiple folders with different permission rules

Bucket Policy

Public & Private object access

Browser URL testing

📂 S3 Folder Structure & Permissions
1️⃣ images/ Folder

Uploaded 2 image files

Image 1:

Public access enabled

Accessible via browser URL

Image 2:

Private access

Access denied when URL is opened

Purpose:
To understand public vs private object access in S3.

2️⃣ mydata/ Folder

Folder-level permission applied

Delete action is explicitly denied

Permission Rule:

❌ s3:DeleteObject – Denied

✅ Read & upload allowed (optional)

Purpose:
To prevent accidental or unauthorized deletion of critical data.

3️⃣ video/ Folder

Upload permission denied

Permission Rule:

❌ s3:PutObject – Denied

Existing objects cannot be overwritten or uploaded

Purpose:
To restrict users from uploading large or unwanted video files.

4️⃣ myfiles/ Folder

Uploaded an important file

Read access denied

Permission Rule:

❌ s3:GetObject – Denied

File is not accessible via browser URL

Purpose:
To secure confidential files from being viewed or downloaded.

🛡️ AWS Services Used

Amazon S3

IAM (Policy Management)

Bucket Policy

Object-level Permissions

⚙️ Implementation Steps

Created an S3 bucket

Created folders: images, mydata, video, myfiles

Uploaded sample files

Applied bucket policies for:

Public access

Private access

Upload deny

Read deny

Delete deny

Tested permissions using browser URLs

✅ Key Learnings

Difference between bucket policy and object permissions

How Deny rules override Allow

Securing sensitive data in S3

Real-time permission testing using browser access

📎 Use Case

This project is useful for:

Cloud security learning

AWS hands-on practice

Resume and interview projects

Real-world S3 access control scenarios

👨‍💻 Author

Om Suryawanshi
🔗 GitHub: https://github.com/omsuryawanshi527

