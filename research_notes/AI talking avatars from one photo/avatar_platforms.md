# Dedicated AI avatar platforms other than HeyGen (Hedra, D-ID, Synthesia, Captions/Mirage, Tavus, Argil, Akool, Vidnoz): one photo or selfie video to a talking clip, state as of Oct 2026

**Method limits (read first).**
1. I could not open any page directly. The sandbox egress proxy returned HTTP 403 on CONNECT for every vendor site I tried (hedra.com, d-id.com, synthesia.io, tavus.io, argil.ai, akool.com, vidnoz.com) and for reddit.com, trustpilot.com, youtube.com, hn.algolia.com, fal.ai, replicate.com and docs.sync.so. WebFetch also failed DNS resolution. GitHub repo access was not enabled for this session.
2. Reddit is also blocked from the search engine's crawler (a search restricted to reddit.com returned "not accessible to our user agent"). So I read no Reddit thread; Reddit opinion appears only where review sites quote it.
3. Everything below comes from the WebSearch tool. It returns a machine-written digest of the result pages plus links, not the pages' own text. Quoted phrases are as the digest relayed them and may be paraphrased. When the digest did not tie a claim to one page, I list the likely pages and mark it "not pinned".
4. The shared web-search budget for this turn (200 calls across all agents) ran out after about 32 of my searches. As a result, newer entrants, D-ID Studio prices, Synthesia's free plan, voice cloning and data-retention rules are unresearched (see Gaps).
5. The newest dated data points are from Aug–Sept 2026, about 1–2 months old. I could not confirm anything live in October 2026.

**Source labels:** [V] vendor's own page or docs · [J] independent journalism · [U] user-review platform (Trustpilot, Product Hunt) · [R] affiliate/SEO review or listicle site · [C] published by a company selling a competing avatar or video product (treat as biased) · [T] third-party pricing tracker or API catalog.

---

## 1. Current plans, prices, free tiers, and the cheapest way to make one 45–60 s clip

### Takeaway
Hedra is the only platform here with a clearly self-serve, per-second API price low enough to make a 60-s photo+audio clip for a few dollars ($1.50 at 540p to $3.75 at 1080p per attempt, official developer page). Two other API routes fit the budget: D-ID's API Build plan (~$18/mo for ~16 min) and Mirage (Captions) Avatar X at $0.15/s (~$9 per 60-s clip). Two routes cost more than $30 for an API-driven clip of *your own* face: Synthesia's API needs the $89/mo Creator plan, and Tavus custom replicas need the $59/mo Starter plan. Prices for Argil, Akool and Vidnoz disagree across 2026 sources. Argil appears to have re-priced sharply around Aug 2026, to $10 and $20/mo plans.

### Cited Findings

#### Hedra
- **Plans (as of Aug 2026, as trackers quote Hedra's pricing page):** Basic $15/mo for 1,500 credits, Creator $30/mo for 5,400 credits and Professional $75/mo for 14,400 credits, all billed monthly. One tracker also lists Business at $150; another lists Teams at $75 and Enterprise as custom. Monthly credits do not roll over. — [T usagepricing.com](https://www.usagepricing.com/blueprint/hedra); [T Scopeful](https://www.scopeful.org/tools/hedra); [V hedra.com/plans](https://www.hedra.com/plans) (not fetched directly)
- **Credit rates on the plans page:** Character-3 costs 3 credits per second of video at 540p and 6 credits/s at 720p. — [V hedra.com/plans](https://www.hedra.com/plans) (via digest)
- **July 29, 2026 repackaging:** a July 2026 pricing analysis says Hedra "merged its native avatar models into a single model, Character-3, priced at 6 credits/second". The tracker's change-log entries are titled "Character-3 / Hailuo lineup" and "packaging". — [T usagepricing activity, 2026-07-29 lineup](https://www.usagepricing.com/blueprint/activity/hedra-2026-07-29-character-3-hailuo-lineup); [T usagepricing activity, 2026-07-29 packaging](https://usagepricing.com/blueprint/activity/hedra-2026-07-29-packaging)
- **Conflicting plan figures:** some 2026 reviews list $20/$50/$100 tiers instead of $15/$30/$75. One aggregator says there is no free tier; another says there is a free tier plus three paid plans. (Not pinned.) — [R lokeshkapoor.com](https://lokeshkapoor.com/blog/hedra-pricing); [R DroidCrunch](https://droidcrunch.com/hedra-review/); [R max-productive.ai "Is It Free?"](https://max-productive.ai/ai-tools/hedra/)
- **API price, official developer page:** 540p 2.5¢/s, 720p 5¢/s, 1080p 6.25¢/s. — [V Hedra Character 3 API page](https://www.hedra.com/develop/models/video/hedra-character-3)
- Magic Hour (checked Sept 2026) reports the same per-second API rates and works out "$1.50, $3.00, or $3.75 before retries" for a 60-s attempt. — [C Magic Hour guide](https://magichour.ai/blog/guide-to-hedra-ai)
- A 2026 blog title, "Hedra pricing 2026: credits burn by the second", reflects how users perceive the cost. — [R dailyaifixs.com](https://dailyaifixs.com/blog/hedra-pricing-2026-credits-burn-by-the-second)

#### D-ID
- **API plans (2026 pages; prices conflict):**
  - **Build:** $18/mo monthly or $14.40/mo annual. 64 credits, up to 16 min of video plus 32 min of streaming.
  - **Launch:** $50/mo monthly; another source gives $35/mo billed annually ($420/yr). 180 credits, 45 min video, 90 min streaming.
  - **Scale:** $198/mo monthly, or $138.6/mo annual ($1,663.2/yr). 800 credits, 200 min video, 400 min streaming.
  - **Enterprise:** custom.
  - **Credit packs:** 180/360/540 for Launch; 800/1,000/1,200 for Scale.
  - Sources: [C Creatify (2026)](https://creatify.ai/blog/d-id-pricing-(2026)-plans-credits-and-what-you-ll-actually-pay); [C Spatius (2026)](https://www.spatius.ai/blog/d-id-pricing-2026/); [R ToolSurf](https://www.toolsurf.com/d-id-pricing-2026/); [R HeyFish](https://heyfish.ai/d-id-review); [R ToolColumn](https://www.toolcolumn.com/pricing/d-id-pricing)
- **Shared balance:** streaming minutes cost half the credits of rendered video. Offline generation, translation and agent activity all draw on the same balance. — same sources (not pinned)
- **API trial (single source):** "$0 for 14 days, up to 3 min video, 10 min streaming". — same source set (not pinned; likely [R HeyFish "Free Credits & Limits"](https://heyfish.ai/d-id-review))
- **Studio watermark:** the low-priced Studio "Lite tier still stamps a watermark across the whole clip". (Not pinned.) — [R AIToolsPolice](https://aitoolspolice.com/reviews/d-id/); [C Media.io (Wondershare)](https://www.media.io/comparison/did-ai-review.html)
- I did not retrieve D-ID Studio plan prices (see Gaps).

#### Synthesia
- **Starter:**
  - $29/mo billed monthly.
  - Annual pricing is quoted three ways: $18/mo; $22/mo (matching an official FAQ annual total of $264); and, on one site, $19 monthly / $14 annual.
  - Includes 10 video min/month, 125+ stock avatars, **3 personal avatars**, no watermark, and 1 editor + 3 guests.
  - **No API.**
  - Sources: [R SaaSPricePulse](https://www.saaspricepulse.com/tools/synthesia); [R CostBench](https://costbench.com/software/ai-video-generators/synthesia/); [R v4v.ai](https://v4v.ai/blog/synthesia-pricing-2026/); [R omidsaffari.com](https://omidsaffari.com/blog/synthesia-pricing); [R AIStackPicks](https://aistackpicks.com/reviews/synthesia-pricing-2026/)
- **Creator:**
  - $89/mo billed monthly; annual $59–$67/mo (official FAQ annual total $804, i.e. $67/mo).
  - Includes 30 min/month, 180+ stock avatars, **5 personal avatars**, 1 editor + 5 guests, and **API access**.
  - The API is capped at 360 min/yr; more requires Enterprise.
  - Sources: same set; [V Synthesia API docs](https://docs.synthesia.io/reference/introduction)
- **Enterprise:** custom pricing on all sources. — same set
- One 2026 review title cites a "$4B" valuation. — [C ezUGC](https://www.ezugc.ai/blog/synthesia-review)

#### Captions (now "Captions by Mirage")
- **Rebrand:** Captions now trades under Mirage (mirage.app), and the help center has moved to help.mirage.app. — [T SaaSworthy (Apr 2026)](https://www.saasworthy.com/product/captions-ai); [V help.mirage.app subscriptions](https://help.mirage.app/docs/subscriptions); [R AutoHustle, "What the Rename Changed"](https://autohustle.me/blog/captions-mirage-pricing-2026)
- **Max plan:** about $24.99/mo, with 500 credits that renew monthly and **up to 30 AI Twins**. Higher tiers have been renamed; for example, "Frontier 2x (formerly Scale 2x)" is 2,800 credits for $139.99. — [V help.mirage.app subscriptions](https://help.mirage.app/docs/subscriptions)
- **Free plan:** includes zero AI credits, so AI twins require Max ($24.99/mo) or higher. — [R Kompozy](https://kompozy.io/reviews/captions-ai); [R Prizmad](https://prizmad.com/review/captions-ai)
- **API (billed separately from app plans):** Mirage Avatar X video generation is **$0.15 per second, billed in 6-second increments**. The captioning API is $0.15/min, with fractional minutes rounded up. The pricing page was last modified in Aug 2026. — [V Captions API pricing](https://captions.ai/help/docs/api/pricing); [V help.mirage.app API pricing](https://help.mirage.app/docs/api/pricing)

#### Tavus
- **Most-cited figures (Aug–Sept 2026):**
  - Free plan: 25 conversational minutes, 25 stock replicas, API access.
  - Starter: $59/mo, with 100 conversation minutes and **custom replicas**; overage $0.37/min.
  - Growth: $397/mo, with 1,250 (or 1,300) minutes and up to 10 concurrent streams.
  - Enterprise: custom.
  - Sources: [R The Rundown (Phoenix-4)](https://www.therundown.ai/tools/phoenix-4); [R ToolsForHumans](https://www.toolsforhumans.ai/ai-tools/tavus); [R OnyxRanked](https://onyxranked.com/tavus-review-2026/)
- **Conflicting figures:**
  - AITroveX (checked Aug 20, 2026): free plan is 20 CVI min/month, 1 concurrent session, 5-min session cap; overage $0.26/CVI min. It warns that "older hidden plan tables may show different numbers". — [R AITroveX](https://aitrovex.com/tool/tavus)
  - UseCarly (verified July 30, 2026): Starter $22/mo (60 min) and Builder $59/mo (175 min). — [R UseCarly](https://www.usecarly.com/blog/tavus-ai/)
  - One aggregator: free plan is 25 CVI min plus 5 min of video generation. — [R dreaming.press](https://dreaming.press/stack/tavus) (not pinned)
  - One review: Tavus's public pricing page and its live dashboard disagree. (Not pinned.) — [R AI Alleyway](https://aialleyway.com/tavus-review/)
- Custom replicas (your own clone rather than a stock face) start on Starter. — [R The Rundown (Phoenix-4)](https://www.therundown.ai/tools/phoenix-4); [R AI Alleyway](https://aialleyway.com/tavus-review/)

#### Argil
- **Possibly current (Aug 2026):**
  - The live pricing page lists **Pro at $10/mo (400 credits)** and **Business at $20/mo (800 credits)**, with yearly billing at "two months free".
  - The older Classic, Pro and Scale plans are retired but still appear in old docs and blogs.
  - API access is listed among the automation features.
  - Source: [R The Rundown](https://www.therundown.ai/tools/argil)
- **Older figures (2026 reviews, possibly outdated):**
  - Classic: $27/mo annual or $39/mo monthly, for 1 avatar and up to 25 min/mo (Argil quotes about 50 × 30-s clips).
  - Pro: $149/mo, which unlocks the AI Influencer builder.
  - Scale: $499 on a coupon site; Techjockey lists about $115/week.
  - Sources: [R Techjockey](https://www.techjockey.com/us/detail/argil); [R AffiliateWeapons](https://affiliateweapons.com/affiliate-tools/argil-ai/); [C Pixo](https://pixo.video/blog/heygen-alternatives)
- **Free access:**
  - Toolchase reports a 5-day free trial plus a free plan with 2 video min and basic avatars. — [R Toolchase](https://toolchase.com/tool/argil/)
  - A Trustpilot reviewer contradicts this: signing up for the advertised trial leads to a paywall. — [U Trustpilot Argil](https://www.trustpilot.com/review/argil.ai)
- **API credit rates (official docs):**
  - 160 credits per minute of video.
  - +20 credits per video in royalties when using Argil's v1 stock avatars.
  - 20 credits per B-roll.
  - The pay-as-you-go page adds 20 credits per minute of voice and 10 per image B-roll.
  - **Purchased pay-as-you-go credits never expire.**
  - More than 60,000 credits/month goes to sales.
  - Sources: [V Argil API pricing](https://docs.argil.ai/resources/api-pricings); [V Argil pay-as-you-go](https://docs.argil.ai/resources/pay-as-you-go-pricings)

#### Akool
- **Plan prices conflict (2026):** PixelPanda lists Pro Tier 1 at $30/mo (600 credits, about 20 min at 1080p). Vidmetoo says "from $18/month on annual billing". — [R PixelPanda](https://pixelpanda.ai/review/akool-ai); [R Vidmetoo](https://www.vidmetoo.com/akool-pricing-explained-plans-credits-and-hidden-costs/)
- **Official API pricing page:** talking photo sits under **Enterprise ("Let's Talk", no public price)** at **10 credits per 5 s**; audio is 0.5 credits/min. — [V Akool API pricing](https://akool.com/api-pricing)
  - A 2026 review blog lists 10 credits per 10 s instead. — not pinned
  - Rewardio, citing the live rate card, agrees with 10 credits/5 s. — [R Rewardio](https://rewardio.com/akool-pricing/)
  - Playcut says 4K talking photos burn 120 credits/min; 1080p talking avatar is about 30 credits/min. — [C Playcut](https://playcut.ai/blog/akool-alternatives/)
- **API access tier conflicts:** Rewardio says API access starts at Pro Max, where streaming avatar and live face swap cost 1.2 credits per 10 s at 1080p. aitwin.ninja lists a Pro API tier from $30/mo. — [R Rewardio](https://rewardio.com/akool-pricing/); [R aitwin.ninja](https://aitwin.ninja/akool-pricing/)
- **Free tier:** "100 starter credits with no card required", per one review. — not pinned among [R Vidmetoo review](https://www.vidmetoo.com/akool-review/), [R EverydayAITuts](https://everydayaituts.com/ai-video-tools/akool-review)
- Subscription credits don't roll over, per media.io citing Akool's terms. — [C Media.io](https://www.media.io/comparison/akool-ai-review.html)

#### Vidnoz
- **Consumer plans (2026; conflicting):** Starter $26.99/mo or $19.99/mo annual; Business $74.99/mo ($56.24/mo annual). Another source lists Starter $22.49/mo and Business $56.99/mo; Enterprise is custom. — [R ToolJunction](https://www.tooljunction.io/ai-tools/vidnoz-ai); [R AIsoTools](https://aisotools.com/pricing/vidnoz); [R CreatorStackClub](https://www.creatorstackclub.com/software/vidnoz-ai)
- **Free web plan (sources disagree):**
  - "Daily free credits (no credit card), 3-minute max per video, 720p export with watermark".
  - Others give 60 credits/day (about 3 min), or 30 credits/day (about 1 min).
  - One says one generation per day.
  - Unused credits don't carry over.
  - Sources: [R Prizmad](https://prizmad.com/review/vidnoz); [R AIToolsPolice](https://www.aitoolspolice.com/reviews/vidnoz/); [C Talkpix](https://www.talkpix.ai/blog/best-talking-photo-apps); [R AIVideoPicks](https://aivideopicks.com/posts/vidnoz-review-2026.html)
- **Official Open API pricing:**
  - Plans: **Free Trial 30 API credits/month**; Pro 1,000 credits/month for $80; Scale 6,000/month for $300; Enterprise custom with a $10,000/yr minimum.
  - Costs: **4 credits per minute of video**, 1 credit per 300 TTS characters, 1 credit per 2 headshot photos, 1 credit per text-to-avatar image.
  - No separate talking-photo price is listed.
  - Source: [V Vidnoz Open API limits](https://www.vidnoz.com/overview/limits.html)

#### Material changes in 2025–2026 (pivots, renames, repricing)
- **Captions → "Captions by Mirage":** users report a forced move to the "Mirage Studio" interface. One Trustpilot reviewer says the company "completely stopped supporting clients who had the previous plan after the Mirage release". — [U Trustpilot captions.ai](https://www.trustpilot.com/review/captions.ai); [U Trustpilot mirage.app](https://www.trustpilot.com/review/mirage.app)
- **Hedra:**
  - July 29, 2026 repackaging, as above.
  - The founder, replying on Trustpilot, called the original product "an extremely buggy thin layer over our video model" and said the company is building "a broader visual communication platform".
  - One reviewer criticized a shift toward meme templates.
  - Sources: [U Trustpilot Hedra](https://www.trustpilot.com/review/hedra.com); [T usagepricing](https://usagepricing.com/blueprint/activity/hedra-2026-07-29-packaging)
- **Argil:** retired its Classic/Pro/Scale plans for much cheaper Pro and Business tiers (Aug 2026). — [R The Rundown](https://www.therundown.ai/tools/argil)
- **D-ID:** the Talks/Clips **Streams** (live-streaming) endpoints are now "legacy", and D-ID steers developers to its Agents SDK and Agents Streams. 2026 reviews frame D-ID around "agentic videos" and visual agents. — [V D-ID Talks Streams overview](https://docs.d-id.com/reference/talks-streams-overview); [R Aivario](https://aivario.com/tools/d-id)
- **Tavus:**
  - Phoenix-4 model.
  - An "Image-to-Replica" blog post (photo-based replicas). One digest said it launched in 2026; a second search could not confirm the date.
  - A consumer "PAL" product.
  - Sources: [V Tavus blog, Introducing Image-to-Replica](https://www.tavus.io/blog/introducing-image-to-replica); [R The Rundown (Phoenix-4)](https://www.therundown.ai/tools/phoenix-4); [R UseCarly, "PAL Maker"](https://www.usecarly.com/blog/tavus-ai/)
- **Synthesia:** Express-2 launched in **Sept 2025** (more than 6 months ago, so possibly superseded). — [J MIT Technology Review, 2025-09-04](https://www.technologyreview.com/2025/09/04/1123054/synthesias-ai-clones-are-more-expressive-than-ever-soon-theyll-be-able-to-talk-back/)
- **Vidnoz:**
  - Reviewers report a move from pay-as-you-go credits to subscriptions, and lost creations after a platform change. — [U Trustpilot Vidnoz](https://www.trustpilot.com/review/www.vidnoz.com)
  - The English API landing page returned 404 when checked on July 29, 2026. — [C Atlas Cloud](https://www.atlascloud.ai/blog/guides/vidnoz-ai-face-swap)
- No shutdowns or acquisitions of these eight platforms showed up in my results. This is absence of evidence, not confirmation.

#### Newer entrants and the ecosystem seen in 2026 sources
- Mirage Avatar X is also sold through fal.ai's model marketplace as `mirage-api/avatar-x/reference-to-video`, which accepts mp3, ogg, wav, m4a and aac audio. — [V fal.ai model page](https://fal.ai/models/mirage-api/avatar-x/reference-to-video)
- Several companies that published 2026 comparisons in my results sell their own avatar or talking-photo products and are potential entrants, but I did not evaluate them: Creatify, Spatius, Magic Hour, Talkpix, Playcut, Pexo, ezUGC, Wondershare (Media.io/Filmora), HitPaw Edimakor and Atlas Cloud. — e.g. [C Spatius vs Tavus](https://www.spatius.ai/blog/spatius-vs-tavus/); [C Talkpix](https://www.talkpix.ai/blog/best-talking-photo-apps)

### Inferences
All figures below are my own arithmetic from the cited numbers.

| Platform | Cheapest in-budget route to one 45–60 s clip | Estimated cost | Main caveats |
|---|---|---|---|
| Hedra (API) | Character-3, photo + audio | 45 s: $1.13 (540p) / $2.25 (720p) / $2.81 (1080p). 60 s: $1.50 / $3.00 / $3.75 per attempt | Unclear whether it bills a prepaid wallet or plan credits; retries add cost |
| Hedra (app) | Basic $15/mo | 1,500 credits ≈ 4 × 60-s attempts at 720p (6 cr/s) or 8 at 540p (3 cr/s) | Credits don't roll over; auto-renew complaints (Q5) |
| D-ID (API) | 14-day trial (3 min video, one source), or Build $18/mo (16 min ≈ 4 credits/min) | $0–$18 | Trial watermark and terms unverified |
| Mirage / Captions (API) | Avatar X, photo or video reference + audio | 45 s billed as 48 s = **$7.20**; 60 s = **$9.00** | 720p only; billed separately; called "Beta" by one catalog |
| Captions (app) | Max $24.99/mo (500 credits, twins) | ≤ $24.99 | Credits per twin video unknown; not API-driven |
| Synthesia | Starter $29/mo monthly (web UI only; 3 personal avatars; 10 min) | $29 | No API below Creator ($89/mo), so the API route is over budget |
| Tavus | Custom replica needs Starter $59/mo | > $30 | Unknown whether Image-to-Replica is on any tier under $30 |
| Argil | Pro $10/mo (400 credits), if the Aug 2026 pricing holds | ≈ 2 × 60-s clips (160 cr/min video + 20 cr/min voice) | Needs a ~2-min training video; unclear which plans include the API; refund complaints |
| Akool | Free 100 starter credits | $0 for ≤ 50 s at the official 10 cr/5 s (≤ 100 s at 10 cr/10 s) | Watermark and commercial-rights status unknown; API tier opaque; worst billing complaints (Q5) |
| Vidnoz | Free web plan (720p, watermarked), or free API trial (30 credits; 4 cr/min video) | $0 | Talking photo via API unconfirmed; free web output watermarked |

- Hedra's subscription credits look cheaper per second than its published API dollar rate. Creator is $30 for 5,400 credits ≈ $0.0056/credit, so 720p at 6 cr/s ≈ $0.033/s, against 5¢/s on the API. That only matters if API calls can draw on plan credits, which is disputed (Q2).
- For an under-$30, API-only, photo-only experiment, the plausible shortlist from this set is Hedra, then D-ID API, then Mirage Avatar X. Akool and Vidnoz are cheaper on paper but their API terms are opaque.

### Gaps
- **D-ID Studio** plan prices and free-trial terms (Lite/Pro/Advanced, minutes, watermark, commercial rights) were not retrieved. Neither were current Express and Premium+ avatar plan requirements.
- **Synthesia's free plan** (minutes, watermark, personal-avatar eligibility) was not covered by any result.
- **Hedra:** no source confirms whether a free tier exists in Oct 2026, or whether free or Basic output is watermarked or carries commercial rights.
- **Akool, Vidnoz, Argil:** current Oct 2026 consumer prices disagree across sources. The live pages could not be fetched.
- **Tavus:** I found no price for pre-rendered (non-conversational) video generation per minute.
- **Commercial rights on free tiers:** not established for any vendor. The user's use is private, so this matters less.
- **Newer entrants not researched** because the search budget ran out. From my pre-mid-2026 knowledge (**unverified in this session; do not cite as fact**), the names worth a follow-up search are ByteDance OmniHuman (via Dreamina/CapCut and API hosts), Kling AI Avatar, open-weight InfiniteTalk/MultiTalk hosted on fal/Replicate/WaveSpeed, VEED Fabric, Sync.so lipsync models (re-lip-sync a selfie video to new audio), Lemon Slice, Creatify Aurora, Higgsfield, and OpenAI Sora 2 "cameos".
- **"Omnia":** one Magic Hour guide is titled "Character 3 tutorial, pricing & Omnia comparison" ([C Magic Hour](https://magichour.ai/blog/guide-to-hedra-ai)). Whether Omnia is a newer Hedra model or a rival's is unverified.

---

## 2. API: self-serve availability, billing, photo + user-audio input, max length, render time, watermarking

### Takeaway
Four vendors document a single-call "image + your own audio file → talking video" API:
- **Hedra Character-3:** start-frame image plus up to 4 audio clips; up to 10 min; 2.5–6.25¢/s.
- **D-ID `/talks`:** `source_url` photo plus an audio script; renders "typically" in 10–30 s.
- **Mirage Avatar X:** image *or* video reference plus required audio; 720p; $0.15/s.
- **Akool talking photo:** `talking_photo_url` + `audio_url`.

Synthesia (Creator plan) and Argil take your own audio but need a pre-built avatar. Tavus is built around real-time conversation and consented replicas. Watermarking of API output was not documented for any vendor in the retrieved material.

### Cited Findings

#### Hedra
- Character-3 is described as Hedra's "latest longform avatar model, audio to video with full multi-language support… talking and singing video with speaker selection up to 10 minutes long". — [V Hedra Character 3 API](https://www.hedra.com/develop/models/video/hedra-character-3); [V model page](https://www.hedra.com/models/video/hedra/character-3)
- **Inputs:** a start-frame image (≤ 10.4 MB) and up to 4 audio clips (each 0.5–600 s, ≤ 104.8 MB). Duration (ms) is optional: leave it out and the video runs as long as the audio; set it and the audio is trimmed or padded with silence. — [V Hedra Character 3 API](https://www.hedra.com/develop/models/video/hedra-character-3)
- **Price:** 540p 2.5¢/s, 720p 5¢/s, 1080p 6.25¢/s. — [V same page](https://www.hedra.com/develop/models/video/hedra-character-3)
- **How credits work (docs):** credits are consumed each time you generate a video through the API, with cost depending on duration, resolution and model version. The docs describe API tiers named Starter, Pro and Enterprise with volume discounts. Those names don't match the consumer plans, so the page may be stale. — [V Hedra docs, How Credits Work](https://hedra.com/docs/pages/getting_started/pricing)
- **Billing conflict:** one review says the API "bills a prepaid dollar wallet, not your studio credits, except for generations made through MCP". Another says it draws on the same credit balance as the web app. (Not pinned.) — [R lokeshkapoor.com](https://lokeshkapoor.com/blog/hedra-pricing); [R ImperialAITools](https://imperialaitools.com/tool/hedra-ai/); [R Fluxnote](https://fluxnote.io/guides/hedra-ai-review); [T CostBench hidden costs](https://costbench.com/software/ai-media-apis/hedra-api/hidden-costs/)
- **Ecosystem:** an unofficial ComfyUI node calls Character-3's API to turn images and audio into talking-avatar videos. It lists about 3.5–7 credits/s; it is unaffiliated, so don't rely on it for pricing. — [GitHub ShmuelRonen/ComfyUI_Hedra](https://github.com/ShmuelRonen/ComfyUI_Hedra)

#### D-ID
- **Create call:** `POST https://api.d-id.com/talks`.
  - `source_url` is the image to animate: an https or s3 link to a jpg, jpeg or png, or a provided studio actor; a default image is used if omitted.
  - `script` is required and is either a text script or an audio script.
  - Optional fields: a `config` object, and `user_data` (1–1000 characters) that is echoed in the response and webhook.
  - Source: [V D-ID Create a talk](https://docs.d-id.com/reference/createtalk)
- **Quickstart ("Create talking head videos from a photo and text"):** posts `source_url` plus a text script with a Microsoft voice ID, then polls `GET /talks/{id}` until the status is done. "The video typically takes 10-30 seconds to process." — [V D-ID photo-avatar quickstart](https://docs.d-id.com/docs/v2-photo-avatar-quickstart); [V Get talk](https://docs.d-id.com/reference/gettalk); [V List talks](https://docs.d-id.com/reference/gettalks)
- The Talks/Clips **Streams** (live) endpoints are "a legacy feature… we highly encourage developers to use the newer Agents SDK or the Agents Streams". — [V D-ID Talks Streams overview](https://docs.d-id.com/reference/talks-streams-overview); [V Clips Streams overview](https://docs.d-id.com/reference/clips-streams-overview)
- A third-party API index lists D-ID as paid with a free trial and self-serve signup. — [T APIs.io D-ID](https://apis.io/providers/d-id/)
- The exact audio-script field name (e.g. `audio_url`), API trial watermarking and max talk length were **not** found in the retrieved docs (see Gaps).

#### Synthesia
- **APIs:**
  - The Video API is asynchronous: submit a job, then poll or receive a webhook.
  - The Upload API (V2) lets you "upload your own image/video assets or custom script audio" (e.g. your own TTS) for use in Video API videos.
  - Sources: [V Synthesia API docs](https://docs.synthesia.io/reference/introduction); [V Synthesia API page](https://www.synthesia.io/api)
- The homepage example is a POST to the v2 videos endpoint, with the Authorization header read from an environment variable and a JSON body holding `title` and an `input` array (script text, avatar ID, background). — [V synthesia.io](https://www.synthesia.io/)
- The API allows up to 360 min of video per year, deducted from the plan's limits, and is available on Creator ($89/mo) and above. — [V Synthesia API docs](https://docs.synthesia.io/reference/introduction); [R AIStackPicks](https://aistackpicks.com/reviews/synthesia-pricing-2026/)
- Docs describe personal-avatar creation in the web UI. Whether the avatar-creation step is exposed through the API was **not confirmed**. — [V Personal avatars docs](https://docs.synthesia.io/docs/personal-avatars)

#### Captions / Mirage
- **Create call:** `POST https://api.mirage.app/v1/videos` (multipart) with `model=mirage-avatar-x`.
  - Input is an **audio clip (required)** plus **either an image reference or a video reference**, not both.
  - Returns a **720p MP4**. Auth uses an `x-api-key` header; Python, JS and curl examples are provided.
  - Sources: [V Avatar X getting started](https://captions.ai/help/docs/api/video-generation); [V Create Video reference](https://captions.ai/help/api-reference/videos/create-video); [V Mirage API overview](https://captions.ai/help/docs/api/overview)
- **Async flow:** poll `GET /v1/videos/{video_id}` through QUEUED, PROCESSING, then COMPLETE, FAILED or CANCELLED. A content endpoint redirects to the final video URL. — [V Mirage API reference](https://captions.ai/help/api-reference/api)
- **Price:** $0.15/s in 6-s increments, billed separately from app subscriptions. — [V Captions API pricing](https://captions.ai/help/docs/api/pricing)
- A third-party API catalog calls the video-generation API "Beta". Help-center pages were updated 28–210 days before the search. — [T api-evangelist/captions-ai](https://github.com/api-evangelist/captions-ai)
- Also available through fal.ai. — [V fal.ai Mirage Avatar X](https://fal.ai/models/mirage-api/avatar-x/reference-to-video)

#### Tavus
- The free plan includes API access (25 stock replicas, 30+ languages). — [R The Rundown](https://www.therundown.ai/tools/tavus); [R The Rundown (Phoenix-4)](https://www.therundown.ai/tools/phoenix-4)
- Developer docs say API flows can use "Image to Face", and users must hold the rights to any images or likenesses they upload. — [V Tavus docs, Faces overview](https://docs.tavus.io/sections/faces/overview)
- Custom replicas are gated to paid tiers, and concurrent real-time streams are capped by tier. — [R AI Alleyway](https://aialleyway.com/tavus-review/); [C Spatius](https://www.spatius.ai/blog/spatius-vs-tavus/)
- One review describes video-trained replicas made from "a short authorized recording" and "image-to-replica creation on eligible tiers". — [R AITroveX](https://aitrovex.com/tool/tavus)

#### Argil
- **Create call:** `POST https://api.argil.ai/v1/videos`. A video is a list of "moments", each with an avatar ID, a transcript **or audio**, and a voice ID. Renders are asynchronous to MP4, and webhooks are available. A separate Avatars API handles cloning and listing avatars. — [V Argil Create a Video](https://docs.argil.ai/api-reference/endpoint/videos.create); [T api-evangelist/argil](https://github.com/api-evangelist/argil); [V Argil llms.txt](https://docs.argil.ai/llms.txt)
- Credit rates are as in Q1, with non-expiring pay-as-you-go credits. — [V Argil API pricing](https://docs.argil.ai/resources/api-pricings)
- Which plans include the API is unclear: Techjockey lists it on both Classic and Scale, which doesn't match other sources. — [R Techjockey](https://www.techjockey.com/us/detail/argil)

#### Akool
- **Talking-photo request (official docs):** `talking_photo_url`, `audio_url`, `resolution` ("720"; a prompt-driven variant uses 1080) and `webhookUrl`. — [V Akool Talking Photo API](https://docs.akool.com/ai-tools-suite/talking-photo)
- **Endpoint path (third-party listing, unverified):** `POST /api/open/v3/content/video/createbytalkingphoto`, with status via `GET /api/open/v3/content/video/infobymodelid`. — [T APIs.io Akool](https://apis.io/providers/akool/)
- Responses include a `deduction_credit` field that reports credits charged per call. — [V Akool Image-to-Video docs](https://docs.akool.com/ai-tools-suite/image2video)
- A `voice_id` is used by both the talking-photo and audio interfaces. VoiceLab docs exist. — [V Akool VoiceLab](https://docs.akool.com/ai-tools-suite/voiceLab); [V Akool audio docs (test site)](https://docstest.akool.io/ai-tools-suite/audio)
- The official API pricing page puts talking photo under Enterprise ("Let's Talk"), so self-serve API access for talking photo is unclear. — [V Akool API pricing](https://akool.com/api-pricing)

#### Vidnoz
- The official Open API pricing (Q1) includes a 30-credit/month free trial. — [V Vidnoz Open API limits](https://www.vidnoz.com/overview/limits.html)
- Atlas Cloud says Vidnoz's published API docs list endpoints for portrait generation, talking avatars and text-to-avatar, with no face-swap API. It also found the English API landing page returning 404 on July 29, 2026. — [C Atlas Cloud](https://www.atlascloud.ai/blog/guides/vidnoz-ai-face-swap)
- Sources disagree on which consumer plan includes the API (Business vs Enterprise). — [R ToolJunction](https://www.tooljunction.io/ai-tools/vidnoz-ai); [R AIsoTools](https://aisotools.com/pricing/vidnoz)

### Inferences

| Platform | Self-serve API | One photo + your own audio in one call | Billing unit | Max length (documented) | Render time (documented) | Watermark on API output |
|---|---|---|---|---|---|---|
| Hedra | Yes | **Yes** (start frame + ≤ 4 audio clips) | $/s (2.5–6.25¢) or credits (disputed) | **10 min** | not found | not found |
| D-ID | Yes (self-serve + trial) | **Yes** (`source_url` + audio script) | subscription credits (~4/min) | not found | **"typically 10–30 s"** | not found |
| Mirage Avatar X | Yes (x-api-key; also fal) | **Yes** (image *or* video ref + required audio) | $0.15/s, 6-s blocks | not found | not found | not found |
| Akool | Docs public; tier opaque | **Yes** (`talking_photo_url` + `audio_url`) | credits (10/5 s official) | not found | not found | not found |
| Vidnoz | Free trial; Pro $80/mo | Unconfirmed | credits (4/min video) | 3 min/video on free web plan (one source) | not found | not found |
| Argil | Yes | Audio yes; needs a trained avatar | credits (160/min) | not found | not found | not found |
| Synthesia | Creator $89+/mo only | Custom audio via Upload API; avatar must exist first | plan minutes (≤ 360/yr) | not found | not found | (paid plans: no watermark) |
| Tavus | Yes (free plan includes API) | Image to Face via API; replicas need consent | conversation minutes | not found | not found | not found |

- For an agent driving curl or Python from a GPU-less Linux box, Mirage and Hedra are the cleanest fits. Mirage documents a multipart upload of local files, an `x-api-key` header and async polling. Hedra's page gives file-size limits for the image and audio, which suggests direct uploads, but I did not verify its upload mechanism or auth header. D-ID and Akool want **hosted URLs** (`source_url` must be https or s3; `talking_photo_url`/`audio_url`). So the agent first needs somewhere to host the files, or an upload endpoint, which I did not verify.
- Mirage's video-reference option is the only documented API path that takes a **short selfie video directly**, without a separate avatar-training step.

### Gaps
- Watermarking of free-trial or low-tier **API** output: no vendor documentation retrieved, for any vendor.
- Render times for Hedra, Mirage, Akool, Vidnoz, Argil and Tavus: not found.
- Max clip length for D-ID, Mirage, Akool, Argil and Synthesia (API): not found.
- D-ID's exact audio-script schema (field names, accepted audio formats) and whether failed talks consume credits through the API.
- Whether Hedra API calls need a minimum prepaid top-up, and how big it is.
- Whether Synthesia personal avatars or Tavus Image-to-Replica can be created *via API*.

---

## 3. Input requirements: single still photo vs selfie video vs studio footage, and which works better

### Takeaway
- **Photo-only, no training step:** Hedra Character-3, D-ID Talks, Mirage Avatar X (image *or* short video reference), Akool talking photo and Vidnoz talking photo.
- **Photo or video, with a recorded consent step:** Synthesia now accepts a single photo or a video for personal avatars, but requires a live consent video. Tavus documents photo-based paths (Image-to-Replica / Image to Face) alongside its consented ~2-min video replicas.
- **Video-trained:** Argil needs about a 2-min recording. Captions claims a twin from about 10 s of footage.
- I found no independent head-to-head of photo-driven versus video-trained likeness quality.

### Cited Findings
- **Hedra:** a single start-frame image plus audio; no training step is described. — [V Hedra Character 3 API](https://www.hedra.com/develop/models/video/hedra-character-3)
  - Reviewers: "busy source images throw it off"; best results come from "a clean portrait with clear audio". (Not pinned.) — [R Lovart](https://www.lovart.ai/blog/hedra-ai-review); [R DroidCrunch](https://droidcrunch.com/hedra-review/); [R PromptsRush](https://promptsrush.com/blog/hedra-review)
- **D-ID:** a single jpg/png via `source_url`. — [V D-ID Create a talk](https://docs.d-id.com/reference/createtalk)
  - A 2026 review says clean, well-lit, front-facing photos with a neutral expression work best. (Not pinned.) — [R TechBotHQ](https://techbothq.com/d-id-review/); [R SmartRemoteGigs](https://smartremotegigs.com/software/d-id/)
- **Synthesia:** "Personal avatars are built from a single photo or a video, and a consent video must be recorded live." Video footage can be .webm, .mp4 or .mov, up to 2 GB. — [V Synthesia personal avatars docs](https://docs.synthesia.io/docs/personal-avatars); [V help center, personal avatar requests](https://help.synthesia.io/en/articles/10371261-how-do-i-use-personal-avatar-requests-in-synthesia); [V custom avatar page](https://www.synthesia.io/features/custom-avatar)
- **Captions/Mirage:**
  - Vendor claim: an AI twin needs "only about 10 seconds of footage".
  - The Avatar X API takes an image or a video reference plus audio.
  - A review says you can build a digital twin from reference footage on Max and up.
  - Sources: [V Captions AI Twin page](https://captions.ai/features/create-ai-twin); [V Avatar X API guide](https://captions.ai/help/docs/api/video-generation); [R Kompozy](https://kompozy.io/reviews/captions-ai)
- **Tavus:**
  - Video replicas come from a short authorized recording, with a written authorization statement read on camera (Tavus blog). A third-party guide describes the consent as verbal and on camera.
  - Image-to-Replica and API "Image to Face" are available on eligible tiers.
  - Sources: [V Tavus blog, How to make an AI clone of yourself](https://www.tavus.io/blog/how-to-make-an-ai-clone-of-yourself); [V Tavus blog, Image-to-Replica](https://www.tavus.io/blog/introducing-image-to-replica); [V Tavus docs, Faces](https://docs.tavus.io/sections/faces/overview); [R eesel.ai](https://www.eesel.ai/blog/tavus)
  - One source says replica quality depends on the source footage. (Not pinned.) — [R OnyxRanked](https://onyxranked.com/tavus-review-2026/)
- **Argil:** clone training "needs only about 2 minutes of footage". — [R Traksource (hands-on)](https://traksource.com/argil-ai-review/); [R The Rundown](https://www.therundown.ai/tools/argil)
- **Akool:** a single photo URL plus an audio URL. — [V Akool Talking Photo API](https://docs.akool.com/ai-tools-suite/talking-photo)
  - A reviewer says its avatars "look stylized rather than like a faithful clone". (Not pinned.) — [R Vidmetoo review](https://www.vidmetoo.com/akool-review/); [R MSPowerUser](https://mspoweruser.com/akool-ai-review/)
- **Vidnoz:** talking photo works from an uploaded image. Clean, high-resolution source photos hold up on simple motion; low-resolution inputs and busy scenes do worse. — [C Pexo](https://pexo.ai/blog/vidnoz-image-to-video-review-1126); [R Unite.AI](https://www.unite.ai/vidnoz-review/)

### Inferences
- The user's two input options map like this:
  - **One photo:** Hedra, D-ID, Mirage, Akool and Vidnoz work directly via API, with no consent recording mentioned in the retrieved docs.
  - **Short selfie video:** Mirage's video-reference API, or the consented replica and twin products (Tavus, Captions twin, Argil, Synthesia). The consented products are either over budget for API use or not API-driven.
- Every photo-driven tool's reviews stress a clean, front-facing, well-lit, uncluttered portrait. That is the cheapest quality lever for the experiment.

### Gaps
- No practitioner A/B of photo-driven versus video-trained likeness (fidelity to the real person) for any of these tools.
- D-ID Express avatars (made from about 1 min of video) and Premium+ (longer footage): current input and consent rules not retrieved.
- Captions twin consent and verification steps: not retrieved.

---

## 4. Practitioner opinions on realism: lip-sync, motion, expression, uncanny valley, artifacts, behaviour past 10–20 s, comparisons

### Takeaway
Independent evidence is thin, and Reddit was unreadable. Most "reviews" are affiliate or competitor content.
- **Photo-driven:** Hedra Character-3 gets the most consistently positive lip-sync and expression comments, with drift in fast speech and frequent re-rolls. Mirage Avatar X twins are called "among the most realistic" but "the tell shows on longer or more emotive scripts".
- **D-ID:** split opinions; older Reddit posts report uncanny-valley problems, and 2026 reviews call it fine for presenters but behind HeyGen in photorealism.
- **Synthesia Express-2:** polished full-body gestures, but MIT Technology Review found it turns everyone into a generic "hyperactive hype man".
- **Tavus:** convincing visuals with a robotic cloned voice.
- **Argil:** decent short-form output with mouth blur in fast speech.
- **Akool / Vidnoz:** usable but stylized or less natural.
- **Against HeyGen:** where sources compare against HeyGen, they mostly rate HeyGen highest for realism.

### Cited Findings

#### Hedra (Character-3)
- **Best-case sync:** on "a clean portrait with clear audio, the sync is among the best you will get from a consumer tool right now". It "handled tongue-twisting phrases cleanly", but "fast speech and hard consonants can still drift". (2026 hands-on review; not pinned.) — [R Lovart](https://www.lovart.ai/blog/hedra-ai-review); [R DroidCrunch](https://droidcrunch.com/hedra-review/)
- **Expression:** eyebrows shift, the head nods, and expressions track the emotion of the words; plosives (p, b) and labials (m, v) show correct lip contact; eyes blink at human cadence. (2026 reviews; not pinned.) — [R PromptsRush](https://promptsrush.com/blog/hedra-review); [R AIMagic](https://aimagic.fun/blog/hedra-review); [C Filmora (Wondershare)](https://filmora.wondershare.com/video-editor-review/hedra-ai-review.html)
- **Cost and resolution:** "credits drain faster than you'd expect, output is capped at 720p, and you'll usually re-roll a generation or two before one lands." (Not pinned.) The 720p cap conflicts with the API's 1080p price tier. — [R DroidCrunch](https://droidcrunch.com/hedra-review/); [R Lovart](https://www.lovart.ai/blog/hedra-ai-review)
- **Older evidence:** a Tom's Guide lip-sync comparison ranked Hedra first, but in the Character-2 era (2024 or early 2025; outdated). — [J Tom's Guide](https://tomsguide.com/ai/ai-image-video/lip-sync-battle-i-put-3-leading-ai-video-tools-to-the-test)
- **Trustpilot users:**
  - Positive: "maintains facial identity much better than other models".
  - Negative: "hand and mouth distortions"; many tries needed to reach "a minimum acceptable standard".
  - Source: [U Trustpilot Hedra (~36–39 reviews, 2025–2026)](https://www.trustpilot.com/review/hedra.com)
- **Red flag on review quality:** one review page cites an "MIT Technology Review study showing a 300% realism gain" that the digest could not verify. (Not pinned.)

#### D-ID
- **Older Reddit posts, quoted by a review site:**
  - A 2024 r/singularity commenter said it "didn't look very realistic while speaking".
  - A 2023 r/StableDiffusion user reported uncanny-valley issues and limited creative control.
  - One comparison rates Synthesia's output better and D-ID faster.
  - **Outdated (2023–2024).** Not pinned; likely [R AIToolsPolice](https://aitoolspolice.com/reviews/d-id/)
- **2026 reviews:**
  - "Lip-sync generally smooth, but in longer conversations or more emotional scenes, certain avatars can still feel slightly artificial or repetitive."
  - Presenter clips are "comfortably above the uncanny valley for most business use cases".
  - A less favourable review: "noticeably inferior to the photorealism offered by competitors like HeyGen, often resulting in an artificial appearance."
  - Not pinned among [R TechBotHQ](https://techbothq.com/d-id-review/), [R FahimAI](https://www.fahimai.com/d-id), [R Agentaya](https://agentaya.com/ai-review/d-id/), [R SmartRemoteGigs](https://smartremotegigs.com/software/d-id/)
- A product-review aggregator reports that reviewers mostly praise how quickly and easily it makes talking-avatar videos, with lip sync and facial animation counted as positives. (Not pinned.) — [U Product Hunt D-ID reviews](https://www.producthunt.com/products/d-id/reviews); [R Faceless.directory](https://faceless.directory/directory/d-id)
- Recent Trustpilot reviewers (mid-2026) praise "realistic avatars, strong lip-sync". — [U Trustpilot D-ID](https://www.trustpilot.com/review/www.d-id.com)

#### Synthesia (Express-1/Express-2 personal avatars)
- MIT Technology Review's reporter tested an Express-2 clone of herself. She found it "remodels every person it's presented with into a polished professional speaker with the body language of a hyperactive hype man". **Sept 2025; independent, sample of one.** — [J MIT Technology Review, 2025-09-04](https://www.technologyreview.com/2025/09/04/1123054/synthesias-ai-clones-are-more-expressive-than-ever-soon-theyll-be-able-to-talk-back/)
- Reviewers call Express-2 "a real generational step". The gains: audio-driven hand and full-body gestures, tighter lip-sync, selectable camera angles and multiple voice styles. (Not pinned.) — [R AIToolAnalysis](https://aitoolanalysis.com/synthesia-review/); [R AIWorthIt](https://www.aiworthit.com/blog/synthesia-review/); [R Cybernews](https://cybernews.com/ai-tools/synthesia-ai-review/)
- **Duration:** "in 60-second blind tests, [Express avatars] fool most casual viewers, but in 5-minute training videos, viewers paying close attention still notice the tells". Method and sample size are not stated. It is also "not great for emotional, heartfelt content". (Not pinned.) — [R AIToolAnalysis](https://aitoolanalysis.com/synthesia-review/); [R Vantaige](https://vantaige.io/ai-tool/synthesia)
- Reddit users quoted by review sites say it "has not yet crossed the uncanny valley" and complain about lip movements; others say viewers ask whether it's a real person. — [C Creatify](https://creatify.ai/review/synthesia-ai); [R Cybernews](https://cybernews.com/ai-tools/synthesia-ai-review/)
- Trustpilot reviewers say "Synthesia has the most realistic avatar-generated results". — [U Trustpilot Synthesia (~1,700–1,800 reviews)](https://www.trustpilot.com/review/synthesia.io)

#### Captions / Mirage Avatar X
- **Vendor claims:** "most audiences won't be able to tell the difference" between real and twin footage. The model was "designed to solve common pitfalls with video avatars: identity preservation and microexpressions". — [V Captions AI Twin](https://captions.ai/features/create-ai-twin); [V Mirage Avatar X blog](https://captions.ai/blog/mirage-avatar-x)
- **Reviews (2026):**
  - "Among the most realistic in the category."
  - "Good but not flawless — the tell shows on longer or more emotive scripts."
  - "Expressiveness is a real strength; per-clip generation burns credits."
  - Not pinned among [R Prizmad](https://prizmad.com/review/captions-ai), [R Kompozy](https://kompozy.io/reviews/captions-ai), [R Fastlane](https://www.usefastlane.ai/review/captions), [C HitPaw Edimakor](https://edimakor.hitpaw.com/ai-video-tools/captions-mirage-review.html)

#### Tavus (Phoenix-3/Phoenix-4)
- **Visuals:** one reviewer found the replica render "the most convincing they had tested… held up on a live call rather than looking like an animated character". — [R AI Alleyway](https://aialleyway.com/tavus-review/) (not pinned)
- **Voice is the weak point:** cloned replica voices are "described by multiple independent reviewers as robotic, lacking the natural emotional cadence"; one says the voice "occasionally sounds like a GPS narrator". (Not pinned.) — [R OnyxRanked](https://onyxranked.com/tavus-review-2026/); [R ToolPorto](https://toolporto.com/reviews/tavus); [R Mariano Rodrigo](https://www.marianorodrigo.com/tavus-conversational-video-ai-review)
- **Vendor claim:** Phoenix "move[s] the entire face", leading to realism. — [V Tavus Phoenix blog](https://www.tavus.io/blog/introducing-phoenix-the-tavus-developer-platform-public-beta)

#### Argil
- **Traksource hands-on (favourable):**
  - Lip-sync and eyebrow movement looked good.
  - But: "slight blur around the mouth during fast speech", "occasional missed blinks", and "hands that can clip through the body".
  - Source: [R Traksource](https://traksource.com/argil-ai-review/)
- **FrankX blog (June 2026):** rates HeyGen highest for realism. It says Argil's avatars are "paced for short-form social video rather than class-leading realism". Rule of thumb: a personal clone or marketing video goes to HeyGen, a faceless short-form channel to Argil. — [R FrankX](https://www.frankx.ai/blog/heygen-vs-synthesia-vs-argil-2026)
- Influencer AI recommends HeyGen for realism and Argil for a personal clone on social feeds. — [R Influencer AI](https://influencerai.net/heygen-vs-argil-vs-synthesia-ai-avatar-video-showdown/)
- Argil's own "best HeyGen alternative" post is promotional. — [C Argil blog](https://www.argil.ai/blog/argil-the-best-heygen-alternative-for-content-creators-2)
- A Trustpilot reviewer calls the videos "low quality" with "unconvincing actors". — [U Trustpilot Argil (4 reviews)](https://www.trustpilot.com/review/argil.ai)

#### Akool
- Talking photo is "not quite as perfect as it sounds", and avatars "look stylized rather than like a faithful clone". (Not pinned.) — [R MSPowerUser](https://mspoweruser.com/akool-ai-review/); [R Vidmetoo](https://www.vidmetoo.com/akool-review/)
- Positive framing: Unite.AI's "The Most Lifelike AI Avatar Yet?". — [R Unite.AI](https://www.unite.ai/akool-avatar-review/)
- Competitor review: Argil's "Honest Take". — [C Argil blog on Akool](https://www.argil.ai/blog/akool-ai-avatars-9416a)

#### Vidnoz
- **Reviews:**
  - "Lip-syncing was on-point" but "the entire video felt a bit rushed and lacked engagement".
  - "Some avatars may still look slightly artificial, especially in close-up."
  - Avatar lip sync "feels less natural than paid competitors".
  - Not pinned among [R Unite.AI](https://www.unite.ai/vidnoz-review/), [C Media.io](https://www.media.io/comparison/vidnoz-ai-review.html), [C Playcut](https://playcut.ai/blog/vidnoz-alternatives/)
- A few Trustpilot users praise avatar and lip-sync quality. — [U Trustpilot Vidnoz](https://www.trustpilot.com/review/www.vidnoz.com)

### Inferences
- For a 45–60 s talking-to-camera clip, the "longer or more emotive script" weakness flagged for Captions and D-ID, and Synthesia's "tells" at 5 min, suggest that 45–60 s sits near the edge where current tools still pass casual viewing.
- Reports of drift in fast speech (Hedra, Argil) suggest a calm, evenly paced script and audio will help.
- Where HeyGen is compared directly (FrankX, Influencer AI, a D-ID review), it is usually rated more realistic than D-ID and Argil. Most of these sources are affiliate content, and none is a blind test.

### Gaps
- No Reddit, Hacker News or YouTube shootout content could be read (fetching blocked; Reddit blocked from search). So there are **no first-hand practitioner threads with sample sizes**.
- No independent blind comparison of Hedra Character-3 vs Mirage Avatar X vs D-ID on the *same* photo and audio was found.
- Behaviour past 20 s is documented only anecdotally (Synthesia 60 s vs 5 min; Captions and D-ID "longer scripts"). Nothing was found for Hedra, Akool or Vidnoz.
- AWS Marketplace hosts many Synthesia reviews (results surfaced pages 68 and 118), but their content was not summarized. — [U AWS Marketplace Synthesia reviews](https://aws.amazon.com/marketplace/reviews/reviews-list/prodview-4gualii44yjze?page=68)

---

## 5. Practitioner complaints: credit burn, failed renders charged, auto-renew and cancellation, refunds, bans, support

### Takeaway
Billing and renewal complaints are the dominant theme for almost every vendor.
- **Akool** has the most severe allegations: repeated card charges, cancelled trials rolling into annual plans, and Trustpilot removing fake reviews.
- **Hedra** (TrustScore about 1.9/5 from about 36–39 reviews): renewals after cancellation, plans "silently re-enabled", refusals, and credits burned on re-rolls.
- **Vidnoz** (2/5 from 82): unclear yearly charges, hard cancellation, free tier that never activated.
- **Argil** (2.5/5 from only 4): trial paywall and refused refunds.
- **D-ID** (1.6/5 from 26 on one regional page): failed renders consuming credits, renewal and refund trouble.
- **Synthesia:** large and mostly positive sample, but complaints about stranded credits, over-eager moderation, AI-only support and an affiliate ban.
- **Captions/Mirage:** polarized; support is praised, but there are forced-migration complaints.

### Cited Findings
- **Hedra (Trustpilot, about 36–39 reviews, TrustScore about 1.9–2/5, 2025–2026):** — [U Trustpilot Hedra](https://www.trustpilot.com/review/hedra.com); [U page 2](https://www.trustpilot.com/review/hedra.com?page=2)
  - "Subscription keeps silently renewed and money charged after cancellation."
  - "My cancelled plan keeps getting re-enabled silently."
  - Conflicting cancellation messages about whether credits are lost immediately.
  - Refund denials, unanswered emails, and support that "keeps summarizing their complaints back to them without resolving anything".
  - Credits used up across many retries.
  - The founder replied publicly, and one long-term user says the platform improved and the team was responsive.
- **D-ID (Trustpilot: IE snapshot 1.6 from 26 reviews; about 40 reviewers on the global page; many negatives from 2023–2025, some from mid-2026):** — [U Trustpilot D-ID](https://www.trustpilot.com/review/www.d-id.com); [U IE page](https://ie.trustpilot.com/review/www.d-id.com)
  - Slow or absent support (one reviewer calls it "excellent", another "nonexistent").
  - **Failed video generations that still consume credits.**
  - Difficulty cancelling or getting refunds after auto-renewal.
  - Watermarks and little video time on low plans.
  - A review site mentions "documented charge-after-cancellation complaints". (Not pinned.) — [R AIToolsPolice](https://aitoolspolice.com/reviews/d-id/)
- **Synthesia (Trustpilot, about 1,700–1,800 reviews, broadly positive but split):** — [U Trustpilot Synthesia](https://www.trustpilot.com/review/synthesia.io)
  - "If you don't have enough credits remaining to generate a complete video, those credits become effectively unusable."
  - A user needed a yearly subscription to get about 6 hours of generation.
  - **Moderation false positives:** a "singles party for professionals" video was flagged as adult content.
  - Charged for a full year upfront after a free trial, and refused a refund.
  - "The support service is just an AI chat."
  - An affiliate says their account was permanently banned and earnings confiscated over a keyword issue.
- **Captions/Mirage (Trustpilot, polarized):** — [U Trustpilot captions.ai](https://www.trustpilot.com/review/captions.ai); [U NZ page](https://nz.trustpilot.com/review/captions.ai); [U Trustpilot mirage.app](https://www.trustpilot.com/review/mirage.app)
  - Ratings: one page 4.3 from 307 reviews; NZ page 1.6 from 72; Captions 2.8 from 118 on the Mirage page.
  - Complaints: cross-device sync problems, web and desktop glitches, a forced move to Mirage Studio, credit-based pricing, and refund denials.
  - Praise: support responsiveness, with some charges refunded or voided.
- **Tavus:** no Trustpilot listing found; results were unrelated businesses. One review notes the public pricing page and dashboard disagree. — [R AI Alleyway](https://aialleyway.com/tavus-review/)
- **Argil (Trustpilot, 2.5/5 from 4 reviews; tiny sample):** — [U Trustpilot Argil](https://www.trustpilot.com/review/argil.ai)
  - The advertised 5-day trial leads to a paywall.
  - Charged after less than 2 days of trial.
  - Refunds refused, including an annual plan and an EU 14-day withdrawal claim.
  - Credits run out quickly; support unresponsive.
  - A complaint filed with Brazil's PROCON consumer agency went unanswered.
- **Akool (Trustpilot; regional pages disagree: 2/5 across 181 reviews vs 4.3 across about 434):**
  - The card was "charged 11 times in half an hour".
  - Unfamiliar charges.
  - A cancelled trial rolled into an annual plan.
  - A $912 annual-plan charge with no receipt.
  - The cancel option was hard to find; the chatbot stalled.
  - Support cancelled a subscription unasked, then refused to reactivate it.
  - Credits expire monthly.
  - Some refunds were granted after dispute; Akool's Trustpilot replies point to admin@akool.com.
  - **Trustpilot notes it removed fake reviews for the company.**
  - Sources: [U Trustpilot Akool](https://www.trustpilot.com/review/akool.com); [U UK page 2](https://uk.trustpilot.com/review/akool.com?page=2); [U CA page 9](https://ca.trustpilot.com/review/akool.com?page=9)
  - A review site reports a $252 annual charge that repeated after cancellation, with refund requests going nowhere. One reviewer found credit burn varied about 12× across features and models. (Not pinned.) — [R Vidmetoo](https://www.vidmetoo.com/akool-review/); [R EverydayAITuts](https://everydayaituts.com/ai-video-tools/akool-review)
- **Vidnoz (Trustpilot, 2/5 from 82 reviews, 45% 1-star; another regional page shows 64; reviews run into Aug 2026):** — [U Trustpilot Vidnoz](https://www.trustpilot.com/review/www.vidnoz.com); [U AU page](https://au.trustpilot.com/review/www.vidnoz.com)
  - Forced shift from pay-as-you-go credits to subscriptions.
  - Repeated payment failures on upgrade.
  - A yearly charge that wasn't clear at checkout.
  - Cancellation hard to find, or requiring an email to support.
  - Free tier "never activated", or the limit reached without use.
  - Browser crashes; creations lost after a platform change.
  - A few smooth cancellations and positive quality reviews.
  - The company replies on Trustpilot and disputed "hidden tools and paid reviews" claims.

### Inferences
- **For a one-off experiment:** prefer metered or prepaid API billing (Hedra per-second, Mirage per-second, Argil's non-expiring pay-as-you-go credits) over subscriptions. Avoid annual plans. If a subscription is unavoidable, cancel auto-renew right after the test and check whether credits survive until period end, since Hedra reviewers report contradictory messages on this and several vendors face silent-renewal complaints. A virtual or limit-capped card limits exposure, which matters most for Akool.
- EU withdrawal rights appear in the Argil complaints. A US user likely has weaker statutory refund leverage, so card chargebacks would be the fallback. This is general inference, not checked against each vendor's terms.
- Re-roll cost matters: reviewers report 1–2+ re-rolls for Hedra, and D-ID users report failed renders being charged. Budget 2–3 attempts per clip.

### Gaps
- G2 and Capterra pages were not reached; only Trustpilot and Product Hunt surfaced.
- None of the Trustpilot samples can be checked for authenticity. Review dates are mixed, and some regional pages duplicate each other.
- Account bans of ordinary (non-affiliate) users for likeness or deepfake moderation: none found.
- No source on whether Hedra, Mirage, Akool or Vidnoz refund credits for failed API renders.

---

## 6. Consent and verification to make a likeness of yourself; data retention and training of uploaded faces and voices (brief)

### Takeaway
In the retrieved material, only Synthesia (a live consent video for personal avatars) and Tavus (explicit, informed consent; an on-camera authorization statement; rights to uploaded images) document a consent gate. The photo-input APIs (Hedra, D-ID, Mirage, Akool, Vidnoz) take an arbitrary image file or URL, and their retrieved docs describe no identity or consent check. Data-retention and model-training terms were not retrieved for any vendor.

### Cited Findings
- **Synthesia:** "a consent video must be recorded live to confirm that Synthesia has the right to create the personal avatar". This applies to avatars built from a single photo or a video. — [V Synthesia personal avatars docs](https://docs.synthesia.io/docs/personal-avatars); [V help center, personal avatar requests](https://help.synthesia.io/en/articles/10371261-how-do-i-use-personal-avatar-requests-in-synthesia)
  - Custom voice creation (cloning) is "available to Enterprise plan users and can be paired with a personal avatar". This conflicts with reviews describing personal avatars as "trained on your face and voice" on self-serve plans. — [V Synthesia custom voices docs](https://docs.synthesia.io/docs/custom-voices); [R AIStackPicks](https://aistackpicks.com/reviews/synthesia-pricing-2026/)
- **Tavus:** the Acceptable Use Policy says "Creating a Customer Replica requires the explicit, informed consent of the individual depicted in the Seed Files". The customer must obtain and maintain that consent, honour revocation requests, and keep use within scope; the policy also covers API-created content. — [V Tavus Acceptable Use Policy](https://www.tavus.io/acceptable-use-policy)
  - A written authorization statement is read on camera. — [V Tavus blog](https://www.tavus.io/blog/how-to-make-an-ai-clone-of-yourself)
  - Image to Face users must hold the rights to the images or likenesses they upload. — [V Tavus docs, Faces](https://docs.tavus.io/sections/faces/overview)
  - A third-party guide notes "a usable source image is not the same as permission". — [R AnyGen](https://www.anygen.io/showcase/tavus-ai/index.html)
- **Hedra:** the Character-3 API takes any start-frame image; no consent step appears in the retrieved developer page. — [V Hedra Character 3 API](https://www.hedra.com/develop/models/video/hedra-character-3)
- **D-ID:** `source_url` takes any jpg or png URL; no consent step appears in the retrieved docs. — [V D-ID Create a talk](https://docs.d-id.com/reference/createtalk)
- **Mirage:** image or video reference plus audio; no consent step appears in the retrieved docs. — [V Avatar X API guide](https://captions.ai/help/docs/api/video-generation)
- **Akool:** `talking_photo_url` plus `audio_url`; no consent step appears in the retrieved docs. — [V Akool Talking Photo API](https://docs.akool.com/ai-tools-suite/talking-photo)

### Inferences
- For a user cloning **themselves**, consent gates are a formality: record the statement or the live consent clip. They do mean those flows need the user's own camera and a browser, which works against an agent-only, API-only pipeline. Photo-in APIs avoid that friction.
- "No consent step appears in the retrieved docs" does **not** mean the terms of service don't require consent. Each vendor's ToS very likely bars non-consensual likeness use, but I did not verify this.

### Gaps
- Retention periods, deletion on request, and whether uploaded faces or voices are used to train models: **not retrieved for any vendor** (the privacy researcher covers this).
- Hedra, D-ID, Argil, Akool, Vidnoz and Captions ToS or acceptable-use clauses on likeness and consent: not retrieved.
- Whether Tavus Image-to-Replica or Synthesia photo avatars still need a live video consent clip when created from a photo: not confirmed. Synthesia's docs imply yes.
