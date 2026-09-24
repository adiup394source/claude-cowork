# WAiFF Outreach Playbook: Evidence-Based Rules for Sponsor and Organizer-Licence Cold Outreach

Prepared 24 September 2026 for Aditya Upadhyay, India Ambassador, World AI Film Festival (WAiFF).
Scope: cold email from adiup394@gmail.com and LinkedIn outreach to (a) sponsors of WAiFF Cannes 2027 (6 to 7 April 2027, Palais des Festivals) and the global editions, and (b) one large Indian company to license and run WAiFF India in December 2026.

How to read the evidence grades used below:

- **A** = large primary dataset with a stated method (Gong Labs, Hunter, Belkins, Backlinko/Pitchbox, Instantly, Woodpecker, Expandi, LinkedIn's own data, Google's own rules).
- **B** = vendor or practitioner dataset with a thinner method, or a single well-known practitioner's field rule (Lavender, Salesloft, Yesware, Chris Baylis, Kim Skildum-Reid).
- **C** = expert opinion or secondary summary; use as a hypothesis to test, not a rule.

A general caveat: open-rate studies are now weak evidence. Apple Mail Privacy Protection pre-loads tracking pixels, and Apple accounted for about 65% of tracked opens in 2026, so "opens" are inflated ([lemlist](https://www.lemlist.com/blog/cold-email-open-rates)). Where studies disagree, this playbook prefers reply-based and meeting-based data (Gong, Hunter, Instantly) over open-based data.

---

## 0. What the first 20 days of your own sent folder says

Before external research, the Gmail export of the campaign (751 first-touch threads sent 5 to 23 September 2026, parsed from the scratchpad `gm/*.tsv` files) shows why replies are near zero. These are measured facts from that export, not estimates.

| Signal in the export | What it was | Benchmark or rule it breaks |
|---|---|---|
| Volume | 751 threads in about 19 days; 223 on a single day (13 Sept); 135 first touches inside one 10-minute window | Safe cold volume from one Gmail inbox is roughly 20 to 40 per day, ramped gradually; sudden bursts are treated as spam behaviour (section 7) |
| Weekend sending | About 51% to 59% of first touches went out on a Saturday or Sunday (range depends on whether export timestamps are UTC or IST); only 5 of 750 landed between 9:00 and 12:00 IST | Best reply windows are Tue to Thu, 8:00 to 12:00 recipient-local ([Belkins](https://belkins.io/blog/best-time-to-send-email), [Salesloft](https://www.salesloft.com/resources/blog/16-tips-to-double-your-reply-rates)) |
| Who received it | 399 of 834 To-addresses (48%) were role inboxes: press@, media@, info@, support@, care@, reservations@, helpline@ | Support and PR desks cannot buy sponsorships; 42 threads got ticket or auto-replies ("Dear Customer", "Dear Valued Guest", "we only respond to editorial") |
| BCC use | 194 threads (26%) carried BCC recipients, some with 10 to 20 BCCs | Multiple hidden recipients read as mass mail and count against Gmail's 500-recipient daily cap (section 6) |
| Bounces | 37 threads hard-bounced, 5 were blocked by the recipient's security gateway, 4 delayed: about 6% of threads | Keep bounces under 2%; above 3% risks throttling ([Puzzle Inbox summary of Google threshold](https://puzzleinbox.com/compare/cold-email-bounce-rate-threshold)) |
| Subject lines | Average 10.6 words; about 74% of threads had an em dash in subject or opening; templated patterns such as "Partnership Opportunity - {X} x World AI Film Festival" and "{X} - license and run the WAiFF India edition" | Best-performing cold subjects are 1 to 4 words, look internal, and avoid selling language ([Gong/30MPC](https://www.30mpc.com/newsletter/4-data-backed-subject-lines-to-get-your-cold-emails-opened)) |
| Openers | "Dear Samsung Team, I hope this email finds you well", "Hi team", "Hi PhonePe team, I'm Aditya Upadhyay" | Timeline or trigger openers reply at about 2.3x problem or generic openers ([Instantly 2026](https://instantly.ai/cold-email-benchmark-report-2026)) |
| Follow-ups | 132 follow-ups began "Following up on the note below, did you get a chance to take a look? Would love to find 15 minutes for a call" | Gong found "I never heard back" style bumps raise replies but cut meetings booked by 14%, and meeting asks convert about half as well as interest asks ([Gong](https://www.gong.io/blog/7-tips-for-writing-the-perfect-follow-up-sales-email-according-to-science), [Gong CTA](https://www.gong.io/blog/this-surprising-cold-email-cta-will-help-you-book-a-lot-more-meetings)). One founder-CEO replied: "I did read it. I'm not sure why you thought I didn't." |
| Human replies | About 20 threads (under 3%) drew a human reply. Most warm ones came from venues, hotels and event agencies (who see you as their customer), not budget holders. Three asked for a phone number | Indian respondents want a phone or WhatsApp number in the signature (section 10) |

Also note a facts problem: WAiFF's own 2027 sponsor deck says "+6000 applications, +80 countries, 13 awards, +300 industry professionals, +5000 participants"; the 2027 partnership proposal says "6,600+ works submitted"; French press reported "nearly 5,500 films, over 80 countries" ([Mediakwest](https://mediakwest.com/world-ai-film-festival-2026/)). The brief's "100+ countries" is not supported by WAiFF's own materials. A marketing lead who Googles one number and finds a different one will discount everything else. Use one sourced set: **6,000+ submissions from 80+ countries in 2026** unless HQ confirms otherwise in writing.

**Implication:** the problem so far is mainly targeting, volume and deliverability, and only then copy. Fixing copy while still blasting role inboxes from a burst-sending Gmail will not change outcomes.

---

## 1. Benchmarks: what "good" looks like, so you can judge progress

| Metric | Average | Good | Source (grade) |
|---|---|---|---|
| Cold email reply rate, all replies | 3.43% (2025 sends) | Top quartile 5.5%+, top decile 10.7%+ | [Instantly 2026](https://instantly.ai/cold-email-benchmark-report-2026) (A) |
| Sequence reply rate | 4.5% | 6.2% for 21 to 50-recipient campaigns | [Hunter State of Email Outreach](https://hunter.io/the-state-of-cold-email) (A) |
| Emails per meeting | Average rep needs 344 cold emails per meeting (about 3 meetings per 1,000) | Top 10% book about 23 per 1,000 | [Gong](https://www.gong.io/blog/does-cold-email-even-work-any-more-heres-what-the-data-says) (A) |
| Executives | C-level are 30.2% less likely to reply than non-execs | They reply to short, priority-led notes | [Gong](https://www.gong.io/blog/do-execs-really-reply-to-cold-email-here-s-what-the-data-says) (A) |
| Unsolicited sponsorship asks | "Well under 5%" response; over 90% of proposals end in the trash | Researched, brand-specific approaches stand out from about 90% of what sponsors receive | [Sponsorship Collective](https://sponsorshipcollective.com/blog/why-sponsors-say-no/), [Power Sponsorship](https://powersponsorship.com/dont-send-a-sponsorship-proposal/) (B) |
| LinkedIn | 28.5% acceptance, 10.4% message reply rate | 3-message sequences reply at 9.8% | [Expandi H2 2026, 13.2M requests](https://expandi.io/state-of-linkedin-outreach-h2-2026/) (A) |

Realistic target for a researched, low-volume WAiFF campaign: 8% to 15% human reply rate on named decision-makers, and 1 qualified call per 15 to 25 well-researched accounts. Small lists win: campaigns under 50 recipients averaged 5.8% replies versus 2.1% for 1,000+ ([Woodpecker](https://woodpecker.co/blog/cold-email-statistics/), A); Hunter found campaigns of 100 or fewer contacts get about 3x the replies of mass blasts ([Hunter 2022 vs 2025](https://hunter.io/blog/cold-email-2022-vs-2025), A).

---

## 2. Subject lines

### 2.1 What the evidence says

| Question | Finding | Grade |
|---|---|---|
| Length | Gong/30MPC (85M cold emails): shorter is better, 1 to 4 words lead; "internal camouflage" wins, e.g. "trial delays", "hiring ops" ([30MPC](https://www.30mpc.com/newsletter/4-data-backed-subject-lines-to-get-your-cold-emails-opened)). Lavender: 2 words optimal, 2-word lines get 1.6x the opens of 5-word lines ([Lavender](https://lavender.ai/blog/cold-email-subject-line-tips)). Belkins (5.5M emails): 2 to 4 words at 46% open versus 34% for 10 words ([Belkins](https://belkins.io/blog/b2b-cold-email-subject-line-statistics)). Outlier: Backlinko found longer subjects had 24.6% higher response in link-building outreach ([Backlinko](https://backlinko.com/email-outreach-study)), a different use case | A (converging) |
| Case | Gong: all-lowercase lines had the highest open rates ([30MPC](https://www.30mpc.com/newsletter/4-data-backed-subject-lines-to-get-your-cold-emails-opened)). Lavender's older data favoured Title Case (not using it cut opens 30%). Conflicting and open-based, so treat case as low-stakes: pick lowercase or sentence case, never ALL CAPS | B |
| Naming them | Personalized subject lines: 46% open vs 35% (Belkins), and replies 7% vs 3% ([Belkins](https://belkins.io/blog/b2b-cold-email-subject-line-statistics)); +30.5% response ([Backlinko](https://backlinko.com/email-outreach-study)) | A |
| Question vs statement | Belkins: question lines led opens at 46%. Lavender: questions lowered opens 56%. Conflict; use statements by default and questions only when the question is specific | B (conflict) |
| Salesy words | Gong: selling language in subject lines cut opens 17.9% ([Martal summary of Gong](https://martal.ca/cold-email-subject-line/)). Yesware: "Invitation To Join" dropped reply rate to 2%; "appropriate person" replied at one-sixth of average ([Yesware](https://www.yesware.com/blog/email-subject-line-analysis/)) | A/B |
| Empty or tricky | Empty subjects raised opens 30% but cut replies 12% ([30MPC](https://www.30mpc.com/newsletter/4-data-backed-subject-lines-to-get-your-cold-emails-opened)). Never use fake "Re:" or "Fwd:" | A |
| Spam-word lists | Single "spam words" matter much less than sender reputation; the risk is stacking promotional phrases (one test: "limited time offer" alone cost 22% inbox placement, stacking three phrases cost 67%) plus all caps, multiple exclamation marks and 3+ links ([MailTester](https://mailtester.com/blog/spam-trigger-word-myths-debunked-deliverability-data/)) | B |

### 2.2 Rules for WAiFF subject lines

1. 2 to 5 words, under about 40 characters, so it survives mobile truncation.
2. Lowercase or sentence case. No emojis, no exclamation marks, no em dashes, no "x" collab formula ("X x WAiFF").
3. Name something specific to them (company, product, programme, or a real recent event) or one concrete WAiFF asset (a named award, the Cannes final, the India edition).
4. Banned words in subject lines: opportunity, partnership opportunity, sponsorship, sponsor, invitation, exclusive, global stage, premium, collaboration, proposal, quick question, following up, checking in, "hope", any price.
5. It must be true and match the first line of the body (a mismatched subject is the fastest way to a spam report).
6. Test in pairs: send two subject variants across 20 to 30 similar accounts each and judge on replies, not opens.

### 2.3 Sponsor track: 25 candidate subject lines

Placeholders in braces. Pick the one that matches the specific idea in the body.

| # | Subject line | Angle it signals |
|---|---|---|
| 1 | {product} award in cannes | Named award |
| 2 | a {product} prize at the palais | Named award, venue prestige |
| 3 | named award idea for {company} | Named award, plain |
| 4 | {company} at cannes, 6 april | Date-anchored |
| 5 | ai films made with {product} | Tool usage by filmmakers |
| 6 | {product} and 6,000 ai filmmakers | Audience scale (verified number only) |
| 7 | one ai video partner for cannes | Category exclusivity |
| 8 | the ai video category at waiff | Category exclusivity |
| 9 | {company} before cannes lions | Timing vs their June Cannes Lions plan |
| 10 | your cannes lions story, earlier | Same, softer |
| 11 | after the {launch name} launch | Trigger event |
| 12 | re your {talk or post topic} | Trigger (only if they really posted or spoke) |
| 13 | {company} creator challenge idea | Branded open call |
| 14 | a {product} challenge for filmmakers | Branded open call |
| 15 | {first name}, a cannes jury seat | Jury or judging role |
| 16 | judging ai films with {company} | Jury or judging role |
| 17 | {company} in 12 festival cities | Global editions reach |
| 18 | road to cannes, with {product} | Global editions feeding the final |
| 19 | idea for {company}'s creator team | Addressed to creator marketing |
| 20 | ai filmmakers who use {product} | Audience fit |
| 21 | {product} demo at the palais | Demo space |
| 22 | 2027 plans for {company} events | Budget-cycle timing |
| 23 | before 2027 event budgets lock | Budget-cycle timing (use Sept to mid-Dec only) |
| 24 | gong li's festival, {company}? | Celebrity proof as a question (use sparingly; test) |
| 25 | {company} and ai cinema in cannes | Plain descriptive fallback |

### 2.4 Organizer (licence) track: 15 candidate subject lines

| # | Subject line | Angle |
|---|---|---|
| 1 | waiff india, december | Plain, internal-looking |
| 2 | the india rights to waiff | Ownership |
| 3 | owning waiff in india | Ownership |
| 4 | {company} and waiff india | Named company |
| 5 | an india edition for {company} | Named company |
| 6 | india's route to cannes 2027 | Winners feed the Cannes final |
| 7 | india's seat at the cannes final | Same, prestige |
| 8 | a cannes festival ip for {company} | New IP |
| 9 | {company}'s next live ip | New IP, for live-events groups |
| 10 | ai film festival, {city}, december | City and date |
| 11 | december in {city}? | Short question (test) |
| 12 | licence question for {company} | Plain |
| 13 | waiff india: who at {company}? | Referral ask (follow-up only) |
| 14 | after {their IP name} | Trigger: their existing festival or IP |
| 15 | india edition, before 15 october | Real validation deadline (use only if HQ confirms the date, section 9) |

---

## 3. Opening line and personalization

### 3.1 Evidence

- **Trigger or timeline openers beat problem openers.** Emails whose first sentence points at a specific, current event (launch, hire, funding, a post) replied at 10.01% versus 4.39% for problem-statement hooks, and booked meetings at 3.4x the rate ([Instantly 2026](https://instantly.ai/cold-email-benchmark-report-2026); [Digital Bloom summary](https://thedigitalbloom.com/learn/cold-outbound-reply-rate-benchmarks/)). (A)
- **Depth beats merge tags.** Emails referencing industry pain, recent triggers or company news reached 17% to 18% replies versus 7% to 9% for basic sends ([Hunter 2022 vs 2025](https://hunter.io/blog/cold-email-2022-vs-2025)); Woodpecker reports advanced personalization at up to 18% versus about 9% ([Woodpecker](https://woodpecker.co/blog/cold-email-statistics/)); Backlinko found body personalization lifted replies 32.7% ([Backlinko](https://backlinko.com/email-outreach-study)). (A)
- **Lead with their priorities, not your pitch.** Gong/30MPC: pitching in a cold email cut replies by up to 57%; leading with the buyer's priorities lifted replies 20%; social proof lifted them 41% ([30MPC](https://www.30mpc.com/newsletter/the-data-backed-cold-email-formula-the-exact-words-length)). (A)
- **Irrelevance is punished.** 73% of B2B buyers actively avoid suppliers who send irrelevant outreach ([Gartner](https://www.gartner.com/en/newsroom/press-releases/2026-03-09-gartner-sales-survey-finds-67-percent-of-b2b-buyers-prefer-a-rep-free-experience)). (A)
- **Speed on triggers.** Practitioner data suggests outreach within 24 to 48 hours of a trigger responds 3 to 5x better than a week later ([Autobound](https://www.autobound.ai/blog/sales-trigger-events-templates)). (C)
- **AI-sounding copy is a liability.** Vendor data claims AI-written cold emails are flagged as spam at 7.8% versus 2.9% for human-written ones; words like "impressed", "fascinated", "innovative approach" read as machine-made ([Phrasly](https://phrasly.ai/blog/ai-vs-human-cold-email-reply-rates/), [Mailbird](https://www.getmailbird.com/ai-generated-email-detection-spam-filter/)). (C, but consistent with what recipients report)

### 3.2 Real vs fake personalization

| Fake (drop it) | Real (use it) |
|---|---|
| "I've been following {Company}'s journey for a while now" | "{Product} 3.0 added {specific feature} on {date}; most of the AI shorts in our 2026 selection used tools doing exactly that." |
| "I hope this email finds you well" / "Greetings of the day" | "Your team ran {activation} at Cannes Lions in June." |
| "As a leader in AI..." | "You're hiring a Head of Creator Partnerships in Mumbai." |
| "Congratulations on your success" | "{Company}'s {IP name} sold out its Bengaluru leg last month." |
| Company-name mail merge in a generic sentence | One fact only a human who looked would know, tied to why WAiFF is relevant this quarter |

### 3.3 "Why you, why now" formula for the first two lines

Line 1 (why you, why now): a dated fact about them that WAiFF connects to.
Line 2 (bridge): one sentence on the WAiFF fact that makes that connection obvious.

Useful WAiFF "why now" hooks that are true today:

- Submissions for WAiFF Cannes 2027 opened 15 September 2026 and close 15 February 2027; finalists are selected 17 February to 7 March 2027 (WAiFF 2027 sponsor deck).
- Road to Cannes editions: Beijing (Sept 2026), Buenos Aires (Oct), Istanbul (Nov), London (Nov), then Abidjan, São Paulo, Seoul, Tokyo, Los Angeles before Cannes, 6 to 7 April 2027 ([WAiFF](https://worldaifilmfestival.com/), sponsor deck).
- Their own events: a model launch, a creator fund, a Cannes Lions activation (Adobe doubled its Cannes Lions spend in 2025 and made 2026 its largest yet, explicitly to court AI-first creators: [Adweek](https://www.adweek.com/brand-marketing/adobe-makes-its-biggest-cannes-lions-bet-yet-amid-race-to-court-creators/)).

---

## 4. The body

### 4.1 Length, reading level, format

| Rule | Evidence | Grade |
|---|---|---|
| First touch 50 to 90 words; 3 to 5 short sentences | Gong/30MPC: replies drop sharply past 100 words, best at 50 to 100 and 3 to 4 sentences ([30MPC](https://www.30mpc.com/newsletter/the-data-backed-cold-email-formula-the-exact-words-length)); Instantly top 10% senders keep emails under 80 words ([Instantly](https://instantly.ai/cold-email-benchmark-report-2026)); Lavender: 25 to 50 words ideal ([Lavender](https://lavender.ai/blog/best-length-cold-email)); Salesloft (3M emails): 25 to 50 words best ([Salesloft](https://www.salesloft.com/resources/blog/16-tips-to-double-your-reply-rates)) | A |
| Reading level grade 3 to 5 | Lavender: 3rd to 5th grade writing replied about 36% better than college level; short mobile-friendly emails get more replies ([Lavender](https://lavender.ai/blog/mobile-matters)) | B |
| Plain text, no HTML design, no images | Plain text reported 15% to 25% better replies for cold outreach; HTML adds spam signals ([Hunter](https://hunter.io/blog/is-html-harming-your-cold-email-deliverability/), [Puzzle Inbox](https://puzzleinbox.com/compare/plain-text-vs-html-cold-email/)) | B |
| No open tracking | Sequences without open tracking replied 68% more (7.4% vs 4.4%) ([Hunter](https://hunter.io/the-state-of-cold-email)) | A |
| Zero or one link, never shortened | One SaaS test: no-link variant beat linked by 26% in replies ([Mailpool](https://www.mailpool.ai/blog/cold-email-attachments-vs-links-whats-safe-in-2026-and-whats-not)); bit.ly style shorteners are flagged by filters ([AWeber](https://blog.aweber.com/email-deliverability/link-shorteners.htm)) | B |
| No attachments in touch 1 or 2 | Woodpecker: messages over 100KB landed in spam at major providers ([Woodpecker](https://woodpecker.co/blog/attachments-cold-email/)); sponsors "never open attachments" and trash anything that asks for money ([Sponsorship Collective](https://sponsorshipcollective.com/blog/five-reasons-sponsorship-prospects-ignore-e-mails/)) | A/B |
| One ask only | Every extra question splits attention; Lavender scores 1 to 2 questions as ideal, Gong's winning CTA is a single interest question | B |
| No ROI claims or big reach numbers | Gong (132,552 emails): ROI language cut meeting success 15% ([Gong](https://www.gong.io/blog/avoid-this-tempting-cold-email-mistake-at-all-costs)) | A |

### 4.2 The five-line structure (use for every first touch)

1. **Observation** (why you, why now): one dated fact about them.
2. **Relevance**: the one WAiFF fact that makes the fit obvious.
3. **Specific idea**: one concrete asset built for them (named award, tool challenge, jury seat, India slot), described in one sentence.
4. **Credibility**: one proof point, not five (Palais des Festivals, Gong Li as 2026 President, founder Marco Landi, 6,000+ submissions from 80+ countries).
5. **Low-friction ask**: an interest question (section 5).

Signature (plain text, 3 to 4 lines): name, "India Ambassador, World AI Film Festival (Cannes)", phone with WhatsApp, and at most one link (worldaifilmfestival.com). No logos, banners or social icons ([GMass](https://www.gmass.co/blog/cold-email-signature/)).

### 4.3 Describing WAiFF in 2 to 3 lines a CMO cares about

Sponsors "don't want to connect with your event. They want to connect with your target market" (Kim Skildum-Reid, [Power Sponsorship](https://powersponsorship.com/sponsor-send-me-a-sponsorship-proposal/)). Chris Baylis: "If you can't describe your project in one sentence and the benefit of being involved, you don't get money" ([Sponsorship Collective](https://sponsorshipcollective.com/blog/five-reasons-sponsorship-prospects-ignore-e-mails/)). So describe the audience and the business outcome, not the festival's greatness.

Template (audience, outcome, activation, measurement):

> WAiFF is the AI film festival at the Palais des Festivals in Cannes (6 to 7 April 2027), founded by former Apple president Marco Landi, with editions in 12+ cities feeding the Cannes final. Its audience is the filmmakers, studios and agencies choosing which AI video tools the industry adopts; 6,000+ films from 80+ countries were entered in 2026. A {Product} award would put your tool in front of them, with the entry data and jury screenings as the proof.

Short variants by buyer:

- **AI video or creative tool:** "Every film in competition is made with generative AI tools, so the entrants are your power users and your next enterprise customers."
- **Hardware, cloud, devices:** "The people rendering 6,000 AI films a year need compute, storage and screens; the Palais is where their work is judged."
- **Creator-economy platform:** "WAiFF has vertical micro-series and music-video categories, the formats your creators already publish."
- **Consumer brand:** "A festival where the audience sees the future of film first, in Cannes, two months before Cannes Lions."

### 4.4 Showing ROI without numbers that cannot be verified

The sponsor deck and proposal include figures such as "1B+ estimated cumulative visibility across Chinese media" and "30M+ target impressions in 2027". These are estimates or targets. Do not put them in cold email: they invite scepticism and Gong finds ROI claims reduce meetings 15%. Instead, **promise measurement, not outcomes**:

- IEG/ESP decision-maker research found sponsors rank rights-holder help with ROI/ROO reporting and post-event audits as the most important services ([TicketManager summary of IEG](https://www.ticketmanager.com/blog/digging-deeper-into-latest-sponsorship-trends-report/)); only 37% of marketers had a standardized way to measure sponsorship ROI and 78% said validating results had grown in importance ([ANA](https://www.ana.net/content/show/id/pr-2013-validate-initiatives)).
- So offer a measurement plan in one line: "We'd agree three measures up front (for example tool usage declared by entrants, creator sign-ups from a unique code, and on-site leads) and report them within 30 days."
- Verifiable proof you can use: Palais des Festivals venue; Gong Li as 2026 President and Claude Lelouch as honorary president ([Screen Daily](https://www.screendaily.com/news/seven-talking-points-from-the-world-ai-film-festival-in-cannes/5215914.article)); founder Marco Landi, former Apple president ([Palais des Festivals](https://en.palaisdesfestivals.com/offers/world-artificial-intelligence-film-festival-waiff-cannes-en-3686586/)); 6,000+ submissions from 80+ countries; 2.5h+ CCTV-6 live programme (sponsor deck). Keep to one per email.

### 4.5 Social proof and name-dropping

- Peer social proof lifted replies 41% in the Gong/30MPC dataset ([30MPC](https://www.30mpc.com/newsletter/the-data-backed-cold-email-formula-the-exact-words-length)). (A)
- Use the most relevant single name. For an AI video company, a peer tool that already holds a named award is the strongest proof (the 2027 deck lists a "CapCut Award" for vertical short drama). Confirm with HQ before naming any current partner, and never name a company that has not signed.
- Celebrity names (Gong Li, Claude Lelouch) establish legitimacy; they do not establish fit. Put them in line 4, never in line 1.
- Never imply a relationship that does not exist ("we're working with {competitor}") unless it is signed and public.

### 4.6 Example first touches (all under 90 words, no em dashes)

**Sponsor, AI video tool**

> Subject: {product} award in cannes
>
> Hi {First name},
>
> {Product} {version} shipped {feature} on {date}; it is already showing up in AI shorts.
>
> Every film at the World AI Film Festival (Palais des Festivals, Cannes, 6 to 7 April 2027) is made with generative AI tools, and 6,000+ were entered in 2026.
>
> Idea: a {Product} Award for the best film made with {Product}, presented at the Cannes final, with a report on how many entrants used it.
>
> Worth a look?
>
> Aditya Upadhyay
> India Ambassador, World AI Film Festival (Cannes)
> +91 {number} (WhatsApp)

(Before sending, confirm with HQ that the entry form can capture tools used. If not, offer a branded challenge instead.)

**Sponsor, consumer tech or device brand**

> Subject: {company} before cannes lions
>
> Hi {First name},
>
> {Company} took {venue or activation} at Cannes Lions this June.
>
> Two months earlier, 6 and 7 April 2027, the Palais des Festivals hosts the World AI Film Festival, founded by former Apple president Marco Landi, with editions in 12+ cities feeding the final.
>
> One idea: {Company} screens the finalists on {device} and presents the audience award.
>
> Open to seeing a one-page outline?
>
> Aditya

**Organizer licence, Indian media or live-events group**

> Subject: waiff india, december
>
> Dear {First name},
>
> {Company} has turned {their IP} into a fixture. An AI film festival is the adjacent format, and WAiFF's India rights are still open.
>
> WAiFF (Cannes, founded by former Apple president Marco Landi) is licensing one company to run its India edition this December. The licensee keeps 100% of local revenue: submissions, tickets, sponsors, workshops. India's top finalists go on to the Cannes Grand Finale.
>
> Would a 20-minute look be useful?
>
> Regards,
> Aditya Upadhyay
> India Ambassador, World AI Film Festival
> +91 {number} (WhatsApp)

(The 100% local revenue and exclusivity terms are from the WAiFF MoU template. "Top finalists go to Cannes" reflects the WAIFF Horizons section of the 2027 deck; confirm the exact wording with HQ.)

---

## 5. Call to action

| CTA type | Evidence | Use for |
|---|---|---|
| **Interest CTA** ("Worth a look?", "Open to seeing a one-page outline?", "Is this on your radar for 2027?") | Gong Labs, 304,174 emails: interest CTAs led to a meeting within 10 days 30% of the time, versus 15% for a specific-time ask and 13% for open-ended; about 2x more effective than asking for a meeting ([Gong](https://www.gong.io/blog/this-surprising-cold-email-cta-will-help-you-book-a-lot-more-meetings)) | Every first touch to executives |
| **Specific-time meeting ask** ("Tuesday 3pm CET?") | Same Gong data: 15% cold, but rises to 37% once interest exists | Only after they reply with interest |
| **Calendar link** | Practitioner data: bare scheduling links in a first touch read as automated and raise effort; a hard "book 30 minutes" ask is reported to halve executive responses ([Salesmotion](https://salesmotion.io/blog/cold-email-executives-reply-rates)). | Never in touch 1; optional as a fallback after offering two times |
| **Offer CTA** ("Can I send the one-page idea?") | Hunter: decision-makers prefer "Can I send more info?" and "Open to learning more?" over an upfront meeting ([Hunter](https://hunter.io/the-state-of-cold-email)); RAIN Group: 71% of buyers want to hear from sellers when looking for new ideas ([RAIN Group](https://www.rainsalestraining.com/sales-research/sales-prospecting-research)) | Senior execs and founders |

For senior executives, the order is: earn a "yes, send it" with an interest or offer CTA, send a one-page idea (not the deck), then propose two specific times in their time zone. In India, also offer a call or WhatsApp; three Indian respondents in your data asked for a number before anything else.

---

## 6. Follow-ups

### 6.1 How many, how far apart, and where replies come from

| Finding | Source (grade) |
|---|---|
| 58% of replies come from step 1; 42% from follow-ups | [Instantly 2026](https://instantly.ai/cold-email-benchmark-report-2026) (A) |
| First follow-up has the highest single-step reply rate (8.4%); 4th about 3.0%; 5th 3.8% in another cut; 4+ follow-ups raise unsubscribes and spam complaints more than 3x | [Belkins](https://belkins.io/blog/sales-follow-up-statistics) (A) |
| One follow-up lifts replies 65.8% (Backlinko); about 22% more prospects convert with one follow-up (Woodpecker) | [Backlinko](https://backlinko.com/email-outreach-study), [Woodpecker](https://woodpecker.co/blog/follow-up-statistics/) (A) |
| Each step is weaker: median email 4 is about half of email 1; emails 5 and 6 about 30% | [Woodpecker](https://woodpecker.co/blog/cold-email-statistics/) (A) |
| 4 to 7 total steps is the platform sweet spot; top performers use 4 to 7 steps under 80 words | [Instantly 2026](https://instantly.ai/cold-email-benchmark-report-2026) (A) |
| It takes about 8 touches across channels to get a first meeting | [RAIN Group](https://www.rainsalestraining.com/blog/how-many-touchpoints-does-it-take-to-make-a-sale) (B) |
| "I never heard back" raises replies but cuts meetings 14%; "following up on my previous note" cuts meetings 5% | [Gong](https://www.gong.io/blog/7-tips-for-writing-the-perfect-follow-up-sales-email-according-to-science) (A) |
| Waiting about 3 days before the first follow-up beats next-day bumps | [Woodpecker summary](https://woodpecker.co/blog/how-to-send-a-follow-up-email-after-no-response/) (B) |

### 6.2 Recommended cadence for WAiFF (4 emails plus LinkedIn, about 3 weeks)

| Day | Channel | Content that must be new | Words |
|---|---|---|---|
| 0 | Email 1 | Five-line email, one idea, interest CTA | 50 to 90 |
| 1 to 2 | LinkedIn | Connection request (blank, or note if top-tier) | 0 to 200 chars |
| 3 to 4 | Email 2, same thread | A second, different concrete idea or a peer example ("Runway built its own AI film festival and took it to IMAX screens; a named award at Cannes gets the same halo without running a festival") | 30 to 60 |
| 7 to 9 | Email 3, same thread or a new thread to a second stakeholder | A real timing fact (submissions close 15 Feb 2027; finalists selected 17 Feb to 7 Mar 2027; Indian FY planning in Jan to Mar) or a short measurement plan | 30 to 60 |
| 10 to 12 | LinkedIn message (if accepted) | Short, no pitch, reference the idea as a question | under 300 chars |
| 16 to 21 | Email 4, breakup | Close the loop politely, offer a referral path or a later date | 25 to 50 |

For the organizer track, compress to about 12 days because December is close (section 9), and add a phone call or WhatsApp after the first reply.

### 6.3 What each follow-up should add

- **New value, not a bump.** Banned openers: "Following up on the note below", "just checking in", "circling back", "did you get a chance to take a look", "bumping this". These teach the reader your emails contain nothing new.
- **A new angle.** Rotate: named award, then branded challenge, then jury or judging seat, then global editions add-on.
- **A specific activation idea** in one sentence, with their product in it.
- **A deadline only if real.** Real deadlines available now: Cannes submissions window closes 15 February 2027; finalist selection 17 February to 7 March 2027; WAiFF must validate a licensee's dates, venue and programme at least 60 days before the event (MoU Article 3), so a mid-December India edition needs validation by mid-October. Never invent "only two slots left".
- **The breakup email** (Chris Voss "no-oriented" framing works on silence once there has been some exchange; do not use it as an opener: [Voss](https://www.linkedin.com/posts/christophervoss_why-you-need-to-use-no-oriented-questions-activity-7108917462938652672-WrCp)). Example: "Should I close the loop on a {Product} award for Cannes? If someone else owns festival partnerships, a name would help, and I won't follow up again." Breakups on cold lists typically draw 5% to 10% ([B2B Sales Training](https://b2bsalestraining.org/sales-breakup-email)). (C)

### 6.4 Threading versus a new subject

- Thread follow-ups 2 and 3 as replies in the same thread: it keeps context and looks like a conversation ([ReviewMyEmails](https://reviewmyemails.com/emailalmanac/cold-outreach-and-sales/cold-email-sequencing-follow-up/follow-ups-same-thread-vs-new)). (B)
- Start a new thread with a new subject when you change the angle substantially, switch to a different stakeholder, or restart after 3+ weeks.
- Never forward the original email to a new person without rewriting it for their role.

---

## 7. Multi-threading: several people at one company

### 7.1 Evidence

- Hunter (25,138 campaigns, about 6.3M companies): companies where two or more people were contacted replied 3.35% versus 1.61% for one person (2.1x); contacting different departments beat the same department (2.30% vs 1.65%); gains fade after the third person ([Hunter](https://hunter.io/blog/should-you-email-more-than-one-person-per-company)). (A)
- Backlinko: messages to several contacts at a site got 93% more responses, with diminishing returns at 5+ ([Backlinko](https://backlinko.com/email-outreach-study)). (A)
- Hunter also found that pairing a named contact with a generic inbox worked: of companies that replied, the generic inbox alone answered 43% of the time. The generic inbox must be the right one (partnerships@, marketing@, events@), not press@ or support@.

### 7.2 CC vs BCC vs separate emails

| Method | Verdict | Why |
|---|---|---|
| **Separate, individually written emails**, staggered 2 to 3 days, each with a role-specific angle | **Do this** | Matches the data; each person owns their own reply; no mass-mail signal |
| CC two stakeholders on a first touch | Avoid | Reads as mass mail, diffuses ownership ("I thought she would answer"), and multiple recipients on a cold message are a filter signal ([Kondo](https://www.trykondo.com/blog/cold-email-deliverability)) |
| **BCC** anyone, including a press inbox | **Stop** | The To recipient cannot see it, so it adds no social proof; the BCC'd person sees they were blind-copied, which reads as a blast; each BCC counts against Gmail's 500-recipient daily cap; reply-all accidents expose the list. It is odd, not clever |
| Email the press@ or media@ inbox about sponsorship | Stop | Press desks handle editorial requests. Your own data: Qatar Airways "only respond to editorial", Synthesia's press office auto-replied, Anthropic's reply came from its external communications agency, and press@epidemicsound.com, media@zerodha.com and APJC_PR@cisco.com bounced |

### 7.3 What to do instead

1. Map 2 to 3 named roles per target company: brand or sponsorship lead (budget), creator or community marketing lead (activation), and events or partnerships lead (execution). For startups, the founder or CMO.
2. Write a different opening line for each role, same core idea.
3. Send to the budget holder first; the second person 2 to 3 days later; add the right generic inbox (partnerships@, events@) only as the third thread.
4. If a support desk replies, ask one question: "Who handles brand partnerships for festivals and events?" Then write fresh to that person, referencing that the support team pointed you to them.
5. Use press@ only for a genuine media partnership (coverage, content), and say so in the first line.

---

## 8. Deliverability for a personal Gmail account

### 8.1 Hard limits and rules

| Rule | Detail | Source |
|---|---|---|
| Daily cap | Personal Gmail: up to 500 recipients per rolling 24 hours, counting To, CC and BCC | [Smartlead summary](https://www.smartlead.ai/blog/gmail-sending-limits) |
| Practical cold ceiling | 20 to 40 new cold emails per day from one inbox, spread across the day; ramp from 10 to 20 per day; never jump from 10 to 200 | [Mailforge](https://www.mailforge.ai/blog/how-many-cold-emails-to-send-per-day), [Mailmeteor](https://mailmeteor.com/blog/gmail-blocked-my-account) |
| Spam complaints | Google asks senders to stay under 0.1% user-reported spam and never reach 0.3% | [Google sender guidelines FAQ](https://support.google.com/mail/answer/14229414?hl=en) |
| Bounces | Keep under 2% (target under 1%); your campaign ran about 6% | [Puzzle Inbox](https://puzzleinbox.com/compare/cold-email-bounce-rate-threshold) |
| Bursts | Sending many emails within minutes is a structural anomaly for Gmail's abuse systems; space sends at least 2 to 5 minutes apart or use Gmail's schedule-send | [Mailmeteor](https://mailmeteor.com/blog/gmail-blocked-my-account) |
| Content | Plain text, no tracking pixel, 0 to 1 link, no shortener, no attachment, no image signature, no ALL CAPS, no stacked promotional phrases | Sections 2 and 4 |
| Reply-to | Reply-To must equal the sending address; never route replies elsewhere | Standard practice |
| Verification | Verify every address (Hunter, NeverBounce, ZeroBounce or similar) within 30 days of sending; treat catch-all domains as risky and send them last | [Bulk Email Checker](https://bulkemailchecker.com/blog/how-to-write-cold-emails-that-dont-bounce/) |
| Guessed addresses | Do not send to pattern-guessed addresses at big corporates without verification; 5 of your threads were blocked outright by corporate gateways (HP, Lenovo, ADATA, PNY), which also dents your reputation | Your export |

### 8.2 Would a branded domain help? Yes, materially.

- Hunter's 2025 data (31M emails): sending from a custom domain produced a 108% higher reply rate than freemail (5.2% vs 2.5%) ([Hunter](https://hunter.io/the-state-of-cold-email)). (A)
- The trust effect matters even more for you: a sponsorship pitch for a Cannes festival from a gmail.com address looks unofficial, and recipients cannot verify you are WAiFF's representative.

Options, best first:

1. **Ask WAiFF HQ (Studio Laffitte / Institut EuropIA) for an official mailbox** such as aditya@worldaifilmfestival.com or india@worldaifilmfestival.com. It inherits an established domain, needs little warm-up, and proves authority. This is the single highest-leverage fix.
2. If HQ declines, register a domain only with HQ's written permission (for example an india-specific domain), set up Google Workspace with SPF, DKIM and DMARC, and warm it 2 to 4 weeks before cold sending ([Warmy](https://www.warmy.io/blog/how-long-to-warm-up-new-domains-before-starting-to-send-campaigns/)). Do not register a lookalike domain without permission: that would present as impersonating the organisation.
3. Until then, keep Gmail but cut volume to 20 to 30 researched emails per day, weekdays only, and let the account recover from the 13 September spike.

### 8.3 Compliance notes (short)

- US recipients: CAN-SPAM applies to B2B commercial email; include a physical postal address and a working opt-out, honoured within 10 business days ([FTC](https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business)).
- France and EU: B2B prospecting to professional addresses is allowed on legitimate interest when relevant to the person's role, with an easy opt-out in every message ([Kahlem Advisory on CNIL](https://www.kahlemadvisory.com/articles/cold-email-france-b2b/)).
- India: the DPDP Act treats work email as personal data; full compliance obligations phase in through 2027 and enforcement on B2B email has been light so far, but keep a clear opt-out line and honour it ([DLA Piper](https://www.dlapiperdataprotection.com/index.html?t=electronic-marketing&c=IN)).
- A plain one-line opt-out ("If this isn't relevant, reply 'no' and I won't write again") satisfies the spirit everywhere and lowers spam reports.

---

## 9. Sponsorship-specific playbook

### 9.1 How brand and partnership leads evaluate a sponsorship

In the order they typically screen (Power Sponsorship, Sponsorship Collective, IEG/ANA):

1. **Audience fit.** "Does this reach the audience we want, at a price that makes commercial sense, from an organizer we trust to deliver?" ([Power Sponsorship](https://powersponsorship.com/how-do-sponsors-evaluate-sponsorship-proposals/)). For WAiFF the honest audience claim is AI filmmakers, studios, agencies, institutions and media, not "the public".
2. **Business objective fit.** Rejections usually come from poor audience fit, weak ROI framing, generic packages, unclear activation ideas, bad timing or no strategic alignment ([Sponsorship Collective](https://sponsorshipcollective.com/blog/why-sponsors-say-no/)).
3. **Activation rights.** Can they do something, not just show a logo: demo space, a session, a challenge, a jury seat. IEG found TV logo exposure among the lowest-valued metrics (52%) ([TicketManager on IEG](https://www.ticketmanager.com/blog/digging-deeper-into-latest-sponsorship-trends-report/)).
4. **Content rights.** Can they use films, finalists, footage and the WAiFF marks in their own channels after the event. Clarify before the call what HQ allows.
5. **Exclusivity.** Category protection is the lever that justifies top prices; practitioners price it at a 20% to 40% premium in contested categories ([Ticket Fairy](https://www.ticketfairy.com/blog/category-exclusivity-without-handcuffs-precision-in-festival-sponsorship-deals)). (C)
6. **Measurement.** Sponsors rank rights-holder help with ROI reporting as the most important service ([TicketManager on IEG](https://www.ticketmanager.com/blog/digging-deeper-into-latest-sponsorship-trends-report/)).
7. **Leverage budget.** Sponsors historically spent about USD 1.90 to 2.20 activating for every USD 1 of rights fee, though IEG now warns against fixed ratios ([IEG](https://www.linkedin.com/pulse/activation-ratios-dead-ieg)). A USD 100k rights fee may imply USD 100k to 200k of total budget, which is why they need lead time.

### 9.2 What makes them say yes to a first call

- A specific idea built around their product and objective, not a menu of tiers. Skildum-Reid: research first so the approach shows you care about their brand needs "which almost nobody does" ([Power Sponsorship](https://powersponsorship.com/dont-send-a-sponsorship-proposal/)).
- A short, clearly bounded ask ("20 minutes to test whether this fits your 2027 creator plan").
- Credibility that can be checked in 10 seconds (official domain, WAiFF site, Palais listing).
- Chris Baylis: the goal of the email is a phone call, not a sale; no package, no attachment ([Sponsorship Collective](https://sponsorshipcollective.com/blog/five-reasons-sponsorship-prospects-ignore-e-mails/)). On the call, get five answers: their sales goal and roadblock, the metric they're graded on, what they've tried, the action they want customers to take, and budget range ([Sponsorship Collective](https://sponsorshipcollective.com/blog/5-discovery-questions-that-get-a-sponsor-to-say-yes/)).

### 9.3 Why sending the deck cold hurts

- Attachments over about 100KB hit spam folders at major providers ([Woodpecker](https://woodpecker.co/blog/attachments-cold-email/)); sponsors report they never open attachments ([Sponsorship Collective](https://sponsorshipcollective.com/blog/five-reasons-sponsorship-prospects-ignore-e-mails/)).
- A deck shows prices and tiers before value is established; Gong finds pitching in cold email cuts replies up to 57%.
- "Just send me a proposal" is usually a polite brush-off; the right response is to ask two or three questions about their objectives first ([Power Sponsorship](https://powersponsorship.com/sponsor-send-me-a-sponsorship-proposal/)).
- Instead: after a "yes", send a one-page, plain-language idea written for them (their objective, the asset, how it would be measured), then walk through the deck live.

### 9.4 Budget cycles and timing

- **Now is the window.** Chris Baylis: from about 15 September to 15 December, companies set next year's budgets and a discovery call is worth "up to 5x" a call at other times; late December is a wash ([Sponsorship Collective](https://sponsorshipcollective.com/blog/best-time-of-year-for-sponsorship/)). (B)
- **Lead time is the real constraint.** Kim Skildum-Reid: there is no magic month, but long lead times win because sponsors need months to plan leverage ([Power Sponsorship](https://powersponsorship.com/what-time-of-year-should-i-seek-sponsorship/)). Cannes 2027 is about 6.5 months away, so a sponsor must decide by roughly December or January to activate properly.
- **Calendar-year companies** (most US and European tech): 2027 budgets are being finalised October to December 2026. Pitch "2027 plans", not "this year".
- **Indian companies** run April to March financial years; budgets for FY2027-28 are approved around January to March 2027 ([Bajaj Finserv](https://www.bajajfinserv.in/what-is-fiscal-year-in-india)). Cannes on 6 to 7 April 2027 falls in the first week of FY2027-28, so Indian sponsors need to be in the plan being drafted now.
- **Cannes season.** Tech and creator brands already budget for Cannes Lions in June (Adobe doubled its Cannes Lions spend in 2025 and made 2026 its largest yet: [Adweek](https://www.adweek.com/brand-marketing/adobe-makes-its-biggest-cannes-lions-bet-yet-amid-race-to-court-creators/)). Position WAiFF as the AI-creator moment two months earlier, in the same city, drawing on the same budget line.
- **Tech is spending.** SponsorUnited reports technology as the leading sponsorship category in F1 (USD 769M, +41% year on year) and AI companies using sponsorship for enterprise access ([SponsorUnited](https://www.sponsorunited.com/reports/2025-markets-report), [Yahoo Sports](https://sports.yahoo.com/sectors/technology/articles/ai-companies-spending-big-on-business-backed-sponsorships39-093000730.html)).

### 9.5 The two strongest angles for WAiFF

**Named award or named competition.** WAiFF's own 2027 deck includes award naming at the EUR 100,000 tier and a named competition at the EUR 400,000 tier, and already lists a "CapCut Award" for vertical short drama. Precedents buyers recognise: the LVMH Innovation Award at VivaTech ([LVMH](https://www.lvmh.com/en/lvmh-x-vivatech-2026)); Adobe's 15-year Sundance presence and Canon's filmmaker space ([Marketing Brew](https://www.marketingbrew.com/stories/2026/02/03/brands-film-festivals-sundance-adobe-acura-canon)); Runway running its own AI Film Festival with Tribeca and IMAX screenings ([Runway](https://runwayml.com/news/runway-imax-aiff-presentation)); Tribeca and OpenAI's year-long AI shorts programme ([Tribeca](https://tribecafilm.com/press-center/press-releases/tribeca-studios-and-openai-launch-ear-long-collaboration-to-support-independent-filmmakers-in-creating-ai-integrated-short-films)). Pitch line: "Runway built a festival to get this halo; a named award at WAiFF gets it without running one."

**Category exclusivity.** "One AI video partner at Cannes" is a concrete, scarce asset. It is only credible if HQ agrees to hold the category; confirm before offering it. Reported precedent for "official tool" status: Adobe Firefly as the approved generative AI tool in a Cannes Lions young-creatives competition (see Adobe's Cannes coverage, [Adobe newsroom](https://news.adobe.com/news/2025/06/cannes-lions-2025-adobe-unites-creativity)). (C: verify before quoting)

### 9.6 Pricing discipline

Never price in cold email or on LinkedIn. When asked, send the official EUR tiers (the current deck lists EUR 50,000 / 100,000 / 200,000 / 400,000 plus international add-ons on request), not the USD figures in older notes, and only after the discovery call.

---

## 10. Organizer licence playbook (India edition, December 2026)

### 10.1 The business case in five lines

1. **Revenue lines the licensee keeps (100% under MoU Article 7):** submission fees (Cannes charges EUR 15 / 30 / 60 per entry by phase, per the 2027 rules), ticketing, local sponsorship packages, hackathons and workshops, broadcast or streaming rights, branded content. Present as a formula with their assumptions (entries x fee + tickets + sponsors), never as a promised number.
2. **Market proof:** India's organised live events segment grew 44% in 2025 to about USD 1.55 billion, projected from INR 145 billion to INR 196 billion by 2028 ([FICCI-EY](https://www.ey.com/en_in/newsroom/2026/03/india-s-media-and-entertainment-sector-grew-9-percent-to-inr-2-point-78-trillion-in-2025-driven-by-digital-and-live-experiences-ficci-ey-report)). 99% of Indian creators surveyed by Adobe use creative generative AI ([Adobe, Aug 2026](https://news.adobe.com/en/apac/news/2026/08/adobe-india-creator-survey-toolkit-2026)). CNBC: India's filmmakers are embracing generative AI faster than Hollywood ([CNBC](https://www.cnbc.com/2026/06/11/how-indian-filmmakers-are-using-generative-ai.html)).
3. **Positioning, stated accurately:** India already has AI film festival activity (IFFI with LTIMindtree ran "India's first AI Film Festival" in Goa in November 2025 with 68 entries from 18 countries: [PIB](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2194363&reg=48&lang=2); Invideo hosted the India AI Film Festival in February 2026: [IAFF](https://indiafilmfestival.ai/)). So do **not** claim "India's first AI film festival". The defensible claim is: "the India edition of the global AI film festival network whose winners compete in Cannes", with territorial exclusivity (MoU Article 2).
4. **Brand and ecosystem:** association with Cannes, Gong Li, Marco Landi; access to WAiFF's international network, delegations and the Cannes Grand Finale (WAIFF Horizons); the Mumbai film-festival calendar has a gap after MAMI paused its 2025 edition ([Variety](https://variety.com/2025/film/festivals/mumbai-film-festival-hiatus-1236465675/)).
5. **Speed to December:** WAiFF supplies brand guidelines and official materials within 15 days of signature (MoU Article 5) plus categories, rules and jury standards; the licensee supplies venue, local marketing and operations.

**Analogues that make licensing feel normal to an Indian board:** BookMyShow co-produces Lollapalooza India under a long-term arrangement with C3 Presents (Live Nation), now in its 5th edition ([Live Nation](https://www.livenationentertainment.com/2022/07/lollapalooza-expands-global-reach-with-the-addition-of-lollapalooza-india/), [Pollstar](https://news.pollstar.com/2026/04/03/how-bookmyshow-is-helping-turn-india-into-a-global-concert-market/)); NODWIN Gaming bought Comic Con India at a Rs 55 crore valuation because live IPs carry sponsorship, ticketing, merchandise and media-rights revenue ([Campaign India](https://www.campaignindia.in/article/nodwin-gaming-acquires-comic-con-india/493967), [Inc42](https://inc42.com/features/decoding-nazara-backed-nodwin-gamings-success-story-amid-the-volatile-indian-esports-arena/)); ReedPop licenses Comic Con editions to local operators in Singapore, Seoul, South Africa and Vienna ([Comics Beat](https://www.comicsbeat.com/reedpop-international-comic-con-presence-report/)); TEDx runs on a licence with strict brand and sponsor rules ([TED](https://www.ted.com/participate/organize-a-local-tedx-event/before-you-start/tedx-rules)). (Some of these companies are already on your contact or exclusion lists; use them as examples, not targets.)

### 10.2 Who decides inside a large Indian company

Decisions in Indian corporates are concentrated at the top; middle managers rarely commit to a new line without senior endorsement ([Global Business Culture](https://www.globalbusinessculture.com/countries/resources/country-profiles/india-business-culture/)). (B) Practical map:

| Company type | Economic buyer | Champion to reach first |
|---|---|---|
| Media or entertainment group | Group CEO or CEO of the live events / IP business | Head of IP, Head of Live Events, Chief Strategy Officer |
| Live-events or ticketing company | Founder-CEO or COO | Head of IP / Festivals, Head of Partnerships |
| Conglomerate (brand-led bet) | Chairman's office or Group CEO | Group CMO / Chief Brand Officer, Group Strategy or New Ventures |
| Tech or education company | Founder-CEO | CMO or Head of Community / Creator programmes |
| Events multinational (India arm) | Country MD | Head of New Launches / Portfolio |

Do not start with company secretaries, investor relations or media-relations inboxes (your data shows MRF's company-secretary route produced a polite no, and Mahindra's media-relations address bounced).

### 10.3 Objections to expect, and a one-line pre-emption for each

| Objection | One line to pre-empt it (only if true; confirm with HQ) |
|---|---|
| Time: "December is 10 weeks away" | "Year one can be a one-day, one-venue format; WAiFF supplies rules, categories, jury standards and the brand kit within 15 days of signing." |
| Hard deadline | "WAiFF validates dates, venue and programme 60 days ahead, so a mid-December date needs sign-off by mid-October; a January date also works if India's finalists are chosen before Cannes finalist selection starts on 17 February." |
| Cost | "The licence fee is the only payment to WAiFF; you keep 100% of local revenue: submissions, tickets, sponsors and workshops." |
| Risk | "WAiFF's 2026 edition drew 6,000+ submissions from 80+ countries; the licence gives you exclusive rights in India for the term." |
| Brand control | "You run it under WAiFF's brand guidelines, and you own every local commercial relationship." (Confirm co-branding rules, e.g. "WAiFF India presented by {Company}", with HQ.) |
| "Why us?" | "{Company} already runs {IP / audience}; this adds a Cannes-linked IP your sponsors can buy into." |
| "Send us the deck" | Send a one-page business case with their numbers after a 20-minute call, not the full agreement. |

---

## 11. India-specific norms and timing

### 11.1 Writing to Indian CXOs

- **Formality:** in traditional groups and conglomerates, open "Dear Mr {Surname}" or "Dear {First name}" (safe middle ground); in startups and tech, "Hi {First name}" is normal. Avoid "Hey" to seniors ([Commisceo](https://www.commisceo-global.com/blog/the-essential-guide-to-indian-business-etiquette)). (B)
- **Relationship first:** warm introductions carry unusual weight in India; mine LinkedIn for second-degree paths (WAiFF HQ, festival alumni, investors) and ask for a one-line intro before cold emailing the chairman's office.
- **Phone and WhatsApp:** over 70% of Indians say they prefer messaging a business to email or calls (consumer survey, [BW Marketing World](https://www.bwmarketingworld.com/article/indians-want-to-connect-with-a-business-the-same-way-they-chat-with-family-friends-report-449606)); three Indian replies in your data asked for a number. Put a mobile with WhatsApp in every signature; move to a call or WhatsApp once they reply, not before.
- **Indirect "no":** "Let me check", "it may be difficult" often mean no; ask a direct, easy question to confirm ("Should I close this for now?").
- **Avoid Indian-English stock phrases that read as templated to global and Indian execs alike:** "I hope this email finds you well", "Greetings of the day", "Kindly", "revert", "do the needful", "Respected Sir".
- **Festival calendar:** Navratri starts 11 October, Dussehra 20 October, Diwali 8 November 2026, with the festive window running about 11 October to 11 November ([Tribune](https://www.tribuneindia.com/news/business/diwali-2026-is-late-26-things-every-clothing-business-must-fix-now)). Indian marketing teams are flat out on festive campaigns then. Push India first touches in the next two weeks (by about 9 October), pause cold India sends during Diwali week (6 to 11 November), and resume from 11 November.

### 11.2 Writing to global execs from an Indian sender

- Credibility cues do the work: official domain (section 8.2), a verifiable title, one link to WAiFF, and a LinkedIn profile whose headline matches the email ("India Ambassador, World AI Film Festival (Cannes)").
- Propose times in their time zone, not yours ("Tue or Wed, 10:00 CET?"). "I'm on Indian Standard Time but can work around your hours" shifts work to them.
- Keep to plain international English; one idea; no flattery.

### 11.3 Send-time table (send in the recipient's 8:00 to 11:00, Tue to Thu; Belkins found 8:00 to 12:00 had the highest reply and meeting rates and Wed/Thu the best days: [Belkins](https://belkins.io/blog/best-time-to-send-email); Salesloft: avoid Friday afternoon and weekends)

| Recipient | Their 8:00 to 11:00 equals (IST) until late Oct / early Nov | After clocks change (Europe 25 Oct, US 1 Nov 2026) |
|---|---|---|
| India | 9:00 to 11:30 IST (use this) | Same |
| UK | 12:30 to 15:30 IST | 13:30 to 16:30 IST |
| France, Germany (CET) | 11:30 to 14:30 IST | 12:30 to 15:30 IST |
| US East | 17:30 to 20:30 IST | 18:30 to 21:30 IST |
| US West | 20:30 to 23:30 IST | 21:30 to 00:30 IST |
| China, Singapore | 5:30 to 8:30 IST | Same |
| Japan, Korea | 4:30 to 7:30 IST | Same |

Use Gmail's schedule-send so emails arrive in their morning without you sending in bursts.

---

## 12. LinkedIn

### 12.1 Connection requests

| Question | Evidence | Rule |
|---|---|---|
| Note or no note? | Belkins (20M+ attempts via Expandi): acceptance 26.42% with a personalized note vs 26.37% without, but post-accept reply rate 9.36% vs 5.44% with a note (72% lift) ([Belkins](https://belkins.io/blog/linkedin-outreach-study)). Other datasets found blank requests accepted more often ([Botdog](https://www.botdog.co/blog-posts/linkedin-acceptance-rates)) | Note for top-tier targets; blank for the rest |
| Free-account limits | Free members get about 200 characters and a limited number of personalized notes per month (reported as 5); Premium has 300 characters and no monthly note cap ([LinkedIn Help](https://www.linkedin.com/help/linkedin/answer/a563153), [Taplio](https://taplio.com/blog/linkedin-connection-request-limit)) | Consider Premium for the campaign period, or reserve notes for the 5 most valuable targets |
| Volume | About 100 invitations per rolling week; 15 to 25 per day for a warmed account ([Expandi](https://expandi.io/blog/linkedin-connections-limit/)) | Stay under 20 per day |
| Timing | Requests sent 6:00 to 11:00 accept at about 32% vs about 24% in the evening ([Expandi H2 2026](https://expandi.io/state-of-linkedin-outreach-h2-2026/)) | Send in their morning |
| Note length | Messages of 150 to 200 characters hit peak reply rates ([Expandi](https://expandi.io/blog/linkedin-outreach-benchmarks-2026/)) | 1 to 2 sentences |

Connection note template (under 200 characters, no pitch): "Hi {First name}, saw {specific: their Cannes Lions session / launch}. I work on the World AI Film Festival in Cannes and follow {Company}'s work in AI video. Would be glad to connect."

### 12.2 After they accept

- Message within 24 to 48 hours; replies fall sharply after 72 hours ([Kondo](https://www.trykondo.com/blog/linkedin-response-rate-tips)). (C)
- No pitch in message 1. The pitch-slap (pitch immediately after connecting) gets around 1% replies in practitioner reports ([Kondo](https://www.trykondo.com/blog/linkedin-pitch-alternatives)). (C)
- Expandi: the second message is the most effective per recipient (8.8%), and three messages is the sweet spot (9.8%); a fourth drops to 7.9% and five or more is worse than one ([Expandi](https://expandi.io/blog/linkedin-outreach-benchmarks-2026/)). (A) So: message 1 opens the door, message 2 carries the idea, message 3 closes the loop.
- LinkedIn's own data: InMails under 400 characters get 22% higher response than average ([LinkedIn](https://www.linkedin.com/business/talent/blog/talent-strategy/these-inmails-get-best-response-rates)). (A) Keep every message under 400 characters.
- Coordinated LinkedIn plus email outperforms either alone (vendor data: 25% higher replies, 40% more meetings for unified sequences) ([Overloop](https://overloop.com/blog/linkedin-vs-email-which-performs-better-for-b2b-outreach)). (B)

### 12.3 Three post-accept frameworks

**A. Sponsor executive (CMO, Head of Brand Partnerships, Head of Creator Marketing)**

Message 1 (day 0 to 1):
> Thanks for connecting, {First name}. Your team's {specific activation or launch} was one of the few I saw aimed squarely at AI filmmakers. Are AI creators a 2027 priority for {Company}, or more of a side bet?

Message 2 (day 3 to 5, after any reply or none):
> One idea I'd value your view on: a {Product} Award at the World AI Film Festival in Cannes (6 to 7 April), judged on films made with {Product}. Worth a one-page outline?

Message 3 (day 10 to 12, only if silent):
> No worries if the timing's off. If someone else owns festival partnerships at {Company}, a name would help, and I'll leave it there.

**B. Organizer executive (CEO of live events / IP, Head of IP, Chief Strategy Officer, Indian company)**

Message 1:
> Thank you for connecting, {First name}. {Their IP} is a model for how Indian live IP scales. Is new IP something {Company} is looking at for 2027?

Message 2:
> The reason I ask: WAiFF (Cannes, founded by former Apple president Marco Landi) is licensing one company to run its India edition this December, keeping all local revenue. Would a 20-minute look be useful? Happy to call or WhatsApp.

Message 3:
> Understood if this isn't a fit now. WAiFF needs to confirm India's dates by mid-October, so I'll close this out unless you'd like the one-page business case.

(Only use the mid-October line once HQ confirms the validation date.)

**C. Senior founder or CEO (AI startup, creator platform)**

Message 1:
> Thanks for connecting, {First name}. {Specific: their recent post, launch, or funding}, congratulations. Curious: do you see AI film festivals as useful for {Company}, or noise?

Message 2:
> Asking because WAiFF in Cannes is open to one named award per category for 2027, and {Product} fits {category}. Open to a two-line summary?

Message 3:
> Last note from me on this. If it's a "not now", I'll check back after your next launch.

Move to a call only after a positive reply: "Great. Would Tue 10:00 or Wed 16:00 {their time zone} work for 20 minutes? Or I can send the outline first."

---

## 13. Pre-send QA checklist (every email must pass all 24)

**Targeting**
1. The recipient is a named person who owns budget, activation or new IP, or a partnerships/events inbox; not press@, media@, support@, care@, info@, reservations@ or the company secretary.
2. The address is verified within the last 30 days (not guessed); catch-alls are flagged.
3. The company is not on EXCLUSIONS.txt (existing partners, already contacted, already in list).
4. No more than 3 people at this company are in the sequence, each with a separate, role-specific email.

**Subject line**
5. 2 to 5 words, lowercase or sentence case, under about 40 characters.
6. No banned words (opportunity, sponsorship, partnership opportunity, invitation, exclusive, global stage, collaboration, proposal, quick question, following up), no price, no "X x WAiFF" formula, no fake Re: or Fwd:.
7. It matches the email's first line.

**Body**
8. First line is a dated, specific fact about them (why you, why now), not "I hope this email finds you well", "Greetings of the day", "Hi team" or "I've been following your journey".
9. One idea, built around their product or IP, stated in one sentence.
10. One credibility point only (Palais, Gong Li, Marco Landi, or 6,000+ submissions from 80+ countries).
11. Every number matches WAiFF's official materials (use 80+ countries, not 100+; 6,000+ submissions) and no estimate or target (1B+ visibility, 30M+ impressions) appears.
12. No price, tier name or "package".
13. 50 to 90 words for a first touch; 30 to 60 for follow-ups; sentences under about 20 words; reading level around grade 5.
14. Exactly one ask, and it is an interest or offer question ("Worth a look?", "Open to a one-page outline?"), not a meeting request or calendar link.
15. Zero or one link, full URL, no shortener; no attachment; no images.
16. No em dashes or en dashes anywhere; no ALL CAPS; no exclamation marks; no emojis.
17. Reads as written by a human: no "impressed", "fascinated", "innovative approach", "synergy", "leverage", "delighted to".

**Signature and compliance**
18. Plain-text signature: name, "India Ambassador, World AI Film Festival (Cannes)", mobile with WhatsApp, one link.
19. A one-line opt-out ("If this isn't relevant, reply 'no' and I won't write again"); a postal address for US recipients.

**Sending**
20. Sent from the official WAiFF mailbox once available; otherwise from Gmail within 20 to 40 cold emails per day, weekdays only.
21. Scheduled for 8:00 to 11:00 recipient-local time, Tuesday to Thursday preferred; no weekend sends; spaced at least a few minutes apart.
22. No CC, no BCC.
23. Open tracking off.
24. The follow-up in the queue adds something new (idea, peer example, real date) and does not start "Following up on the note below".

---

## 14. The ten rules that matter most (summary)

1. **Fix targeting before copy.** Write to named owners of budget or new IP; stop emailing press, support and care inboxes (48% of your recipients so far). (Hunter, Gartner, your data)
2. **Send far fewer, far better emails.** 20 to 40 researched emails per weekday, no bursts, no weekends; small campaigns reply about 3x better than blasts. (Hunter, Woodpecker, Google)
3. **Get an official WAiFF mailbox.** Custom-domain senders get 108% more replies than freemail, and it proves authority. (Hunter)
4. **Keep bounces under 2%** by verifying every address; your campaign ran about 6%. (Google threshold summaries)
5. **Short, internal-looking subject lines** of 2 to 5 words that name them or one concrete asset; no "opportunity", "sponsorship" or "X x WAiFF". (Gong/30MPC, Belkins, Yesware)
6. **Open with a dated trigger about them;** timeline hooks reply 2.3x better than problem hooks. (Instantly)
7. **50 to 90 words, one idea, no pitch, no deck, no ROI claims;** pitching cuts replies up to 57% and ROI language cuts meetings 15%. (Gong)
8. **Ask for interest, not a meeting;** interest CTAs book about 2x the meetings; no calendar links on touch 1. (Gong)
9. **Follow up 3 times with new value** over about 3 weeks, threaded; never "following up on the note below"; 42% of replies come from follow-ups. (Instantly, Belkins, Gong)
10. **Sell a specific, measurable asset now:** a named award or category exclusivity for sponsors, a Cannes-linked India IP with 100% local revenue for licensees, while September to mid-December budgets are being set; promise measurement, not reach. (Sponsorship Collective, Power Sponsorship, IEG/ANA)

---

## Sources

### Cold email data
- Gong, interest CTA study (304,174 emails): https://www.gong.io/blog/this-surprising-cold-email-cta-will-help-you-book-a-lot-more-meetings
- Gong, do execs reply to cold email: https://www.gong.io/blog/do-execs-really-reply-to-cold-email-here-s-what-the-data-says
- Gong, ROI language mistake (132,552 emails): https://www.gong.io/blog/avoid-this-tempting-cold-email-mistake-at-all-costs
- Gong, does cold email still work (28M+ emails): https://www.gong.io/blog/does-cold-email-even-work-any-more-heres-what-the-data-says
- Gong, follow-up email science: https://www.gong.io/blog/7-tips-for-writing-the-perfect-follow-up-sales-email-according-to-science
- Gong, 85M cold email guide: https://www.gong.io/resources/guides/how-to-master-cold-email-get-the-data-backed-guide-based-on-85-million-emails
- 30 Minutes to President's Club with Gong, subject lines: https://www.30mpc.com/newsletter/4-data-backed-subject-lines-to-get-your-cold-emails-opened
- 30MPC, data-backed cold email formula: https://www.30mpc.com/newsletter/the-data-backed-cold-email-formula-the-exact-words-length
- 30MPC and Gong report PDF: https://tactics.30mpc.com/hubfs/The%20Ultimate%20Cold%20Email%20Data%20Report-1.pdf
- Lavender, subject line tips: https://lavender.ai/blog/cold-email-subject-line-tips
- Lavender, email length: https://lavender.ai/blog/best-length-cold-email
- Lavender, benchmark report: https://lavender.ai/blog/the-cold-email-benchmark-report
- Lavender, mobile: https://lavender.ai/blog/mobile-matters
- Belkins, subject line study: https://belkins.io/blog/b2b-cold-email-subject-line-statistics
- Belkins, response rates: https://belkins.io/blog/cold-email-response-rates
- Belkins, follow-up statistics: https://belkins.io/blog/sales-follow-up-statistics
- Belkins, best time to send: https://belkins.io/blog/best-time-to-send-email
- Belkins, LinkedIn outreach study: https://belkins.io/blog/linkedin-outreach-study
- Backlinko and Pitchbox, 12M outreach emails: https://backlinko.com/email-outreach-study
- Instantly, Cold Email Benchmark Report 2026: https://instantly.ai/cold-email-benchmark-report-2026
- Woodpecker, cold email statistics: https://woodpecker.co/blog/cold-email-statistics/
- Woodpecker, follow-up statistics: https://woodpecker.co/blog/follow-up-statistics/
- Woodpecker, follow-up after no response: https://woodpecker.co/blog/how-to-send-a-follow-up-email-after-no-response/
- Woodpecker, attachments: https://woodpecker.co/blog/attachments-cold-email/
- Hunter, State of Email Outreach: https://hunter.io/the-state-of-cold-email
- Hunter, emailing two people at one company: https://hunter.io/blog/should-you-email-more-than-one-person-per-company
- Hunter, cold email 2022 vs 2025: https://hunter.io/blog/cold-email-2022-vs-2025
- Hunter, HTML and deliverability: https://hunter.io/blog/is-html-harming-your-cold-email-deliverability/
- Salesloft, 16 tips (3M emails): https://www.salesloft.com/resources/blog/16-tips-to-double-your-reply-rates
- Yesware, subject line analysis: https://www.yesware.com/blog/email-subject-line-analysis/
- Mailshake, benchmarks 2026: https://mailshake.com/blog/cold-email-benchmarks-2026/
- Apollo, subject lines: https://www.apollo.io/insights/how-to-write-an-effective-cold-email-subject-line-that-gets-opened
- Sales.co, emailing the CEO: https://sales.co/research/should-you-cold-email-the-ceo
- Digital Bloom, hook benchmarks: https://thedigitalbloom.com/learn/cold-outbound-reply-rate-benchmarks/
- Autobound, trigger events: https://www.autobound.ai/blog/sales-trigger-events-templates
- Martal, subject line summary of Gong data: https://martal.ca/cold-email-subject-line/
- lemlist, Apple MPP and open rates: https://www.lemlist.com/blog/cold-email-open-rates
- Salesmotion, emailing executives: https://salesmotion.io/blog/cold-email-executives-reply-rates
- ReviewMyEmails, threading: https://reviewmyemails.com/emailalmanac/cold-outreach-and-sales/cold-email-sequencing-follow-up/follow-ups-same-thread-vs-new
- B2B Sales Training, breakup emails: https://b2bsalestraining.org/sales-breakup-email
- Phrasly, AI vs human reply rates: https://phrasly.ai/blog/ai-vs-human-cold-email-reply-rates/
- Mailbird, AI email detection: https://www.getmailbird.com/ai-generated-email-detection-spam-filter/
- Gartner, B2B buyer survey 2026: https://www.gartner.com/en/newsroom/press-releases/2026-03-09-gartner-sales-survey-finds-67-percent-of-b2b-buyers-prefer-a-rep-free-experience
- RAIN Group, prospecting research: https://www.rainsalestraining.com/sales-research/sales-prospecting-research
- RAIN Group, touches to a meeting: https://www.rainsalestraining.com/blog/how-many-touchpoints-does-it-take-to-make-a-sale
- Chris Voss, no-oriented questions: https://www.linkedin.com/posts/christophervoss_why-you-need-to-use-no-oriented-questions-activity-7108917462938652672-WrCp

### Deliverability and compliance
- Google, email sender guidelines FAQ: https://support.google.com/mail/answer/14229414?hl=en
- Smartlead, Gmail sending limits: https://www.smartlead.ai/blog/gmail-sending-limits
- Mailforge, cold emails per day: https://www.mailforge.ai/blog/how-many-cold-emails-to-send-per-day
- Mailmeteor, Gmail blocked account: https://mailmeteor.com/blog/gmail-blocked-my-account
- Puzzle Inbox, bounce threshold: https://puzzleinbox.com/compare/cold-email-bounce-rate-threshold
- Puzzle Inbox, plain text vs HTML: https://puzzleinbox.com/compare/plain-text-vs-html-cold-email/
- Bulk Email Checker, pre-flight checklist: https://bulkemailchecker.com/blog/how-to-write-cold-emails-that-dont-bounce/
- Mailpool, attachments vs links: https://www.mailpool.ai/blog/cold-email-attachments-vs-links-whats-safe-in-2026-and-whats-not
- AWeber, link shorteners: https://blog.aweber.com/email-deliverability/link-shorteners.htm
- MailTester, spam word myths: https://mailtester.com/blog/spam-trigger-word-myths-debunked-deliverability-data/
- GMass, cold email signatures: https://www.gmass.co/blog/cold-email-signature/
- Kondo, CC and deliverability: https://www.trykondo.com/blog/cold-email-deliverability
- Warmy, domain warm-up: https://www.warmy.io/blog/how-long-to-warm-up-new-domains-before-starting-to-send-campaigns/
- FTC, CAN-SPAM guide: https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business
- Kahlem Advisory, cold email in France (CNIL): https://www.kahlemadvisory.com/articles/cold-email-france-b2b/
- DLA Piper, electronic marketing in India: https://www.dlapiperdataprotection.com/index.html?t=electronic-marketing&c=IN

### LinkedIn
- Expandi, State of LinkedIn Outreach H2 2026: https://expandi.io/state-of-linkedin-outreach-h2-2026/
- Expandi, LinkedIn outreach benchmarks 2026: https://expandi.io/blog/linkedin-outreach-benchmarks-2026/
- Expandi, weekly invitation limit: https://expandi.io/blog/linkedin-connections-limit/
- Botdog, acceptance rates: https://www.botdog.co/blog-posts/linkedin-acceptance-rates
- LinkedIn Help, personalize invitations: https://www.linkedin.com/help/linkedin/answer/a563153
- Taplio, connection request limits: https://taplio.com/blog/linkedin-connection-request-limit
- LinkedIn, InMail response data: https://www.linkedin.com/business/talent/blog/talent-strategy/these-inmails-get-best-response-rates
- Kondo, pitch-slap: https://www.trykondo.com/blog/linkedin-pitch-alternatives
- Kondo, response rate tips: https://www.trykondo.com/blog/linkedin-response-rate-tips
- Overloop, LinkedIn vs email: https://overloop.com/blog/linkedin-vs-email-which-performs-better-for-b2b-outreach

### Sponsorship practice and data
- Sponsorship Collective, five reasons sponsors ignore emails: https://sponsorshipcollective.com/blog/five-reasons-sponsorship-prospects-ignore-e-mails/
- Sponsorship Collective, best time of year: https://sponsorshipcollective.com/blog/best-time-of-year-for-sponsorship/
- Sponsorship Collective, five discovery questions: https://sponsorshipcollective.com/blog/5-discovery-questions-that-get-a-sponsor-to-say-yes/
- Sponsorship Collective, why sponsors say no: https://sponsorshipcollective.com/blog/why-sponsors-say-no/
- Sponsorship Collective, sponsorship emails that convert: https://sponsorshipcollective.com/blog/sponsorship-emails-that-convert/
- Sponsorship Collective, discovery call script: https://sponsorshipcollective.com/blog/the-discovery-call-script-that-turned-one-meeting-into-a-six-figure-deal/
- Power Sponsorship, "just send me a proposal": https://powersponsorship.com/sponsor-send-me-a-sponsorship-proposal/
- Power Sponsorship, don't send a proposal until: https://powersponsorship.com/dont-send-a-sponsorship-proposal/
- Power Sponsorship, time of year: https://powersponsorship.com/what-time-of-year-should-i-seek-sponsorship/
- Power Sponsorship, how sponsors evaluate proposals: https://powersponsorship.com/how-do-sponsors-evaluate-sponsorship-proposals/
- TicketManager, IEG decision-makers survey summary: https://www.ticketmanager.com/blog/digging-deeper-into-latest-sponsorship-trends-report/
- IEG, activation ratios: https://www.linkedin.com/pulse/activation-ratios-dead-ieg
- ANA, sponsorship validation survey: https://www.ana.net/content/show/id/pr-2013-validate-initiatives
- ANA, sponsorship measurement study 2018: https://www.ana.net/content/show/id/pr-2018-sponsorship-measurement
- SponsorUnited, 2025 Markets Report: https://www.sponsorunited.com/reports/2025-markets-report
- Yahoo Sports on SponsorUnited AI sponsorship data: https://sports.yahoo.com/sectors/technology/articles/ai-companies-spending-big-on-business-backed-sponsorships39-093000730.html
- Ticket Fairy, category exclusivity: https://www.ticketfairy.com/blog/category-exclusivity-without-handcuffs-precision-in-festival-sponsorship-deals
- Adweek, Adobe at Cannes Lions: https://www.adweek.com/brand-marketing/adobe-makes-its-biggest-cannes-lions-bet-yet-amid-race-to-court-creators/
- Adobe newsroom, Cannes Lions 2025: https://news.adobe.com/news/2025/06/cannes-lions-2025-adobe-unites-creativity
- Marketing Brew, why brands sponsor Sundance: https://www.marketingbrew.com/stories/2026/02/03/brands-film-festivals-sundance-adobe-acura-canon
- Runway and IMAX, AI Film Festival: https://runwayml.com/news/runway-imax-aiff-presentation
- Runway AI Festival: https://aif.runwayml.com/
- Deadline, Runway festival expands: https://deadline.com/2026/01/runway-ai-festival-adding-new-categories-1236700233/
- Tribeca and OpenAI programme: https://tribecafilm.com/press-center/press-releases/tribeca-studios-and-openai-launch-ear-long-collaboration-to-support-independent-filmmakers-in-creating-ai-integrated-short-films
- LVMH x VivaTech 2026: https://www.lvmh.com/en/lvmh-x-vivatech-2026

### Licensing and franchise models
- TED, TEDx rules: https://www.ted.com/participate/organize-a-local-tedx-event/before-you-start/tedx-rules
- TED, TEDx licensing tiers: https://www.ted.com/participate/organize-a-local-tedx-event/before-you-start/event-types/licensing-tiers
- Startup Grind, working with sponsors: https://www.startupgrind.com/blog/sg-guide-working-with-sponsors/
- Comics Beat, ReedPop licensing: https://www.comicsbeat.com/reedpop-international-comic-con-presence-report/
- Campaign India, NODWIN acquires Comic Con India: https://www.campaignindia.in/article/nodwin-gaming-acquires-comic-con-india/493967
- Inc42, NODWIN live IP model: https://inc42.com/features/decoding-nazara-backed-nodwin-gamings-success-story-amid-the-volatile-indian-esports-arena/
- Live Nation, Lollapalooza India: https://www.livenationentertainment.com/2022/07/lollapalooza-expands-global-reach-with-the-addition-of-lollapalooza-india/
- Pollstar, BookMyShow and India's concert market: https://news.pollstar.com/2026/04/03/how-bookmyshow-is-helping-turn-india-into-a-global-concert-market/

### WAiFF and India context
- Screen Daily, seven talking points from WAiFF Cannes: https://www.screendaily.com/news/seven-talking-points-from-the-world-ai-film-festival-in-cannes/5215914.article
- Palais des Festivals listing: https://en.palaisdesfestivals.com/offers/world-artificial-intelligence-film-festival-waiff-cannes-en-3686586/
- Mediakwest, WAiFF 2026: https://mediakwest.com/world-ai-film-festival-2026/
- WAiFF official site: https://worldaifilmfestival.com/
- WAiFF internal documents in scratchpad (not public): WAIFF_2027_Sponsor_Deck.txt, WAIFF_Partnership_Proposal_2027.txt, WAiFF_2027_MoU_Short.txt, WAIFF_2027_Competition_Rules.txt
- FICCI-EY M&E report 2026: https://www.ey.com/en_in/newsroom/2026/03/india-s-media-and-entertainment-sector-grew-9-percent-to-inr-2-point-78-trillion-in-2025-driven-by-digital-and-live-experiences-ficci-ey-report
- Adobe, India creators survey 2026: https://news.adobe.com/en/apac/news/2026/08/adobe-india-creator-survey-toolkit-2026
- CNBC, Indian filmmakers and generative AI: https://www.cnbc.com/2026/06/11/how-indian-filmmakers-are-using-generative-ai.html
- PIB, IFFI and LTIMindtree AI Film Festival: https://www.pib.gov.in/PressReleasePage.aspx?PRID=2194363&reg=48&lang=2
- India AI Film Festival (Invideo): https://indiafilmfestival.ai/
- News On Air, WAVES 2025: https://www.newsonair.gov.in/indias-first-waves-2025-summit-concludes-in-mumbai
- Variety, MAMI hiatus: https://variety.com/2025/film/festivals/mumbai-film-festival-hiatus-1236465675/
- Bajaj Finserv, India fiscal year: https://www.bajajfinserv.in/what-is-fiscal-year-in-india
- Tribune, Diwali 2026 dates: https://www.tribuneindia.com/news/business/diwali-2026-is-late-26-things-every-clothing-business-must-fix-now
- Commisceo, Indian business etiquette: https://www.commisceo-global.com/blog/the-essential-guide-to-indian-business-etiquette
- Global Business Culture, India: https://www.globalbusinessculture.com/countries/resources/country-profiles/india-business-culture/
- BW Marketing World, messaging preference in India: https://www.bwmarketingworld.com/article/indians-want-to-connect-with-a-business-the-same-way-they-chat-with-family-friends-report-449606

Method note: WebFetch was egress-blocked, so figures were taken from search-result snippets of the cited pages and cross-checked across at least two sources where possible. Where a figure appears only in a vendor summary, it is graded B or C above. Numbers from your own campaign come from the Gmail export files in the scratchpad (751 threads, 5 to 23 September 2026).
