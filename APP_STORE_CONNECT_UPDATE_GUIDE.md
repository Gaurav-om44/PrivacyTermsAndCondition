# App Store Connect Update Guide

## Required Updates for Auto-Renewable Subscriptions

Apple has rejected the submission because it's missing required information for auto-renewable subscriptions. Follow this roadmap to fix the issue.

## Roadmap

### Step 1: Create Privacy Policy HTML File

1. Create a new file: `privacy-policy.html`

2. Add the following content:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ITHAC Privacy Policy</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            color: #333;
        }
        h1 {
            color: #000;
            border-bottom: 2px solid #F5C542;
            padding-bottom: 10px;
        }
        h2 {
            color: #555;
            margin-top: 30px;
        }
        p {
            margin-bottom: 15px;
        }
        .last-updated {
            color: #888;
            font-style: italic;
        }
    </style>
</head>
<body>
    <h1>Privacy Policy</h1>
    <p class="last-updated">Last Updated: [DATE]</p>
    
    <h2>Introduction</h2>
    <p>
        ITHAC ("we," "our," or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our mobile application.
    </p>
    
    <h2>Information We Collect</h2>
    <p>
        We collect information that you provide directly to us, including:
    </p>
    <ul>
        <li>Account information (email, name)</li>
        <li>Subscription information</li>
        <li>Usage data and analytics</li>
        <li>Device information</li>
    </ul>
    
    <h2>How We Use Your Information</h2>
    <p>
        We use the information we collect to:
    </p>
    <ul>
        <li>Provide and maintain our services</li>
        <li>Process subscription payments</li>
        <li>Send you updates and notifications</li>
        <li>Improve our app and user experience</li>
        <li>Comply with legal obligations</li>
    </ul>
    
    <h2>Data Security</h2>
    <p>
        We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction.
    </p>
    
    <h2>Third-Party Services</h2>
    <p>
        Our app uses third-party services that may collect information used to identify you, including:
    </p>
    <ul>
        <li>Firebase (authentication and analytics)</li>
        <li>RevenueCat (subscription management)</li>
        <li>Apple (in-app purchases)</li>
    </ul>
    
    <h2>Your Rights</h2>
    <p>
        You have the right to:
    </p>
    <ul>
        <li>Access your personal information</li>
        <li>Request correction of inaccurate data</li>
        <li>Request deletion of your data</li>
        <li>Opt-out of certain data collection</li>
    </ul>
    
    <h2>Contact Us</h2>
    <p>
        If you have questions about this Privacy Policy, please contact us at:
    </p>
    <p>
        Email: [YOUR_EMAIL]<br>
        Website: [YOUR_WEBSITE]
    </p>
    
    <h2>Changes to This Policy</h2>
    <p>
        We may update this Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "Last Updated" date.
    </p>
</body>
</html>
```

3. Replace `[DATE]` with the current date
4. Replace `[YOUR_EMAIL]` with your contact email
5. Replace `[YOUR_WEBSITE]` with your website URL (if applicable)

### Step 2: Create Terms of Service HTML File (Optional)

If you want a custom Terms of Service page, create `terms-of-service.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ITHAC Terms of Service</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            color: #333;
        }
        h1 {
            color: #000;
            border-bottom: 2px solid #F5C542;
            padding-bottom: 10px;
        }
        h2 {
            color: #555;
            margin-top: 30px;
        }
        p {
            margin-bottom: 15px;
        }
        .last-updated {
            color: #888;
            font-style: italic;
        }
    </style>
</head>
<body>
    <h1>Terms of Service</h1>
    <p class="last-updated">Last Updated: [DATE]</p>
    
    <h2>1. Acceptance of Terms</h2>
    <p>
        By accessing and using the ITHAC mobile application, you accept and agree to be bound by the terms and provision of this agreement.
    </p>
    
    <h2>2. Subscription Terms</h2>
    <p>
        ITHAC Premium offers auto-renewable subscriptions:
    </p>
    <ul>
        <li>Monthly: $89.99/month</li>
        <li>Quarterly: $224.97 every 3 months ($74.99/month)</li>
        <li>Annual: $839.88 per year ($69.99/month)</li>
    </ul>
    
    <h2>3. Auto-Renewal</h2>
    <p>
        Subscriptions automatically renew unless canceled at least 24 hours before the end of the current period. Payment will be charged to your Apple ID account at confirmation of purchase.
    </p>
    
    <h2>4. Cancellation</h2>
    <p>
        You can cancel your subscription at any time through your Apple ID account settings. Cancellation will take effect at the end of the current billing period.
    </p>
    
    <h2>5. Refunds</h2>
    <p>
        Refund requests must be submitted through Apple's refund process. We do not process refunds directly.
    </p>
    
    <h2>6. User Responsibilities</h2>
    <p>
        You are responsible for maintaining the confidentiality of your account and password. You agree to notify us immediately of any unauthorized use of your account.
    </p>
    
    <h2>7. Limitation of Liability</h2>
    <p>
        ITHAC shall not be liable for any indirect, incidental, special, consequential, or punitive damages resulting from your use of the service.
    </p>
    
    <h2>8. Contact Information</h2>
    <p>
        For questions about these Terms of Service, contact us at: [YOUR_EMAIL]
    </p>
</body>
</html>
```

### Step 3: Deploy to Vercel

1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm i -g vercel
   ```

2. **Create a new directory for hosting**:
   ```bash
   mkdir ithac-policies
   cd ithac-policies
   ```

3. **Copy your HTML files**:
   ```bash
   cp privacy-policy.html ithac-policies/
   # Optional: cp terms-of-service.html ithac-policies/
   ```

4. **Deploy to Vercel**:
   ```bash
   vercel
   ```

5. **Follow the prompts**:
   - Set up and deploy? Yes
   - Which scope? Select your account
   - Link to existing project? No
   - Project name: `ithac-policies` (or your preferred name)
   - Directory: `.` (current directory)
   - Override settings? No

6. **Get your URLs**:
   After deployment, Vercel will provide URLs like:
   - `https://ithac-policies.vercel.app/privacy-policy.html`
   - `https://ithac-policies.vercel.app/terms-of-service.html` (if created)

7. **Note your production URL**:
   The production URL will be something like: `https://ithac-policies.vercel.app`

### Step 4: Update App Store Connect

#### 4.1 Update Privacy Policy URL

1. Go to App Store Connect
2. Navigate to: Your App → App Privacy
3. Find "Privacy Policy URL" field
4. Enter your Vercel URL: `https://ithac-policies.vercel.app/privacy-policy.html`
5. Click "Save"

#### 4.2 Update App Description with Terms of Use (EULA)

1. Go to App Store Connect
2. Navigate to: Your App → App Information → Description
3. Add the following text at the end of your description:

```
---

TERMS OF USE (EULA)
By downloading and using ITHAC, you agree to Apple's Standard License Agreement (EULA).
View Apple's EULA at: https://www.apple.com/legal/internet-services/itunes/dev/stdeula/

PRIVACY POLICY
We are committed to protecting your privacy. View our Privacy Policy at: 
https://ithac-policies.vercel.app/privacy-policy.html

SUBSCRIPTION INFORMATION
ITHAC Premium offers auto-renewable subscriptions:
- Monthly: $89.99/month
- Quarterly: $224.97 every 3 months ($74.99/month)
- Annual: $839.88 per year ($69.99/month)

Subscriptions automatically renew unless canceled at least 24 hours before the end of the current period. Payment will be charged to your Apple ID account at confirmation of purchase.
```

4. Replace `https://ithac-policies.vercel.app/privacy-policy.html` with your actual Vercel URL
5. Click "Save"

### Step 5: Verify App Contains Required Information

The app has been updated to include all required subscription information:

- Title of subscription - Displayed in plan cards (e.g., "ITHAC Premium Annual")
- Length of subscription - Shown for each plan (1 Month, 3 Months, 1 Year)
- Price of subscription - Displayed clearly (e.g., "$839.88 per year")
- Price per unit - Shown for annual and quarterly plans (e.g., "$69.99 per month")
- Functional links to Privacy Policy - Clickable link in subscription screen
- Functional links to Terms of Use - Clickable link in subscription screen

### Step 6: Test the App

Before resubmitting:

1. Test subscription screen:
   - Navigate to subscription/paywall screen
   - Verify all subscription information is visible
   - Verify links to Privacy Policy and Terms of Service work
   - Test on both simulator and device

2. Test links:
   - Tap "Terms of Service" link - should navigate to terms screen
   - Tap "Privacy Policy" link - should navigate to privacy policy screen
   - Verify both screens load correctly

3. Test Vercel URLs:
   - Open Privacy Policy URL in browser: `https://ithac-policies.vercel.app/privacy-policy.html`
   - Verify it loads correctly
   - Verify it's publicly accessible (no login required)

### Step 7: Resubmit to App Store

After completing all steps:

1. Go to App Store Connect
2. Navigate to your app submission
3. Verify App Description includes Terms of Use link (Apple's EULA)
4. Verify Privacy Policy URL is set correctly
5. Click "Submit for Review"

## Quick Checklist

- [ ] Created privacy-policy.html file
- [ ] Updated privacy-policy.html with your information
- [ ] Deployed to Vercel
- [ ] Copied Vercel Privacy Policy URL
- [ ] Added Terms of Use (Apple EULA) link to App Description in App Store Connect
- [ ] Set Privacy Policy URL in App Store Connect
- [ ] Verified subscription information is visible in app (title, length, price, price per unit)
- [ ] Verified Privacy Policy link works in app
- [ ] Verified Terms of Service link works in app
- [ ] Tested Vercel URLs are publicly accessible
- [ ] Tested on simulator
- [ ] Tested on device
- [ ] Resubmitted to App Store Connect

## Important Notes

1. URLs must be functional - Apple reviewers will click these links
2. URLs must be publicly accessible - No login required
3. Using Apple's standard EULA - No need to create custom Terms of Service HTML
4. Privacy Policy must be complete - Should explain data collection and usage
5. Vercel URLs are permanent - They won't change unless you delete the project

## Support

If you need help:
- Vercel Documentation: https://vercel.com/docs
- Apple's EULA: https://www.apple.com/legal/internet-services/itunes/dev/stdeula/
- Apple Guidelines: https://developer.apple.com/app-store/review/guidelines/#subscriptions
