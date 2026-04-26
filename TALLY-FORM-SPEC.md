# Tally Form Spec — Brand Questionnaire

Build this form in Tally (free tier). All copy below is final. Match the section structure and field types exactly so the submission data is consistent across clients.

---

## Form metadata

- **Form title (internal):** Brand Questionnaire
- **Form name shown to client:** Brand Questionnaire
- **Theme:** match Roni's brand
  - Background: `#FAF9F7`
  - Text: `#1A1A1A`
  - Primary button: `#1A1A1A` background, `#F5F3EF` text
  - Accent (if Tally lets you set it): `#D4A853`
  - Font: DM Sans (Tally has it in their library)

---

## Cover page (welcome screen)

**Title:** Brand Questionnaire

**Subtitle / description:**
15 minutes. No right or wrong answers. This helps me understand your business, your audience, and what you are building toward.

**Button text:** Start

---

## Section A — Your Business

### Question A1
**Type:** Long answer (paragraph)
**Required:** Yes
**Question:** What does your business do, and who does it serve?
**Description:** Be as specific as possible. Include what makes you different from others in your space.
**Placeholder:** Your answer...

### Question A2 (split into two short answers shown side by side if Tally supports, otherwise stacked)
**Type:** Short answer × 2
**Required:** Both yes
**Question (group label):** How long have you been in business, and where are you based?
**Field 1:** Years in business
**Field 2:** Location / City

### Question A3
**Type:** Multiple choice (multi-select / checkboxes)
**Required:** Yes
**Question:** What is the main goal of this project?
**Options:**
- Launch a new brand / business
- Refresh an existing brand
- Build or redesign a website
- Full brand + website package

---

## Section B — Your Audience

### Question B1
**Type:** Long answer
**Required:** Yes
**Question:** Who is your ideal client or customer?
**Description:** Describe them specifically: age, profession, values, what they are looking for.
**Placeholder:** Your answer...

### Question B2
**Type:** Long answer
**Required:** Yes
**Question:** What do you want people to feel when they land on your site or see your brand?
**Placeholder:** Your answer...

### Question B3
**Type:** Long answer
**Required:** Yes
**Question:** List 3 brands (in any industry) whose look and feel you admire. Why?
**Description:** They do not need to be in your field. What draws you to them?
**Placeholder:** Your answer...

---

## Section C — Design Direction

### Question C1
**Type:** Short answer
**Required:** Yes
**Question:** How would you describe your brand in 3 words?
**Description:** No overthinking. First words that come to mind.
**Placeholder:** e.g. warm, bold, grounded

### Question C2
**Type:** Long answer
**Required:** No
**Question:** Are there any colors, styles, or visual elements you want to avoid?
**Placeholder:** Your answer...

### Question C3
**Type:** Long answer
**Required:** No
**Question:** Anything else I should know before we start?
**Placeholder:** Your answer...

---

## Final page (so Roni knows who submitted)

### Question Z1
**Type:** Short answer
**Required:** Yes
**Question:** Your name

### Question Z2
**Type:** Email
**Required:** Yes
**Question:** Your email
**Description:** So Roni can confirm receipt and follow up if anything is unclear.

---

## Thank you / confirmation page

**Heading:** Thank you, {your name}.

**Body:**
Your answers are with Roni. You will receive a confirmation within 24 hours. In the meantime, the next step is uploading your content materials. Your shared folder link is in your kickoff email.

**Button:** Back to your project home
**Button URL:** [will be the deployed Welcome page URL, e.g. `https://onboarding.ronimargolin.com/perry-pesi/`]

---

## Tally settings to enable

- ✅ **Save and resume** (under form settings → general). This is the key feature.
- ✅ **Email notifications** to `hello@ronimargolin.com` on every submission
- ✅ **Auto-sync to Google Sheet** (under integrations) → optional but recommended for searchable history
- ✅ **Submission limit per respondent**: keep at default (no limit, since same client can edit and re-submit during onboarding if needed)
- ❌ **CAPTCHA**: off (low traffic, no spam concerns)

---

## Per-client variant pattern

For each new client (Perry, Hayley, etc.):

1. **Duplicate the master form** in Tally
2. Rename it: `Brand Questionnaire — [Client Name]`
3. Update the Thank you button URL to point to that client's Welcome page
4. Copy the new form's URL
5. Plug that URL into the client's `index.html` Welcome page (Step 1 button)

That's it. ~30 seconds per client.

---

## Reference: the deprecated HTML version

The HTML version at `questionnaire.html` is deprecated. Do not link to it. Keep it in the repo as a backup reference until the Tally version is verified working with a real submission.
