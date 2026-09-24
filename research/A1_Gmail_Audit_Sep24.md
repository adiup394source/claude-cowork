# A1: Gmail forensics of the WAiFF India cold-email campaign (2 to 24 Sep 2026)

Prepared 24 Sep 2026 from adiup394@gmail.com, read-only. Nothing in Gmail was sent, drafted, labelled or changed.

**Notation.** Many of the emails contain em dashes. This report does not reproduce them: wherever an original email or subject had an em dash, the quote shows **[ED]** instead. Dates and times are IST unless marked UTC.

## 0. Evidence base and method

- **Scope boundary.** I paged through every sent thread dated after 1 Sep 2026 (891 threads). The boundary was taken as 2 Sep 00:00 IST, which is 1 Sep 18:30 UTC. That is the reading the Operating Brief uses: its section 6a counts the Radisson Blu and EPAM sends as in scope, and they left at 01:11 and 03:13 IST on 2 Sep. The 15 threads sent before that point were counted from their timestamps but not opened or summarised.
- **Excluded.** 19 sent threads (4 Sep, 17:08 to 17:30 UTC) belong to Aditya's separate startup-fundraising campaign, which the Brief (section 18) says to keep out of every WAiFF file. They are excluded here too.
- **Analysed:** 857 WAiFF threads, 101 bounce notices, 166 non-bounce inbound messages from 96 senders, and about 50 full message bodies. Those bodies cover every subject pattern and every follow-up wave, plus every thread with a human reply that mattered. Counts come from parsing the Gmail metadata of all 857 threads. Template-level findings come from the sampled bodies. Where a body finding is extrapolated to a whole wave, the report says so.
- **Cross-checks.** WAIFF_India_Outreach_Tracker.xlsx (Gmail Tracker 555 rows, Replies Tracker, Pipeline Summary), WAIFF_OPERATING_BRIEF.md (sections 2 to 4, 6, 7, 8, 10, 16, 18, 20), WAIFF_Channel_Templates.md and WAIFF_Refinement_Log.xlsx.

---

## 1. Numbers

### 1.1 Volume

| Item | Count (recomputed from Gmail) |
|---|---|
| WAiFF threads with at least one sent message, 2 to 23 Sep | **857** |
| First-touch cold emails (new subject, new thread) | **570** |
| Follow-up emails | **379**: 274 sent as brand-new threads with a faked "Re:" subject, plus 105 sent inside the original thread |
| Replies inside live conversations | 41 visible (13 conversation threads plus 28 in-thread replies). Long threads hide some later messages, so the real number is higher |
| **Total WAiFF emails sent** | **about 990 in 22 days** |
| Unique companies pitched (first-touch threads merged by domain and brand) | **about 478** |
| Companies that got 2 or more *separate cold pitches* with different subjects, not follow-ups | **77 companies, 92 extra first-touch threads** |
| Companies that got 3 or more emails in total | 122 (50 got 4 or more; Samsung and YuVerse got 7; PhonePe and hoichoi 6) |

**Sponsor vs organizer split (first touches).** Organizer track ("organize and own", "license and run", "Organizer Opportunity"): **42 threads, 40 companies**. Sponsor track: **528 threads, about 438 companies**. Organizer pitches went out on only four days: 3 Sep (10), 5 Sep (2), 22 Sep (10) and 23 Sep (18), plus two one-offs.

**Per-day volume (IST).**

| Day (IST) | Weekday | First touches | Follow-ups (new thread) | Follow-ups (in thread) | Conversation mail |
|---|---|---|---|---|---|
| 2 Sep | Wed | 17 | | | |
| 3 Sep | Thu | 45 | | | 6 |
| 4 Sep | Fri | 3 | | | |
| 5 Sep | Sat | 60 | | | 1 |
| 6 Sep | Sun | 38 | | | 1 |
| 7 Sep | Mon | 56 | 45 | | 6 |
| 8 to 11 Sep | Tue to Fri | 6 | 1 | 2 | 6 |
| 12 Sep | Sat | 29 | | | |
| **13 Sep** | **Sun** | **100** | **135** | | |
| 14 Sep | Mon | 29 | 40 | | 4 |
| 15 to 16 Sep | | 0 | | | |
| 17 Sep | Thu | 15 | | | |
| 18 Sep | Fri | 8 | | | |
| 19 Sep | Sat | 1 | | 66 | 4 |
| 20 Sep | Sun | 56 | | | |
| 21 Sep | Mon | 0 | | | 12 |
| 22 Sep | Tue | 23 | | 37 | |
| 23 Sep | Wed | 84 | 53 | | 1 |
| **Total** | | **570** | **274** | **105** | **41** |

The volume came in bursts. Sunday 13 Sep alone carried 235 emails, then nothing went out on 15 to 16 Sep or 21 Sep. The Brief's ramp (section 8) was never followed, and the burst pattern is itself a spam signal.

**Send timing.** 227 of 570 first touches (40%) left between 00:00 and 03:59 IST. 284 (50%) went out on a Saturday or Sunday: 194 on Sundays, 90 on Saturdays. The whole 20 Sep batch (56 sends) left between 00:00 and 02:12 IST on a Sunday. The follow-ups were machine-gunned in bursts of a few minutes each:

- 13 Sep: 135 emails between 16:47 and 16:51 IST, on a Sunday.
- 14 Sep: 40 emails between 16:14 and 16:18 IST.
- 19 Sep: 66 emails between 15:59 and 16:09 IST, on a Saturday.
- 23 Sep: 53 emails between 15:57 and 16:15 IST.

### 1.2 Bounces

- **101 bounce notices** (95 hard, 6 delay notices that later failed). They covered **at least 73 unique dead addresses**: 71 parsed, plus press.india@sony.com and one LG address whose notices are truncated.
- **67 WAiFF threads hit at least one hard bounce.** In **45 of them the To: address itself was dead**, so unless a BCC address was alive, the email reached nobody.
- First touches: **51 of 570 (8.9%) bounced at least one address, and 31 (5.4%) lost the primary To.** The Brief's warning line is 3% (section 8).
- **Causes:**
  - "Address not found": 80 notices. The biggest source was guessed or stale personal addresses: grace.gabel@, sabrina.mohan@ and stephanie.yu@lenovo.com; 4 of 8 Adani addresses; pallavi.walia@microsoft.com; five Blackmagic staff addresses in one send; alex.liu@, peter@ and prnews@sensetime.com (all three, so the 23 Sep SenseTime email reached no one); eric.brown@pugetsystems.com; santhosh.a@sunnetwork.in.
  - Blocked by policy: 12 notices. Lyca's info@ accepts allowed senders only; OPPO's vivienne.chen@ is blocked by a mail-flow rule, and was bounced on 20 Sep and again on 23 Sep; Nestle, HP, PNY and ADATA blocked the message.
  - Domains that do not exist: contact@razer-media.com; business@help.envato.com, 3 times.
  - Personal webmail: murat_gebeceli@yahoo.com and shami_aywah@hotmail.com.
- **13 addresses were mailed again after they had already bounced:** grace.gabel@lenovo.com 4 times (3, 7, 14 and 23 Sep); press.india@sony.com 4 times (3, 7, 14 and 23 Sep); tshobhana@primefocustechnologies.com, info@lycaproductions.in and business@help.envato.com 3 times each; Nestle (both addresses), Aputure, Accor (shareena@), Epidemic Sound, yaqi.ren@ddhl.com, mediaalerts@shutterstock.com, Support@gan.ai and vivienne.chen@oppo.com twice each. Nobody pruned the follow-up lists against earlier bounces.
- **Personal-email recipients.** 18 sends carried 35 personal Gmail, Hotmail or Yahoo addresses in To or BCC: 4 on 2 Sep, and 14 in the 17 Sep "Global" blast. The Brief (section 6) forbids this.

### 1.3 Replies by type

Unit: companies. The 166 non-bounce inbound messages come from 81 distinct companies.

| Reply type | Companies | Who |
|---|---|---|
| **Human, positive or engaged** (asked for a call, meeting, details or contact) | **13** | EPAM, Radisson Blu, NVIDIA (Kavita Aroor), Vidu, IA-Meetings, Sennheiser (via its agency 2020msl), YuVerse, ShareChat, Cooke Optics, Filmustage, MCI Group, Wonder Studios, Cascadeur (conditional) |
| **Human, venue or vendor selling to WAiFF** | **7** | The Leela, Trident/Oberoi, Grand Hyatt Mumbai, Yashobhoomi IICC, Novotel Juhu, NESCO/Bombay Exhibition Centre, Getty Images (sold its own paid-assignment service) |
| **Human decline** | **10**, plus 2 recorded only in the tracker | Dell, Ideogram, Anthropic (its PR agency), MiniMax, Moonshot/Kimi, Hedra (the CEO), Vast.ai, ILM, MRF, Acer India. Tracker only: NVIDIA PR policy decline (Shristi Mahnot); Filmustage after the call |
| Automated or AI-agent decline | 3 | AssemblyAI (AI agent, 3 times), InVideo (AI support assistant), Canva (no-reply "focussed on our existing partnerships") |
| Support desk routed, forwarded or redirected | 15 | Nikon, boAt, MG Motor, Speechify (person left), HeyGen, NVIDIA Inception, AMD University Program, hoichoi, OpusClip, Dailyhunt/VerSe, Banca Transilvania, ASUS service care, Tilta tech support, Magnific, RODE |
| Out of office or left the company | 5, plus Dell and Radisson counted above | BenQ, Samsung (2), Michelin, DigitalOcean, Conde Nast |
| Auto-acknowledgement or bot only | 29 | Zoho, Freshworks, Zscaler ("no longer monitored"), Synthesia, BFL, Stability, Panasonic helpline, LG customer care, Perplexity bots, DNEG ("we don't accept applications by email"), Google press, ITC Hotels, Lemon Tree, Qatar Airways (editorial only), Postman, DomoAI, Z.ai, PixVerse and others |
| Bounce only | see 1.2 | |

**Reply rates (denominator about 478 companies):**

- Any non-bounce response: 81, or **16.9%**. That is flattering, because 36% of these (29 of 81) are autoresponders.
- A human-written answer from a prospect (engaged, declined, or venue/vendor): 30, or **6.3%**.
- Engaged: 13, or **2.7%**. **Conversations that reached price or a proposal: 0. Money: 0.**
- **Sponsor track:** engaged 12 of about 438 (2.7%); any human 28 (6.4%).
- **Organizer track:** engaged 1 of 40 (IA-Meetings, 2.5%); decline 1 (MRF); any human 2 of 40 (5.0%). 5 of the 40 organizer companies bounced at least one address (Lyca, Prime Focus, EY, the Mahindra media address, a Sun TV BCC). None of the 22 "WAIFF India [ED] an opportunity to organize and own the India edition" emails got a human reply.
- **Calls actually held from email:** at least 6: Radisson (3 Sep), YuVerse (7 Sep), IA-Meetings (8 Sep), Sennheiser's agency (14 Sep), MCI (21 Sep) and Filmustage (23 Sep). None converted.

**Tracker cross-check.** The Gmail Tracker marks only 30 rows "Bounced = Y" and 28 rows "Reply = Y". Gmail shows at least 67 threads with hard bounces, and 81 responding companies of which 30 are human. The tracker understates bounces by about half and has no way to tell an auto-ack from a human. Its "523 companies emailed" (Refinement Log, 24 Sep) counts rows, including repeats and forms. The recount here is about 478 unique companies, of which 77 were pitched more than once as if new.

---

## 2. Subject-line inventory

All 570 first-touch subjects, grouped into 19 patterns. Median length: 63 characters and 11 words (maximum 98 characters, 17 words). 411 of 570 subjects (72%) contain an em dash; across all 857 threads the figure is 530. 265 contain "Partnership Opportunity", "Sponsorship Opportunity" or "Global Partnership". 194 threads use "WAIFF" in capitals.

| # | Pattern (em dash shown as [ED]) | Sends | Dates | Names the company? | Reads as | Outcome (human replies in bold) |
|---|---|---|---|---|---|---|
| S01 | "Partnership Opportunity with WAIFF India [ED] [Co] x World AI Film Festival" | 25 | 2, 3, 5 Sep | Yes | Formulaic marketing | **EPAM (positive), Radisson (positive, then parked), Sennheiser agency (meeting)**; Zoho, Freshworks and Zscaler bots; Adani x2 and Myntra bounced |
| S02 | "WAIFF India Edition - Partnership Opportunity with [Co]" | 4 | 3 Sep | Yes | Formulaic | NVIDIA Inception redirect ("program for startups") |
| S03 | "WAIFF India x [Co] [ED] AI Cinema Partnership" | 30 | 3 Sep | Yes | Formulaic | **NVIDIA (Kavita, via india-pr), Vidu (Han), Dell decline** (after two follow-ups); Nikon routed; 5 bots; Sony, Lenovo and Mirage bounced |
| O01 | "WAIFF India [ED] an opportunity to organize and own the India edition" | 22 | 3, 5, 22 Sep | **No** | Generic, identical for all 22 | 0 human; DNEG auto x4; Lyca, Prime Focus and Mahindra bounced |
| S04 | "Partnering with WAiFF India [ED] [Co] x World AI Film Festival" | 2 | 4 Sep | Yes | Formulaic | GoPro bounced; Christie silent |
| S05 | "Partnership Opportunity - [Co] x World AI Film Festival" | 48 | 5 Sep (Sat) | Yes | Formulaic | **Exhibitions India (reply), Yashobhoomi (venue sales), Hedra (decline 16 days later), ILM (decline, after the 23 Sep follow-up)**; boAt forwarded; Microsoft bounced |
| S06 | "[Category] Partnership Opportunity [ED] WAIFF India x [Co]", e.g. "AI Compute & Infrastructure Partnership Opportunity" | 10 | 6 Sep (Sun) | Yes | Marketing | **IA-Meetings (meeting), YuVerse (call)**; AMD routed to its University Program; Intel bounced; 2 sends had an empty To (all BCC) |
| S07 | Institutional one-offs, e.g. "WAIFF India Edition, Mumbai (Dec 2026) [ED] exploring Maharashtra Film City as a venue partner" | 4 | 5 Sep | Yes | Official | 0 |
| S08 | Casual: "an AI film festival, [Co]" / "WAiFF x [Co] [ED] India, this December" / "[Co] [ED] a Cannes-born festival lands in Mumbai" / "WAiFF's India launch [ED] [Co] fit?" | 28 (about 20 companies: CBFC, IndiaAI, PhonePe and hoichoi each got 3 within 16 minutes) | 6 Sep (Sun) | Yes | Most human-sounding and shortest (40 chars) | **Anthropic decline (after the note-less follow-up), Grand Hyatt venue sales x2**; hoichoi redirect x3 |
| S09 | Hook-led: "[their initiative] and an AI/international film festival landing in Mumbai", e.g. "Hawa Badlegi, Anurag Kashyap, and an AI film festival in Mumbai" | 56 | 7 Sep (Mon, 01:00 IST) | Yes, and names their campaign | Best-crafted subjects of the campaign | **Trident (venue), NESCO (venue)**; MG Motor routed; 3 bots; Nestle blocked |
| S10 | "[Partnership/Sponsorship] Opportunity [ED] [Co] x World AI Film Festival (India Edition, Mumbai)" | 70 | 12 to 13 Sep (Sat/Sun night) | Yes | Longest (84 chars), formulaic | **Cooke Optics (positive), Novotel (venue)**; Canva auto-decline; 5 bots; 5 bounces |
| S11 | "Partnership Opportunity [ED] [Co] x World AI Film Festival" (incl. "extending your existing partnership" to TF1, Fnac, MiniMax) | 34 | 13 Sep (Sun) | Yes | Formulaic | **MiniMax decline (existing partner, on the do-not-contact list)**; InVideo AI decline; Kingston bounced |
| S12 | "[Co] x World AI Film Festival [ED] India 2026" | 67 | 13, 14, 22 Sep | Yes | Shortish (51), neutral | **ShareChat (positive), Cascadeur (conditional), Wonder Studios (positive after the 19 Sep follow-up), Ideogram (decline), Vast.ai (decline)**; Speechify, HeyGen and Dailyhunt routed. The best-performing pattern, even though the body had a merge bug (section 3) |
| S13 | "[Co] x World AI Film Festival [ED] A Global Partnership Opportunity for the AI Creation Era" | 22 | 17 to 18 Sep | Yes | Longest (88), hype | **Acer India decline**; ASUS service care; Dell and Samsung OOO; 5 Blackmagic and 3 personal-address bounces |
| S14 | "[Co] x World AI Film Festival [ED] A Partnership Opportunity in AI Filmmaking" | 57 | 20 Sep (Sun, 00:00 to 02:12 IST) | Yes | Formulaic | **Filmustage (positive, then a call), Kimi (decline)**; OPPO, PNY and ADATA blocked; Kuku, Cartesia and Collective Artists bounced |
| S15 | Bespoke one-to-one, e.g. "WAIFF x Getty Images \| Strategic Global Creative Partnership", "WAIFF x hoichoi / SVF [ED] Strategic Partnership: India Edition (Dec 15) & Cannes 2027" | 7 | 8 to 18 Sep | Yes | Corporate. The SVF subject leaks the internal date | **Getty (vendor upsell)**; SVF and Turing silent |
| S16 | Festival-sponsor angle: "[Co] x WAiFF [ED] [their festival sponsorship]", e.g. "Rolex x WAiFF [ED] Rolex and Cinema, one chapter further" | 30 | 23 Sep, all at 02:0x IST | Yes | Clever, but copy-heavy | 0 human; Pinterest auto; Cartier BCC bounced |
| S17 | Apollo wave: "[Co]'s [hook], extended to Cannes / on a global stage / in front of the filmmakers..." | 36 | 23 Sep (21:00 to 22:00 IST) | Yes | Short (49), natural | 0 human after about 1 day; DigitalOcean OOO; SenseTime all bounced |
| O02 | "[Co] [ED] license and run the WAiFF India edition" | 18 | 23 Sep | Yes | Blunt, transactional | **MRF decline** ("doesn't fit into our plans"); Conde Nast OOO; EY bounced |

**Follow-up subject patterns.**

- FU7: "Re: [Co] x WAiFF India, December 2026" (45).
- FU13: "Re: [original subject]" (135).
- FU14: "Re: WAIFF India [ED] an opportunity..." and "Re: WAIFF India x [Co] [ED] AI Cinema Partnership" (40).
- FU23: "Re: [original subject]" (54).

**84 of the 287 "Re:" threads carry a subject that never appeared in any earlier email to that company.** For example, the 7 Sep follow-ups were titled "Re: Netweb Technologies x WAiFF India, December 2026", but the 3 Sep original was "WAIFF India x Netweb Technologies [ED] AI Cinema Partnership". A "Re:" on a subject the reader never received is a classic spam and deception tell.

**What the subject data says.**

1. The only subject style with several human replies was the plain "[Co] x World AI Film Festival [ED] India 2026" (S12: 5 human replies from 67 sends, 7.5%). The hook-led S09 subjects were the most personal, but their replies were only hotel and venue sales desks. That is a targeting problem, not a subject problem.
2. "Partnership Opportunity" and "Global Partnership Opportunity for the AI Creation Era" read as vendor spam, and press or support desks triage them that way. Synthesia: "If you're a journalist or have an editorial inquiry..." Qatar Airways: "we only respond to editorial requests".
3. The organizer subject O01 did not name the company, and got 0 human replies from 22 sends.
4. 72% of subjects carry an em dash. That is against Brief section 7, and it is the signature of machine-generated copy.

---

## 3. Body analysis: the template versions over time

### 3.1 Version map and metrics

Word counts cover the body up to the sign-off. The grade is the Flesch-Kincaid grade level: 12 or more is college reading level. "Claims" means distinct factual assertions about WAiFF in the body. "Ask at word" is how far into the email the first request appears.

| Version | Dates, sends | Sample | Words | FK grade | WAiFF claims | Ask at word | The ask | Personalisation | Link / sign-off | Recipients / timing |
|---|---|---|---|---|---|---|---|---|---|---|
| **V1** "hope this finds you well" | 2 Sep (S01, 17+) | Tech Mahindra | 435 | 14.0 | about 8 | about 430 (last line) | "walk you through the sponsorship tiers... brief Google Meet this week?" | 2 paragraphs of Wikipedia-style praise ("149,000+ professionals across 90+ countries") | plain URL; "Best regards" | **14 of 17 sent to undisclosed-recipients with everything in BCC**; 8 em dashes; 00:17 to 03:56 IST |
| **V2** "AI Cinema Partnership" and organizer v1 | 3 Sep (S03 30, O01 10) | Nikon / DNEG | 341 / 383 | 13.2 / 11.5 | about 10 | 329 / 371 | "short call this week?" | 1 real fact (Nikon ZR via RED; DNEG's Dune Oscar) | Google-redirect URL | organizer version states EUR 50,000 and EUR 400,000 |
| **V3** short | 5 Sep (S05, 48) | Gan.ai / Hedra | 136 / 158 | 9.4 / 10.7 | 3 | 125 / 146 | "Could we find 15 minutes...?" | Often thin ("Gan.ai's growth in personalized AI video generation is a good example...") | redirect URL | **greeting "Hi," or "Dear Respected Team"; says "India edition to Cannes"** |
| **V4** category-partner bullets | 6 Sep morning (S06, 10) | Yotta | 411 | 13 or more | about 5, plus 6 promised benefits | about 400 | "walk you through the sponsorship tiers... Google Meet" | Brochure praise | plain URL | "hope this email finds you well"; 6 em dashes; 2 sends had an empty To |
| **V5** casual | 6 Sep evening (S08, 28) | Anthropic | 151 | 12.8 | about 7 | 151 | "Worth a 15-minute call this week?" | 1 line of reasoning, no fact | redirect URL | 3 em dashes; **the same pitch re-sent 3 times within 16 minutes to CBFC, IndiaAI, PhonePe and hoichoi** |
| **V6** hook-led | 7 Sep (S09, 56) | Havells / Databricks | 222 / 310 | 10.9 / 9.7 | about 13 | end | "I would like 15 minutes with whoever owns brand marketing" (no question) | **Best in the campaign: a specific campaign and cast** | redirect URL | most sent 01:15 to 01:40 IST on Monday; Databricks variant lists 6 sponsor benefits |
| **V7** "I am writing because" | 12 to 13 Sep (S10, 70) | Mastercard / Jio | 202 / 194 | 12.8 / 13.0 | about 9 | end | "short call, or point me to the right person" | Good for Mastercard (it sponsored the Reply AI Film Festival and BCCI) | "Website:" + redirect | **at least 10 went to investor-relations, company-secretary or legal inboxes and about 15 to customer-care or support desks**; says "Jury President Gong Li" |
| **V8** "Apple Global / measurable return / moving fast" | 13 to 14 Sep (S11 34, S12 54) and 20 Sep (S14 57) | WBD / ShareChat / Kimi / Filmustage | 259 to 299 | 11 to 12 | about 13 | about 280 | "short call this week or next?" | 1 fact, often generic ("Vast.ai just achieved SOC 2") | redirect URL | **merge bug "[Co]'s India edition is launching in Mumbai"** (13 to 14 Sep); unverifiable ROI line; false urgency; the 20 Sep batch left 00:00 to 02:12 IST Sunday |
| **V9** "Global Partnership for the AI Creation Era" | 17 to 18 Sep (S13, 22) | Dell | **1,008** | 11.2 | about 18 | no question at all | "quick Google Meet... Let me know what day works" | Product-catalogue praise | plain URL | **To: Board_of_Directors@, investor_relations@, Media.Relations@ plus 15 BCC incl. 2 Gmail**; Lenovo had 22 addresses visible in To, Gigabyte 17; EUR 450k / EUR 400k |
| **V10** 22 Sep | S12b 13, O01v2 10 | Nintendo / IFP | 256 / 421 | 12.3 / 13.2 | 13 / 17 | end | "short call this week or next?" | Good for IFP (named person, real stats) | redirect URL | IFP states the licence prices |
| **V11** Apollo, "third Cannes edition" | 23 Sep (S16 30, S17 36, O02 18) | Rolex / HONOR / MRF | 330 / 358 / 459 | 13.1 / 14.5 / 13.8 | about 15 | end | "A 15 minute call would tell us fast whether there's a real fit here." (no question) | Good hooks for festival sponsors (Rolex and Cinema, Campari, Chopard) | redirect URL | **"Hi team" to a named person's address** in about 30 sends; 2 to 3 named BCCs per company; 94% used BCC; 02:00 IST (S16) and 21:00 to 22:00 IST (S17) |

Other measurements:

- **Reading level.** 15 of 21 scored first-touch samples are at grade 11 or above (up to 14.5); the rest score 9.4 to 10.9. Average sentence length runs 20 to 30 words.
- **Length.** The Brief's "under 180 words" rule (section 7) was met only by V3, V5 and some follow-ups.
- **Where the ask sits.** In every first-touch version the ask is the last line, after 130 to 1,000 words. That breaks the Brief's section 16 finding: "State your purpose in the first sentence, not the third".

### 3.2 Verbatim openings (first ~120 words of each version)

**V1, 2 Sep, Tech Mahindra** (undisclosed-recipients; 4 BCC: alliances@, socialmedia@, mktg@, media.relations@)
> Dear Team Tech Mahindra, I hope this email finds you well. I've been following Tech Mahindra's journey for a while now [ED] what you've built as a global leader in technology consulting and digital solutions is truly remarkable. With 149,000+ professionals across 90+ countries serving 1,100+ clients, you're enabling enterprises to achieve transformative scale at unparalleled speed. Your full spectrum of services [ED] from consulting, IT, and enterprise applications to AI & analytics, cloud, and network services [ED] positions you as a comprehensive partner for businesses navigating the digital age. What stands out is that you were the first Indian company in the world to be awarded the Sustainable Markets Initiative's Terra Carta Seal... *(continues: "...the world's first and largest international film festival dedicated exclusively to AI-generated cinema... We are now launching the India Edition on 15th December 2026...")*

**V2, 3 Sep, Nikon** (To: NindSupport@nikon.com, a customer-support inbox)
> Dear Nikon Team, The Nikon ZR, your first-ever cinema camera, born directly from Nikon's acquisition of RED Digital Cinema, is a genuinely significant move into filmmaking, and cinema cameras are the tools behind everything WAiFF exists to celebrate. I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF), the world's first and largest film festival built entirely around AI-generated cinema. WAiFF was founded by Marco Landi, former President and COO of Apple, part of the task force that brought Steve Jobs back to the company in 1997, together with the Institut EuropIA and the Alpes-Maritimes Department in France. Our flagship edition is held every year at the Palais des Festivals in Cannes, the same venue as the Cannes Film Festival... *(continues: "...more than 5,500 submissions from 80+ countries... Genario and MiniMax Hailuo are already part of our sponsor network...")*

**V2 organizer, 3 Sep, DNEG** (To: info@dneg.com, which auto-replies "we no longer accept resumes or applications via email")
> Dear DNEG Team, DNEG's Oscar win for Visual Effects on Dune: Part Two at the 2025 Academy Awards is a genuine milestone, an Indian-founded company at the top of the world's VFX craft. I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF), the world's first and largest film festival built entirely around AI-generated cinema... *(4th paragraph: "As organizer, you take full ownership of running the India edition every year, for a licensing fee of EUR 50,000... There's also an upgrade to Global WAiFF Partner status for EUR 400,000...")*

**V3, 5 Sep, Gan.ai** (To: Support@gan.ai, which bounced)
> Hi, Gan.ai's growth in personalized AI video generation is a good example of the kind of Indian AI-video company we want to see more of at WAiFF. I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF). Our Cannes flagship this year drew 6,000+ applications from 100+ countries, with national editions now running in Seoul, Kyoto and Istanbul. **We're bringing an India edition to Cannes in December 2026**, built around AI-driven filmmaking. A large share of WAiFF's submissions and audience come from exactly the kind of AI-assisted creative work Gan.ai builds. A partnership at the India edition puts Gan.ai in front of that community at a formative moment for the category. Could we find 15 minutes for a call this week or next?...

**V4, 6 Sep, Yotta** (third separate pitch to Yotta in 4 days)
> Dear Team Yotta, I hope this email finds you well. I've been following Yotta's journey for a while now [ED] what you've built as a comprehensive suite of cloud, data center, and managed services is truly impressive. Powering digital transformation with scalable cloud, colocation, and managed services, you've established yourself as a critical enabler of India's digital economy. Your state-of-the-art infrastructure, cutting-edge AI capabilities, and commitment to data sovereignty are empowering organizations to innovate securely and efficiently... *(continues: "...I'm inviting Yotta to be our official AI Compute & Infrastructure Partner. As our AI Compute & Infrastructure Partner, Yotta will: Showcase Your AI Infrastructure... Global Visibility... Thought Leadership...")*

**V5, 6 Sep, Anthropic** (To: press@anthropic.com)
> Hi Anthropic team, I'm Aditya Upadhyay, India Ambassador for WAiFF [ED] the AI film festival that started at Cannes and is now landing in Mumbai this December. Reaching out because Anthropic has a direct stake in how generative AI gets portrayed in culture and film. WAiFF's flagship Cannes edition runs under President Gong Li and Honorary President Claude Lelouch, with national editions already running in Seoul, Kyoto, and Istanbul [ED] this isn't a first-year experiment, it's an organization scaling fast across 15+ countries and 30+ cities. We're building the founding sponsor group for the India edition: international press, national press, **Bollywood and international artists**, and a brand-new category getting its own stage [ED] AI filmmaking... Worth a 15-minute call this week?

**V6, 7 Sep, Havells** (To: a named brand manager)
> Hi Amit, Hawa Badlegi stood out for who it put in front of the camera. Having Anurag Kashyap alongside Varun Dhawan and Yuzvendra Chahal is a genuinely filmmaker-literate choice for a consumer electricals brand, and it lines up with Havells saying openly that ad investment is going up, not flat. I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF). WAiFF was founded in 2025 by Marco Landi, the former President and COO of Apple, and its flagship runs in Cannes at the Palais des Festivals. This year's Cannes edition took 6,000+ applications from 100+ countries, put 80 projects into official competition, granted 13 awards, and drew 300+ industry professionals and 5,000+ participants...

**V7, 13 Sep IST, Mastercard** (To: a named person)
> Dear Barkha, I am writing because Mastercard has already done exactly what I would like to discuss. Mastercard was the Premiere Partner of the Reply AI Film Festival, and in India Mastercard took title sponsorship of all BCCI international and domestic home matches. That combination, a global appetite for AI film culture and a proven willingness to anchor major properties in India, is rare. I am Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF)... 5,000+ participants, **under Jury President Gong Li** with Claude Lelouch as Honorary President...

**V7 to an investor-relations desk, 13 Sep IST, Reliance Jio** (To: investor.relations@ril.com)
> Dear Reliance team, I am writing about a partnership and would be grateful if this could be routed to the Jio brand or partnerships team, as this was the published contact I could verify...

**V8, 14 Sep IST, Warner Bros. Discovery** (To: a named person, Diego)
> Hi Diego, I saw Max renew "The Pitt," starring Noah Wyle, for a second season, and Warner Bros. Discovery's crossover between Tom and Jerry and the ITTF World Cup Macao 2026. I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF). WAiFF was founded in 2025 by Marco Landi, the former President and COO of **Apple Global**... Our flagship event is held annually at the Palais des Festivals in Cannes, the same venue as the Cannes Film Festival... **WBD's India edition is launching in Mumbai this December**... Partners see real, measurable return: an estimated media value well above the partnership investment... **This is moving fast, and I'd rather bring this to you directly before it's fully allocated.**

The same merge bug appears in every other V8 email from 13 to 14 Sep that was checked: "ShareChat's India edition", "Vast.ai's India edition", "Ideogram AI's India edition" and "Cascadeur's India edition". It is template-level, so it probably hit most of the 54 S12 emails of 13 to 14 Sep. The 20 Sep S14 variant fixed it to "WAiFF's India edition" but kept the ROI line and the urgency line (Kimi and Filmustage).

**V9, 17 Sep, Dell** (To: Media.Relations@, **Board_of_Directors@dell.com, investor_relations@dell.com**; 15 BCC including arps23@gmail.com and chhabranidhi@gmail.com. Sent 3 days after Dell Media Relations had written "Unfortunately, we won't be able to explore a collaboration at this time.")
> Dear Dell Team, I hope this message finds you well. I am writing to you with genuine admiration for what Dell has built over the decades. From your foundational work in personal computing to your rise as a global leader in workstations, gaming hardware, and enterprise solutions, Dell has consistently stood at the intersection of performance and reliability. The Precision workstations have become the backbone of professionals and creators worldwide. The Alienware brand has become synonymous with elite gaming. The XPS series has redefined what a premium laptop can be... *(later: "The global press is calling this the '1895 Lumiere brothers moment'... Our 2026 edition drew over 6,000 film submissions from 80 countries... Oscar-winner Roger Avary... an estimated media value exceeding 450,000 euros against a 400,000 euro global reference budget... we are planning a dedicated India Edition of the festival as well")*

**V10, 22 Sep, IFP** (organizer, To: a named person)
> Hi Ritam, IFP's Season 16 pulling 64,328 festival attendees and 53,000+ challenge participants from 42 countries is exactly the kind of proven, large-scale creative-festival infrastructure this opportunity needs, and the 50-Hour Filmmaking format shows you already understand how to run a real filmmaker competition, not just a brand event. I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF)... *(4th paragraph: "I am not writing to ask IFP to sponsor an existing event. I am offering the India edition itself... The license fee is 50,000 euros...")*

**V11, 23 Sep, Rolex** (To: lisa.cross@rolex.com, greeted as "Hi team")
> Hi team, Rolex being an official partner of Cannes, Venice and TIFF simultaneously through your Rolex and Cinema program is the strongest example anywhere of a brand treating film festivals as a genuine heritage platform, not a one-off placement. I'm Aditya Upadhyay... Our flagship event runs every year at the Palais des Festivals in Cannes, the same venue as the Cannes Film Festival, and **this April we're building toward our third Cannes edition, on April 6 and 7, 2027**... *(5th paragraph, a sentence with no antecedent: "WAiFF is building the same kind of platform for the next generation of filmmaking, AI-assisted cinema, and would be a natural extension of that program as it looks at where the industry is actually heading.")*

**V11 organizer, 23 Sep, MRF** (To: companysecretary@mrfmail.com)
> Hi team, MRF Racing running the Formula 2000 season year after year, and the MRF Challenge's track record across multiple countries, show decades of real experience organizing and funding large live events at an international level. I'm Aditya Upadhyay... WAiFF was founded in 2025 through the shared vision of Marco Landi... and **Charles Ange Ginesy, President of the Departement des Alpes-Maritimes**... Agnes Jaoui as our **2027** Jury President... *(later: "An organizer licenses WAiFF for India for a one time fee of EUR 50,000... Licensing WAiFF's India edition brings that same organizing capability into a new category... backed by India's largest tyre maker's resources.")*

### 3.3 Flags across the bodies

**A. Factual errors and unverifiable claims.** The Brief (section 2) says "if a claim isn't in this table, don't put it in an email."

| Error | Where | Approximate sends |
|---|---|---|
| Wrong festival name: "World AI **International** Film Festival (WAIFF)" | Perplexity, 3 Sep; Hedra CEO reply, 21 Sep | 2, but to high-value readers |
| "We're bringing an India edition **to Cannes** in December 2026" | V3, 5 Sep | up to 48 |
| Merge bug "**[Company]'s** India edition is launching in Mumbai" | V8, 13 to 14 Sep (5 of 5 checked) | up to 54 |
| Exact internal date "15th December", "Dec 15" | V1 (2 Sep); SVF subject and body; Kimi rebuttal; Cooke reply | about 20 |
| Superseded figures "5,500 submissions from 80+ countries", contested "53 countries" | V1, V2, V4 | about 70 |
| "80 countries" in some emails vs "100+ countries" in others | Dell blast, Kimi and Cooke replies | inconsistent across 30+ |
| "Genario" named as sponsor or award partner (banned in the Brief, 3 Sep) | V2; 19 Sep follow-up (66); Kimi, Cooke and ShareChat replies | about 110 |
| "Apple **Global**"; Landi "**famously orchestrated** the return of Steve Jobs" (the Brief forbids the overstatement) | V8, V9, V11; Cooke reply | about 250 |
| **Charles Ange Ginesy as co-founder** | V9, V11 (S17 and O02), SVF, Cooke | about 80 |
| "**Jury** President Gong Li" (she was Festival President) | V7 | up to 70 |
| "this year's jury includes Agnes Jaoui as President, alongside Roger Avary, Elsa Zylberstein **and Gong Li**" | 23 Sep follow-up | 54 |
| "Agnes Jaoui as our **2027** Jury President" | V11 | 54 |
| "**this April** we're building toward our **third** Cannes edition, on April 6 and 7, 2027". Aditya's own ShareChat reply says the 2025 edition ran in **Nice** | V11 | 84 |
| Editions that are not in the Brief's verified list, called "running" or "confirmed": Japan, China, Argentina, UK (V1 and V4); Brazil and Los Angeles (V2); Berlin (V11); Moscow and Berlin (Hedra reply); Beijing and Tokyo (Kimi and Cooke replies) | several | about 120 |
| Unverifiable hype: "world's first and largest" (V1, V2, V4, V7), "1895 Lumiere brothers moment" (V9, SVF), "the undisputed Mecca of cinema" (V9), "Bollywood and international artists" (V5) | several | about 120 |
| **Unverifiable ROI**: "Partners see real, measurable return: an estimated media value well above the partnership investment" | V8 (S12 13 to 14 Sep, S14 20 Sep) | about 110 |
| "We are in conversation with companies such as **NVIDIA** and Sennheiser". NVIDIA's PR had declined sponsorship; this also names one prospect to another | 19 Sep follow-up | 66 |
| "same venue as the Cannes Film Festival" (invites exactly the confusion the Brief warns about) | V2, V8, V10, V11 | about 235 |

**B. Prices in sponsor mail** (the Brief bans this).

- "estimated media value above 450,000 euros against a 400,000 euro budget": 19 Sep follow-up (66), V9 (22), SVF.
- Organizer prices (EUR 50,000 and EUR 400,000) are allowed and appear in O01, O02, V10 and the 23 Sep organizer follow-up.

**C. Decks and links** (the Brief: "never send the Canva link or any presentation file... no exceptions").

- A Canva link to Radisson (3 Sep, straight after the call).
- A Google Drive link plus a PDF "WAIFF_2027_Sponsor_Deck-1.pdf" to ShareChat (14 Sep).
- "WAIFF_Partnership_Proposal_2027-1.pdf" to the Hedra CEO (21 Sep).
- A deck to MCI (21 Sep).

**D. Broken link formatting.** **25 of 28 sampled bodies** show the website as a Google redirect wrapper, not a clean link: `https://www.google.com/url?q=https://worldaifilmfestival.com/&source=gmail&ust=...&sa=E`. The copy was pasted out of rendered Gmail. Redirect wrappers are a phishing and spam signal, and every recipient sees an ugly link. The 4 Sep Character.AI email even carries a mangled inline link: "The (https://www.google.com/url?q=http://c.ai&...) series".

**E. Em dashes.**

- Bodies: V1, V4 and V5 (for example, 8 in Tech Mahindra and 6 in Yotta).
- The 13 Sep follow-up, sent 135 times: "Following up on the note below [ED] did you get a chance to take a look?"
- 72% of first-touch subjects.

**F. Mixed asks.**

- V1, V4 and V2 sponsor versions: "walk you through the sponsorship tiers" (a tier menu before any interest).
- The Reliance/Jio email offers "several conversations here rather than one" (AI stack, JioStar content and a venue at once).
- The 19 Sep follow-up: "Each national edition is run by a local organizer who licenses the WAiFF name... Warner Bros. Discovery can come in for Cannes and the global network, for India, or both". Sponsor, organizer and global partner all in one sponsor email.
- V9 buries India: "I should also mention that we are planning a dedicated India Edition."

**G. Walls of text.**

- 19 Sep follow-up: 686 words.
- Dell blast: 1,008 words.
- Replies to warm leads: ShareChat about 1,100 words with ALL-CAPS headings; Cooke about 1,100; Kimi about 1,500; Hedra 1,180 and then 1,022.

**H. Sign-offs.** Inconsistent.

- "Aditya Upadhyay, India Ambassador, World AI Film Festival (WAiFF)" in most emails.
- From 17 Sep: "Aditya Vardhan Upadhyay, Ambassador, World AI Film Festival, +91 7689906665".
- SVF: "Founder & CEO, Quantum Leap AI".
- Calendar invites went out from a second address (adiup398@gmail.com, to the Sennheiser agency, 10 Sep).
- All mail comes from a personal gmail.com account. There is no WAiFF domain.

**I. BCC and CC.**

- 208 of 570 first touches used BCC: 587 BCC addresses in total, up to 20 on one email.
- 24 went to "undisclosed-recipients" with everything in BCC, and 2 had an empty To. **6 of these went out on 17 to 18 Sep, two weeks after the Brief banned the practice on 3 Sep.**
- 16 had several visible To addresses (Lenovo 22, Gigabyte 17, Razer 7, Acer 6).
- CC appeared only in conversation threads (9).
- V11 in particular BCC'd 2 to 3 named executives per company, sourced from Apollo lists, while greeting the To as "Hi team".

**J. Duplicate and re-pitch sends.**

- CBFC, IndiaAI Mission, PhonePe and hoichoi each got the same pitch 3 times within 16 minutes on 6 Sep.
- The 23 Sep Apollo wave re-pitched **at least 26 companies** that had already been pitched on 19 to 22 Sep, under new subjects, as if first contact. Examples: VOSS (same person, rachel.chambers@, on 20 and 23 Sep), Oakley (claire.barry@, both dates), Itau (imprensa@, both dates), DigitalOcean (sponsorship@, both), UiPath (pr@, on 22 and 23 Sep), SideFX (media@, on 22 and 23 Sep), and Times Group (22 and 23 Sep).

---

## 4. Follow-ups

**Coverage.**

- 249 of about 478 companies (52%) received at least one real follow-up.
- Of the 334 companies first contacted by 14 Sep (10 or more days ago), **86 (26%) never got a follow-up**.
- 193 companies received exactly one email in total.
- Gap from first touch to first follow-up: median 6 days, range 3 to 20. The Brief's cadence (section 10) is Day 4, Day 11, Day 25. In practice the timing was irregular.

**The waves, verbatim:**

| Wave | Sends | Format | Gap | What it said | New value? |
|---|---|---|---|---|---|
| FU7, 7 Sep | 45 | **New thread with a "Re:" subject that differs from the original** | 4 days | "Following up on my note from 3 September about the World AI Film Festival and its India edition. Since I wrote, let me add the part most people ask about first. WAiFF's existing sponsors are CapCut (ByteDance), MiniMax, JW Marriott Cannes, LOTTE, Morphic and Skolae... What a partnership includes is already defined... A dedicated prize delivered on stage at the closing ceremony. A video screened at the opening..." (230 words) | Yes (sponsor roster and benefits), but long, and it discloses the benefit menu the Brief says to keep for calls |
| FU13, 13 Sep (Sunday) | 135 | **New thread, "Re:" subject, nothing quoted below** | 6 to 8 days | "Following up on the note below [ED] did you get a chance to take a look? Would love to find 15 minutes for a call this week or next. I'm on Indian Standard Time but can work around your hours." (40 words) | **None. A pure bump that points to a note the reader cannot see.** Anthropic's reply quotes back exactly this and nothing else, which proves the "note below" never arrived |
| FU14, 14 Sep | 40 | New thread, "Re:" | about 11 days | "One update since I last wrote. Our 2027 flagship is now fixed for 6 and 7 April 2027 at the Palais des Festivals in Cannes... Each national edition is run by a local organizing partner... Worth fifteen minutes to walk through what organizing the India edition would involve for Qube?" (163 words) | **Yes. The best follow-up of the campaign** (one new fact, one clear ask) |
| FU19, 19 Sep (Saturday) | 66 | In thread | 6 to 7 days | "Hi team, I wrote to you last week about [Co] and the World AI Film Festival, and I wanted to follow up properly, with more detail than a first note allows..." then 9 paragraphs, **EUR 450k / EUR 400k**, "We are in the early stages of planning a WAiFF India edition in Mumbai", "in conversation with companies such as NVIDIA and Sennheiser" (686 words) | Adds detail, but it is a wall of text with a price. It opens "Hi team" even to named people (for example Diego at WBD, after the first email said "Hi Diego"). Produced **Wonder Studios (positive)** and **Vast.ai ("Not interested, thanks.")** |
| FU22a, 22 Sep | 22 | In thread | 9 to 17 days | "Quick update since I last wrote. Two more WAiFF editions just got confirmed for October 2026, in Buenos Aires and Montreal/Vancouver... Still keen to find 15 minutes for a call..." (80 words) | Yes, one new fact. Good length |
| FU22b, 22 Sep | 15 | In thread | 10 days | "Hi Priya, Following up on the note below, in case it got buried. Would love 15 minutes this week or next if there's interest." (36 words) | None. A bump, but at least the note is really below this time |
| FU23, 23 Sep | 53 | **New thread, "Re:", nothing quoted below** | 10 to 20 days | "Hi team, Following up on my note below about a partnership between [Co] and the World AI Film Festival (WAiFF). Quick update since I last wrote: our Cannes flagship is now locked for April 6-7, 2027 at the Palais des Festivals, and this year's jury includes Agnes Jaoui as President, alongside Roger Avary, Elsa Zylberstein and Gong Li. Happy to jump on a short call, or if there's a better contact on your side for partnerships, just point me their way." (81 words; the organizer version adds EUR 50k / EUR 400k) | One fact, stated wrongly (Gong Li is not jury). The good "better contact" ask arrives too late. Produced the **ILM decline** 4 hours later |

**Follow-ups that hurt:**

- **274 follow-ups (72%) went out as new threads with a fake "Re:"**, so there is no quoted context. 135 of them say "the note below" when there is none.
- **Dead addresses were re-mailed** in every wave: Lenovo and Sony 4 times each.
- **Warm or closed leads got generic mass follow-ups.** NVIDIA's india-pr@ got the 23 Sep "Hi team" bump while Kavita Aroor's review was pending in a separate thread. Canva was followed up on 19 Sep after it had already declined on 12 Sep (a second auto-decline came back). Dell was blasted at board level on 17 Sep after declining on 14 Sep.
- **The one proven follow-up line was never used as a standalone touch.** Brief section 10 calls the Day-25 "If the timing's wrong, is there someone else I should speak to?" the best-performing follow-up. The closest is the tail of FU23.

---

## 5. Every human reply: what triggered it, how Aditya answered, how fast

Times are IST. "Lag" is the time from their message to Aditya's first substantive answer.

### 5.1 Engaged or positive (13 companies)

| # | Who | Their words (verbatim) | Triggered by | Aditya's response and lag | Outcome to date |
|---|---|---|---|---|---|
| 1 | **EPAM**, Nandini Bhatnagar, Sr Director Marketing (2 Sep 14:49) | "Lets speak next week after 9th.. My colleague Sameena will help set something up." | V1, 2 Sep 03:13, all BCC (5 addresses, 2 of them personal Gmail) | 3 Sep 11:13 (**20 h**): "Thank you, after the 9th works well. I'm free anytime after 12:00 PM IST..."; chased 11 Sep | No slot proposed, no invite sent. Cold since 2 Sep |
| 2 | **Radisson Blu**, Anuj Kumar, Marketing Manager South Asia (3 Sep) | "Sure, lets connect now sending an invite" | V1, 2 Sep | Call held 3 Sep. **39 minutes after the invite, Aditya sent only a Canva deck link.** A long update followed on 7 Sep ("sorry for taking a little time to get back to you"), **4 days** later | Anuj, 14 Sep: "Thanks for the detailed update... **We understand a lot is still being finalised on your end, so we'll...**" Parked |
| 3 | **NVIDIA**, Kavita Aroor, Head Enterprise & Developer Marketing South Asia (3 Sep 18:40) | "Thanks, Aditya. Great initiative. Can you share the Top highlights from 2025 and publicly available data points thr this conference. We will review this internally and revert in a couple of weeks." | V2, 3 Sep, to india-pr@. Shristi Mahnot declined sponsorship as policy and introduced Kavita | 4 Sep 00:01 (**5 h**), a fact sheet (good); chase 19 Sep. **Then on 23 Sep a generic "Hi team, Following up on my note below..." bump went to india-pr@** | No reply for 21 days |
| 4 | **Vidu**, Han, Head of Operations (8 Sep 15:12) | "India is a market we're very interested in, and I'd love to learn more about how you envision working..." | V2, 3 Sep, to support@vidu.com (support forwarded it) | **56 min**, a very long reply (28 KB), then 10 Sep: "I am not just looking for sponsors; I have developed specific plans created entirely for Vidu", then 19 Sep. **Vidu's support inbox was also re-pitched cold on 13 Sep** ("Vidu AI (Shengshu Technology) x World AI Film Festival [ED] India 2026") | Silent since 8 Sep |
| 5 | **IA-Meetings**, Sony Sankaran and Pooja Menon (7 Sep) | "Yes tomorrow works! 3 to 5 pm." / "3pm works for us. please send a meeting link" | S06, 6 Sep | Same day: "Sent you a invite do accept". Meeting 8 Sep. **Then on 13 Sep a note-less bump ("Following up on the note below [ED] did you get a chance to take a look?") went to sales@ia-meetings.com, with 3 BCC** | No further reply |
| 6 | **Sennheiser**, via its agency 2020msl, Muskan Rahaman (10 Sep) | "Thank you. Can you also share the invite with the following id's as well? nivedita.tiwari@2020msl.com arpita.luthra@..." | S01 Sennheiser send (2 to 3 Sep, 21 BCC across the client and its agencies) | Same day: "I have sent a meeting invitation from my email address, **adiup398@gmail.com**" / "Done please send them to accept". Call 14 Sep; recap the same day; chase 19 Sep | Silent since 14 Sep |
| 7 | **YuVerse**, Ajay (call 7 Sep), then Siya Bhatia (21 Sep 15:45) | Siya: "Thank you for reaching out and for sharing the details... The opportunity sounds interesting..." then "**Please share the details once here. Once we go through the details, post that we can connect.**" | S06, 6 Sep, plus the 13 Sep note-less bump to Ajay | **2 min**: "Why dont we connect over google meet have certain things to share..." (ignoring her ask), then a 35 KB email 1 h later; then a 23 Sep bump to connect@ | Silent |
| 8 | **ShareChat**, Soumitra Maity, Head of PR & Communications (14 Sep 10:29) | "Could you pls share your contact details to discuss this in detail?" | **V8 with the merge bug** ("ShareChat's India edition is launching in Mumbai"), 14 Sep 03:10 | **4 min**: "This is my number. +917689906665". Then 2 h 17 min: an ~1,100-word wall with ALL-CAPS headings. Then 11 min: "Here are the material please go through it also the details regarding india edition is as of now being finalized so cannot give numbers regarding our india edition..." plus a Drive link and a PDF deck | Silent for 10 days. No call was scheduled |
| 9 | **Cooke Optics**, Peter Dorai, Director of Sales IMEA (15 Sep 13:46) | "I would like to understand more about the event and **what do you refer exactly as a Collaboration**. Kindly elaborate and we will discuss and get back to you on the same." | V7, 13 Sep, to sales@cookeoptics.com | **3 days 10.6 h**: ~1,100 words. Leaks "The India Edition on December 15th"; says "80 countries"; lists Berlin and Beijing; ends "the answer to anything not on this list is yes". He had given his mobile number; there is no sign Aditya called | Silent |
| 10 | **Filmustage**, Ivan (21 Sep 13:23) | "Hi Aditya! Many thanks for reaching out! Let's set up a call this week to discuss possible cooperation options." | V8/S14, 20 Sep 02:03 (Sunday), to support@ | **56 min**: "Yes, let's discuss." Then "Lets do it on tue or wed this week i am available during 3-6 pm indian standard time." Ivan sent the invite; call on 23 Sep; a 46 KB recap afterwards | Declined after the call (per the tracker; Aditya confirmed 24 Sep) |
| 11 | **MCI Group**, Prachi Chhabra (21 Sep 13:24) | A Teams invite: "MCI group partnership with India Edition of the World AI Film Festival" | Not traceable to an email in this inbox (probably LinkedIn or a call) | "I will attend the meeting." Then a 94 KB email and the sponsor deck PDF | Unknown |
| 12 | **Wonder Studios**, Louis (21 Sep 17:27) | "We're keen to learn more about how Wonder Studios might engage. **As a startup we're still careful with capacity**, so any collaboration would need to stay relatively light on our side for now... Could you share a few times that work for you this week for a short call?" | V8, 14 Sep, then the 686-word 19 Sep follow-up | **2 h 12 min**: "**Well tuesday , thursday , friday works for me but timings will be between 3 to 6 pm ist.**" No dates, no invite, no time-zone help | Silent |
| 13 | **Cascadeur**, Tom Borovskis, Business Development (14 Sep 19:28) | "Before arranging a call, could you please send me the current partnership deck for the Mumbai edition, including the available sponsorship options and their price range? It would also be helpful to know the confirmed date and what is included in each partnership level. **To be transparent, our budget for financial event sponsorships is limited.** We are generally more open to product-based cooperation, for example providing Cascadeur licenses as awards..." | **V8 with the merge bug** ("Cascadeur's India edition is launching in Mumbai") | **No reply in 10 days** | Lost |

Also: Exhibitions India Group (Tariq) replied to the 5 Sep email. His message could not be located; Aditya answered on 7 Sep with "Happy to work around your calendar. I am available at 8 PM IST today, or tomorrow...", and nothing followed. The tracker also records Balaji Telefilms, Laqshya Live and "Hayat" as replies or meetings "reported by Aditya", with no matching Gmail thread.

### 5.2 Venue and vendor desks (7): human, but they were selling to WAiFF

| Who | Their words | Trigger | Aditya's handling |
|---|---|---|---|
| Trident BKC (Puja Singh, Madhura Sarkar, Tarun Mediratta), 7 to 11 Sep | Madhura: "We would be happy to connect with you at 12pm tomorrow (IST)... please share with us the virtual link." Puja: "we regret to inform you that the biggest ballroom at the..." Tarun, 11 Sep: "**We tried reaching out to you, however your phone is unreachable.**" | S09, 7 Sep 01:20 | 8 Sep: "Sorry tarun just saw your mail why dont you call me directly +917689906665". **No answer to the 11 Sep "phone unreachable" email** |
| Grand Hyatt Mumbai (Rupal Mathur, 7 Sep; Stephanie Gururani, Director of Sales & Marketing, 14 Sep) | Rupal: "Kindly share your direct contact number and a suitable time to connect". Stephanie: "Please share a number where we can reach out." | S08, 6 Sep, then the 13 Sep bump | To Rupal, 12 min: "This is my number. +917689906665 do send me a message over whatsapp **as i get hundreds of calls** we can connect around 5 p..." **Stephanie never got an answer** |
| Yashobhoomi IICC (Prabhjot Bedi), 7, 8 and 14 Sep | "Kindly let us know a convenient time for a call this week" | S05, 5 Sep | Dropped (a Delhi venue) |
| Novotel Juhu (Saahil), 18 Sep | "Thank you for considering Novotel Mumbai Juhu Beach as the preferred destination for the event. To better..." | S10, 13 Sep | Not answered |
| NESCO / Bombay Exhibition Centre (Harsh Mukherjee), 22 Sep | "Will appreciate to connect with you over a call." | S09, 7 Sep, then the 13 Sep bump | Not answered |
| Getty Images (Josh Norton), 11 Sep | "...regarding **photo and video coverage opportunities for your events**... Getty Assignments..." (Getty pitched its paid service) | Bespoke email to Juliette Cuijpers, 10 Sep | Not answered |
| The Leela (Aparna Singh), 3 to 4 Sep | A venue quote for "your upcoming event on 15th December 2026" | Aditya's own venue request, not a sponsor pitch | Decision left to Aditya; the quote expired |

The Refinement Log's 24 Sep line is confirmed: "Venues replied only to sell rooms." **Every hotel or venue pitched as a sponsor that answered with a person answered as a seller.**

### 5.3 Declines (verbatim) and reasons

| Company | Reply | Reason class | Trigger | What Aditya did |
|---|---|---|---|---|
| Dell, Media Relations (14 Sep) | "Thank you for your interest in Dell Technologies to be part of your festival. Unfortunately, we won't be able to explore a collaboration at this time." | Not now | V2, then FU7 and FU14 | **3 days later, the 1,008-word V9 blast to Board_of_Directors@, investor_relations@, Media.Relations@, 15 BCC, and a second copy to another Dell employee** |
| Ideogram, Customer Success (14 Sep) | "We don't currently have a dedicated marketing resource in place to properly explore something like this right now, so we'll have to pass at this time." | No resources | V8 with the merge bug | None |
| Anthropic, external comms agency (14 Sep) | "the Anthropic team is currently heads down and focused on competing priorities, and we're not able to accommodate additional media or event opportunities at this time." | No capacity | V5, then the note-less bump | None |
| MiniMax (14 Sep) | "We appreciate the opportunity, but we're not in a position to pursue extending..." | Already a partner (**on the do-not-contact list**) | S11, "extending your existing partnership" | None |
| Moonshot / Kimi BD (20 Sep) | "we do not think it is the right fit for us at this stage: Kimi's models are currently focused on language and reasoning capabilities, and we do not offer video-generation (AIGC) capabilities today... If our roadmap expands into video generation in the future, WAiFF would be a natural partner to revisit." | Product fit | V8/S14 | **A ~1,500-word rebuttal the next day**: "I want to respectfully push back on one point... You are invited. You are needed." It also leaked "15 December", said "80 countries", named "Genario" and "Berlin, Beijing", and was signed "Aditya Vardhan Upadhyay" |
| Hedra, Michael Lingelbach, Founder/CEO (21 Sep) | "We haven't focused on AI 'characters' or avatars in over a year, we're focusing on our inference business. Given that, I don't see a fit here." | Product fit (the hook was more than a year out of date) | V3, 5 Sep | 1,180 words plus a PDF. CEO: "**There was a significant amount of AI used in this response to the point where I found it difficult to read.**" A spat followed (section 8, W2). CEO: "normally when people send a proposal asking me to potentially spend 10s of thousands of dollars, it's usually a hand written note. I never respond with AI written emails fyi." |
| Vast.ai, Head of Growth (21 Sep) | "Not interested, thanks." | None given | V8 with the merge bug, then the 686-word follow-up | None |
| ILM, Ian Kintzle, Sr Manager Publicity (23 Sep) | "Given the AI angle of the festival, this is not something we'd be interested in." | Brand risk / AI stance | V3, 5 Sep, the 13 Sep bump, the 23 Sep bump | None |
| MRF, Pratip Francis (24 Sep) | "Hi, thanks but doesn't fit into our plans." | Wrong target for an organizer pitch | O02, to companysecretary@ | None |
| Acer India, via its outsourced desk Startek (17 Sep) | "Thank you for your interest in partnering with Acer. Regrettably, we have already established partnerships..." | Already committed | V9 blast | None |
| AssemblyAI, an AI support agent (5 Sep) | "we don't have a partnership or sponsorship program that evaluates festival collaborations, and this isn't a request we forward to leadership." | Channel does not exist | 3 Sep send | Aditya: "**Just Send it to leadership they will evaluate it**", then "**Just relax let them see it review it and reply**". Bot: "We've already declined this, and repeating the request won't change the outcome." |
| Canva (auto, 12 and 19 Sep) | "We are currently focussed on our existing partnerships, and not exploring new partnerships..." | Already committed | S10, then a follow-up *after* the decline | |

**Why they declined:**

- **Wrong fit**, 4: Hedra, Kimi, ILM ("AI angle"), MRF.
- **No budget, capacity or people**, 4: Ideogram, Anthropic, Cascadeur (wants a product swap), Wonder (keep it "light").
- **Already committed**, 3: Canva, Acer, MiniMax (already a WAiFF partner).
- **Wrong channel or program**, 8 desks: AssemblyAI, NVIDIA Inception ("a program for startups... please reach out to info@nvidia.com"), AMD ("beyond the scope of AMD University Program"), OpusClip ("We recommend joining our Affiliate Program"), Zoho (reseller partner program), Perplexity (publisher program), Qatar Airways (editorial requests only), DNEG (job applications).
- **Not interested, no reason**, 2: Vast.ai, Dell.
- **Too early or unconcrete**, 1: Radisson ("a lot is still being finalised on your end").

Nobody said "send the deck" as a reason to decline. The two prospects who asked for material (Cascadeur and NVIDIA) wanted **price range, what's included, the confirmed date, and proof**. The campaign rules withheld exactly those.

### 5.4 What the engaged replies had in common

1. **The company's own product touches filmmaking or creators, or its business is events.** That covers 10 of 13: Vidu, Filmustage, Cascadeur, Wonder, Cooke, YuVerse, ShareChat, IA-Meetings, MCI and Sennheiser. The other 3 were India marketing heads replying to an India pitch (EPAM, Radisson, NVIDIA India). **The 88 luxury, finance and global-brand emails of 17 to 23 Sep (S13, S16, S17) produced zero engaged replies.**
2. **The hook was specific and current.** Examples: Nikon ZR via RED; Filmustage's script breakdown; "325 million+ monthly active users" for ShareChat; Cascadeur's keyframe animation. Replies with a generic or stale hook came back as declines (Hedra's 2025 Series A about avatars; Gan.ai's "growth in personalized AI video" bounced).
3. **They answered fast, within about 7 to 49 hours of the email that triggered them.** Speed on Aditya's side decided nothing. He answered ShareChat in 4 minutes and still lost it, because the answer was a phone number followed by a wall of text.
4. **Every engaged reply asked for something concrete:** a date, a price range, what's included, proof, a definition of "collaboration", or a phone number. Aditya answered with either a one-liner ("This is my number", "Well tuesday , thursday , friday works for me") or a 1,000-plus-word essay, often days later. **He sent a calendar invite himself in only 2 of 13 cases (IA-Meetings, and Sennheiser's agency from a different Gmail account). None of the 13 received a one-page, priced, dated proposal.**

---

## 6. Targeting problems visible in the mail

**Recipient inbox type for the 570 first touches (To field):**

| Inbox type | Count | Share |
|---|---|---|
| Named individual | about 205 | 36% |
| Press / PR / comms / marketing shared inbox | about 166 | 29% |
| Generic info@, contact@, support@, sales@, reservations@, help@, care@ | about 129 | 23% |
| **Partnerships / sponsorship / BD inbox** | **26** | **4.6%** |
| No To (BCC only) | 26 | 5% |
| Investor relations / company secretary / legal / board | 16 first touches, plus 3 multi-address blasts with IR or board in To | 3% |
| Careers / campus | 2 (e.g. campuspromotion@asml.com) | |

**The autoresponders show where the mail landed:**

- **Customer service:** Panasonic ("Dear Customer, Thank you for Submitting your request"); LG ("sorry to hear that you have been experiencing issue with your LG Product"); ASUS ("Thank you for contacting ASUS Service Care"); BenQ ("Case Creation Notice"); boAt ("Dear boAthead... click the chat link"); Tilta (a "Technical Support" ticket closed "after 14 days of inactivity").
- **Hotel reservations:** Lemon Tree ("Dear Guest"); ITC Hotels ("Guest Contact Centre. Please advise the hotel name"); Trident ("considering a stay with us").
- **Press desks:** Synthesia ("If you're a journalist or have an editorial inquiry"); Qatar Airways ("we only respond to editorial requests"); Google press ("If you are not a member of the press...").
- **Wrong programs:** AMD, logged as "AUP Donation Request"; Zoho ("exploring Zoho's range of products"); DNEG ("we no longer accept resumes").

**Investor relations, company secretary or legal inboxes used as the To:**

- investor.relations@ril.com, investor.service@bajajfinserv.in, ir@paytm.com (twice), ir@yatra.com, investor-help@vipbags.com, investor@nerolac.com.
- corp.secretarial@groww.in, nykaacompanysecretary@nykaa.com, co.sec@saregama.com, companysecretary@mrfmail.com, cs@torrentpower.com.
- legal@bajajelectricals.com, IR@corsair.com.
- Board_of_Directors@dell.com and investor_relations@dell.com; ircontactus@samsung.com; Investor@asus.com, stakeholder@asus.com and ACIN_CEO_feedback@asus.com.

**Too small to pay USD 100k to 450k (and they said so):**

- Wonder Studios: "As a startup we're still careful with capacity".
- Cascadeur: "our budget for financial event sponsorships is limited".
- Ideogram: "don't currently have a dedicated marketing resource".
- Dozens more early-stage tools were pitched: Krikey, DomoAI, Fliki, Pictory, Rokoko, Move AI, Scenario, Genmo, Artflow, Gan.ai, NeuralGarage, Renderforest, Vidnoz, Simplified, Cuebric, Kaiber, Quantmpic, Laowa, Ulanzi and others.

**Bodies with no sponsorship budget by design (about 20 sends).** CBFC (3 times in 16 minutes), the Ministry of Information & Broadcasting, the IndiaAI Mission (3), Maharashtra Tourism (2), Maharashtra Film City, NFDC's co-production desk, the FTII registrar, SRFTI, Startup India, CII, FICCI (2), T-Hub and IICC.

**Mismatched pitches:**

- **About 20 semiconductor and enterprise B2B firms with no creator or consumer audience:** ASML, TSMC, Arm, Texas Instruments, Analog Devices, Cadence, Renesas, GlobalFoundries, STMicro, SK Hynix, Micron, Graphcore, Cerebras, NXP, Synopsys, Zscaler, Genpact, Tredence and HPE.
- **VFX houses that are publicly wary of AI:** ILM ("Given the AI angle of the festival..."), Weta, Framestore, MPC, DNEG and Digital Domain.
- **The organizer licence (EUR 50,000 to run a film festival) offered to industrial groups through company-secretary or PR inboxes:** MRF, Tata Steel, Torrent Power, JK Tyre, Mahindra, EY India's media desk (bounced), Sula, Delta Corp, GMR and RPSG. MRF: "doesn't fit into our plans".
- **Hotels and venues pitched as sponsors:** 7 replied, all as sellers.
- **Legacy consumer brands contacted through retail care desks:** Haldiram's care@ (bounced), Parle care@ (bounced), Bisleri wecare@, SpiceJet custrelations@, and Phoenix Marketcity's customer "smile center".

**Do-not-contact breaches (9 companies, about 13 emails):**

- **Existing partners:** Station F, TF1, Fnac Darty and MiniMax, all "extending your existing partnership", 13 Sep. Also ByteDance/CapCut (13 Sep) and CloudWalk (20 Sep).
- **Co-founder exclusions:** Eros (13 Sep); ZEE (4 Sep, plus follow-ups on 13 and 22 Sep); JioStar (4 Sep, plus a 13 Sep follow-up).
- MiniMax answered with a decline.

**Collisions with live conversations:**

- Vidu's support inbox was re-pitched cold on 13 Sep while its Head of Operations was mid-conversation.
- NVIDIA received 4 separate threads (2 undisclosed-recipient blasts, the 17 Sep "Global" blast, and a 23 Sep bump) around the Kavita thread.
- Dell was re-pitched at board level after it declined.

---

## 7. Top 12 problems, ranked by likely impact on reply rate

**1. The mail went to inboxes that cannot buy sponsorship.**

- *Evidence.*
  - Only 26 of 570 first touches (4.6%) went to a partnerships, sponsorship or BD address.
  - 129 went to info@, support@, sales@ or reservations@, and 16 went to investor relations, company secretaries or legal.
  - The autoresponders prove where it landed: "Dear Customer", "Dear Guest", "Dear boAthead", "AUP Donation Request", "we only respond to editorial requests", "we no longer accept resumes".
  - 15 companies' support desks merely forwarded the message; 29 sent only a bot reply.
- *Fix.*
  - Never send to support@, care@, helpline@, reservations@, sales@, IR, company-secretary or legal addresses.
  - Pick one named brand, marketing or partnerships head per company from LinkedIn, and verify the address (Hunter or Apollo "verified" only).
  - If no such person exists, use the LinkedIn InMail route rather than a desk inbox.

**2. The offer and the targets do not match, so even a perfect email cannot convert.**

- *Evidence.*
  - The product pitched until 22 Sep was an India edition in "December 2026" with no venue, no date that could be shared, and no organizer.
  - Radisson: "a lot is still being finalised on your end".
  - Aditya himself to ShareChat: "cannot give numbers regarding our india edition". The 19 Sep follow-up said: "We are in the early stages of planning a WAiFF India edition".
  - Targets included about 20 chip and enterprise B2B firms, about 20 government bodies, dozens of seed-stage startups ("careful with capacity", "budget... is limited"), VFX houses that dislike AI (ILM), hotels (all 7 human replies were sales pitches back), and industrial groups for a EUR 50,000 organizer licence (MRF: "doesn't fit into our plans").
- *Fix.*
  - **Sponsor track:** sell Cannes 2027 (6 to 7 Apr) plus named editions, and only to brands that already buy festival or culture sponsorship (Rolex, Campari, Chopard, Kering, Lavazza, IWC, Swarovski, UBS, Visa, AT&T, Rogers types) or that sell to filmmakers (camera, lens, audio, post, AI video tools with Series B or later funding).
  - **Organizer track:** only companies whose business is events or festival IP (IFP, Kyoorius, e4m, Adgully, IA-Meetings, MCI, Wizcraft, Teamwork Arts types).
  - Drop government bodies, chip makers, pre-Series-B startups and hotels (a hotel is a venue vendor, not a sponsor).

**3. Warm leads were mishandled. 13 engaged replies produced 0 proposals.**

- *Evidence.*
  - Cascadeur asked for "price range... confirmed date... what is included" and **got no reply in 10 days**.
  - Cooke asked "what do you refer exactly as a Collaboration" and was answered **82 hours later with ~1,100 words**.
  - Wonder Studios asked for times and got "Well tuesday , thursday , friday works for me but timings will be between 3 to 6 pm ist."
  - ShareChat got a bare phone number, then ~1,100 words, then a deck link, and went silent.
  - Trident wrote "your phone is unreachable" and was never answered. Grand Hyatt (Stephanie Gururani), NESCO, Novotel and Getty were never answered.
  - Vidu and IA-Meetings, both mid-conversation, were hit with cold re-pitches or note-less bumps.
  - Kimi and Hedra declines got 1,000 to 1,500-word rebuttals.
- *Fix.*
  - Answer every human reply within 24 hours, before any new outreach.
  - Keep the answer under 120 words, respond to the exact question, attach **one** single-page PDF (the what, the date, the tiers and a price range for the Cannes 2027 packages), and send a calendar invite for a specific slot in their time zone.
  - Never argue with a decline. Reply once: "Understood, thank you. May I check back when you move into video?"

**4. Deliverability and sender reputation were damaged, so many emails were likely filtered.**

- *Evidence.*
  - Sent from a personal gmail.com account.
  - Bursts of 100 to 235 emails in 4-minute windows, and 50% of first touches on weekends.
  - 40% of first touches sent between 00:00 and 04:00 IST.
  - 25 of 28 sampled bodies carry a google.com/url redirect wrapper as the website link.
  - About 9% of first touches bounced (5.4% lost the To), and 13 dead addresses were re-mailed up to 4 times.
  - 24 all-BCC "undisclosed-recipients" sends, 22-address visible To lists, 35 personal Gmail/Hotmail/Yahoo recipients.
  - Near-identical templates sent to hundreds.
  - 84 "Re:" subjects the recipient never received.
- *Fix.*
  - Get a Google Workspace mailbox on the WAiFF domain (already requested in the Refinement Log) with SPF, DKIM and DMARC, and warm it up.
  - Cap sending at 30 to 40 a day, Tuesday to Thursday, 10:00 to 12:00 in the recipient's time zone.
  - Paste links as plain text (`https://worldaifilmfestival.com`), never copied from rendered Gmail.
  - Suppress every address that has bounced once. One To, no BCC.

**5. Factual errors and merge bugs destroyed credibility where it mattered most.**

- *Evidence (section 3.3).* Examples:
  - "[Company]'s India edition is launching in Mumbai" (up to 54 sends).
  - "India edition to Cannes" (up to 48).
  - "Jury President Gong Li" (up to 70).
  - "Gong Li" listed in the jury (54).
  - "this April... third Cannes edition" for April 2027 (84).
  - Ginesy as co-founder (about 80).
  - "Apple Global" (about 250).
  - Genario (about 110), a festival name the Brief bans (twice), "15th December" leaks, and "80" vs "100+" countries.
  - Several of these went to people who then engaged or declined (ShareChat, Cascadeur, Ideogram, Vast.ai, the Hedra CEO, Kimi). A senior reader who spots one error discounts everything else.
- *Fix.*
  - A locked 3-line fact block, copied verbatim from Brief section 2 and never regenerated.
  - Before sending, render every merge field and grep the batch for "'s India edition", "this April", "Jury President Gong Li", "Global", "Genario", "15" and "Dec".

**6. Emails were too long and too hard to read, and the ask came last.**

- *Evidence.*
  - First-touch bodies run 136 to 1,008 words (typically 220 to 460).
  - Flesch-Kincaid grade 11 to 14.5, with 20 to 30-word sentences.
  - About 13 claims about WAiFF before the reader learns what is being asked.
  - Several versions end without a question at all: "A 15 minute call would tell us fast whether there's a real fit here"; "I would like 15 minutes with whoever owns brand marketing"; "Let me know what day works best."
- *Fix.*
  - 60 to 110 words.
  - Line 1: the specific hook. Line 2: what WAiFF is, in one sentence with **two** numbers. Line 3: the specific proposal for them (for example "a named Best AI Cinematography award at Cannes 2027"). Line 4: one yes/no question.
  - Move everything else to the one-page PDF sent after a reply.

**7. The copy reads as AI-generated, and a CEO said so.**

- *Evidence.*
  - Em dashes in 72% of subjects and in 3 body templates, plus the 135-send bump.
  - "I hope this email finds you well" and "I've been following X's journey for a while now [ED] what you've built... is truly remarkable" (V1, V4).
  - Hype: "undisputed Mecca of cinema", "1895 Lumiere brothers moment", "global movement fundamentally rewriting the multi-billion-dollar entertainment industry".
  - Hedra's CEO: "There was a significant amount of AI used in this response to the point where I found it difficult to read... when people send a proposal asking me to potentially spend 10s of thousands of dollars, it's usually a hand written note."
- *Fix.*
  - Write or heavily edit each first line by hand.
  - Banned list: em dashes, "I hope", "truly", "remarkable", "journey", "cutting-edge", "at the center of", "Mecca", "movement".
  - Read each email aloud before sending.

**8. The same companies were re-pitched as if new, including do-not-contact partners.**

- *Evidence.*
  - 77 companies got 2 or more separate cold pitches (92 extra threads). PhonePe, hoichoi, Samsung and YuVerse got 6 to 7 emails each.
  - CBFC, IndiaAI, PhonePe and hoichoi got the same pitch 3 times in 16 minutes.
  - The 23 Sep Apollo wave re-pitched at least 26 companies from 19 to 22 Sep; VOSS, Oakley and Itau got the same person on both dates.
  - 9 do-not-contact companies were emailed (Station F, TF1, Fnac, MiniMax, ByteDance, Eros, CloudWalk, ZEE, JioStar), and MiniMax declined.
- *Fix.*
  - One master company list keyed by domain.
  - A hard check before each send against sent mail (`in:sent to:@domain`) and the do-not-contact list.
  - One sequence per company: first touch plus 2 follow-ups, then stop.

**9. The follow-up mechanics were broken.**

- *Evidence.*
  - 274 of 379 follow-ups (72%) went out as new threads with a fake "Re:" subject. 135 of them say "Following up on the note below [ED] did you get a chance to take a look?" with nothing below; Anthropic's reply proves only the bump arrived.
  - Named people were greeted "Hi team" in follow-ups (for example Diego at WBD) and in about 30 Apollo first touches.
  - Follow-ups went to companies that had already declined (Canva) or were in live threads (NVIDIA, IA-Meetings, Vidu, Sennheiser).
  - 86 of 334 older companies never got a follow-up at all.
- *Fix.*
  - Always reply inside the original thread.
  - Two follow-ups only: Day 4 (two lines plus one new fact) and Day 10 ("If the timing's wrong, who should I speak to?").
  - Skip anyone who has replied, declined or bounced. Use their name.

**10. Unverifiable ROI claims, false urgency, prices in sponsor mail, and name-dropping prospects.**

- *Evidence.*
  - "Partners see real, measurable return: an estimated media value well above the partnership investment" (about 110 sends).
  - "This is moving fast, and I'd rather bring this to you directly before it's fully allocated" (about 150).
  - "an estimated media value above 450,000 euros against a 400,000 euro budget" (about 90 sponsor emails). The Brief bans prices in sponsor mail.
  - "We are in conversation with companies such as NVIDIA and Sennheiser" (66), after NVIDIA's PR had declined sponsorship.
- *Fix.* Remove all of it. Replace with one verifiable proof point: "JW Marriott Cannes, MiniMax and TF1 are partners". Never name live prospects.

**11. Mixed and confused asks.**

- *Evidence.*
  - One email offers sponsor, organizer, global partner, "Cannes and the global network, for India, or both" (the 19 Sep follow-up).
  - V1, V2 and V4 open with "walk you through the sponsorship tiers" before any interest.
  - The Dell blast buries India ("we are planning a dedicated India Edition as well").
  - The Reliance email offers "several conversations here rather than one".
- *Fix.* One role and one package per email. Sponsor emails name one concrete asset (a named award, a keynote slot at Cannes 2027). Organizer emails go only to event companies and state the licence in one line.

**12. Weak credibility infrastructure.**

- *Evidence.*
  - A personal gmail.com sender (B2B forms reject it, per the Refinement Log).
  - Three different signatures: "India Ambassador", "Aditya Vardhan Upadhyay, Ambassador", and "Founder & CEO, Quantum Leap AI".
  - Calendar invites sent from a second address (adiup398@gmail.com).
  - Decks sent as a Canva link and a Drive link against the Brief.
  - No appointment letter and no ambassador page link.
  - A casual register with buyers: "as i get hundreds of calls", "Just relax let them see it review it and reply", "Man, your own organisation is based out of AI".
- *Fix.*
  - A WAiFF-domain mailbox and one signature (name, "India Ambassador, World AI Film Festival", WAiFF site, LinkedIn).
  - A link to the ambassador listing on the WAiFF site, if it exists.
  - A one-page PDF that is attached only after a reply.
  - A written tone rule: no one-liners and no arguments with buyers.

---

## 8. The 5 best and 5 worst emails sent

"Best" is relative: none of these produced money. They are the emails that did the most right, or that actually opened a door.

### Best

**B1. Havells, 7 Sep 01:47 IST, To: a named brand manager (V6). No reply, but the best-constructed first touch.**
> Hi Amit,
>
> Hawa Badlegi stood out for who it put in front of the camera. Having Anurag Kashyap alongside Varun Dhawan and Yuzvendra Chahal is a genuinely filmmaker-literate choice for a consumer electricals brand, and it lines up with Havells saying openly that ad investment is going up, not flat.
>
> I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF). WAiFF was founded in 2025 by Marco Landi, the former President and COO of Apple, and its flagship runs in Cannes at the Palais des Festivals. This year's Cannes edition took 6,000+ applications from 100+ countries, put 80 projects into official competition, granted 13 awards, and drew 300+ industry professionals and 5,000+ participants. The 2026 jury sits under President Gong Li, with Claude Lelouch as Honorary President and Jean-Michel Jarre as Ambassador. National editions have already run in Seoul, Kyoto and Istanbul, and the festival now spans 15+ countries and 30+ cities.
>
> The India edition comes to Mumbai in December 2026, and we are building the founding partner group now. A brand that already casts a real filmmaker in its campaigns is a natural fit for a festival built around the craft of filmmaking itself. I would like 15 minutes with whoever owns brand marketing or partnerships to explore it. I am on IST and can work around your hours.
>
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (WAiFF)
> https://www.google.com/url?q=https://worldaifilmfestival.com/&source=gmail&ust=1788812221015000&sa=E

*Critique.* The hook is specific, recent and flattering in a credible way: a named campaign, named talent, and the company's own ad-spend statement. It goes to a named person, has no em dashes, and runs 222 words at grade 10.9. Weaknesses:

- It sent at 01:47 IST on a Monday.
- It packs 13 claims about WAiFF into one paragraph.
- It ends on a statement, not a question.
- "whoever owns brand marketing" tells Amit he may be the wrong person.

Cut the credential paragraph to one sentence and ask "Worth 15 minutes this week?"

**B2. Mastercard, 13 Sep 00:46 IST, To: Barkha Patel (V7). No reply.**
> Dear Barkha,
>
> I am writing because Mastercard has already done exactly what I would like to discuss. Mastercard was the Première Partner of the Reply AI Film Festival, and in India Mastercard took title sponsorship of all BCCI international and domestic home matches. That combination, a global appetite for AI film culture and a proven willingness to anchor major properties in India, is rare.
>
> I am Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF), the international film festival dedicated to AI-generated cinema, founded in 2025 by Marco Landi, former President and COO of Apple. The 2026 Cannes edition at the Palais des Festivals drew over 6,000 applications from 100+ countries, 80 projects in official competition, 13 awards, 300+ industry professionals and 5,000+ participants, under Jury President Gong Li with Claude Lelouch as Honorary President.
>
> The India Edition comes to Mumbai in December 2026 and the founding partner group is being formed now. Given Agent Pay and the settlement infrastructure work this year, Mastercard has a genuine technology story to tell here, not only a logo placement.
>
> Would you be open to a short call, or point me to the right person on the sponsorship side? I am on IST.
>
> Best regards,
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (WAiFF)
> Website: https://www.google.com/url?q=https://worldaifilmfestival.com/&source=gmail&ust=1789326984739000&sa=E

*Critique.* The best "why you" in the campaign: Mastercard already sponsored an AI film festival and anchors big Indian properties. It has a dual ask (a call, or a pointer to the right person). But it contains a factual error ("Jury President Gong Li"), went out after midnight on a Saturday night, was addressed to someone with no confirmed sponsorship role, and the link is a Google redirect.

**B3. Filmustage, 20 Sep 02:03 IST, To: support@ (V8/S14). Got "Let's set up a call this week", then a call on 23 Sep.**
> Hi Team,
>
> Filmustage's AI-powered script breakdown and scheduling platform has become a real tool for production teams handling global, multi-language projects, and you've built that into a genuinely profitable business with a lean team.
>
> I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF). WAiFF was founded in 2025 by Marco Landi, the former President and COO of Apple who was part of the task force that brought Steve Jobs back to Apple in 1997. Our flagship event is held annually at the Palais des Festivals in Cannes. The 2026 edition drew 6,000+ applications from 100+ countries and brought together 5,000+ industry professionals, with Gong Li as our 2026 President, Claude Lelouch as Honorary President, and Jean-Michel Jarre as Ambassador. Confirmed global partners already include JW Marriott Cannes, MiniMax, TF1, Fnac and Pathé, and we've been covered by Screen Daily, Le Monde, the BBC and Paris Match. We now run national editions across 15+ countries and 30+ cities, with more announced every month, all building toward Cannes 2027.
>
> WAiFF's India edition is launching in Mumbai this December, and I think there's a strong, specific fit for Filmustage here: the filmmakers and production teams at WAiFF are exactly the pre-production audience Filmustage is built for, and this is a direct way to put your platform in front of them. Partners see real, measurable return: an estimated media value well above the partnership investment, on top of international PR, red-carpet association, and direct access to the people shaping this industry.
>
> This is moving fast, and I'd rather bring this to you directly before it's fully allocated. Would you be open to a short call this week or next to talk through the fit for Filmustage?
>
> I'm on Indian Standard Time but can work around your hours.
>
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (WAiFF)
> https://www.google.com/url?q=https://worldaifilmfestival.com/&source=gmail&ust=1789936392863000&sa=E

*Critique.* It worked because of **relevance**: a film pre-production SaaS company pitched to filmmakers. Its own flaws are still there:

- "Hi Team" to a support inbox.
- The unverifiable ROI line.
- False urgency ("before it's fully allocated").
- Partners who are on the do-not-contact list named as proof (MiniMax, TF1, Fnac).
- 299 words, and sent at 02:03 IST on a Sunday.

The call then ended in a decline. Filmustage is a small team, and nothing in the email qualified budget.

**B4. IFP, 22 Sep 19:41 IST, To: Ritam (organizer, V10). No reply yet.**
> Hi Ritam,
>
> IFP's Season 16 pulling 64,328 festival attendees and 53,000+ challenge participants from 42 countries is exactly the kind of proven, large-scale creative-festival infrastructure this opportunity needs, and the 50-Hour Filmmaking format shows you already understand how to run a real filmmaker competition, not just a brand event.
>
> I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF). WAiFF was founded in 2025 by Marco Landi, the former President and COO of Apple, part of the task force that brought Steve Jobs back to Apple in 1997. The flagship is held every year at the Palais des Festivals in Cannes, the same venue as the Cannes Film Festival. We started as a single edition in 2025 with over 1,500 submissions. The 2026 Cannes edition drew 6,000+ applications from 100+ countries, 80 projects in official competition, 300+ industry professionals and 5,000+ participants, with Gong Li as our 2026 President, Claude Lelouch as Honorary President, Agnes Jaoui as Jury President and Jean-Michel Jarre as Ambassador, backed by the Departement des Alpes-Maritimes and the City of Cannes. Confirmed global partners include JW Marriott Cannes, MiniMax, TF1, Fnac and Pathe, with coverage from Screen Daily, Le Monde, the BBC and Paris Match. In one year we have grown to national editions in Seoul, Kyoto and Istanbul, with Buenos Aires and Montreal/Vancouver confirmed for October 2026, now running across 15+ countries and 30+ cities and adding more every month, all building toward Cannes 2027.
>
> I am not writing to ask IFP to sponsor an existing event. I am offering the India edition itself: full ownership and control of running WAiFF India every year, under an organizer license. The license fee is 50,000 euros, and the organizer keeps all sponsorship revenue raised on top of that, along with rights to the official WAiFF brand and direct access to WAiFF's global network of filmmakers, studios and AI companies traveling in for the event. There is also a Global WAiFF Partner upgrade at 400,000 euros for direct integration into the Cannes flagship itself, not just the India edition.
>
> The India edition needs to launch this December, so this window is short, and I would rather bring it to an organizer who already runs a proven filmmaking-challenge format and has real sponsor infrastructure than build one from nothing. IFP's scale and film-specific format make this a natural fit.
>
> Would you be open to a short call this week or next to walk through it properly? I'm on Indian Standard Time but happy to work around your hours.
>
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (WAiFF)
> https://www.google.com/url?q=https://worldaifilmfestival.com/&source=gmail&ust=1790172665253000&sa=E

*Critique.* The right **kind** of organizer target: a festival operator with a proven filmmaker-competition format. It names the person, uses real stats, and explains the licence clearly. It is too long (421 words, grade 13.2), puts the licence price before any interest, and the "same venue as the Cannes Film Festival" line invites confusion. It would be stronger at 100 words with the price saved for the call.

**B5. Qube Cinema follow-up, 14 Sep 16:18 IST (FU14, organizer).**
> Hi team,
>
> One update since I last wrote. Our 2027 flagship is now fixed for 6 and 7 April 2027 at the Palais des Festivals in Cannes, and the India edition sits on the road to it.
>
> The structure is the part worth a minute. Each national edition is run by a local organizing partner who owns and runs that edition end to end, selects its best AI films, and sends them into the Road to Cannes Selection to compete at the Palais finale. The organizer keeps the sponsorship revenue they generate on top of the licence.
>
> For a sense of the level, the 2026 edition had Gong Li as Festival President, Claude Lelouch as Honorary President and Agnes Jaoui as Jury President, with Roger Avary, Aissa Maiga, Elsa Zylberstein and Ruby Yang on the jury.
>
> Worth fifteen minutes to walk through what organizing the India edition would involve for Qube? I am on Indian Standard Time and can work around your hours.
>
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (WAiFF)
> https://www.google.com/url?q=https://worldaifilmfestival.com/&source=gmail&ust=1789469282367000&sa=E

*Critique.* The best follow-up of the campaign: one new fact (the Cannes 2027 date), one sentence on how the organizer model works, a short proof line, and a single binary ask naming the company. Its faults: it was sent as a new thread with a "Re:" subject, and it went to sales@qubecinema.com (a sales desk).

### Worst

**W1. Dell, 17 Sep 18:58 IST (V9). To: Media.Relations@dell.com, Board_of_Directors@dell.com, investor_relations@dell.com. BCC: 15 addresses, including arps23@gmail.com and chhabranidhi@gmail.com. Sent 3 days after Dell had declined in writing.** Excerpt (the full body is 1,008 words):
> Dear Dell Team,
>
> I hope this message finds you well. I am writing to you with genuine admiration for what Dell has built over the decades. From your foundational work in personal computing to your rise as a global leader in workstations, gaming hardware, and enterprise solutions, Dell has consistently stood at the intersection of performance and reliability. The Precision workstations have become the backbone of professionals and creators worldwide. The Alienware brand has become synonymous with elite gaming. The XPS series has redefined what a premium laptop can be. The Latitude and OptiPlex lines have powered businesses and institutions across the globe. And your recent push into AI PCs, edge computing, and sustainable technology shows you are not just keeping pace with the future, you are helping define it. The way you have served professionals, gamers, creators, and enterprises, understanding that they all demand uncompromising performance and reliability, speaks volumes about your vision. Your commitment to pushing boundaries is something I have always respected.
>
> My name is Aditya Vardhan Upadhyay, and I am reaching out as the India Ambassador for the World AI Film Festival. I wanted to personally share an opportunity that I believe aligns perfectly with what Dell represents and where the future of content creation is heading.
>
> The World AI Film Festival was founded in 2025 by Marco Landi, the former President and COO of Apple Global who famously orchestrated the return of Steve Jobs, alongside Charles Ange Ginesy, President of the Alpes-Maritimes Department. The global press is calling this the "1895 Lumiere brothers moment" for the 21st century. This is not just a festival. It is a global movement fundamentally rewriting the multi-billion-dollar entertainment industry.
>
> Our flagship event takes place at the iconic Palais des Festivals in Cannes, the undisputed Mecca of cinema. Our 2026 edition drew over 6,000 film submissions from 80 countries and brought together more than 5,000 top-tier industry executives, investors, and creators. The organization is backed by global cinema legends like Gong Li, Claude Lelouch, and Oscar-winner Roger Avary, alongside major studios like Pathe and Banijay. Our official partners already include tech and media titans like CapCut, MiniMax, Canal+, TF1, and JW Marriott.
>
> [...three paragraphs of product-line praise and "Imagine a Precision-branded award..."...]
>
> Beyond the flagship Cannes event, Dell would be marketed across every national edition we run. From Los Angeles to Tokyo, from London to Sao Paulo, your brand would be visible in every market where creators gather. And I should also mention that we are planning a dedicated India Edition of the festival as well, which would offer additional localized visibility and engagement opportunities. However, my primary focus in reaching out to you is the global partnership, as I believe that is where Dell can unlock the most value across all our editions and the Cannes flagship.
>
> The business case is strong. For our 2027 season, we are projecting 30 Million+ targeted global impressions. Our partners consistently see a return on investment significantly greater than 1, with an estimated media value exceeding 450,000 euros against a 400,000 euro global reference budget. You get unmatched international PR, premium digital visibility, and direct networking access to the leaders shaping the future of global media.
>
> [...]
>
> I would love to jump on a quick Google Meet to show you the full scope of what we can build together. Let me know what day works best for your schedule.

*Critique.* Almost every rule is broken at once:

- The board, IR and personal Gmail addresses got an unsolicited 1,000-word pitch after an explicit decline.
- A brochure-style opening paragraph (140 words of product-line praise).
- Unverifiable press quotes ("1895 Lumiere brothers moment").
- Wrong or overstated facts ("famously orchestrated the return of Steve Jobs", Ginesy as co-founder, "80 countries").
- Sponsor pricing and an ROI claim.
- India demoted to an afterthought.
- No question in the ask.

Result: an out-of-office and a "no longer employed" auto-reply. About 20 companies got the same template on 17 to 18 Sep (22 sends), and one human answered: Acer's outsourced desk, with a decline.

**W2. Hedra CEO thread, 21 Sep (Aditya's 3rd and 4th messages, after the CEO declined and then flagged AI-written text).**
> [Aditya, 21 Sep 19:51 IST, after the CEO wrote 'There was a significant amount of AI used in this response to the point where I found it difficult to read.']
> It is a specific message which contains all the relevant information
> whenever you could analize it.
>
> [CEO sends a screenshot. Aditya, 21 Sep 20:48 IST:]
> Man, your own organisation is based out of AI, and now AI is somehow
> becoming a disadvantage
>
> I had an opportunity that I presented to you. Of course, it’s completely up
> to you to evaluate it and decide whether it makes sense. But not even
> reading it and simply sending me a screenshot saying it was AI-generated is
> a little funny.
>
> At this point, why are we even emailing each other? Why don’t we just
> physically handwrite our emails and leave them in each other’s mailboxes at
> home?
>
> I mean, we’re literally living in the age of AI. [crying-face emoji]
>
> [CEO: 'I did read it... normally when people send a proposal asking me to potentially spend 10s of thousands of dollars, it's usually a hand written note. I never respond with AI written emails fyi.' Aditya, 21 Sep 22:25 IST, 1,022 words, opening:]
> Hi Michael, At the end of the day, what matters is the information and the opportunity itself. But since you seem to prefer a handwritten note, consider this my handwritten version of the message. We are in technology, and technology is ultimately going to be leveraged. I genuinely did not know that you preferred something handwritten, otherwise I would have approached it differently. I am not going to write everything on paper and send it physically because I believe the way we work today is through technology, and that is not the same as not taking something seriously. I have spoken with and presented opportunities to a number of companies and senior people, including conversations around companies like NVIDIA. Ultimately, every company has its own way of evaluating opportunities, deciding what aligns with its objectives, and deciding whether it wants to invest or partner. That is completely fair. What I would ask is simply to look at the material I have shared before making a judgment based on the format in which it was presented. ...

*Critique.* Arguing with a founder-CEO who had personally replied, sarcasm, an emoji, then a 1,022-word "handwritten version" that repeats the wrong festival name ("the World AI International Film Festival") and invents editions ("Mumbai, Berlin, Moscow"). This burns the brand with exactly the founder network (AI video startups) the campaign most needs. A one-line thank-you would have kept the door open.

**W3. Tech Mahindra, 2 Sep 23:50 IST (V1). To: undisclosed-recipients. BCC: alliances@, socialmedia@, mktg@, media.relations@.** Full text:
> Dear Team Tech Mahindra,
>
> I hope this email finds you well.
>
> I've been following Tech Mahindra's journey for a while now [ED] what you've built as a global leader in technology consulting and digital solutions is truly remarkable. With 149,000+ professionals across 90+ countries serving 1,100+ clients, you're enabling enterprises to achieve transformative scale at unparalleled speed. Your full spectrum of services [ED] from consulting, IT, and enterprise applications to AI & analytics, cloud, and network services [ED] positions you as a comprehensive partner for businesses navigating the digital age.
>
> What stands out is that you were the first Indian company in the world to be awarded the Sustainable Markets Initiative's Terra Carta Seal, recognizing your leadership in creating a climate and nature-positive future. As part of the Mahindra Group, founded in 1945, you carry forward a legacy of excellence while pioneering the future of AI and digital transformation. That combination of heritage and innovation is exactly the kind of leadership that should be part of this conversation.
>
> I'm Aditya Upadhyay, the India Ambassador for the World AI Film Festival (WAiFF) [ED] the world's first and largest international film festival dedicated exclusively to AI-generated cinema.
>
> WAiFF was founded by Marco Landi, former President of Apple, and is backed by visionary leaders including the President of the Alpes-Maritimes Department and the Mayor of Cannes. Our flagship event is held annually at the Palais des Festivals in Cannes. The festival has experienced extraordinary growth: from over 1,500 submissions across 53 countries in our inaugural 2025 edition to over 5,500 submissions from 80+ countries in 2026. We now host national "Road to Cannes" editions across the globe [ED] in Japan, Korea, China, Brazil, Argentina, UK, and more [ED] each sending their best AI films to compete at the Cannes finale.
>
> We are now launching the India Edition on 15th December 2026, and I'm personally curating the founding group of sponsors.
>
> For Tech Mahindra, this represents a unique opportunity to establish early visibility with India's rapidly growing AI and filmmaking community, gain a direct connection to WAiFF's prestigious international network, and secure a seat at the table while this category is still being defined. Given Tech Mahindra's deep expertise in AI, analytics, customer experience, and digital transformation [ED] combined with your strong Indian roots and global reach [ED] your presence would be a natural and powerful fit. And this kind of foundational positioning is hard to replicate once the ecosystem matures.
>
> I would love to walk you through the sponsorship tiers and explore where Tech Mahindra fits best. Would you be open to a brief Google Meet this week?
>
> Looking forward to your response.
>
> Best regards,
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (WAiFF)
> Website: https://worldaifilmfestival.com/

*Critique.*

- Blind BCC to four shared inboxes.
- Opens with "I hope this email finds you well", then 170 words of company-brochure praise that Tech Mahindra already knows.
- 8 em dashes.
- Unverifiable ("world's first and largest") and superseded ("5,500 from 80+") claims, and running editions that did not exist ("Japan... China... Argentina, UK").
- **Leaks the exact internal date ("15th December 2026").**
- Asks to walk through "sponsorship tiers" before any interest.
- 435 words, grade 14.

It was the first template, and 14 of its 17 sends went all-BCC.

**W4. Warner Bros. Discovery, 14 Sep 03:11 IST, To: Diego (V8 with the merge bug).** Full text:
> Hi Diego,
>
> I saw Max renew "The Pitt," starring Noah Wyle, for a second season, and Warner Bros. Discovery's crossover between Tom and Jerry and the ITTF World Cup Macao 2026.
>
> I'm Aditya Upadhyay, India Ambassador for the World AI Film Festival (WAiFF). WAiFF was founded in 2025 by Marco Landi, the former President and COO of Apple Global who was part of the task force that brought Steve Jobs back to Apple in 1997. Our flagship event is held annually at the Palais des Festivals in Cannes, the same venue as the Cannes Film Festival. The 2026 edition drew 6,000+ applications from 100+ countries and brought together 5,000+ industry professionals, with Gong Li as our 2026 President, Claude Lelouch as Honorary President, and Jean-Michel Jarre as Ambassador. Confirmed global partners already include JW Marriott Cannes, MiniMax, TF1, Fnac and Pathe, and we've been covered by Screen Daily, Le Monde, the BBC and Paris Match. We now run national editions across 15+ countries and 30+ cities, with more announced every month, all building toward Cannes 2027.
>
> WBD's India edition is launching in Mumbai this December, and I think there's a strong, specific fit here: WBD's work blending entertainment IP with live global events is exactly the kind of association WAiFF India can offer. Partners see real, measurable return: an estimated media value well above the partnership investment, on top of international PR, red-carpet association, and direct access to the people shaping this industry.
>
> This is moving fast, and I'd rather bring this to you directly before it's fully allocated. Would you be open to a short call this week or next to talk through the fit for Warner Bros. Discovery?
>
> I'm on Indian Standard Time but can work around your hours.
>
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (WAiFF)
> https://www.google.com/url?q=https://worldaifilmfestival.com/&source=gmail&ust=1789422106805000&sa=E

*Critique.*

- "**WBD's India edition** is launching in Mumbai" tells a studio executive the email is a mail-merge that broke. The same bug went to ShareChat, Cascadeur, Ideogram, Vast.ai and probably most of the 54 sends that day.
- "Apple Global" is wrong.
- The ROI and urgency lines are unverifiable pressure.
- 291 words, sent at 03:11 IST.
- The hook ("I saw Max renew The Pitt...") is trivia, not a reason WBD would sponsor.
- The 19 Sep follow-up then opened "Hi team" to the same named person and added 686 words and a price.

**W5. The note-less bump, 13 Sep 16:47 to 16:51 IST, sent 135 times as new threads with "Re:" subjects.** Full text:
> Following up on the note below [ED] did you get a chance to take a look?
>
> Would love to find 15 minutes for a call this week or next. I'm on Indian Standard Time but can work around your hours.
>
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (WAiFF)
> https://www.google.com/url?q=https://worldaifilmfestival.com/&source=gmail&ust=1789384765458000&sa=E

*Critique.* The "note below" does not exist: each email was a new thread. Anthropic's agency reply quotes back exactly these 40 words and nothing else. It has an em dash, adds no new value, carries a redirect link, went out on a Sunday, and went in a 4-minute burst to 135 inboxes, including dead addresses (Nestle, Aputure, Accor, Epidemic Sound, Shutterstock and Gan.ai all bounced again), live conversations (YuVerse's Ajay after his call, IA-Meetings after its meeting) and customer-care desks. It is the single most spam-like action in the campaign.

*Dishonourable mention:* the reply to AssemblyAI's support agent (6 Sep 00:26 and 00:27 IST): "Just Send it to leadership they will evaluate it" and "Just relax let them see it review it and reply".

---

## Appendix: key counts at a glance

| Metric | Value |
|---|---|
| WAiFF emails sent, 2 to 23 Sep | about 990 (570 first touches, 379 follow-ups, 41+ conversation replies) |
| Unique companies | about 478 (sponsor about 438, organizer 40) |
| Companies pitched more than once as new | 77 |
| First-touch bounce rate (any / To lost) | 8.9% / 5.4% |
| Dead addresses re-mailed after bouncing | 13 |
| Companies with any non-bounce response | 81 (16.9%) |
| Human-written prospect replies | 30 (6.3%): 13 engaged, 10 declines, 7 venue/vendor |
| Engaged rate, sponsor / organizer | 2.7% / 2.5% |
| Calls held | at least 6 |
| Proposals with price and date sent to engaged prospects | 0 |
| Human replies left unanswered | Cascadeur, Grand Hyatt (Stephanie), Trident (Tarun, 11 Sep), NESCO, Novotel, Getty |
| Share of first touches to a partnerships/sponsorship inbox | 4.6% |
| First touches sent on weekends / 00:00 to 04:00 IST | 50% / 40% |
