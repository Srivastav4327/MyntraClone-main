# Myntra Clone

This is a responsive clone of the popular e-commerce website Myntra. It includes a homepage with a navigation bar, search bar, main banner, category sections, and a footer. The project is built using HTML and CSS.

## Table of Contents

- [Demo](#demo)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)
- [Contact](#contact)
- [AWS Implementation](#aws-implementation)
- [License](#license)

## Demo

You can view a live demo of the project [here](https://priyanshuksharma.github.io/MyntraClone/).


## Features

- Responsive navigation bar with links to different sections.
- Search bar with placeholder text.
- Main banner image.
- Category sections with images and hover effects.
- Footer with multiple columns for different links.

## Technologies Used

- HTML5
- CSS3

## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

You need a modern web browser to view the project.

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/PriyanshuKSharma/MyntraClone.git
   ```
2. Navigate to the project directory
   ```sh
   cd MyntraClone
   ```
3. Open `index.html` in your web browser
   ```sh
   open index.html
   ```

## Folder Structure

```
myntra-clone/
├── images/
│   ├── myntra_logo.webp
│   ├── banner.jpg
│   ├── offers/
│   │   ├── 1.png
│   │   ├── 2.png
│   │   ├── ...
│   ├── categories/
│       ├── 1.jpg
│       ├── 2.jpg
│       ├── ...
├── index.html
└── index.css
```

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## AWS Implementation

Step 1: Create an AWS Account
If you don’t already have an AWS account, sign up at AWS.

Step 2: Choose a Hosting Option
There are multiple ways to host a website on AWS, depending on your requirements. The most common options are:

1. Amazon S3 (Static Websites): For static websites (HTML, CSS, JS).
2. Amazon EC2 (Dynamic Websites): For dynamic websites requiring server-side processing.
3. AWS Amplify (Web and Mobile Apps): Simplifies the process of deploying full-stack web and mobile apps.
4. Amazon Lightsail: Simplifies the setup of virtual private servers.

Step 3: Set Up a Static Website with Amazon S3
This is suitable for hosting simple static websites.

Create a Bucket:

Open the [@Amazon S3 console](https://console.aws.amazon.com/console/home?nc2=h_ct&src=header-signin).
1. Click on “Create bucket”.
2. Provide a bucket name (this should be unique across all of AWS).
3. Choose a region and configure other settings as per your needs.
4. Click on “Create bucket” at the bottom.

Upload Your Website Files:

1. Click on your newly created bucket.
2. Click on the “Upload” button.
3. Add your website files (HTML, CSS, JS, images, etc.).
4. Click on “Upload” to start the upload process.

Enable Static Website Hosting:

1. Click on your bucket and go to the “Properties” tab.
2. Scroll down to the “Static website hosting” section.
3. Select “Use this bucket to host a website”.
4. Specify the index document (e.g., index.html) and an error document (e.g., error.html).
5. Save the changes.

Make Your Bucket Public:

Go to the “Permissions” tab.

Edit the “Bucket policy” to allow public access. You can use the following policy (replace YOUR-BUCKET-NAME with your bucket name):

## Setting S3 Bucket Policy

To set the S3 bucket policy, use the following bash script:

```
#Go to the “Permissions” tab.
#Edit the “Bucket policy” to allow public access. You can use the following policy (replace YOUR-BUCKET-NAME with your bucket name):

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}
```
Access Your Website:

The website will be available at the bucket’s endpoint, which you can find in the “Static website hosting” section.

## Contact

Priyanshu K Sharma - [@Twitter](https://x.com/itspriyanshuks)
            [@PriyanshuKSharma](https://github.com/PriyanshuKSharma)

Project Link: https://github.com/PriyanshuKSharma/MyntraClone.git <br>
AWS Hosting: http://myntraclonebypriyanshu.s3-website.ap-south-1.amazonaws.com/

## License
This project is not currently licensed.

