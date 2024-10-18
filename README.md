# Amazon S3 Static Website Hosting Project

This project demonstrates how to use Amazon S3 to host a static website by creating a bucket, uploading files, and enabling static website hosting. The setup generates a unique endpoint URL for easy access to the hosted site.

## Overview

This project guides you through setting up a static website on Amazon S3. By the end, you'll have a fully functional website accessible via a unique S3 endpoint URL. The project covers creating an S3 bucket, uploading an `index.html` file, and configuring the bucket for static website hosting.

## Features

- Easy deployment of static websites on Amazon S3.
- Generates a unique URL for public access to your site.
- Configurable for multiple environments (dev, QA, live).
- Supports hosting assets like images, CSS, and JavaScript.

## Prerequisites

Before starting, ensure you have the following:
- An AWS account with S3 permissions
- Basic knowledge of HTML
- AWS CLI installed (optional, for easier setup)

## Setup and Installation

1. **Create an S3 Bucket:**
    - Navigate to the S3 service in your AWS console.
    - Create a new bucket and ensure the bucket name is globally unique.
  
2. **Enable Static Website Hosting:**
    - Go to the `Properties` tab of your bucket.
    - Scroll to **Static website hosting** and click **Edit**.
    - Choose **Enable** and select **Host a static website**.
    - Set `index.html` as the **Index document**.
  
3. **Upload Files:**
    - Upload `index.html` and any other supporting assets (CSS, JS, images) to your S3 bucket.
    - Make sure your files are publicly accessible by setting the appropriate permissions.

4. **Configure Permissions:**
    - Go to the **Permissions** tab, and set up a bucket policy to allow public access.
    - Example policy:
      ```json
      {
        "Version": "2012-10-17",
        "Statement": [
          {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your-bucket-name/*"
          }
        ]
      }
      ```

## Configuration

Make sure the following settings are configured:
- **Bucket Name:** Unique and identifiable name (e.g., `my-site-dev`, `my-site-qa`).
- **Index Document:** Set to `index.html`.
- **Permissions:** Ensure files are publicly accessible.

## Usage

1. **Access Your Website:**
    - Once the bucket is set up, AWS will provide an endpoint URL.
    - You can find this URL under the **Static website hosting** section of the **Properties** tab.
    - Use this URL to access your hosted site.

2. **Make Updates:**
    - To update your site, replace the existing files in your S3 bucket.
    - Refresh the browser to see the latest changes.

## Additional Resources

- [Amazon S3 Documentation](https://docs.aws.amazon.com/s3/index.html)
- [How to Use AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html)

## Contact

For any questions or suggestions, please reach out to:

- LinkedIn - https://www.linkedin.com/in/anesi-daniella-igunma-11775716b/
