# SecureIT Website - Customization Guide

## Quick Edit locations in index.html

### Company Information
```
Line ~280-284: Contact Information section
- Email: info@secureit.com
- Phone: +1 (555) 123-4567
- Address: 123 Security Lane, Tech City, TC 12345
```

### Brand Name
Replace all instances of "SecureIT" with your company name:
- Line ~167: Logo/Navigation
- Line ~180: Page title
- Line ~327: Footer copyright

### Color Scheme
Primary color: `#0066cc` (Blue)
Secondary color: `#004499` (Darker Blue)

Find and replace in `<style>` section:
- `#0066cc` → Your primary color
- `#004499` → Your secondary color (darker)

### Hero Section (Main Banner)
```
Line ~180-182: 
- Heading: "Secure Your Business. Empower Your Growth."
- Subheading: "Enterprise-grade cybersecurity, 24/7 support, and strategic IT consulting"
```

### About Section
```
Line ~198-201:
- Update company description
- Modify statistics (500+, 99.9%, 24/7)
```

### Services Section
Update the 6 service cards (Lines ~215-245):
1. **Cybersecurity** (🔐)
2. **24/7 IT Support** (🛠️)
3. **IT Consulting** (💼)
4. **Cloud Solutions** (☁️)
5. **Data Protection** (📊)
6. **System Integration** (🔧)

Change emojis, titles, and descriptions to match your services.

### Testimonials Section
Replace sample testimonials (Lines ~290-302) with real client feedback

### Blog Navigation
Link to: `blog.html` (already configured)

### Contact Form
```
Line ~332-336: Form fields
- Name input
- Email input
- Message textarea
```

## CSS Classes Reference

```css
.hero           /* Main banner section */
.service-card   /* Individual service box */
.portfolio-item /* Case study card */
.testimonial-card /* Client testimonial */
.contact-form   /* Contact form */
```

## Color Palette

Current colors:
- Primary: `#0066cc` (Professional Blue)
- Secondary: `#004499` (Dark Blue)
- Background: `#f8f9fa` (Light Gray)
- Text: `#333` (Dark Gray)
- White: `#fff`

Suggested alternative palettes:
- **Tech Green**: `#00a86b` primary, `#008c4a` secondary
- **Professional Red**: `#cc0000` primary, `#990000` secondary
- **Modern Purple**: `#7c3aed` primary, `#6d28d9` secondary

## Image Placeholders

Replace these text placeholders with actual images:
- Service icons: Use Font Awesome or custom SVGs
- Portfolio images: Add screenshots from your work
- Blog featured images: Add tech/security related images

## Meta Data (SEO)

Update the `<head>` section:
```html
<title>SecureIT - Cybersecurity & IT Solutions</title>
```

Add to improve SEO:
```html
<meta name="description" content="Your company description">
<meta name="keywords" content="cybersecurity, IT support, consulting">
<meta name="author" content="Your Name">
```

## Forms and Functionality

The contact form currently shows an alert. To make it functional:

1. **Option A - EmailJS** (Recommended)
   - Sign up at emailjs.com
   - Update line ~360 with your service ID

2. **Option B - Backend API**
   - Create a backend endpoint
   - Update form submission to POST to your API

3. **Option C - FormSubmit**
   - Add to form: `action="https://formsubmit.co/your@email.com"`
   - Remove the JavaScript submission handler

## Analytics

Add Google Analytics tracking:
```html
<!-- Add to <head> section -->
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR_GA_ID');
</script>
```

## Responsive Breakpoints

Configured for:
- Desktop: 1200px+ (full layout)
- Tablet: 768px - 1199px
- Mobile: < 768px (single column)

## Navigation Structure

```
Home → index.html#home
About → index.html#about
Services → index.html#services
Portfolio → index.html#portfolio
Testimonials → index.html#testimonials
Contact → index.html#contact
Blog → blog.html
```

## Blog Page Customization

Edit `blog.html` to update:
- Blog post titles
- Publication dates
- Article excerpts
- Blog images

## Performance Checklist

- [ ] Compress images under 100KB
- [ ] Use WebP format for images
- [ ] Minify CSS/JavaScript
- [ ] Add caching headers
- [ ] Test on mobile devices
- [ ] Check page speed (Google PageSpeed Insights)
- [ ] Test form submissions

---

Need help? Check DEPLOYMENT.md for Docker and Kubernetes instructions.
