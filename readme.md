# VOID.GFX Portfolio — Setup Guide

## Folder Structure
```
zivvo-portfolio/
├── index.html        ← Main portfolio page
├── contact.html      ← Contact page with all socials
├── styles/
│   └── main.css      ← All shared styles
├── images/
│   └── (put ALL your images in here)
└── README.md         ← This file
```

---

## How to Edit Your Info

### 1. Your Name & Brand
Search for `VOID.GFX` in both HTML files and replace with your brand name.
Search for `YOUR NAME` and replace with your real name.

### 2. Add Your Photo (About section)
- Put your photo in the `/images/` folder (e.g. `photo.jpg`)
- In `index.html`, find the about section and replace:
  ```html
  <div class="about-image-placeholder">...</div>
  ```
  with:
  ```html
  <img src="images/photo.jpg" alt="Your Name" style="width:100%;height:100%;object-fit:cover;" />
  ```

### 3. Add Your Projects
- Put your project images in `/images/` folder (e.g. `project1.jpg`, `project2.jpg`)
- In `index.html`, find each `<!-- PROJECT 1 -->` block
- Inside `.project-img`, add your image:
  ```html
  <img src="images/project1.jpg" alt="Project Name" />
  ```
- Fill in the project title, category, and description
- Replace `href="#"` with your project link (Behance, Instagram, etc.)
- **Cards with no image stay hidden automatically — clean!**

### 4. Edit Contact Links (contact.html)
Replace every `YOURUSERNAME`, `YOURHANDLE`, `YOURID`, `YOURCHANNEL` with your real info.
Replace `your@email.com` with your real email.
To delete a card you don't use (e.g. YouTube), delete the entire `<a class="contact-card youtube">` block.

### 5. Update Stats (Hero section)
Find the three `00+` stat numbers and replace with your real numbers:
- Projects Done
- Clients Served  
- Years Active

### 6. Change Your Skills
Find `.skills-grid` in `index.html` and edit the skill badges to match your actual tools.

---

## How to Publish (Free)

1. Go to **netlify.com** and create a free account
2. Drag and drop the entire `zivvo-portfolio` folder onto Netlify
3. You get a free live link instantly — no coding needed!
4. Optional: connect a custom domain later

---

## How to Open Locally
Just open `index.html` in your browser — no server needed.
Right click → Open with → Chrome/Firefox

---

© 2026 — Your portfolio, your rules.
