 # Step-by-Step Guide to Host a Static Website on AWS
### Project Title:
Static Website Hosting on AWS Using S3, CloudFront, and Route 53
### Project Description:
This project demonstrates how to host a fully functional static website (built with HTML, CSS, and JavaScript) on Amazon Web Services (AWS) using Amazon S3 for file storage, CloudFront for content delivery, and Route 53 for domain name management—without using HTTPS/SSL certificates (ACM).
The main goal is to create a cost-effective, scalable, and globally distributed static site infrastructure that delivers web content with low latency and high availability.
### Project Architecture:
![image alt](https://github.com/shrujan23/Host-Static-Website-on-AWS/blob/fc467097f4b2dc1ab776e897e6ac50b87aba19ae/3e8eab8d-4e4c-4862-bb0c-693ab708ee57.png)
### Services Used:
Amazon S3: Used to store and host static website files like index.html, style.css, script.js, and images.
Amazon CloudFront: Configured as a CDN to cache and deliver content across multiple edge locations for faster access.
Amazon Route 53: Configured to map a custom domain (e.g., mystaticweb1-1.com) to the CloudFront distribution.
### Outcome:
Website is accessible via a custom domain and/or CloudFront URL
Fast, secure (optional), and scalable static content delivery
Hands-on experience with core AWS services used in web hosting
### Prerequisites:
* AWS Account
* Your domain name (registered in Route 53 or elsewhere)
* Basic static site files (HTML/CSS/JS)
## Steps to Deploy

* Step 1: Create & Upload Your Website to S3:
  * Click "Create bucket"
  * Bucket name: mystaticweb1-1 (must be globally unique)
  * Uncheck Block all public access
  * Acknowledge the warning
* Click Create Bucket
  * Upload your site files:
  * Click into the bucket
  * Click Upload
  * Upload index.html, style.css, etc.
  * After upload, select each file → click Actions > Make public
* Step 2: Enable Static Website Hosting
  * Go to the bucket
  * Click Properties
  * Scroll to Static website hosting
  * Click Edit
  * Enable it
  * Index document: index.html
  * (Optional) Error document: error.html
* Click Save changes

Now you’ll get a public endpoint like:
 ```Bash
        http://mystaticweb11.com.s3-website-us-east-1.amazonaws.com
```
* Step 3 : Connect a Custom Domain with Route 53:
  * Go to Route 53 → Register or use an existing domain.
  * Create a Hosted Zone for your domain (e.g., example.com).
  * Create a Record Set:
    * Type: A (IPv4)
    * Alias: Yes
    * Alias target: Use the S3 website endpoint (from step 4)
    * TTL: 300 seconds
*  Now visiting http://mystaticweb11.com.s3-website-us-east-1.amazonaws.com should show your S3 website.

For queries write to us at: Shrujan990@gmail.com
