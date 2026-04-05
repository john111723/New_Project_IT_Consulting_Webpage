# SecureIT Website Deployment Guide

## Quick Start

### Local Testing (No Docker)
Simply open `index.html` in your web browser to see the website locally.

### Docker Deployment

#### Build the Docker image:
```bash
cd new-docer
docker build -t secureit-website:v1 -f Dockerfile.dev .
```

#### Run the container:
```bash
docker run -p 8080:80 secureit-website:v1
```

Access the website at: `http://localhost:8080`

### Docker Compose (Recommended)

From the root directory:

```bash
docker-compose up -d --build
```

Check the status:
```bash
docker-compose ps
```

Stop the service:
```bash
docker-compose down
```

View logs:
```bash
docker-compose logs -f secureit-website
```

### Kubernetes Deployment

```bash
kubectl apply -f new-docer/nginx.yaml
```

Check the deployment:
```bash
kubectl get pods
kubectl get svc
```

Get the LoadBalancer URL:
```bash
kubectl get svc my-nginx-router
```

## Customization Steps

### 1. Update Company Information
Edit `index.html` and replace:
- Line with "SecureIT" → Your company name
- Contact email: `info@secureit.com`
- Contact phone: `+1 (555) 123-4567`
- Address: `123 Security Lane, Tech City, TC 12345`

### 2. Personalize Services
Find the "Our Services" section and modify:
- Service descriptions
- Service icons (emoji)
- Service titles

### 3. Add Real Testimonials
Replace the sample testimonials with actual client quotes

### 4. Update Case Studies
Add your real project results in the portfolio section

### 5. Change Colors
Primary color: `#0066cc` (blue) - search and replace with your preferred color

## File Descriptions

| File | Purpose |
|------|---------|
| `index.html` | Main website homepage |
| `blog.html` | Blog listing page |
| `Dockerfile.dev` | Docker build instructions |
| `.dockerignore` | Files to exclude from Docker |
| `nginx.yaml` | Kubernetes deployment config |
| `README.md` | Project documentation |
| `DEPLOYMENT.md` | This file |

## Performance Tips

1. **Image Optimization**: Add actual images in place of placeholder colors
2. **Caching**: Configure nginx caching in production
3. **CDN**: Consider using a CDN for static assets
4. **SEO**: Add meta descriptions and keywords

## SSL/HTTPS Setup

For production, add SSL certificates to Nginx:

```dockerfile
COPY your-cert.pem /etc/nginx/ssl/
COPY your-key.pem /etc/nginx/ssl/
```

Configure nginx to use them.

## Monitoring

Monitor your container with:
```bash
docker stats secureit-website
```

## Troubleshooting

### Port Already in Use
```bash
docker-compose down
# Or change port in docker-compose.yml
```

### Container Won't Start
```bash
docker logs secureit-website
```

### Website Not Accessible
- Check if the container is running: `docker ps`
- Verify port mappings: `docker port secureit-website`
- Check Kubernetes service: `kubectl get svc`

## Next Steps

1. ✅ Customize contact information
2. ✅ Add real company content
3. ✅ Deploy to Docker
4. ✅ Set up SSL certificate
5. ✅ Configure domain name
6. ✅ Set up email notifications for contact form

---

For help, refer to:
- Docker docs: https://docs.docker.com
- Kubernetes docs: https://kubernetes.io/docs
- Nginx docs: https://nginx.org/en/docs
