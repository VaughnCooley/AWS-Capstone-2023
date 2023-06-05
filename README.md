# AWS Capstone 2023

GitHub Repository for the AWS Capstone Project lab. This documentation is for a proof-of-concept cloud infrastructure for an example university's web application.
Below is a complete documented process for creating this proof of concept design.

## Task 1: Planning
The planning phase required an outline of the cloud infrastructure, created in this case with the use of [LucidChart](https://www.lucidchart.com/pages/ "LucidChart") and an esitmate of the monthly and annual cost of the services, provided in this case by the [AWS Pricing Calculator](https://calculator.aws/#/ "AWS Pricing Calculator"). Below is the cloud diagram outline (top) and AWS Pricing Calculator esitamte (bottom).

![AWS Cloud Diagram](/images/AWS-diagram.png "AWS Cloud Diagram")
![AWS Pricing Calculator estimate](/images/AWS-calculator.png "AWS Pricing Calculator estimate")

## Task 2: Creating Cloud Infrastructure
Once the planning phase is complete, the next step is to work within AWS to create a suitable infrastructure for the web application to reside on. The first step when working with AWS is to create a VPC separate from the default that is created alongside the root user's account. Creating a new VPC allows for more precise control of how it is structured. For this infrastructure, a VPC was designed to be split across two availability zones, with one public subnet and one private subnet in each availability zone, an IPv4 CIDR block of 10.0.0.0/16, and a NAT gateway in one Avaialbility Zone. This infrastructure is pictured below in AWS' VPC Management Console, with the created VPC being titled "test".
![AWS VPC Management Console](/images/AWS-vpc-creation.png "AWS VPC Management Console")

**In a professional web application scenario, placeholder names such as "test-vpc" would be replaced with titles such as "University-vpc", "Business-vpc", et cetera. Creating services for the purpose of testing is a vital step in developing any cloud infrastructure, and for the sake of time efficiency, some test services are included in the final proof of concept infrastructure. Other instances of test names will be identifed by bolded text throughout this documentation.**
