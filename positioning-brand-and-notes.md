# Mohamed Selim — positioning, brand and build notes

Everything here is drawn from your CV and from the projects you've built. Nothing is invented. Where a figure or a fact would help but I can't verify it, it's marked.

---

## A. Where you actually stand

Your CV currently reads as "real estate salesperson with an engineering degree." That undersells you in one direction and oversells nothing, which is the worst combination: it makes you look like a category of person there are thousands of in Cairo.

The truth is more specific and more valuable. You sell **industrial land to manufacturers**. That is a capital-investment sale, not a property sale. The buyer is committing to a plant, a workforce and a decade. The cycle is long, the questions are technical, and the person on the other side is often a foreign company deciding whether to enter Egypt at all. Very few salespeople can hold both halves of that conversation. You can, because you were an MEP engineer before you were a consultant.

Three things make your profile unusual, in order of commercial value:

1. **Industrial and manufacturing investment exposure.** Foreign and local investors, land, utilities, approvals. This is the scarce part, and it's your newest experience. It should lead everything.
2. **The engineering background, used commercially.** Not a second career. It's the reason you get a second meeting.
3. **Sales management at a small company.** Building a team, the process, the targets, and working across marketing, operations and finance. This is what makes you promotable rather than just employable.

Below those, and deliberately below: your work on CRM, reporting and AI. It's real and it's a genuine differentiator, but it must sit as supporting evidence. Lead with it and you become "the sales guy who's into AI," which is a weaker and more crowded position than "the industrial BD guy who also builds his own systems."

### Two honest weaknesses

- **No numbers anywhere.** Every line of your CV describes activity, not outcome. Fix this first; see section H.
- **A gap between 05/2024 and 01/2025**, and a career that moves between companies quickly (four employers between 2020 and 2023). Nobody will hold the gap against you, but they will ask. Have one clean sentence ready and, if it was a job search or a break, say so plainly. The best version is the true one, delivered without discomfort.

### The five positioning options, judged

| | Positioning | Verdict |
|---|---|---|
| 1 | Business Development + Industrial Investment | **Recommended.** Scarcest, best paid, matches your current role and where you're heading. |
| 2 | B2B Sales + Business Development | Safe but generic. Competes with everyone. Use as the fallback keyword layer, not the headline. |
| 3 | Commercial + Industrial Development | Close second. Slightly more developer-side; narrows you to real estate developers. |
| 4 | Sales + Technology + AI | Premature. Your title doesn't support it and a hiring manager will test it hard. Keep as a supporting section. |
| 5 | Technical + Commercial Professional | True but vague. Nobody recruits for "technical and commercial." |

**Primary positioning: Business Development and Industrial Investment, backed by an engineering background and a working interest in sales systems.**

Everything on the site is built to that. One identity, three supports.

---

## B. The brand, in the words you'd actually use

**Headline (LinkedIn, CV, site):**
Sales | Investment Consulting | Account Management

**One line:**
I sell to investors. I work out what they are trying to achieve, advise them on where the money should go, and stay with it until it closes.

**Three lines (LinkedIn About opening):**
I sell industrial land to companies setting up manufacturing in Egypt, both local and foreign. I trained as a mechanical engineer and worked in MEP design before moving into sales, so the technical half of an investor's questions isn't a problem. Before this I ran the sales team at a startup, which taught me more about business than any single deal has.

**In a room, 20 seconds:**
"I'm at Elsewedy Industrial Development. I work with investors who want to build a factory here — some Egyptian companies expanding, some foreign manufacturers looking at the market for the first time. My background is mechanical engineering, so I can usually answer the technical questions in the first meeting instead of promising to come back."

**Tone rules for anything you write from now on:** short sentences, concrete nouns, no adjectives you can't defend. If a sentence would look the same on someone else's profile, cut it.

---

## C–D. The website

`mohamed-selim.html` — one file, no build step, no framework, no libraries. Only external call is Google Fonts (Archivo + Newsreader), and it falls back cleanly to system fonts if that fails.

Structure, in order: hero, short introduction, the path (seven stages, interactive), experience (six roles, expandable), engineering-in-a-sales-job, how you think about sales, things you've built, education, off the clock, contact.

**Before you publish, do these six things:**

0. Add a portrait as `portrait.jpg` next to the file (landscape, plain background, natural light). The hero canvas shows it automatically and falls back to the drawing until then.

1. Put your CV PDF next to the HTML file and name it `Mohamed-Selim-CV.pdf` (the two Download CV buttons point at that name). Fill the placeholders first.
2. Search the file for `ADD A REAL FIGURE HERE`. Three comments mark where a number would strengthen the page. Add them if you have them, delete the comments either way.
3. Decide whether you want the "Things I've built" section public. It's the most memorable part of the site and the most likely to start a conversation, but it names NABRA. If you'd rather keep that quiet while you're employed, cut that one entry and keep the other three.
4. Update the `canonical` and `og:url` tags in the head with your real domain.
5. Read the "off the clock" paragraph out loud. If it doesn't sound like you, rewrite it in your own words. That one paragraph does most of the work of making the site feel human.

---

## E. The CV

**`Mohamed_Selim_CV.docx`** — one page, one version, for everything. A PDF copy sits beside it.

No second version, and **no numbers or placeholders**. Every bullet describes what you actually do rather than pointing at a figure you'd have to justify. If a recruiter wants results, they'll ask, and you can answer with real numbers in the conversation instead of committing them to paper.

Plain Word: no tables, columns, text boxes, icons or graphics. Standard headings (`PROFESSIONAL SUMMARY`, `CORE COMPETENCIES`, `PROFESSIONAL EXPERIENCE`, `TECHNOLOGY`, `EDUCATION & CERTIFICATIONS`) that every parser recognises, dates as MM/YYYY, company and title on one line each so the career reads in about eight seconds.

It leads with **Sales**, names qualification as the strength, and covers the AI and CRM work under Technology. Tailor by deleting, never by rewriting — cut two Archplan bullets for a role that doesn't care about engineering, rather than starting a second file that drifts out of date.

## F. The assistant on the site

A chat panel, bottom right, that answers questions about you.

It is **not** a language model. It runs entirely in the visitor's browser, matching their question against about thirty answers written from your own record, with rarity-weighted scoring, a synonym table, phrase matching and an off-topic guard. Verified against 27 varied questions with no wrong routing.

That design is deliberate, and it's the same reasoning as the CRM copilot: an API key sitting in a public HTML file is a key anyone can take, and a real model with no grounding will eventually invent a figure about you and say it with confidence. Here, hallucination is impossible by construction — a human wrote every sentence. When it doesn't know, it says so and points at your email.

It covers: who you are, what you do day to day, how you qualify, the technical questions you can field, AI use, what you've built, each role, why you left engineering, education, certifications, languages, location, why hire you, **where you're weaker**, and contact. Salary is deflected to you.

To edit an answer, open the file, find `var K=[` near the bottom, and change the text. To add a topic, copy an existing block and give it an `id`, keywords in `k`, the answer in `a`, and follow-up chips in `c`. Add the id to the `PRIMARY` list with the two or three words that should point at it strongly.

If you ever want a real model behind it, that needs a small server to hold the key. Tell me and I'll build the proxy.

## G. Sales technology profile — what you can honestly claim

**Confirmed by experience**
- CRM and pipeline management, lead and account records, follow-up scheduling
- Sales forecasting, target setting, performance reporting
- Sales process design, cycle planning, weekly review cadence
- Commercial offer preparation and pricing structures
- SolidWorks (CAD); MEP design for HVAC, plumbing, firefighting

**Project experience (built by you, outside employment)**
- A role-based CRM in use by a sales team: lead ownership, permissions, follow-up queues, offer generation, management reporting
- A pipeline assistant inside that CRM that answers questions from company records with no external model call
- An industrial locations and offer-generation platform

**Working knowledge / area of interest**
- Prospecting, lead enrichment and contact discovery as a discipline
- Sales automation and workflow tooling
- Dashboards and sales analytics

**Verify before you claim any of these**
Salesforce. Apollo. SignalHire. Power BI. HubSpot or any other named CRM. Your actual Excel level.

I left all of these off the website and marked them in the CV. If you have used any of them at work — even for a few months — name it, because recruiters and ATS filters match on those exact strings. If you have only read about them, leave them out. The gap between "familiar with Salesforce" and being asked to demonstrate it in a second interview is where credibility goes to die.

---

## H. What to send me to make this materially stronger

In rough order of impact:

1. **Elsewedy numbers.** Plots or square metres sold, contract value, number of investors you've brought in, how many are foreign, which countries. Even a range or a "since January" figure.
2. **Weaverbird numbers.** How many people did you hire and manage? What was the target and what percentage did you deliver? Revenue or units closed under your management?
3. **The 05/2024 – 01/2025 gap.** What were you doing? One sentence is enough and it may well belong on the CV.
4. **Foreign investor detail.** Which markets or nationalities have you dealt with? "Investors from Turkey, China and the Gulf" is a much stronger line than "foreign investors."
5. **Languages.** Arabic and English are assumed; confirm your English level and add any others.
6. **Tools.** Answers to the verify list above.
7. **Svreico and B2B numbers.** Units sold, accounts managed, deal sizes.
8. **A photograph**, if you want one on the site. Editorial, plain background, natural. The site works without one; if you add one, it must be good, because a weak photo will undo the rest.
9. **Your domain name**, so I can set the canonical and Open Graph tags properly.
10. **Whether the CRM you built is officially sanctioned at Elsewedy.** It changes how boldly you can describe it in an interview.

---

## I. Design system (current build)

Warm off-white `#F6F5F0` with a faint grid, one accent `#F2521B`, black used only for the marquee, the open item in a list, and the contact block. Plus Jakarta Sans throughout. Pill navigation, arch portrait, collapsible lists.

## J. Final review notes

**Section order:** Hero → About → What I sell (Started / Then / Now / Alongside) → Why the engineering matters → Work experience → Things I've built → Education → Contact. Eight sections, each introducing something new.

**Three conflicts between your master brief and your own instructions, resolved in your favour:**

1. The brief says the site must stay light with no dark sections and a restrained accent. You chose this direction deliberately after seeing four others. Kept.
2. The brief asks for `[INSERT NUMBER]` placeholders in the CV. You told me explicitly you don't want numbers or placeholders. The CV stays clean.
3. The brief warns against chatbots. You asked for the assistant, and it is grounded so it cannot invent claims. Kept.

**Latest pass:** the second portrait block in About became a facts panel (Experience / Now / Sells / Before / Education / Training), which is what a recruiter scans for in the first ten seconds. "What I sell" now leads with Now, then Before, then Started. Content is visible without JavaScript and in print; the scroll reveal only runs once the browser confirms it can.

**What is still missing, and only you can supply it:** the portrait. `portrait.png`, cut out on a transparent background, shoulders up. The hero arch and the About block both pick it up automatically.

**Verified:** no console errors, no horizontal overflow at 1440/834/393, single H1 with correct H2/H3 order, every image has alt text, every link has an accessible name, focus rings present, reduced-motion respected, assistant answering correctly after the restructure, 3KB of dead CSS removed.
