# Suryavanshi's Tech - Setup Guide

## 🚀 Quick Start Guide

This guide will help you set up your portfolio website on GitHub Pages with a custom domain.

---

## Part 1: Setting Up GitHub Pages (No Coding Required!)

### Step 1: Create a GitHub Account
1. Go to [github.com](https://github.com)
2. Click "Sign Up" and create your free account
3. Verify your email address

### Step 2: Create a New Repository
1. Click the "+" icon in the top right corner
2. Select "New repository"
3. Name it: `yourusername.github.io` (replace `yourusername` with your actual GitHub username)
   - Example: If your username is `suryavanshi`, name it `suryavanshi.github.io`
4. Make it **Public**
5. Check "Add a README file"
6. Click "Create repository"

### Step 3: Upload Your Website Files
1. Click "Add file" → "Upload files"
2. Drag and drop the `index.html` file I created for you
3. Click "Commit changes"
4. Your site is now live at `https://yourusername.github.io`!

---

## Part 2: Adding Your Custom Domain (Optional)

### Step 1: Buy a Domain
1. Go to a domain registrar like:
   - Namecheap.com
   - GoDaddy.com
   - Google Domains
2. Search for your desired domain (e.g., `suryavanshitech.com`)
3. Purchase it (usually $10-15/year)

### Step 2: Configure DNS Settings
In your domain registrar's dashboard:
1. Find "DNS Settings" or "Manage DNS"
2. Add these records:

**For apex domain (suryavanshitech.com):**
- Type: `A`
- Host: `@`
- Value: `185.199.108.153`

Add three more A records with these values:
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

**For www subdomain:**
- Type: `CNAME`
- Host: `www`
- Value: `yourusername.github.io`

### Step 3: Configure GitHub
1. Go to your repository on GitHub
2. Click "Settings" → "Pages"
3. Under "Custom domain", enter your domain (e.g., `suryavanshitech.com`)
4. Check "Enforce HTTPS" (after DNS propagates, usually 24 hours)

---

## Part 3: How to Update Your Portfolio (Easy!)

### Adding a New Project

1. Go to your repository on GitHub
2. Click on `index.html`
3. Click the pencil icon (Edit this file)
4. Find this section (around line 450):

```html
<!-- Example Project 3 -->
<div class="project-card">
    <div class="project-image">PROJECT IMAGE</div>
    <div class="project-content">
        <h3>Cloud Infrastructure</h3>
        <p>Scalable microservices architecture...</p>
        <div class="project-tags">
            <span class="tag">AWS</span>
            <span class="tag">Docker</span>
            <span class="tag">Kubernetes</span>
        </div>
    </div>
</div>
```

5. Copy this entire block and paste it below
6. Change the text:
   - `<h3>Cloud Infrastructure</h3>` → Your project name
   - `<p>Scalable microservices...</p>` → Your project description
   - `<span class="tag">AWS</span>` → Your technologies

7. Click "Commit changes"
8. Your site updates automatically!

### Adding Project Images

1. Upload your image to an image hosting service:
   - [Imgur.com](https://imgur.com) (Free)
   - [ImgBB.com](https://imgbb.com) (Free)
   - Or keep them in your GitHub repo

2. In your project card, replace:
   ```html
   <div class="project-image">PROJECT IMAGE</div>
   ```
   
   With:
   ```html
   <div class="project-image" style="background: url('YOUR_IMAGE_URL') center/cover;">
   </div>
   ```

### Changing Your Social Links

Find this section (around line 490) and replace `#` with your actual URLs:

```html
<div class="social-links">
    <a href="https://github.com/yourusername">GitHub</a>
    <a href="https://linkedin.com/in/yourprofile">LinkedIn</a>
    <a href="https://twitter.com/yourhandle">Twitter</a>
    <a href="mailto:your.email@example.com">Email</a>
</div>
```

---

## Part 4: Customizing Colors & Style

All colors are defined at the top of the file. To change them, edit these values:

```css
:root {
    --void-black: #0a0a0f;          /* Background color */
    --deep-violet: #6b2ff5;         /* Primary violet */
    --electric-violet: #a855f7;     /* Lighter violet */
    --violet-glow: #c084fc;         /* Accent glow */
    --silver: #e2e8f0;              /* Text color */
    --platinum: #f8fafc;            /* Bright text */
}
```

Want different colors? Just change the hex codes!
- Use [Coolors.co](https://coolors.co) to find color palettes
- Use [ColorHunt.co](https://colorhunt.co) for inspiration

---

## Part 5: Troubleshooting

### My site isn't showing up
- Wait 5-10 minutes after uploading
- Check that your repository is named correctly: `yourusername.github.io`
- Make sure the file is named `index.html` (not `Index.html`)

### Custom domain not working
- DNS changes can take up to 24-48 hours
- Make sure you added all the A records correctly
- Check if HTTPS is enforced (turn it off temporarily if it causes issues)

### Image not showing
- Make sure the image URL is public and accessible
- Use direct image links (ending in .jpg, .png, etc.)
- Test the URL in a new browser tab

---

## Part 6: Making Updates Without Coding

### Option 1: GitHub Web Editor (Easiest)
1. Click on any file in your repository
2. Click the pencil icon to edit
3. Make changes
4. Click "Commit changes"
5. Wait 1-2 minutes for the site to update

### Option 2: Prose.io (Recommended for Blog Posts)
1. Go to [Prose.io](https://prose.io)
2. Authorize with GitHub
3. Select your repository
4. Edit your content in a nice interface
5. Click "Save" → Changes publish automatically

---

## Tips for Success

✅ **DO:**
- Update projects regularly
- Use high-quality images (at least 1200px wide)
- Keep descriptions concise but informative
- Add real links to your social profiles
- Test on mobile devices

❌ **DON'T:**
- Use copyrighted images without permission
- Leave placeholder text like "PROJECT IMAGE"
- Forget to commit changes
- Use too many different fonts or colors

---

## Next Steps

1. ✅ Upload `index.html` to GitHub
2. ✅ Replace example projects with your real projects
3. ✅ Add your project images
4. ✅ Update social links
5. ✅ (Optional) Set up custom domain
6. ✅ Share your portfolio with the world!

---

## Need Help?

- GitHub Pages Documentation: https://pages.github.com
- GitHub Community Forum: https://github.community
- Free images: https://unsplash.com
- Color palettes: https://coolors.co

**Remember:** Your website updates automatically every time you commit changes to GitHub. No need to redeploy or run commands!

---

Enjoy your luxurious tech portfolio! 🚀✨
