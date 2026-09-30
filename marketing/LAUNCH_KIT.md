# QBOFlow Launch Kit

Copy-paste posts for promoting **https://akatetron.github.io/QBOFlow/**.

**Golden rules (so posts don't get removed or your account banned):**
- Read each community's self-promotion rules first. Many allow it only on certain days or in certain threads.
- Post one place per day, and stay to answer comments for the first 2 hours.
- Never post the same text in many subreddits at once. Reddit auto-flags that as spam.
- Be upfront that you built it ("I made…"). Honesty gets upvotes; disguised ads get banned.

---

## Day 1: Get indexed by Google and Bing (do this first)

1. **Google Search Console:** https://search.google.com/search-console
   - Add property → **URL prefix** → `https://akatetron.github.io/QBOFlow/`
   - Verify with the **HTML tag** method. Send me the tag and I'll add it to the page.
   - Sitemaps → submit `sitemap.xml`
   - URL Inspection → paste the site URL → **Request indexing**
2. **Bing Webmaster Tools:** https://www.bing.com/webmasters. Import from Google Search Console (one click). This also covers DuckDuckGo and Yahoo.

---

## Hacker News: "Show HN"

Post at https://news.ycombinator.com/submit on a weekday morning, US time.

**Title:** `Show HN: QBOFlow – Convert bank CSVs to QuickBooks .QBO files, fully in-browser`
**URL:** `https://akatetron.github.io/QBOFlow/`

**First comment (post it yourself right away):**
> Hi HN! Many banks only export CSV, but QuickBooks wants .QBO (Web Connect/OFX) files. The existing converters either charge a subscription or make you upload your bank statements to their server, which felt wrong for financial data.
>
> QBOFlow is a single static HTML page. PapaParse reads the CSV in the browser and plain JS writes the OFX 1.0.2 SGML file. A Content-Security-Policy with `connect-src 'none'` means the page can't send data anywhere, even if a CDN were compromised. It's open source, so you can check this yourself.
>
> It handles messy bank exports: preamble rows above the header, debit/credit columns, `(45.20)` and `1.234,56` style amounts, and DD/MM vs MM/DD auto-detection. FITIDs are hashed from the transaction contents, so re-importing overlapping statements doesn't create duplicates.
>
> Feedback welcome, especially CSV formats from your bank that break it.

---

## Reddit

Tailor each post to its subreddit, and post in only one per day.

### r/QuickBooks and r/Bookkeeping (answer-style post)

**Title:** `I made a free CSV → QBO converter that runs entirely in your browser (no uploads)`
> My bank only gives CSV exports, and every converter I found was either paid or wanted me to upload statements to their server. So I built one that runs 100% locally in the browser: https://akatetron.github.io/QBOFlow/
>
> - Drop in the CSV, map the date/payee/amount columns (it guesses them for you)
> - Supports single Amount or separate Debit/Credit columns
> - Preview before downloading the .QBO
> - Free, no account, and you can turn off wifi after the page loads and it still works
>
> Import it via File → Utilities → Import → Web Connect (Desktop) or Banking → Upload transactions (Online). If your bank's CSV doesn't convert cleanly, tell me and I'll fix it.

### r/SideProject, r/InternetIsBeautiful, r/webdev (Saturdays only: "Showoff Saturday")

**Title:** `QBOFlow: a zero-upload CSV to QuickBooks converter in a single HTML file`
> Built a finance tool with no backend at all. The CSV is parsed and converted in browser memory, and a CSP blocks all outbound network requests so data physically can't leave the page. Stack: vanilla JS, PapaParse, Tailwind, GitHub Pages. Would love feedback on the UX! https://akatetron.github.io/QBOFlow/

**Also worth trying:** r/smallbusiness (only in their weekly promo thread), r/Accounting (only when answering a question), r/freelance, r/selfhosted, r/privacy (lead with the privacy angle).

### Evergreen tactic (the best long-term traffic source)

Search Reddit, Quora and the QuickBooks Community (https://quickbooks.intuit.com/learn-support/) for:
`csv to qbo`, `convert csv quickbooks`, `bank only exports csv`, `web connect file`.
Reply to real questions with a genuinely helpful answer that explains the import steps, and mention the tool at the end. Old threads keep ranking on Google for years.

---

## Product Hunt

Launch at https://www.producthunt.com/posts/new at 12:01 AM Pacific time, Tuesday to Thursday.
- **Name:** QBOFlow
- **Tagline (60 chars):** `Convert bank CSVs to QuickBooks files, 100% in your browser`
- **Topics:** Fintech, Privacy, Productivity, Accounting
- **Thumbnail/gallery:** `og-image.png` from this repo, plus screenshots of each step
- **Maker comment:** reuse the Hacker News first comment above.

---

## Indie Hackers

Post in https://www.indiehackers.com/ under "Show IH":
**Title:** `I launched a free, privacy-first CSV → QuickBooks converter. Here's how it works`
Focus on the story: the problem, why zero-upload matters, the tech choices and what you learned. IH readers like build stories more than feature lists.

---

## X / Twitter

> Banks export CSV. QuickBooks wants .QBO. 🙃
>
> I built QBOFlow: a free converter that runs 100% in your browser.
> 🔒 Zero uploads
> 🚫 No sign-up
> ✈️ Works offline
> ♻️ Duplicate-safe re-imports
>
> https://akatetron.github.io/QBOFlow/
>
> #buildinpublic #QuickBooks #bookkeeping #indiehackers

## LinkedIn

> Small business owners and bookkeepers: if your bank only exports CSV, getting transactions into QuickBooks is a pain, and most converters either charge monthly or ask you to upload your bank statements to a stranger's server.
>
> I built QBOFlow, a free tool that converts CSV statements to QuickBooks .QBO files entirely inside your browser. Nothing is uploaded, and there's no account to create.
>
> 👉 https://akatetron.github.io/QBOFlow/
>
> If you work with clients who struggle with bank imports, I'd appreciate a share. 🙏

---

## Free directories (submit once each)

| Site | Notes |
|---|---|
| AlternativeTo (https://alternativeto.net) | List it as an alternative to paid CSV-to-QBO converters |
| SaaSHub (https://www.saashub.com) | Free listing |
| Uneed (https://www.uneed.best) | Free launch queue |
| Peerlist (https://peerlist.io) | Weekly project launches |
| BetaList (https://betalist.com) | Free queue (can be slow) |
| GitHub | Add topics to the repo; star-worthy READMEs get discovered |

---

## Email / word of mouth

Send a short personal note (not a mass email) to bookkeepers, accountants or small-business friends you actually know:
> Hey! I made a free tool that turns bank CSV exports into QuickBooks .QBO files, all inside your browser so nothing is uploaded. Would you try it on one of your statements and tell me if anything breaks? https://akatetron.github.io/QBOFlow/
