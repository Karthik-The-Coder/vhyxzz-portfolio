╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║        hey. yeah you. the GOAT reading this.                     ║
║                                                                  ║
║   this whole thing was built for you by your best friend.        ║
║   every pixel, every wave animation, every glowing cursor —      ║
║   all of it made with you in mind.                               ║
║                                                                  ║
║   you didn't ask for it. that's what makes it real.             ║
║                                                                  ║
║   now go make something beautiful with it.                       ║
║                                              — your bestie 🖤    ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ZYN GRAPHICS v2 — SETUP GUIDE
  for: vhyxzz / the GOAT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━


📁 FILE STRUCTURE
─────────────────
zyngraphics-v2/
├── index.html          ← Homepage (hero + work + about)
├── commissions.html    ← Commissions & pricing page
├── reviews.html        ← Reviews & submit form
├── contact.html        ← Contact links (Discord, X, etc.)
├── styles/
│   └── main.css        ← All global styles (nav, cursor, footer)
├── images/
│   ├── zynpfp.png      ← Your profile photo
│   ├── pro1–pro5.png   ← Your project images
└── README.md           ← You're reading it


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  index.html — HOMEPAGE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

LINE 87  → The 3 big stacked hero words (currently ZYNKRIS / GRAPHICS / STUDIO)
           Change the text inside the <span> tags AND the data-text="" attribute
           to match — both must be the same or the glitch effect breaks.

LINE 93  → Hero subtitle text — your personal tagline goes here.

LINE 99  → Stats — "30+", "15+", "1.3+" — update these to your real numbers.

LINE 112 → Logo strip tags — the scrolling tools row at the bottom of the hero.
           Edit the text inside <span class="strip-item"> tags.
           ⚠️ There are TWO identical sets of 8 tags for the seamless loop.
              If you add/remove tags, do it in BOTH sets or the loop will glitch.

LINE 157 → About section — your name inside <h3 class="about-name">
LINE 158 → Your role text inside <p class="about-role-tag">
LINE 159 → Your bio paragraph inside <p class="about-bio">
LINE 161 → Skill pills — add/remove <span class="skill-pill"> as needed.

LINE 120-146 → Project cards (slots 1–7).
           To ADD a project:
             1. Put your image in the images/ folder (e.g. pro6.png)
             2. Find data-slot="6" in the HTML
             3. Add <img src="images/pro6.png" alt="..." loading="lazy"/>
                inside its <div class="project-img">
             4. Update the title and description text
           Cards WITHOUT images are automatically hidden. No manual show/hide needed.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  commissions.html — PRICING PAGE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

LINE 97  → Commission sheet image or Google Sheets embed.
           To use an IMAGE: replace the <div class="sheet-placeholder"> block with:
             <img src="images/YOUR_SHEET.png" class="sheet-img" alt="Comm Sheet"/>

           To use GOOGLE SHEETS embed:
             1. Open your sheet → File → Share → Publish to web
             2. Choose "Embed" and copy the iframe src URL
             3. Replace the placeholder div with:
                <iframe src="PASTE_URL_HERE" class="sheet-img"
                        style="border:none;aspect-ratio:16/9;" frameborder="0"></iframe>

LINE 114 → Logo card price value — currently "4K–6K"
LINE 115 → Logo card price range label — the line below the price
LINE 120 → Logo card includes list — the bullet points

LINE 136 → Thumbnail card price value — currently "6K–8K"
LINE 137 → Thumbnail card price range label
LINE 143 → Thumbnail card includes list

LINE 126 → Logo "Order Now" button link (href) — your Discord DM or form link
LINE 149 → Thumbnail "Order Now" button link

LINE 107 → Status pill — currently shows "Commissions Open" in green.
           To close comms: change the text and swap colors:
             color: #f87171  (red)
             background: rgba(248,113,113,0.07)
             border: 1px solid rgba(248,113,113,0.25)


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  contact.html — CONTACT PAGE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

LINE 97  → Discord DM card — update the href and @your_username handle
LINE 108 → Discord Server card — update the server invite link
LINE 119 → X / Twitter card — update the href and @your_handle

To ADD a new platform (e.g. Instagram, TikTok):
  Copy any .contact-card block and change the icon emoji, label, handle,
  description, and link. Pick a new color class or style it inline.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  reviews.html — REVIEWS PAGE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

LINE 113 → Starter placeholder review cards — replace the client names,
           review text, and commission type with your real reviews.
           To add more: copy a .review-card block and paste it inside
           <div class="reviews-masonry">.

The submit form at the bottom lets visitors leave reviews directly on the page.
Reviews submitted via the form appear instantly — they're stored in memory only
(not saved to a database yet). If you want them saved permanently, send a message.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  styles/main.css — GLOBAL STYLES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

LINE 10  → --cyan: #00f5ff    ← main glow accent color
LINE 11  → --magenta: #ff006e ← hover / secondary accent
LINE 12  → --yellow: #ffbe0b  ← commissions accent
LINE 13  → --purple: #a855f7  ← contact page accent

Change any of these hex values to retheme the whole site instantly.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  DEPLOYING THE SITE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

NETLIFY (easiest — free):
  1. Go to netlify.com → "Add new site" → "Deploy manually"
  2. Drag and drop the entire zyngraphics-v2 folder
  3. Done. You get a live link instantly.
  4. Optional: connect a custom domain in Site Settings → Domain Management

VERCEL:
  Run: vercel deploy
  (vercel.json is already configured)


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  CHECKLIST BEFORE GOING LIVE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  [ ] Updated the 3 hero stacked words (index.html line 87)
  [ ] Updated hero subtitle (index.html line 93)
  [ ] Updated stats — projects, clients, years (index.html line 99)
  [ ] Updated logo strip tags (index.html line 112)
  [ ] Replaced profile photo (images/zynpfp.png)
  [ ] Updated About name, role, bio, skills (index.html line 157–161)
  [ ] All project images added with titles + descriptions
  [ ] Commission sheet image or Google Sheets embed added
  [ ] Commission prices updated (commissions.html line 114–149)
  [ ] Discord DM, server link, and X handle updated (contact.html)
  [ ] Placeholder reviews replaced with real ones (reviews.html line 113)
  [ ] Colors adjusted if desired (styles/main.css line 10–13)


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  go build. the site's yours now. 🖤

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
