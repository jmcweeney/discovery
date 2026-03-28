# Deploy Instructions — Alan Website Discovery
## Two steps: Formspree (email) → Vercel (hosting)

---

## STEP 1 — Set Up Formspree (5 minutes)

Formspree handles receiving Alan's answers and routing them to jeff@addl.co.

1. Go to **https://formspree.io** and create a free account (use jeff@addl.co)
2. Click **+ New Form**
3. Name it: `Alan Website Discovery`
4. Set the email to: `jeff@addl.co`
5. Click **Create Form**
6. Copy your **Form ID** — it looks like `xpwzabcd` (8 characters)
7. Open `index.html` in any text editor
8. Find this line (near the top of the `<form>` tag):
   ```
   action="https://formspree.io/f/REPLACE_WITH_YOUR_FORM_ID"
   ```
9. Replace `REPLACE_WITH_YOUR_FORM_ID` with your actual Form ID:
   ```
   action="https://formspree.io/f/xpwzabcd"
   ```
10. Save the file.

**Done.** Formspree free tier allows 50 submissions/month — plenty for this project.

---

## STEP 2 — Deploy to Vercel (5 minutes)

1. Go to **https://vercel.com** and sign up (free) with your GitHub, Google, or email
2. From the Vercel dashboard, click **Add New → Project**
3. Choose **"Deploy from your computer"** or click **"Browse"** to upload
4. Drag and drop the entire `alan-discovery` folder into the upload area
5. Vercel will detect it as a static site automatically
6. Click **Deploy**
7. In ~30 seconds you'll get a live URL like:
   ```
   https://alan-discovery.vercel.app
   ```

**Optional — Custom URL:**
- In Vercel project settings → **Domains**
- Add a custom domain like `discovery.addl.co` if you want it on your own domain
- Vercel provides free SSL automatically

---

## STEP 3 — Send Alan the Link

Once deployed, copy the Vercel URL and send Alan something like:

> "Hey Alan — I've put together a quick questionnaire to capture your vision for the site. Takes about 10–15 minutes. Hit submit when you're done and your answers come straight to me: **[your-vercel-url]**"

---

## What Happens When Alan Submits

1. His name, email, and all checked items/answers get sent to **jeff@addl.co**
2. Formspree formats it as a clean email with all fields labeled
3. Alan's email address is set as the reply-to, so you can reply directly to him
4. The page shows Alan a confirmation screen

---

## Troubleshooting

- **Form not sending?** Double-check the Form ID in `index.html` matches exactly what Formspree shows
- **Vercel deploy fails?** Make sure both `index.html` and `vercel.json` are in the same folder
- **Want to test first?** Open `index.html` in a browser locally — everything works except the email send (that requires a live domain)

---

*Built by Additional Corporation · jeff@addl.co*
