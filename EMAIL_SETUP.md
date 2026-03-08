# Email Notification Setup Guide

## Step 1: Create EmailJS Account
1. Go to https://www.emailjs.com/
2. Sign up for free account
3. Verify your email

## Step 2: Add Email Service
1. Go to Email Services
2. Click "Add New Service"
3. Choose Gmail/Outlook/etc
4. Connect your email account

## Step 3: Create Email Template
1. Go to Email Templates
2. Click "Create New Template"
3. Use this template:

**Template Name:** business_confirmation

**Subject:** 
```
Thank You for Listing {{business_name}} on PakBizBranches!
```

**Content (HTML):**
```html
<!DOCTYPE html>
<html>
<head>
    <style>
        body { font-family: Arial, sans-serif; line-height: 1.6; color: #333; }
        .container { max-width: 600px; margin: 0 auto; padding: 20px; }
        .header { background: linear-gradient(135deg, #0f2b3d, #1e4a6f); color: white; padding: 30px; text-align: center; border-radius: 10px 10px 0 0; }
        .content { background: #f8fafc; padding: 30px; border-radius: 0 0 10px 10px; }
        .business-card { background: white; padding: 20px; border-radius: 10px; margin: 20px 0; border-left: 4px solid #0f2b3d; }
        .logo { max-width: 100px; height: auto; margin: 10px 0; }
        .button { display: inline-block; background: #0f2b3d; color: white; padding: 12px 30px; text-decoration: none; border-radius: 5px; margin: 20px 0; }
        .footer { text-align: center; color: #666; font-size: 12px; margin-top: 30px; }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🎉 Welcome to PakBizBranches!</h1>
        </div>
        <div class="content">
            <p>Dear {{to_name}},</p>
            
            <p>Thank you for listing your business with us! We're excited to have <strong>{{business_name}}</strong> on Pakistan's leading business directory.</p>
            
            <div class="business-card">
                <h2>📋 Your Business Details</h2>
                <img src="{{logo_url}}" alt="Business Logo" class="logo">
                <p><strong>Business Name:</strong> {{business_name}}</p>
                <p><strong>Category:</strong> {{category}}</p>
                <p><strong>City:</strong> {{city}}</p>
                <p><strong>Address:</strong> {{address}}</p>
                <p><strong>Phone:</strong> {{phone}}</p>
                <p><strong>WhatsApp:</strong> {{whatsapp}}</p>
                <p><strong>Description:</strong> {{description}}</p>
            </div>
            
            <p><strong>Status:</strong> Your listing is currently under review. We'll approve it within 24-48 hours.</p>
            
            <p>Once approved, your business will be visible to millions of potential customers across Pakistan!</p>
            
            <center>
                <a href="{{listing_url}}" class="button">View Your Listing</a>
            </center>
            
            <div class="footer">
                <p>Need help? Contact us at support@pakbizbranhces.online</p>
                <p>&copy; 2025 PakBizBranches. All rights reserved.</p>
                <p><a href="https://pakbizbranhces.online">Visit Website</a></p>
            </div>
        </div>
    </div>
</body>
</html>
```

## Step 4: Get Your Keys
1. Go to Account > API Keys
2. Copy your Public Key
3. Copy your Service ID
4. Copy your Template ID

## Step 5: Update add.html
Replace in add.html:
- `YOUR_PUBLIC_KEY` with your Public Key
- `YOUR_SERVICE_ID` with your Service ID  
- `YOUR_TEMPLATE_ID` with your Template ID

## Template Variables Used:
- {{to_email}} - Recipient email
- {{to_name}} - Contact person name
- {{business_name}} - Business name
- {{category}} - Business category
- {{city}} - City
- {{address}} - Full address
- {{phone}} - Phone number
- {{whatsapp}} - WhatsApp number
- {{description}} - Business description
- {{listing_url}} - Direct link to listing
- {{logo_url}} - Logo image URL

## Testing
1. Submit a test business listing
2. Check email inbox
3. Verify all details are correct
4. Click "View Your Listing" button

## Free Tier Limits
- 200 emails/month
- Upgrade for more: https://www.emailjs.com/pricing/
