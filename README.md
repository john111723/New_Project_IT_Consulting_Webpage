# SecureIT - Professional IT Services Website

A modern, responsive website for an IT service business specializing in cybersecurity, 24/7 support, and IT consulting.

## Features

- **Responsive Design**: Mobile-first approach that works on all devices
- **Modern Aesthetic**: Clean, professional design with a blue color scheme
- **Multiple Sections**:
  - Hero section with call-to-action
  - About section with key statistics
  - Services showcase (6 main services)
  - Case studies/portfolio
  - Client testimonials
  - Contact form
  - Blog page with featured articles

## Pages

- **index.html** - Main homepage with all sections
- **blog.html** - Blog listing page with recent posts

## Services Highlighted

1. **Cybersecurity** - Threat detection, penetration testing, security audits, compliance
2. **24/7 IT Support** - Technical support, monitoring, incident response
3. **IT Consulting** - Strategic planning, infrastructure design, digital transformation
4. **Cloud Solutions** - Migration, management, optimization
5. **Data Protection** - Backup, disaster recovery, governance
6. **System Integration** - Seamless integration with existing infrastructure

## Customization

You can easily customize:

- **Company Name**: Replace "SecureIT" with your business name
- **Contact Information**: Update email, phone, and address in the Contact section
- **Services**: Modify service descriptions in the Services grid
- **Testimonials**: Add real client testimonials
- **Case Studies**: Replace with your actual project highlights
- **Colors**: Change the primary color from `#0066cc` (blue) to any color code
- **Content**: Update all text content to match your business

## Docker Setup

Build and run with Docker:

```bash
docker build -t secureit-website:v1 -f Dockerfile.dev .
docker run -p 8080:80 secureit-website:v1
```

Access at `http://localhost:8080`

## Kubernetes Deployment

The website is configured to run in Kubernetes. See `nginx.yaml` for the deployment configuration.

```bash
kubectl apply -f nginx.yaml
```

This will:
- Create a LoadBalancer service on port 8080
- Deploy 5 replicas of the website
- Serve on containerPort 80 internally

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## File Structure

```
new-docer/
├── index.html          # Main homepage
├── blog.html           # Blog page
├── config.yaml         # Configuration
├── Dockerfile.dev      # Docker build configuration
├── nginx.yaml          # Kubernetes deployment
└── README.md          # This file
```

## Features Implemented

✅ Fully responsive design
✅ Smooth scrolling navigation
✅ Contact form with validation
✅ Service cards with hover effects
✅ Professional testimonials section
✅ Case studies showcase
✅ Mobile-friendly layout
✅ Docker containerization
✅ Kubernetes ready

## License

© 2024 SecureIT. All rights reserved.
