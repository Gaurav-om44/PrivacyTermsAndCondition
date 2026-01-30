# ITHAC Legal Documents Website

This repository contains the Privacy Policy and Terms & Conditions web pages for ITHAC, optimized for deployment on Vercel.

## Files

- `index.html` - Landing page with links to both documents
- `privacy-policy.html` - Privacy Policy page
- `terms-and-conditions.html` - Terms and Conditions page
- `styles.css` - Shared stylesheet for all pages
- `vercel.json` - Vercel configuration for routing and headers

## URLs

After deployment to Vercel, the pages will be accessible at:

- Home: `https://your-project.vercel.app/`
- Privacy Policy: `https://your-project.vercel.app/privacy-policy` or `/privacy-policy.html`
- Terms & Conditions: `https://your-project.vercel.app/terms-and-conditions` or `/terms-and-conditions.html` or `/terms`

## Deployment to Vercel

### Option 1: Using Vercel CLI

1. Install Vercel CLI (if not already installed):
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

3. Follow the prompts:
   - Set up and deploy? **Yes**
   - Which scope? Select your account
   - Link to existing project? **No** (for first deployment)
   - Project name: `ithac-policies` (or your preferred name)
   - Directory: `.` (current directory)
   - Override settings? **No**

4. For production deployment:
   ```bash
   vercel --prod
   ```

### Option 2: Using Vercel Dashboard

1. Go to [vercel.com](https://vercel.com)
2. Click "New Project"
3. Import your Git repository or drag and drop the folder
4. Configure project settings (if needed)
5. Click "Deploy"

### Option 3: Using Git Integration

1. Push this repository to GitHub/GitLab/Bitbucket
2. Connect your repository to Vercel
3. Vercel will automatically deploy on every push

## Features

- ✅ Responsive design (mobile-friendly)
- ✅ Clean, modern UI
- ✅ SEO-friendly meta tags
- ✅ Print-friendly styles
- ✅ Multiple URL routes for easy access
- ✅ Security headers configured
- ✅ Fast static site generation

## Customization

Before deploying, you may want to update:

1. **Contact Information**: Update email addresses in both HTML files
2. **Website URL**: Update website links if different
3. **Last Updated Dates**: Update the dates in both HTML files
4. **Company Information**: Adjust any company-specific details

## Testing Locally

You can test the pages locally using a simple HTTP server:

```bash
# Using Python
python3 -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## App Store Connect Integration

Use these URLs in App Store Connect:

- **Privacy Policy URL**: `https://your-project.vercel.app/privacy-policy`
- **Terms of Service**: Reference Apple's EULA or link to `/terms-and-conditions`

## Support

For issues or questions:
- Vercel Documentation: https://vercel.com/docs
- Vercel Support: https://vercel.com/support

