# Task: Reframe Portfolio Site for Health IT — HCA St. Petersburg Application

## Setup
The entire site is a single file: `index.html` (552 lines). No other files need to be touched.
Mount the PortfolioSite folder, read `index.html`, make the 4 edits below, validate, then commit.

---

## Edit 1 — Hero Headline (line 347)

**Find:**
```html
<h2 class="hero-headline">Jacob Ziolkowski — Web Systems &amp; IT Support</h2>
```

**Replace with:**
```html
<h2 class="hero-headline">Jacob Ziolkowski — Health Informatics &amp; IT</h2>
```

---

## Edit 2 — Homepage Bio (lines 348–352)

**Find:**
```html
          <p class="summary-placeholder">
            Early-career IT professional focused on accessible web experiences and front-line support for high-visibility production systems.
            I maintain and troubleshoot standards-compliant university sites, turn non-technical stakeholder requests into clear, structured web updates, and resolve issues across CMS, Windows, and macOS environments.
            Drawing from roles as a Web Admin Assistant with FSU ITS and IT Helpdesk Technician with FSU's College of Communication &amp; Information, I bring structured troubleshooting, precise documentation, and clear communication that keep teams productive—explore my experience and projects below.
          </p>
```

**Replace with:**
```html
          <p class="summary-placeholder">
            Early-career Health Informatics and IT professional completing a B.S. in Information Communication &amp; Technology with a certificate in Health Informatics at Florida State University.
            I design and build patient-centered health IT solutions — from AI-enhanced telehealth diagnostics to chronic condition tracking apps — and bring hands-on IT systems experience from production environments at FSU.
            My focus is the intersection of clinical data, health technology, and usable design. Explore my projects and experience below.
          </p>
```

---

## Edit 3 — Add Health IT Skills Tags (lines 393–405)

**Find** the closing `</div>` of the skills-tags block:
```html
            <span class="skill-tag">Time &amp; ticket management</span>
          </div>
```

**Replace with:**
```html
            <span class="skill-tag">Time &amp; ticket management</span>
            <span class="skill-tag">Health Informatics</span>
            <span class="skill-tag">FHIR &amp; EHR Systems</span>
            <span class="skill-tag">HIPAA Compliance</span>
            <span class="skill-tag">Clinical Informatics</span>
            <span class="skill-tag">Patient-Centered Design</span>
          </div>
```

---

## Edit 4 — Portfolio Grid: Add HIT Prototype Card First, Move SkinSync Second

The portfolio grid currently has 6 cards in this order:
1. FSU ITS Web Content Management
2. FSU CCI IT Helpdesk Support
3. SkinSync App Prototype
4. Interactive Resume Website
5. ThinkAI / Canva AI Workshop Presentation
6. Information Architecture & Documentation Project

**Target order:**
1. HIT Solution Prototype ← NEW card, insert first
2. SkinSync App Prototype ← already exists, move to position 2
3. FSU ITS Web Content Management
4. FSU CCI IT Helpdesk Support
5. Interactive Resume Website
6. ThinkAI / Canva AI Workshop Presentation
7. Information Architecture & Documentation Project

**Step 4a — Insert the new HIT Prototype card at the very start of the `.portfolio-grid` div**, immediately after `<div class="portfolio-grid">`:

```html
            <article class="project-card">
              <div class="thumb-placeholder">[HIT Prototype] <span class="placeholder-label">Thumbnail</span></div>
              <div class="body">
                <div class="title">HIT Solution Prototype</div>
                <p class="desc">Designed an AI-Enhanced Telehealth Diagnostics System to close the physical exam gap in remote patient care. The platform integrates wearable biometrics, computer vision, and an AI diagnostic support engine with FHIR-compliant EHR export — providing physicians with structured, exam-quality data during virtual appointments. Built to serve patients in rural, mobility-limited, and home-bound settings where in-person care is inaccessible.</p>
                <ul class="skills-list">
                  <li>FHIR &amp; EHR integration</li>
                  <li>AI diagnostic support systems</li>
                  <li>Health IT system design</li>
                  <li>Clinical workflow prototyping</li>
                  <li>Patient-centered UX</li>
                </ul>
              </div>
            </article>
```

**Step 4b — Move the SkinSync card** (currently card 3) to immediately follow the new HIT Prototype card (position 2). It already exists — cut it from its current location and paste it as the second card.

The SkinSync card to move is:
```html
            <article class="project-card">
              <div class="thumb-placeholder">[SkinSync] <span class="placeholder-label">Thumbnail</span></div>
              <div class="body">
                <div class="title">SkinSync App Prototype</div>
                ...
              </div>
            </article>
```

---

## Verification

After making all edits:
1. Take a screenshot of the site in the browser — confirm headline reads "Health Informatics & IT"
2. Scroll to Portfolio — confirm HIT Solution Prototype is the first card
3. Confirm SkinSync is immediately second
4. Confirm 5 new health IT skill tags appear in the Experience section

---

## Git Commit

Once verified, commit with:
```
git add index.html
git commit -m "Reframe site for health IT — update headline, bio, skills, add HIT prototype card"
```

GitHub Pages will auto-deploy within ~60 seconds of pushing. Push with:
```
git push
```

---

## Notes
- **Do NOT change** the visual design, color scheme, CSS, or layout
- **Do NOT move or rename** any other files in the repo
- **Do NOT** copy .docx or .rtf files from the Resume folder into this repo
- The `.rtf` files already in this folder (IR Homepage Final Criteria.rtf, etc.) are class reference docs — leave them as-is
