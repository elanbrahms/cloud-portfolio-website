\# Cloud Portfolio Website



\## Overview



This project is a \*\*static portfolio website hosted entirely on AWS\*\*. It demonstrates how to deploy and distribute a website using cloud-native services without managing servers.



The website is stored in \*\*Amazon S3\*\*, delivered globally through \*\*Amazon CloudFront\*\*, and can optionally be mapped to a custom domain using \*\*Amazon Route53\*\*. The architecture focuses on scalability, security, and performance using AWS best practices.



This project was built to strengthen hands-on experience with \*\*static site hosting, CDN configuration, and cloud architecture design\*\*.



\---



\## Architecture



Client → Route53 → CloudFront → S3 Bucket → Static Website Files



\### Key Components



\- \*\*Route53 (Optional)\*\*  

&#x20; Provides DNS resolution for a custom domain name and routes traffic to CloudFront.



\- \*\*CloudFront\*\*  

&#x20; Acts as a global \*\*Content Delivery Network (CDN)\*\*. It caches website content at edge locations around the world, reducing latency and improving performance.



\- \*\*S3 Bucket\*\*  

&#x20; Stores the static website files including HTML, CSS, JavaScript, and images.



\---



\## Architecture Explanation



When a user visits the website, the request is first resolved through DNS using \*\*Route53\*\* (if a custom domain is configured). The request is then routed to \*\*CloudFront\*\*, which checks if the content is cached at a nearby edge location.



If the content is cached, CloudFront returns it immediately. If not, CloudFront retrieves the content from the \*\*S3 bucket origin\*\*, caches it, and then delivers it to the user.



This architecture improves performance by reducing the distance between users and the website content while keeping the storage layer simple and scalable.



\---



\## Request Flow



1\. The user enters the website URL in their browser.

2\. Route53 resolves the domain name to the CloudFront distribution.

3\. The request is sent to the nearest CloudFront edge location.

4\. CloudFront checks whether the content is cached.

5\. If not cached, CloudFront retrieves the content from the S3 bucket.

6\. The website files are returned to the user's browser.



\---



\## AWS Services Used



\- \*\*Amazon S3\*\* – Static file storage

\- \*\*Amazon CloudFront\*\* – Global content delivery network

\- \*\*Amazon Route53 (optional)\*\* – DNS management

\- \*\*AWS IAM\*\* – Access control and permissions



\---



\## Project Structure



