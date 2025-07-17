# EmailJS Setup Guide for Portfolio Contact Form

## 📧 EmailJS Configuration Steps

### 1. Create EmailJS Account
1. Go to [EmailJS.com](https://www.emailjs.com)
2. Sign up for a free account
3. Verify your email address

### 2. Create Email Service ✅ DONE
1. Go to **Email Services** in your dashboard
2. Click **Add New Service**
3. Choose **Gmail** (recommended)
4. Connect your Gmail account (`tauhid04023@gmail.com`) ✅
5. Note the **Service ID**: `service_p1768ak` ✅

### 3. Create Email Template
1. Go to **Email Templates** in your dashboard
2. Click **Create New Template**
3. Use this template:

```html
Subject: Portfolio Contact from {{from_name}}

From: {{from_name}} <{{from_email}}>
To: Tauhidur Rahman Tauhid <tauhid04023@gmail.com>

Message:
{{message}}

---
This email was sent from your portfolio contact form.
Reply directly to this email to respond to {{from_name}}.
```

4. Note the **Template ID**: `template_iei2reb` ✅

### 4. Get Public Key ✅ DONE
1. Go to **Account** → **General**
2. Copy your **Public Key**: `ME4yAKoPTNO_E9CCR` ✅

### 5. Update Your Code
Replace these placeholders in your `index.html`:

```javascript
// Replace these with your actual EmailJS credentials
emailjs.init("ME4yAKoPTNO_E9CCR"); // Public Key updated ✅
emailjs.send("service_p1768ak", "template_iei2reb", { // All IDs updated ✅
    from_name: name,
    from_email: email,
    message: message,
    to_name: "Tauhidur Rahman Tauhid",
    to_email: "tauhid04023@gmail.com"
});
```

### 6. Test Your Form
1. Open your portfolio locally
2. Fill out the contact form
3. Check your email for the message
4. Verify the form shows success/error messages

## 🔧 Configuration Variables

Update these in your `index.html`:

- ✅ `service_p1768ak` → Your Gmail Service ID (DONE)
- ✅ `ME4yAKoPTNO_E9CCR` → Your EmailJS Public Key (DONE)
- ✅ `template_iei2reb` → Your Email Template ID (DONE)

🎉 **ALL CONFIGURATION COMPLETE!** 🎉

## 📱 Benefits of EmailJS

✅ **Works on GitHub Pages** - No backend server needed
✅ **Mobile-friendly** - Works on all devices
✅ **Reliable delivery** - Uses your Gmail account
✅ **Free tier** - 200 emails/month
✅ **Real-time feedback** - Shows success/error messages
✅ **Professional** - Emails come from your Gmail

## 🚀 Deployment Ready

Once configured, your contact form will work perfectly on:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting

## 📋 Free Tier Limits

- 200 emails/month
- 2 email services
- 2 email templates
- Basic support

Perfect for a portfolio website!

## 🔒 Security Notes

- Your public key is safe to expose in client-side code
- EmailJS validates requests to prevent spam
- Rate limiting is automatically applied
- No sensitive credentials in your HTML

---

**Next Steps:**
1. Set up your EmailJS account
2. Get your credentials
3. Replace the placeholder values in `index.html`
4. Test the form locally
5. Deploy to GitHub Pages

Your contact form will then work perfectly for all visitors!
