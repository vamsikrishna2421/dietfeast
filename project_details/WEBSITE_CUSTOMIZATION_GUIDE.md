# DIET FEAST - Website Customization Guide

This guide shows you exactly where to modify the HTML/CSS code to customize your pitch website.

---

## 🎨 Easy Customizations (Find & Replace)

### 1. Change Company Name (FitMeal → Diet Feast)

**Find in the HTML:**
```html
<div class="nav-logo">🍽️ FitMeal</div>
```

**Replace with:**
```html
<div class="nav-logo">🍽️ Diet Feast</div>
```

**Find:**
```html
<h1>🍽️ FitMeal</h1>
<p>Ultra-Low Calorie Meal Prep Delivery - Worcester, MA</p>
```

**Replace with:**
```html
<h1>🍽️ Diet Feast</h1>
<p>Ultra-Low Calorie Meal Prep Delivery - Worcester, MA</p>
```

---

### 2. Change Social Media Links

**Find:**
```html
@dietfeast
#lowcalmeals #mealprep #fitfood #worcester #localbusiness
```

**Update with your actual:**
- Instagram handle
- Facebook page
- TikTok (if applicable)
- Contact email/phone

---

### 3. Update Membership Plan Names & Descriptions

**In the Membership Plans section, you can:**
- Change plan names (e.g., "Starter" → "Weekly Kick-Start")
- Update descriptions
- Adjust pricing
- Change badges (BEST VALUE, POPULAR, etc.)

**Example - Find:**
```html
<div class="plan-name">🌟 Starter Plan</div>
<div class="plan-price">$74.99<small>/month</small></div>
```

**Replace with:**
```html
<div class="plan-name">🌟 Weekly Kick-Start</div>
<div class="plan-price">$79.99<small>/month</small></div>
```

---

## 🎨 Design Customizations (Color & Style)

### Change Color Scheme

All colors are defined at the top of the `<style>` section:

```css
:root {
    --primary: #2563eb;        /* Blue */
    --accent: #f97316;         /* Orange */
    --success: #10b981;        /* Green */
    --bg: #0f172a;             /* Dark background */
    --surface: #1e293b;        /* Card background */
    --text: #e2e8f0;           /* Main text */
    --text-muted: #94a3b8;     /* Muted text */
    --border: #334155;         /* Borders */
}
```

**Popular color combinations:**

**Modern Blue:**
```css
--accent: #3b82f6;     /* Bright blue */
--success: #06b6d4;    /* Cyan */
```

**Green (Health/Growth):**
```css
--accent: #10b981;     /* Emerald */
--success: #34d399;    /* Light green */
```

**Purple (Premium):**
```css
--accent: #a855f7;     /* Purple */
--success: #ec4899;    /* Pink */
```

**Change Logo Emoji**

The website uses food emojis. Options:
- 🍽️ (current - plate)
- 🥗 (salad)
- 🍲 (bowl)
- 🥘 (paella/dish)
- 💪 (strength - fitness angle)
- ⚡ (energy)
- 🎯 (goal-focused)

**Replace in nav and hero:**
```html
<div class="nav-logo">🥗 Diet Feast</div>
<h1>🥗 Diet Feast</h1>
```

---

## 📝 Content Updates (By Page)

### Home Page

**Update the hero section:**
```html
<p>Ultra-Low Calorie Meal Prep Delivery - Worcester, MA</p>
<p style="color: var(--text-muted); margin-bottom: 0;">100-200 cal meals that look & taste like 500+ calories</p>
```

You can customize this to your unique message.

**Update Executive Summary stats:**
```html
<div class="stat-card">
    <div class="stat-value">$9.99</div>
    <div class="stat-label">Per meal (37% margin)</div>
</div>
```

Change any of these numbers based on your actual business.

**Update "Why FitMeal" to "Why Diet Feast":**
```html
<h3>Why Diet Feast?</h3>
<ul>
    <li><span class="highlight">Shirataki Noodles</span> - Only 10 calories...</li>
    ...
</ul>
```

---

### Ingredients Page

**Update Amazon links:**

Find:
```html
<a href="https://www.amazon.com/Hethstia-Shirataki-Low-Carb-Fettuccine-Calorie/dp/B0D4TQBQ7Z" target="_blank">
```

Replace with your preferred product link.

**Update cost breakdown tables:**

Find:
```html
<tr>
    <td>🍗 Chicken Breast</td>
    <td>Costco/Local Market</td>
    <td>$3.00/oz</td>
    <td>$2.50</td>
</tr>
```

Update numbers based on your actual local prices.

---

### Membership Plans Page

**Update plan pricing & benefits:**

Each plan is a `<div class="plan-card">`. Update:
- `.plan-name` - Plan name
- `.plan-price` - Monthly price
- `.plan-details ul` - List of benefits
- `.highlight` - Cost per meal

**Example:**
```html
<div class="plan-name">🔥 Popular Plan</div>
<div class="plan-price">$139.99<small>/month</small></div>
<p style="color: var(--text-muted); margin: 1rem 0;">5 meals x 2 weeks</p>
```

---

### Prep Schedule Page

**Update daily routine times:**

Find:
```html
<h3>Morning (6-8 AM) - Protein Prep (45 min)</h3>
```

Adjust times based on your actual schedule.

**Update cooking instructions:**

Find:
```html
<li><strong>Chicken:</strong> Thaw, slice, season, pan-sear 5 min each side</li>
```

Replace with your exact cooking methods.

---

### Equipment Page

**Update equipment costs:**

Find:
```html
<li><strong>Large Skillet/Wok:</strong> $30-50</li>
```

Update with actual prices from your research.

---

### Market Page

**Update target customer profile:**

Find:
```html
<li>Age: 20-50 years old</li>
<li>Income: $40k-120k annual</li>
```

Customize based on your actual research.

**Update competitor names & prices:**

Find:
```html
<li><strong>Weight loss meals are expensive:</strong> $13.99-16.99/meal from HelloFresh, Factor</li>
```

Update if you have different competitors.

**Update local references:**

Find:
```html
Worcester, Massachusetts (USA)
Worcester metro area
Local gyms in Worcester area
```

Keep or update based on your actual service area.

---

## 🔧 Advanced Customizations

### Add New Sections

You can duplicate a page and create a new one:

```html
<!-- Template for new page -->
<div id="new-page-name" class="page">
    <section>
        <h2>New Page Title</h2>
        <!-- Your content here -->
    </section>
</div>
```

Then add a navigation link:
```html
<li><a onclick="showPage('new-page-name')" class="nav-link">New Page</a></li>
```

### Add Recipe Cards

Create a new page with recipes:

```html
<div id="recipes" class="page">
    <section>
        <h2>Our Recipes</h2>
        <div class="grid">
            <div class="card">
                <h3>Chicken Teriyaki</h3>
                <p><strong>Calories:</strong> 150</p>
                <p><strong>Protein:</strong> 25g</p>
                <ul>
                    <li>Shirataki noodles</li>
                    <li>Grilled chicken breast</li>
                    <li>Broccoli & bell pepper</li>
                </ul>
            </div>
        </div>
    </section>
</div>
```

### Add Photo Gallery

Add an images section with meal photos:

```html
<h3 style="text-align: center; margin: 3rem 0;">Our Meals in Action</h3>
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem;">
    <img src="your-image.jpg" style="width: 100%; border-radius: 8px;">
    <img src="your-image-2.jpg" style="width: 100%; border-radius: 8px;">
</div>
```

---

## 📱 Mobile Optimization Tips

The website is already mobile-responsive, but you can optimize further:

1. **Shorter hero text on mobile:**
   Add: `@media (max-width: 600px) { .hero h1 { font-size: 1.5rem; } }`

2. **Stack tables vertically on mobile:**
   Tables are already responsive - they'll wrap automatically

3. **Test on phones:** Open in Chrome DevTools → Toggle device toolbar

---

## 🚀 Before Deploying

### Checklist
- [ ] Update all company references (FitMeal → Diet Feast)
- [ ] Update prices to your actual prices
- [ ] Update social media handles
- [ ] Update phone number & email (if including)
- [ ] Update local references (gyms, neighborhoods)
- [ ] Update color scheme (if desired)
- [ ] Test on mobile
- [ ] Test all navigation links
- [ ] Update Instagram handle in social links
- [ ] Proofread all text

---

## 💾 How to Use the Code

### Option 1: Online (Easiest)
1. Copy all HTML code from the file
2. Paste into an online editor (CodePen, Replit, JSFiddle)
3. Edit in the browser
4. Share the link

### Option 2: Local File
1. Save as `diet-feast.html`
2. Open in any text editor (VS Code, Notepad++, etc.)
3. Edit and save
4. Open in web browser (double-click the file)
5. Share the .html file

### Option 3: Web Hosting
1. Upload to a web host (Vercel, Netlify, GitHub Pages - all free)
2. Get a URL
3. Share with co-founders

---

## 📊 Suggested Updates for Your Business

Based on the description, I recommend updating:

1. **Add your photo/video:** Hero section with a meal photo
2. **Add testimonials section:** Screenshots of customer praise
3. **Add FAQ page:** Common questions about the service
4. **Add contact form:** Email signup for interested co-founders
5. **Add timeline graphic:** Visual of the 3-phase roadmap
6. **Add team section:** You + co-founder profiles (add later)

---

## 🎯 Next Steps

1. **Download the HTML file** from outputs
2. **Make these quick changes:**
   - Replace "FitMeal" → "Diet Feast"
   - Update colors to match your brand
   - Update phone/email
3. **Test in browser** (open .html file locally)
4. **Share with co-founders** (upload to Vercel or email .html file)
5. **Gather feedback** and iterate

---

## 🆘 Common Issues & Fixes

**"Colors aren't changing"**
- Make sure you're editing the `:root` section in `<style>`
- Clear browser cache (Ctrl+Shift+Delete)

**"Links don't work"**
- Make sure `onclick="showPage('page-id')"` matches the `id="page-id"` in the page divs
- Check spelling of page names

**"Styling looks weird on mobile"**
- Check the `@media` section at bottom of CSS
- Test with browser DevTools device emulator

**"Want to add a logo image"**
- Replace emoji in `.nav-logo` with: `<img src="your-logo.png" style="height: 30px;">`

---

**Happy customizing! Your pitch website is ready to impress co-founders.** 🚀

