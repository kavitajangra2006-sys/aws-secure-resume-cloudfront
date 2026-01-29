Secure Resume Hosting on AWS (S3 + CloudFront)

Project Description
This project demonstrates how to securely host a resume using Amazon S3 and
Amazon CloudFront by following Zero Trust security principles.

The resume was stored in a private S3 bucket and accessed only through
CloudFront using Origin Access Control (OAC). All direct public access to S3
was blocked and HTTPS was enforced.

Note:
AWS resources were deleted after project completion to avoid free-tier charges.
Screenshots and documentation are provided for validation.

Architecture
User → CloudFront (HTTPS) → S3 (Private Bucket)

Detailed architecture explanation:
architecture/architecture.txt

Implementation Steps
Step-by-step implementation details are documented in:
architecture/steps.txt

Security Highlights
- S3 Block Public Access enabled (all settings ON)
- CloudFront Origin Access Control (OAC)
- HTTPS enforcement (HTTP redirected to HTTPS)
- AWS WAF enabled in monitor mode
- Direct S3 object access blocked (AccessDenied)

Validation
- Direct S3 object access returned AccessDenied
- Resume was accessible only via CloudFront HTTPS URL
- CloudFront cache invalidation performed when required

Screenshots
All configuration and validation screenshots are available in the screenshots/
folder.

Key Learnings
- Secure content delivery using CloudFront and OAC
- Zero Trust architecture implementation
- Importance of correct object naming and cache invalidation
- Practical experience with AWS CDN and security services

Author
Kavita
Aspiring Cloud & Cybersecurity Engineer
