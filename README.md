# AWS Static Portfolio Website (S3 + CloudFront)

## 📌 Project Overview
This project demonstrates how to host a responsive static portfolio website using **AWS S3** and serve it securely over **HTTPS using CloudFront**.  
The goal of this task is to understand cloud object storage, static website hosting, CDN usage, caching, and HTTPS configuration.

The website is a single-page portfolio built with HTML and CSS and deployed using real-world AWS best practices.

---

## 🚀 Live Website
👉 **Live URL (CloudFront HTTPS):**  
https://dm2c82tdaajp5.cloudfront.net/

---

## 🛠️ Technologies Used
- HTML5
- CSS3
- AWS S3 (Static Website Hosting)
- AWS CloudFront (CDN + HTTPS)
- Git & GitHub

---

## 📂 Project Structure
.
├── index.html
├── styles.css
├── assets
│ └── screenshots
│ ├── 01-live-site-cloudfront.png
│ ├── 02-cloudfront-distribution.png
│ ├── 03-cloudfront-https-policy.png
│ ├── 04-s3-bucket-overview.png
│ ├── 05-s3-static-hosting.png
│ └── 06-s3-bucket-policy.png
└── README.md


---

## 🧩 Features
- Responsive single-page portfolio layout
- Hero section with CTA button
- Projects section with three project cards
- Footer with contact details
- Hosted on AWS S3
- Secured using CloudFront HTTPS
- CDN enabled for faster global delivery

---

## ⚙️ Step-by-Step Implementation

### 1️⃣ Create Static Website
- Developed a single-page portfolio using HTML and CSS
- Used Google Fonts and responsive layout techniques

---

### 2️⃣ Create S3 Bucket
- Created an S3 bucket with a unique name
- Disabled "Block all public access"
- Enabled **Static Website Hosting**
- Set `index.html` as the index document

---

### 3️⃣ Configure Bucket Policy
Added a bucket policy to allow public read access:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}

4️⃣ Upload Website Files

Uploaded index.html, styles.css, and assets to the S3 bucket
Verified website access using the S3 website endpoint

5️⃣ Create CloudFront Distribution

Created a CloudFront distribution with S3 as the origin
Set Viewer Protocol Policy to Redirect HTTP to HTTPS
Set default root object to index.html
Enabled global edge locations.

6️⃣ Verify HTTPS Access

Accessed website using CloudFront domain
Confirmed HTTPS lock icon and secure delivery

📸 Screenshots (Proof of Work)

Live Website (CloudFront HTTPS)
CloudFront Distribution
CloudFront HTTPS Policy
S3 Bucket Overview
Static Website Hosting Enabled
S3 Bucket Policy

🎯 Learning Outcomes

Understood AWS S3 static website hosting
Learned how bucket policies work
Configured CloudFront as a CDN
Enabled HTTPS using CloudFront
Gained hands-on experience with real cloud deployment

👤 Author

SHRADDHA NAYAK
Aspiring Cloud / DevOps Engineer
