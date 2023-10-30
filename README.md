# AWS Auto Maintenance Page Display Lambda Function

## Table of Contents
- [Overview](#overview)
- [Purpose](#purpose)
- [Diagram](#diagram)
- [Configuration](#configuration)
  - [Prerequisites](#prerequisites)
  - [Configuration Steps](#configuration-steps)

## Overview
This project provides an AWS Lambda function that automatically changes the TTL of a domain to a minimum value of 60 seconds, activates S3 web hosting, and configures the domain to point to the S3 hosting page. This functionality is designed to display a maintenance page when your website is undergoing maintenance.

## Purpose
The purpose of this AWS Lambda function is to simplify the process of setting up an automatic maintenance page for your website. It ensures that the domain TTL is minimized, activates S3 web hosting, and configures the domain to point to the S3-hosted maintenance page when needed.

## Diagram

![image](https://github.com/Jindding/awsLambda-auto-redirect-to-parkingpage/assets/49447802/7b293c9a-d518-47b3-937a-6c212080a4fb)

![image](https://github.com/Jindding/awsLambda-auto-redirect-to-parkingpage/assets/49447802/b12fd971-0ec8-43ae-8ba7-91a6960b8037)

![image](https://github.com/Jindding/awsLambda-auto-redirect-to-parkingpage/assets/49447802/6d658ab6-95c2-47db-b6cb-04d24c3ab623)


## Configuration
Before you can use this Lambda function, you need to configure it with your AWS credentials and specify the necessary parameters. Here's what you need to do:

### Prerequisites
- You should have an AWS account and access to the AWS Management Console.
- Ensure that you have the necessary IAM permissions for Route 53 and S3.

### Configuration Steps
1. **Access Key and Secret Key**: Replace the placeholders in the code with your AWS Access Key and Secret Key. It's recommended to use IAM roles and avoid hardcoding credentials for better security.

2. **Region**: Make sure the `region` variable is set to your desired AWS region.

3. **Domain and Hosted Zone ID**: Replace `YOUR-DOMAIN` with your domain name and `YOUR-HOSTED-ZONE-ID` with the ID of your Route 53 hosted zone.

4. **S3 Bucket Name**: Set `YOUR-BUCKET-NAME` to the name of the S3 bucket you want to use for hosting the maintenance page.

5. **Maintenance Page Configuration**: Customize the maintenance page by uploading an HTML file to the specified S3 bucket and update the `IndexDocument` and `ErrorDocument` values in the code accordingly.
