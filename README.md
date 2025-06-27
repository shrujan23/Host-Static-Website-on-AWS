 # Step-by-Step Guide to Host a Static Website on AWS
### Project Title:
Static Website Hosting on AWS Using S3, CloudFront, and Route 53
### Project Description:
This project demonstrates how to host a fully functional static website (built with HTML, CSS, and JavaScript) on Amazon Web Services (AWS) using Amazon S3 for file storage, CloudFront for content delivery, and Route 53 for domain name management—without using HTTPS/SSL certificates (ACM).
The main goal is to create a cost-effective, scalable, and globally distributed static site infrastructure that delivers web content with low latency and high availability.
### Services Used:
Amazon S3: Used to store and host static website files like index.html, style.css, script.js, and images.
Amazon CloudFront: Configured as a CDN to cache and deliver content across multiple edge locations for faster access.
Amazon Route 53: Configured to map a custom domain (e.g., mystaticweb1-1.com) to the CloudFront distribution.
### Outcome:
Website is accessible via a custom domain and/or CloudFront URL
Fast, secure (optional), and scalable static content delivery
Hands-on experience with core AWS services used in web hosting
