# TechConf 2025 Website

A static website for a technology conference hosted on AWS EC2. The website features a responsive design with schedule information, speaker profiles, and conference details.

## Live Demo

Visit the [website](http://3.14.128.54/index.html)

## 📋 Features

- Responsive design that works on desktop and mobile
- Three-page layout (Home, Schedule, Speakers)
- Interactive schedule timeline
- Speaker profiles with descriptions
- Modern UI with gradient accents
- Smooth animations and transitions

## 🛠 Technology Stack

- HTML5
- CSS3
- AWS EC2 for hosting
- Apache Web Server

## 🏗 Project Structure

```plaintext
frontend/
├── public/
│   ├── index.html      # Home page
│   ├── schedule.html   # Conference schedule
│   ├── speakers.html   # Speaker profiles
│   ├── css/
│   │   └── styles.css  # Styling
│   └── images/
│       └── speakers/   # Speaker photos
```

##  Deployment

The website is deployed on AWS EC2 using Apache web server:

1. Launch EC2 instance
2. Install Apache
```bash
sudo yum update -y
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
```

3. Deploy files
```bash
sudo cp -r frontend/public/* /var/www/html/
```

## 🔧 Development

To run this project locally:

1. Clone the repository
```bash
git clone https://github.com/yourusername/CloudDatabase.git
```

2. Navigate to project directory
```bash
cd CloudDatabase/frontend/public
```

3. Open `index.html` in your browser

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

##  Future Enhancements

### 1. AWS S3 Integration
- Move static assets to S3 bucket
- Implement CloudFront CDN
- Optimize image delivery and caching
- Reduce EC2 load

### 2. Database Layer (Amazon RDS)
- User registration and authentication
- Dynamic speaker profiles
- Event schedule management
- Session booking system

### 3. Backend Development
- RESTful API with Node.js/Express
- AWS Lambda functions
- API Gateway integration
- User session management

### 4. Additional AWS Services
- SES for email notifications
- EventBridge for scheduling
- DynamoDB for real-time features
- CloudWatch for monitoring

### 5. Infrastructure as Code
- Terraform/CloudFormation templates
- CI/CD pipeline with GitHub Actions
- Automated deployments
- Environment management

## 📋 Implementation Priority
1. Asset Migration to S3
2. Database Setup
3. API Development
4. Authentication System
5. Email Notifications

## 🔄 Architecture Evolution
```plaintext
Current:
Client -> EC2 (Apache) -> Static Files

Future:
Client -> CloudFront -> S3 (Static Assets)
                    -> API Gateway -> Lambda -> RDS
                                           -> DynamoDB
                                           -> SES
```

## ✍️ Author

Daniel Osuoha

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details