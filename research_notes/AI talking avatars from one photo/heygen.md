# HeyGen (web app + API) for a lip-synced talking clip from one photo or a short selfie video — notes as of 2026-10-23

Method note (applies to every section): this research sandbox's egress proxy refused connections to www.heygen.com, help.heygen.com, docs.heygen.com and developers.heygen.com, and the search tool cannot reach reddit.com. Official HeyGen facts below come from search-engine summaries and snippets of the named official pages, cited to those pages. They were not read in full, so re-check exact numbers on the live pages before spending money. Separately, I read HeyGen's own PyPI, npm and GitHub package files directly. The shared web-search budget ran out before I could cover the ToS/AUP likeness clauses, voice-clone quality reviews, G2/BBB ratings and YouTube transcripts; those are listed under Gaps. Source labels: **[official]** = HeyGen-owned page; **[3P]** = third-party blog or review site; **[competitor]** = a site that appears to sell a competing AI video/avatar product; **[user]** = an individual user review or forum post. Short quoted fragments from Trustpilot, BBB, G2 and review blogs are search-snippet wording and may be lightly paraphrased; check the live page before quoting any of them verbatim in the report. Quotes from HeyGen docs are likewise snippet text.

## 1. Current web plans (Free, Creator, Pro, Business, Enterprise): price, credits, free-tier limits, photo-avatar / digital-twin / Avatar IV–V access

### Takeaway
Free gives about 3 watermarked videos a month, each up to 1 minute (1–3 depending on region), and Avatar IV is capped at 3 uses a month, each up to 1 minute. That is enough for a single watermarked browser test of a 45–60 s clip. Creator ($29/mo, or about $24/mo billed annually) is the cheapest watermark-free tier at about 600 credits, roughly 30 minutes of Avatar IV. It is a recurring subscription, used mainly in the browser, and billed separately from the API.

### Cited Findings
- **Free (Oct 2026):** $0; "3 videos a month, watermarked"; "Videos up to 1 minute each". The pricing table lists Avatar IV as "Free: 3 uses/month" with a 1-minute maximum per Avatar IV video. — [HeyGen pricing [official]](https://www.heygen.com/pricing)
- **Free, per the avatars page (Oct 2026):** "The Free plan includes 1 to 3 videos (it varies by region)", shared at 720p with a watermark. It also includes "One Custom Video Avatar, plus 500+ ready-made presenters" and one voice clone. — [HeyGen avatars page [official]](https://www.heygen.com/avatars). Sources conflict on Free resolution: some third-party reviews say 720p, while HeyGen's pricing pages give no Free resolution. — [HeyGen pricing [official]](https://www.heygen.com/pricing)
- **Creator removes branding** and allows "Videos up to 30 minutes and 1080p export". — [HeyGen pricing [official]](https://www.heygen.com/pricing)
- **Creator price and credits (third-party, Aug–Oct 2026):** $29/month or about $24/month billed annually, 600 credits/month. One roundup says it checked HeyGen's pricing page on 2026-10-18. At about 20 credits per Avatar IV minute, 600 credits ≈ 30 minutes of Avatar IV per month. — [Arcade [3P]](https://www.arcade.software/post/heygen-pricing); [Fastlane [3P]](https://www.usefastlane.ai/pricing/heygen); [Justin McKelvey [3P]](https://justinmckelvey.com/blog/heygen-pricing)
- **Credit-burn conflict:** HeyGen's help center lists Avatar IV "Photo Look" at 16 credits/min, while a 2026 HeyGen blog table says 20 credits/min. The 16-credit figure most likely comes from this help-center article, but the snippet didn't say which one. — [Avatar & Voice FAQ [official]](https://help.heygen.com/en/articles/15544929-avatar-voice-faq-troubleshooting-best-practices-and-credits)
- **Older or conflicting Creator figures (likely outdated):**
  - 200 credits ≈ 10 min of Avatar IV, from a May 2026 review. — [AI Tool Analysis [3P], May 2026](https://aitoolanalysis.com/heygen-review/)
  - "Avatar IV (their best avatar tech) is limited to 5 minutes monthly on the $29/month plan", with realistic avatars plus fast processing pushing the price to $59/month. — [ezUGC [competitor, AI UGC-video tool]](https://www.ezugc.ai/blog/heygen-review)
  - The newest roundups agree on 600 credits. — [Arcade [3P]](https://www.arcade.software/post/heygen-pricing)
- **Pro:** from $49/month for 1,000 base credits, with 4K export; credit tiers run up to 100,000 credits for $4,300/month (third-party, 2026). — [Arcade [3P]](https://www.arcade.software/post/heygen-pricing); [Magic Hour [competitor]](https://magichour.ai/blog/heygen-pricing); [Pexo [competitor]](https://pexo.ai/blog/heygen-pricing-7649)
- **Business:** $149/month for the first seat plus $20 per extra seat, with 1,500 shared credits (extra seats add no credits) and videos up to 60 minutes. It is reportedly the only plan that can buy top-up credits, at about $5 per 100 credits. Creator users reportedly can't buy credits and must upgrade, and Pro users must move to a higher Pro tier. Annual subscribers keep unused credits until renewal. (Third-party, 2026.) — [Arcade [3P]](https://www.arcade.software/post/heygen-pricing); [Flowith [3P]](https://flowith.io/blog/heygen-pricing-free-vs-creator-vs-business-plan/); [camclo3d [3P]](https://camclo3d.com/blog/heygen-pricing-credits-explained)
- **Conflict on top-ups:** one 2026 guide says "Generative Credit Packs" cost about $15 for 300 credits, roughly $5 per extra Avatar IV minute. The search snippets didn't say which of these pages it was. — [eesel [3P]](https://www.eesel.ai/blog/heygen-pricing); [Vidmetoo [3P]](https://www.vidmetoo.com/heygen-pricing-detailed-review-of-all-plans/)
- **Enterprise:** custom, sales-led pricing. — [Arcade [3P]](https://www.arcade.software/post/heygen-pricing)
- **Web vs API billing:** usage through an API key is billed against a separate pay-as-you-go API balance and does not use the web subscription's credits. Free web users can still use the API by funding that balance from $5 (third-party roundups, 2026). — [G2 Learn article [3P]](https://www.g2.com/articles/heygen-api-pricing); [Fastlane [3P]](https://www.usefastlane.ai/pricing/heygen)
- **Avatar V timeline:**
  - Product Hunt launch 2026-04-10 (aggregator). — [hunted.space [3P]](https://www.hunted.space/product/heygen)
  - Live walkthrough webinar 2026-04-15. — [HeyGen events page [official]](https://www.heygen.com/en-ca/events/introducing-avatar-v-a-live-walkthrough-of-heygens-most-advanced-ai-avatar-model-yet)
  - Release note dated 2026-05-04: "highly realistic, identity-consistent video generation from a simple 15-second recording", with multi-angle stability and long-form performance. — [Releasebot aggregator [3P]](https://releasebot.io/updates/heygen)
  - Launch post: [HeyGen blog [official]](https://www.heygen.com/blog/announcing-avatar-v)
  - Site banner: "Say hello to Avatar V… Create yours free" (marketing; it doesn't say what "free" covers). — [HeyGen blog banner [official]](https://www.heygen.com/blog/heygen-october-2025-release)
- **Photo avatars vs digital twins:**
  - Avatar V supports **Digital Twins only**, meaning video-based avatars. — [Enterprise Pricing docs [official]](https://developers.heygen.com/docs/enterprise-pricing)
  - Avatar V is "aimed at real human video-based identities rather than every character type". — [WhatAIDoINeed [3P]](https://whataidoineed.com/tool/heygen)
  - A single photo therefore runs on Avatar IV (or Avatar III); see §3.

### Inferences
- For $0, the Free web tier can probably make one watermarked Avatar IV photo-avatar clip of up to 1 minute. It is browser-only, because free API credits ended in Feb 2026 (§2).
- Creator at $29 fits the $30 ceiling only on monthly billing, and only if cancelled before renewal. Given the cancellation and auto-renewal complaints in §6, a $5–$20 prepaid API top-up is the lower-risk way to pay for this experiment.
- Avatar V, the most realistic engine, needs a short selfie video (a "digital twin"), not a photo.

### Gaps
- I could not read the live pricing page in full, so the per-tier matrix is unverified. Open points: how many photo avatars and digital twins each tier allows, whether Free and Creator can create Avatar V twins, and Avatar V minute caps per tier.
- Free-tier resolution (720p vs 1080p) and whether US accounts get 1 or 3 free videos remain unresolved.
- Prices are assumed to be US list prices; regional variation was not verified.

## 2. API billing: pay-as-you-go, per-engine rates, free credits, watermark, max length, render time, rate limits

### Takeaway
Since Feb 2026 the HeyGen API has been prepaid pay-as-you-go: $5 minimum, no subscription, no free API credits, and credits expire after 12 months. The official help center (indexed as updated around 2026-10-21) gives these per-minute rates:

| Engine / item | Official help-center rate |
|---|---|
| Avatar IV photo avatar | about $2.31/min |
| Avatar IV digital twin | about $4.83/min |
| Avatar V digital twin | about $7.20/min |
| Photo avatar creation (one-time) | about $1.32 per call |
| Digital twin creation (one-time) | about $2.13 per call |

HeyGen's own blog and enterprise docs quote different per-second figures, so verify these live. At these rates, one 45–60 s render costs about $2–$3 on the photo path or about $5.40–$7.20 with an Avatar V twin.

### Cited Findings
- **Billing model:** "start with $5 on a pay-as-you-go basis, with no monthly commitment". — [HeyGen FAQ [official]](https://www.heygen.com/faq)
- **Help-center pricing details (indexed ~2026-10-21):**
  - Pay-as-you-go API credits expire after 12 months.
  - HeyGen stopped offering free API credits starting February 2026.
  - Usage is billed in USD by engine, avatar type and length.
  - Avatar V Digital Twin: $7.20/min (144 credits), i.e. $0.12/s.
  - Avatar IV Digital Twin: $4.83/min.
  - Avatar IV Photo Avatar: $2.31/min (46 credits), about $0.0385/s.
  - There is no separate 4K price for Avatar IV or V; requests are billed at the 1080p rate.
  - Avatar creation: Digital Twin $2.13 per call (43 credits); Photo Avatar $1.32 per call.
  - — [HeyGen API Pricing Explained [official]](https://help.heygen.com/en/articles/10060327-heygen-api-pricing-explained)
- **Conflicting official figures:**
  - Enterprise docs: 1 credit = $0.50. Avatar V (Digital Twins only) costs 0.1 credits/s ($0.05/s, $3/min), and an Avatar IV Photo Avatar also costs 0.1 credits/s ($0.05/s). — [Enterprise Pricing [official]](https://developers.heygen.com/docs/enterprise-pricing)
  - HeyGen blog (~2026-10-07 to 10-09): Avatar IV photo avatars at $0.05/s "from a $5 prepaid wallet". — [AI Video Generator Pricing Compared (2026) [official blog]](https://www.heygen.com/blog/ai-video-generator-pricing)
  - Two other HeyGen posts give Avatar V via the API at $0.05/s and $0.0667/s. The snippets didn't say which post gave which figure. — [Best AI Avatar & Talking-Head APIs [official blog]](https://www.heygen.com/blog/best-ai-avatar-talking-head-apis); [Photo vs Digital Twin vs Avatar V [official blog]](https://www.heygen.com/blog/photo-avatar-vs-digital-twin-vs-avatar-v-vs-instant-avatar)
  - A page in the same heygen.com-restricted search, probably a blog comparison, lists avatar creation at $1.00 per call. — [HeyGen blog [official], attribution uncertain](https://www.heygen.com/blog/best-ai-avatar-talking-head-apis)
- **Third-party rate table (2026; the search tool merged several pages, so figures aren't tied to one page):**
  - Avatar III: about $1/min at 720p/1080p, about $1.20/min at 4K.
  - Avatar IV: $3/min for photo avatars, $4/min for digital twin or studio avatars.
  - Video Agent: $2 per prompted minute.
  - Translation: $1 (Speed, audio-only), $2 (Speed, lip-sync) or $4 (Precision, lip-sync) per source minute.
  - Enterprise adds dedicated developer support, "Digital Twin Creation and Proofread APIs" and discounted rates.
  - — [G2 Learn [3P]](https://www.g2.com/articles/heygen-api-pricing); [DIY AI [3P]](https://diyai.io/ai-tools/video-generation/heygen-pricing/); [Fastlane [3P]](https://www.usefastlane.ai/pricing/heygen); [Anam [competitor, real-time avatars]](https://anam.ai/blog/heygen-pricing)
- **Watermark:** the Free web plan is watermarked and Creator removes branding. — [HeyGen pricing [official]](https://www.heygen.com/pricing). I found **no statement on whether API output carries a HeyGen watermark**. The API does offer a custom PNG/JPEG watermark overlay, "available as a premium option for select Enterprise customers". — [Create Video reference [official]](https://developers.heygen.com/reference/create-video); [Changelog [official]](https://developers.heygen.com/changelog)
- **Maximum length:**
  - Avatar video can run up to 30 minutes (on Enterprise, the limit is per scene). — [Usage Limits [official]](https://developers.heygen.com/docs/usage-limits)
  - Audio-driven video length follows the audio, up to 30 minutes. — [Audio to Video [official]](https://developers.heygen.com/audio-to-video)
  - Separately, the prompt-based heygen-video-1 model makes clips of 5–15 s or "auto" per its model docs, versus 4–15 s per the changelog. It is not suited to a 45–60 s talking head. — [HeyGen Video model [official]](https://developers.heygen.com/docs/models/heygen-video); [Changelog [official]](https://developers.heygen.com/changelog)
- **Render time:**
  - Developer docs: on standard plans, expect "5x–10x the final video length (e.g. a 1-min video takes ~5–10 min)". Enterprise gets a priority queue. If a video has been "processing for more than 24 hours", contact support with the video_id. The snippets didn't name the exact docs page. — [Video Details [official]](https://developers.heygen.com/video-details); [Quick Start [official]](https://developers.heygen.com/docs/quick-start)
  - Web-app help article: the regular queue "is just under 24h on average during weekdays", faster at weekends. — [HeyGen Video Processing Times [official]](https://help.heygen.com/en/articles/9655503-heygen-video-processing-times)
- **Concurrency:** the pay-as-you-go API allows 10 concurrent video jobs, counting avatar renders, Video Agent sessions and translations. Going over returns 429 with a Retry-After header. — [Usage Limits [official]](https://developers.heygen.com/docs/usage-limits). Enterprise gets 20 slots, plus "burst" of up to 50 more per workflow type at 1.5× the contract rate (burst added Sept 2026). — [Burst Concurrency [official]](https://developers.heygen.com/docs/burst); [Changelog [official]](https://developers.heygen.com/changelog)
- **Rate limits:** read 1,000/min, write 30/s, "heavy" 120/min; 429 responses now include X-RateLimit headers (changelog). — [Changelog [official]](https://developers.heygen.com/changelog)
- **Outdated free-credit note:** HeyGen's own local MCP README (April 2025) still says an API key "Includes 10 Free Credits per Month". Free API credits were removed in Feb 2026. — [heygen-mcp on PyPI [official, 2025]](https://pypi.org/project/heygen-mcp/); [HeyGen API Pricing Explained [official]](https://help.heygen.com/en/articles/10060327-heygen-api-pricing-explained)

### Inferences
- **Per-render cost for a 45–60 s clip** (help-center rates, with the $0.05/s blog/enterprise figure in brackets):

  | Path | 45 s | 60 s | One-time creation |
  |---|---|---|---|
  | Avatar IV photo avatar | ≈ $1.73 [$2.25] | ≈ $2.31 [$3.00] | $1.32 |
  | Avatar IV digital twin | ≈ $3.62 | ≈ $4.83 | $2.13 |
  | Avatar V digital twin | ≈ $5.40 | ≈ $7.20 | $2.13 |

- **What $30 buys:** a $10 top-up covers about 3 one-minute photo-avatar iterations. About $20 covers a photo test plus an Avatar V twin with two one-minute renders (≈ $1.32 + $2.31 + $2.13 + 2 × $7.20 ≈ $20.16). Both fit under $30 with no subscription.
- A prepaid wallet avoids the auto-renewal and cancellation problems in §6. Treat any top-up as a sunk cost, since credits expire in 12 months and refund terms are strict (§6).
- One render should take roughly 5–10 minutes, so an agent should poll for status rather than block.

### Gaps
- Exact live per-second rates conflict between official pages; verify at heygen.com/api-pricing, which this sandbox could not reach.
- Not found: top-up increments above $5, auto-recharge behaviour, and whether the one-step `type: "image"` path also charges the $1.32 photo-avatar creation fee.
- No source says whether API output is watermark-free. It is likely, since API output is paid per second, but unconfirmed.
- Webhook/callback support for job completion was not researched (search budget ran out).

## 3. API mechanics for this job: photo-to-video endpoints, user-supplied audio, voice cloning, hostnames, auth

### Takeaway
HeyGen's current v3 REST API documents two ways to make a talking video from one photo:
- **One step:** `POST /v3/videos` with `type: "image"`, the photo, a script and a voice.
- **Two steps:** create a photo avatar with `POST /v3/avatars`, then call `POST /v3/videos` with `type: "avatar"`.

It accepts **your own audio file** (`audio_asset_id` or `audio_url`, MP3/WAV up to 32 MB) in place of HeyGen text-to-speech, and offers voice cloning through `POST /v3/voices/clone`, which is in beta and whose plan-gating is unclear. Auth is an `X-Api-Key` header. Hosts seen so far are api.heygen.com for the API and resource2.heygen.ai for video downloads, plus a presigned-upload host that isn't documented in what I found.

### Cited Findings
- **One-step photo-to-video:** `POST /v3/videos` with `type: "image"` and an image object (a URL or an uploaded asset ID), plus a script and voice ID. Uploads go first to `POST /v3/assets`, whose returned asset ID is then reused. — [Photo to Video [official]](https://developers.heygen.com/photo-to-video); [Create Video reference [official]](https://developers.heygen.com/reference/create-video)
- **Two-step photo avatar:** create a photo avatar with `/v3/avatars` (creation type "photo"), then generate with `type: "avatar"` and the avatar ID. The avatar_id passed to video creation is "the look ID from the avatar looks list, not the group ID". — [Photo Avatar [official]](https://developers.heygen.com/photo-avatar); [Create Avatar [official]](https://developers.heygen.com/docs/create-avatar)
- **Engine selection:** Avatar IV is used by default when `engine` is omitted, and `{ "type": "avatar_v" }` selects Avatar V "on eligible looks" (digital twins only, per §1). An "expressiveness" option applies to photo avatars on Avatar IV and defaults to low. — [Photo Avatar [official]](https://developers.heygen.com/photo-avatar); [Photo to Video [official]](https://developers.heygen.com/photo-to-video)
- **Engine conflict:** one HeyGen page calls Avatar III a dedicated photo-to-video pipeline, while another says photo avatars use the avatar_iv engine. — [Photo to Video [official]](https://developers.heygen.com/photo-to-video); [Photo Avatar [official]](https://developers.heygen.com/photo-avatar)
- **Photo input rules conflict:** the Avatar IV API launch post says Avatar IV handles angled and profile photos and both lifelike and stylized characters. The photo-avatar page recommends one front-facing photo. — [Announcing the Avatar IV API [official]](https://www.heygen.com/blog/announcing-the-avatar-iv-api); [Photo Avatar [official]](https://developers.heygen.com/photo-avatar)
- **Different product: Image to Video.** "HeyGen Video" with `mode: "image_to_video"` builds a whole prompted scene with the image as its first frame (short clips; see §2). — [Image to Video [official]](https://developers.heygen.com/image-to-video); [HeyGen Video model [official]](https://developers.heygen.com/docs/models/heygen-video)
- **User-supplied audio:**
  - Upload audio to `POST /v3/assets` (MP3 or WAV, up to 32 MB). Larger files use a presigned direct-upload flow.
  - Then call `POST /v3/videos` with `audio_asset_id` or `audio_url` instead of `script`. These are mutually exclusive with `script`, so send exactly one audio source.
  - Video length follows the audio, up to 30 minutes.
  - The documented example uses `"type": "avatar", "avatar_id": "YOUR_AVATAR_ID", "audio_asset_id": "YOUR_AUDIO_ASSET_ID"` with an avatar you own, and includes a full Python upload → create → poll example.
  - — [Audio to Video [official]](https://developers.heygen.com/audio-to-video); [Assets [official]](https://developers.heygen.com/assets)
  - The Studio endpoint accepts the same audio fields. — [HeyGen Studio [official]](https://developers.heygen.com/studio-videos)
- **Large uploads:** `POST /v3/assets/direct-uploads` with filename, content_type and exact size_bytes returns an asset_id, a presigned `upload_url` and `upload_headers`. You PUT the file to that URL, then call "complete". — [Upload Assets [official]](https://developers.heygen.com/docs/upload-assets); [Create Asset Upload [official]](https://developers.heygen.com/reference/create-asset-upload)
- **Speech-to-Speech:** converts a recording using an existing voice ID. — [Speech to Speech [official]](https://developers.heygen.com/docs/voices/speech-to-speech)
- **Voice cloning via API:**
  - `POST /v3/voices/clone` creates a clone from an audio file and returns a `voice_clone_id`; poll `GET /v3/voices/…` until the status is "complete". — [Clone a Voice [official]](https://developers.heygen.com/reference/clone-a-voice)
  - Input: an instant clone takes exactly one recording, as `asset_id`, `url` or `base64`. A professional clone takes 1–10 recordings of the same speaker totalling at least 20 minutes. — [Instant Voice Clone [official]](https://developers.heygen.com/docs/voices/heygen-voice-instant-clone); [Professional Voice Clone [official]](https://developers.heygen.com/docs/voices/professional-voice-clone)
- **Voice-clone plan-gating conflict:**
  - The clone reference page shows an example error: "Voice cloning is not available on the free tier. Please upgrade your plan." — [Clone a Voice [official]](https://developers.heygen.com/reference/clone-a-voice)
  - The instant-clone guide describes a per-account clone allowance, with `400 resource_limit_reached` when it's exceeded. — [Instant Voice Clone [official]](https://developers.heygen.com/docs/voices/instant-voice-clone)
  - The changelog says the single-recording clone "remains available to all API plans". — [Changelog [official]](https://developers.heygen.com/changelog)
  - The models page lists Instant Clone as "Beta. Free to create during the preview". Professional clones are paid, one purchased slot per voice. — [Models [official]](https://developers.heygen.com/models)
  - Free-plan workspaces get 20 clone calls and 20 voice-design calls per rolling 24 hours by default. — [Text to Speech [official]](https://developers.heygen.com/docs/voices/heygen-voice-speech)
- **Auth and key handling:** HeyGen's own MCP client source (heygen-mcp 0.0.3) sets `base_url = "https://api.heygen.com/v2"` and sends the key in an `X-Api-Key` header. Its README passes the key through the env var `HEYGEN_API_KEY`. — [heygen-mcp on PyPI [official]](https://pypi.org/project/heygen-mcp/) (wheel source read directly, 2026-10-23)
- **Hostnames:**
  - Current uploads go through `api.heygen.com/v3/assets`. — [Assets [official]](https://developers.heygen.com/assets)
  - Finished-video `video_url` values are served from `resource2.heygen.ai`, shown in a retrieve-response example. — [HeyGen Video docs [official]](https://developers.heygen.com/docs/models/heygen-video)
  - `upload.heygen.com/v1/asset` (returns an image_key for the legacy `/v2/photo_avatar/avatar_group/create`) appears only in a third-party skill listing. It looks like the legacy v1/v2 flow. — [skills.rest listing [3P]](https://skills.rest/skill/heygen-x-manist)
  - `files2.heygen.ai` was not documented in any result.
  - The hosted MCP is at `mcp.heygen.com` (§4). — [MCP Overview [official]](https://developers.heygen.com/mcp/overview)
  - The web app is `app.heygen.com`, referenced in the heygen-mcp source. — [heygen-mcp on PyPI [official]](https://pypi.org/project/heygen-mcp/)
- **Third-party access path:** HeyGen's Video Agent model is also listed on the API aggregator Runware; its terms and coverage of avatars were not checked. — [Runware docs [3P]](https://runware.ai/docs/models/heygen-video-agent)

### Inferences
- **Most likely agent flow** (curl/Python, no GPU):
  1. Upload the photo with `POST /v3/assets`.
  2. Upload a 45–60 s MP3/WAV with `POST /v3/assets`. A 60 s WAV is about 5.8 MB (48 kHz mono 16-bit) or about 10.6 MB (44.1 kHz stereo), well under 32 MB.
  3. Create a photo avatar with `POST /v3/avatars`, or try the one-step `type: "image"`. Whether the one-step path accepts audio instead of a script is unverified; the audio example uses `type: "avatar"`.
  4. Create the video with `POST /v3/videos` (`type: "avatar"`, `avatar_id` = look ID, `audio_asset_id`).
  5. Poll for status, then download from resource2.heygen.ai.
- Uploading assets avoids hosting the user's face or voice at a public URL, which `image_url`/`audio_url` would require. That suits a private experiment.
- Passing your own audio lets the clip "sound like you": either a real recording or a clone from another vendor. That sidesteps the uncertain plan-gating and the unknown quality of HeyGen's voice clones.
- **Sandbox allowlist:** at minimum `api.heygen.com` and `resource2.heygen.ai`, plus whatever host the presigned `upload_url` points to (probably cloud storage; unknown). Possibly also `upload.heygen.com` for legacy tools, and `mcp.heygen.com` if using MCP. A safer start is to allowlist `*.heygen.com` and `*.heygen.ai`, run a test, and then narrow the list.
- This research sandbox default-denied `www.heygen.com`, `docs.heygen.com` and `developers.heygen.com` (direct observation, 2026-10-23), so explicit allowlisting is a real prerequisite, not a formality.

### Gaps
- I could not read the v3 API reference in full. Still unverified: the exact status-polling and download endpoint paths (e.g. `GET /v3/videos/{id}`), whether `video_url` is a signed URL and when it expires, the presigned-upload host, whether v3 also uses `X-Api-Key` (likely, since v2 does), and whether `type: "image"` accepts `audio_asset_id`.
- Whether digital-twin creation is available to pay-as-you-go keys or Enterprise-only is unclear. A third-party summary lists "Digital Twin Creation … APIs" as an Enterprise add-on — [G2 Learn [3P]](https://www.g2.com/articles/heygen-api-pricing) — but the official consent docs describe a self-serve webcam flow (§7).
- Whether a HeyGen voice clone created in the web app can be used through the API key was not verified.

## 4. Official HeyGen MCP server or connector, and community MCP servers

### Takeaway
HeyGen runs an **official hosted remote MCP server** at `https://mcp.heygen.com/mcp/v1/`. It authenticates with OAuth, not an API key, draws on **web-plan credits**, and HeyGen recommends Creator or above. Its documented tools cover avatar videos from a script or audio, listing voices and avatars, render status, a Video Agent and translation, so it is not limited to motion graphics. The older official local `heygen-mcp` Python server is stale (v0.0.3, April 2025, v2 API, no photo-avatar support). HyperFrames is a separate open-source HTML-to-MP4 motion-graphics framework from HeyGen; it can pull in HeyGen avatar media but is not an avatar engine.

### Cited Findings
- **Hosted MCP:** add a custom connector named HeyGen with remote MCP server URL `https://mcp.heygen.com/mcp/v1/` and "Authenticate with OAuth". No API key or local install is needed. — [HeyGen MCP Overview [official]](https://developers.heygen.com/mcp/overview)
- **Hosted MCP tools (third-party guides, 2026):** "Create avatar videos from a script or audio (create_video)", a single-prompt video agent, video translation with lip-sync, listing voices and avatars, and checking render status. It works with Claude web and Claude Code. "HeyGen recommends a Creator plan or above, and every video uses your plan credits." One guide says the earlier local server is "now community-maintained, but the hosted one is the supported default." — [Carly [3P]](https://www.usecarly.com/blog/claude-heygen-integration/); [The AI School [3P]](https://the-aischool.com/mcp/heygen)
- **Local `heygen-mcp`:**
  - PyPI package by Eddy Kim (eddy@heygen.com), MIT licence; versions 0.0.1–0.0.3 were all uploaded 2025-04-15/16, so it is about 18 months old.
  - Tools: `get_remaining_credits`, `get_voices` (first 100 only), `get_avatar_groups`, `get_avatars_in_avatar_group`, `generate_avatar_video`, `get_avatar_video_status`.
  - Its roadmap still lists "Photo Avatar APIs Support" and "SSE And Remote MCP Server with OAuth Flow" as unchecked.
  - The README says: "This project is in early development… official support is limited."
  - — [heygen-mcp on PyPI [official]](https://pypi.org/project/heygen-mcp/) (metadata and wheel read directly, 2026-10-23)
  - The GitHub README at `heygen-com/heygen-mcp`, main and master branches, returned HTTP 404 via raw.githubusercontent.com on 2026-10-23. The repo may have been moved, renamed or made private; unverified. — [GitHub repo link from PyPI](https://github.com/heygen-com/heygen-mcp)
- **Directories listing HeyGen MCP servers:** PulseMCP ("Official HeyGen MCP Server"), Zapier MCP (HeyGen actions through Zapier), Playbooks, MCP Market, MCP.Directory, Glama and ExplainX. — [PulseMCP](https://www.pulsemcp.com/servers/heygen-avatar-video); [Zapier MCP](https://zapier.com/mcp/heygen); [Playbooks](https://playbooks.com/mcp/heygen-com/heygen-mcp); [MCP Market](https://mcpmarket.com/server/heygen); [MCP.Directory](https://mcp.directory/servers/heygen); [Glama](https://glama.ai/mcp/servers/@heygen-com/heygen-mcp); [ExplainX](https://explainx.ai/mcp-servers/heygen)
- **HyperFrames:**
  - "An open-source framework for turning HTML, CSS, media, and seekable animations into deterministic MP4 videos… Built for agents", Apache-2.0.
  - It renders in headless Chrome with FFmpeg, locally, in Docker or on Lambda/cloud, and ships a Claude Code plugin.
  - Its `/media-use` skill can "get or make… voiceover, avatar and generated video… with HeyGen or free local tools".
  - npm `hyperframes` is at 0.8.186, last modified 2026-10-22.
  - — [HyperFrames GitHub README [official]](https://github.com/heygen-com/hyperframes); [npm: hyperframes](https://www.npmjs.com/package/hyperframes)
- **Other official SDK:** `@heygen/streaming-avatar` 2.1.1 (modified 2026-05-12) is for real-time interactive avatars, not rendered clips. — [npm: @heygen/streaming-avatar](https://www.npmjs.com/package/@heygen/streaming-avatar)
- **Legacy community skill:** one third-party "heygen" agent skill uses the legacy `upload.heygen.com/v1/asset` → `/v2/photo_avatar/avatar_group/create` flow. — [skills.rest [3P]](https://skills.rest/skill/heygen-x-manist)

### Inferences
- For a headless Linux sandbox with an API key in an env var, the **v3 REST API is the better fit** than the hosted MCP. The hosted MCP needs an interactive OAuth sign-in and bills against a web subscription; Creator at $29/mo uses up almost the whole budget.
- The stale local `heygen-mcp` can't do photo avatars and targets the v2 API, so it is not useful here.
- HyperFrames matters only for adding overlays or captions afterwards; it doesn't replace the avatar API.

### Gaps
- The full tool list and parameters of the hosted MCP were not read from HeyGen's docs. Unverified: whether it supports photo-avatar creation or audio upload, and whether it works on the Free plan.
- I couldn't search GitHub for community HeyGen API clients or MCP servers and their issue trackers, because the GitHub API in this sandbox is limited to configured repositories.

## 5. Realism: photo avatar vs digital twin, Avatar IV/V, lip-sync, artifacts, convincingness, voice clones

### Takeaway
Reviewers mostly rate **Avatar V digital twins** (built from a ~15 s selfie video) as HeyGen's most realistic output; one hands-on test scored it 9/10. They still say it is not indistinguishable from real footage. **Single-photo "talking photo" avatars** are rated lower: one review calls them uncanny beyond about 15 seconds, which is shorter than the 45–60 s target. English lip-sync is praised. Reported failure modes are "dead" eyes in long or emotional scripts, lip-sync breaking on fast speech or heavy accents, and oversized mouths from wide-smile source photos. I found no independent blind test and no evidence about fooling people who know the subject.

### Cited Findings
- **Avatar V hands-on (ThePlanetTools, review blog, 2026):** "the most realistic digital twin" they had generated, scored 9/10. They would use it as the face of a brand channel, but it "is not a substitute for a real person on camera in vulnerable moments"; the review cites a 0.840 face-similarity score. — [ThePlanetTools [3P]](https://theplanettools.ai/blog/heygen-avatar-v-tested-hands-on-review-2026)
- **More measured view (DIY AI, review site, 2026):** HeyGen scored 8.2/10 overall but 7.7/10 for video quality. Avatar V is recommended for realistic, video-trained human digital twins and called a weaker buy for cinematic scenes. — [DIY AI [3P]](https://diyai.io/ai-tools/video-generation/reviews/heygen-review/)
- **Risk note:** "higher realism increases consent, impersonation, disclosure and brand-safety risk". — [WhatAIDoINeed [3P]](https://whataidoineed.com/tool/heygen)
- **YouTube:** a review titled "HeyGen Avatar V Review: The Most Realistic AI Digital Twin I've Tested" (title only; transcript not retrieved). — [YouTube [3P]](https://www.youtube.com/watch?v=cEJw8zew08E)
- **Talking-photo realism (2026 review blogs; the snippets don't say which blog wrote which line):**
  - Talking-photo animations look "uncanny for anything longer than 15 seconds".
  - HeyGen is "not indistinguishable from human footage, though… professional enough for most viewers".
  - English lip-sync is called best-in-class, while non-English output can show "accent slips or uncanny moments".
  - Reviewers credit Avatar IV with full-body motion, micro-expressions, natural head movement and hand gestures.
  - — [Venture Harbour [3P, affiliate-style listicle]](https://ventureharbour.com/best-ai-avatar-software/); [PromptsRush [3P]](https://promptsrush.com/blog/heygen-review); [Ortem Tech [3P]](https://ortemtech.com/blog/heygen-review-2026-ai-avatar-video-generator/); [ezUGC [competitor]](https://www.ezugc.ai/blog/heygen-review)
- **Vendor-leaning claim to discount:** Avatar IV replicates people closely enough that "standard viewing conditions do not trigger the uncanny valley response". — same review set as above, flagged by the search tool as vendor-leaning.
- **User forum (date unknown, predates Avatar V, so older engines):** eyes can look "dead" in long or emotional scripts, and lip-sync breaks with fast speech or heavy accents. Single thread; small sample. — [pjirc forum [user]](https://pjirc.com/t/heygen-ai-review-realistic-ai-avatars-or-not/2288)
- **G2 user reviews (dates not visible):** "facial expressions and lip sync are very natural". On cost: "Ten minutes of 'premium quality' feels too little for the price." — [G2 HeyGen reviews [user]](https://www.g2.com/products/heygen); [G2 review page [user]](https://www.g2.com/survey_responses/heygen-review-8526804)
- **HeyGen's own troubleshooting:** a wide "cheese" smile in the source photo can produce an oversized mouth; use a subtle smile. — [Avatar & Voice FAQ [official]](https://help.heygen.com/en/articles/15544929-avatar-voice-faq-troubleshooting-best-practices-and-credits)
- **Vendor marketing (discount accordingly):** Avatar V is "the most lifelike avatar ever made" and "the Most Realistic AI Avatar Ever". — [HeyGen blog [official]](https://www.heygen.com/blog/announcing-avatar-v)

### Inferences
- A **single-photo Avatar IV clip of 45–60 s is likely to show some uncanny artifacts** (stiff or odd eyes, mouth shape, limited head motion), going by the "uncanny beyond ~15 s" report. A 15 s selfie video turned into an Avatar V digital twin is the higher-realism route but costs more (§2) and requires a consent step (§7).
- Using the user's own clean audio recording should give the most "sounds like me" result and avoids judging an untested HeyGen clone. Speak at a moderate pace, since fast speech reportedly breaks lip-sync.
- Most realism praise comes from review/affiliate blogs and HeyGen marketing. Independent signal is thin: one forum thread and a few G2 lines.

### Gaps
- **Reddit (r/HeyGen, r/aivideo and others) was not reachable by the search tool**, so the main practitioner forum is missing. Hacker News, Product Hunt reviews, X/Twitter creator posts and YouTube transcripts were not covered (search budget ran out).
- No source tested whether friends or family could tell a HeyGen clip of someone they know from real footage.
- **The quality of HeyGen voice clones was not researched** (search budget ran out).
- Specific artifact reports on teeth, blinking, hands and gestures for Avatar IV/V were not found beyond the items above.

## 6. Billing and support complaints: credit burn, failed renders, auto-renewal, cancellation, refunds, bans, support quality

### Takeaway
2026 Trustpilot and BBB complaints follow a pattern around **web subscriptions**: hard cancellation (sometimes only through a support ticket), charges after cancelling, credits vanishing after a pause or auto-resume, and refunds refused under a 15-day policy. Support experiences are mixed, with some fast refunds. HeyGen's help center says failed or cancelled renders are never charged; a Reddit thread cited by a third party disagrees. The two blog-reported Trustpilot averages conflict (2.3/5 vs 3.6/5).

### Cited Findings
- **Trustpilot snippets (2026):**
  - Cancelling is hard: one reviewer says the only route was a support ticket.
  - One reviewer was charged after cancelling; another asked to cancel after the first month but "was still charged multiple times".
  - A paused subscription's credit balance "vanished" when the pause lapsed and the plan auto-resumed.
  - Some refund requests went unresolved ("unresponsive… no proper resolution or refund"), while another reviewer says support "was very fast and helpful, and gave a refund since the product did not work for their needs".
  - HeyGen's public reply says it is "taking active changes to make the credit system a bit more clear".
  - — [Trustpilot (US, p.9) [user]](https://www.trustpilot.com/review/heygen.com?page=9); [Trustpilot (CA, p.2) [user]](https://ca.trustpilot.com/review/heygen.com?page=2); [Trustpilot (AU) [user]](https://au.trustpilot.com/review/heygen.com); [Trustpilot (IE, p.5) [user]](https://ie.trustpilot.com/review/heygen.com?page=5); [Trustpilot (SE) [user]](https://se.trustpilot.com/review/heygen.com)
- **Trustpilot averages conflict (blogs, not live data):** "2.3 out of 5 across 1,623 reviews" (as of April 2026; more than 6 months old, possibly outdated) vs "3.6 (2,486 reviews, 18% one-star)" (as of July 2026). One blog analysed a sample of 100 Trustpilot reviews. The snippets don't say which figure came from which blog. — [Rain AI Services [3P]](https://rainaiservices.com/reviews/heygen-review/); [Toruclip [3P, possible competitor]](https://toruclip.com/blog/heygen-review)
- **Failed renders, official:** "if a video is cancelled mid-way or failed- you will not be charged any Credits under any circumstances". The help center suggests cancelling and resubmitting, then contacting support. — [HeyGen Video Processing Times [official]](https://help.heygen.com/en/articles/9655503-heygen-video-processing-times)
- **Failed renders, conflicting report:** a Reddit thread, cited by a third-party blog, says failed video renders still consume credits. I couldn't access Reddit to confirm it or its size. — [AdMake [3P, possible competitor]](https://admakeai.com/blog/heygen-pricing-explained); [Rain AI Services [3P]](https://rainaiservices.com/reviews/heygen-review/)
- **Credit refunds for failures:** a third-party troubleshooting guide says support does refund credits for documented rendering failures; have the video ID ready. — [FixAITools [3P]](https://fixaitools.com/heygen-error/); see also [TechSifted [3P]](https://techsifted.com/troubleshooting/heygen-not-working/)
- **Refund policy text (an apparent third-party copy, not verified on HeyGen's site):** refunds "not allowed after 15 days, especially when the credits have been used". Technical rendering problems may be refunded "if you provide us with the video ID and specify the problematic part". — [atlas-kb copy [3P, unverified]](https://atlas-kb.com/atlas-4cwembs21w/articles/610545-refund-policy)
- **BBB complaints:** refunds denied despite a claimed technical problem. One complainant says HeyGen "refused to refund the remaining unused months, citing a strict internal 15-day refund policy". The number and dates of complaints were not visible. — [BBB HeyGen complaints [user]](https://www.bbb.org/us/ca/los-angeles/profile/artificial-intelligence/heygen-1216-1000026007/complaints)
- **Credit confusion:** the main drawback is a pricing and credit system "many users find expensive and confusing". — [Pexo [competitor]](https://pexo.ai/blog/heygen-review-7390); also [G2 user](https://www.g2.com/products/heygen) ("Ten minutes of premium quality feels too little for the price")
- **Inactive Free accounts:** HeyGen's terms let it delete a Free Plan account after six months of no use, on reasonable notice. — [HeyGen Terms [official]](https://www.heygen.com/terms)

### Inferences
- The complaints are a **recurring pattern**, not a single angry review: several Trustpilot regions plus BBB, all concentrated on recurring subscriptions (auto-renewal, cancellation, unused months, pause/resume).
- A one-time prepaid API top-up avoids most of this exposure. The residual risks are a non-refundable unused balance and possible disputes over failed renders, so log every video_id.
- If the web Creator plan is used for the experiment, cancel right after the test and screenshot the confirmation.

### Gaps
- No data was found on **account bans** or suspensions, for example for moderation of real-person likenesses.
- Not found: G2 and Capterra star ratings and counts, the BBB rating and complaint volume, and Reddit sample sizes (Reddit blocked; search budget ran out).
- HeyGen's own refund policy page was not read directly.

## 7. Consent and verification: real-person avatars, own-photo avatars, and whether the API applies the same checks

### Takeaway
HeyGen's developer docs say consent verification applies **only to video-based digital twins**, including Avatar V. A twin can't be generated until the subject records consent through a webcam link valid for 24 hours; only whitelisted Enterprise accounts may upload a pre-recorded consent video. **Photo avatars (`type: "photo"`) need no consent step**: the docs say they "depict no real, identifiable person", and their consent status is null. So a self-photo avatar can be made end-to-end by an agent through the API, while a selfie-video twin needs one manual consent step in a browser.

### Cited Findings
- **Developer docs, Avatar Consent:**
  - A digital twin can't be generated until there is proof the person agreed to be cloned.
  - "Consent applies only to digital twin avatars. Photo avatars (type: "photo") and prompt-to-avatar characters (type: "prompt") depict no real, identifiable person and do not require consent."
  - Consent appears as a status field, null for photo avatars.
  - The default flow is a webcam flow that sends the subject a link valid for 24 hours; "whitelisted enterprise accounts can pass a pre-recorded consent_video". Links expire and a new one must be requested.
  - — [Avatar Consent [official]](https://developers.heygen.com/docs/avatar-consent); [Create Avatar [official]](https://developers.heygen.com/docs/create-avatar)
- **Help center:** consent is required "for every video-based Digital Twin". If you are creating an avatar for someone else, that person must record their own consent video. — [Recording your Consent Video [official]](https://help.heygen.com/en/articles/12092609-recording-your-consent-video); [Create your first Digital Twin with Avatar IV [official]](https://help.heygen.com/en/articles/12089286-create-your-first-digital-twin-video-avatar-with-avatar-iv)
- **Third-party guide (MindStudio, AI-agent platform, 2026):** the person in the consent clip must be the same person as in the footage, and screen recordings or AI-generated clips fail verification. Avatar V twins come from about 15 s of video. — [MindStudio: Avatar V explained [3P]](https://www.mindstudio.ai/blog/what-is-heygen-avatar-v-digital-twin-explained); [MindStudio: Avatar 5 [3P]](https://www.mindstudio.ai/blog/what-is-heygen-avatar-5)
- **Biometric data use:** HeyGen's Biometric Information Privacy Notice says it collects face geometry and, where applicable, voiceprints when someone creates a custom avatar. Per excerpts, the privacy policy also covers biometric use for identity verification and requires explicit consent. — [Biometric Information Privacy Notice [official]](https://www.heygen.com/biometric-privacy-notice); [Privacy Policy [official]](https://www.heygen.com/privacy)

### Inferences
- For the user's own single photo, the **API path has no documented consent or ID gate**, so an agent can run it end-to-end.
- The Avatar V route needs the user, as the subject, to open a HeyGen consent link and record on a webcam within 24 hours. That is one human-in-the-loop browser step; the rest can be done through the API.
- The docs' claim that photo avatars depict "no real, identifiable person" doesn't match a user uploading a real selfie. HeyGen's general terms probably still require rights to any likeness uploaded, but this is unverified.

### Gaps
- **The ToS and acceptable-use clauses on real-person likeness and photo avatars of real people were not read** (search budget ran out). Unknown: whether HeyGen's web app adds checks for photo avatars of real people (e.g. moderation or celebrity filters), and whether an ID or liveness check is ever required beyond the consent video.
- Whether the web app's consent flow matches the API's webcam-link flow exactly was not confirmed.

## 8. Data: retention of photos, videos, voice samples and avatars; training use; deletion

### Takeaway
HeyGen's biometric notice says biometric data (face geometry, voiceprints) is kept only as long as needed, and that face geometry is "permanently destroyed" after the avatar is made. A third-party compliance guide says instead that geometry stays while the avatar is active and is deleted within 60 days after avatar or account deletion. Third-party readings of whether user content trains HeyGen's models conflict (an email opt-out vs excluded by default). Accounts can be deleted permanently under Settings → Account. I found no retention period for uploaded API assets or rendered videos.

### Cited Findings
- **Official biometric notice:** biometric information is kept only as long as needed for the specific purpose, not indefinitely. For avatar creation, face geometry is permanently destroyed after the avatar is made. — [Biometric Information Privacy Notice [official]](https://www.heygen.com/biometric-privacy-notice)
- **Third-party reading of retention:** avatar geometry remains while the avatar is active and is deleted within 60 days after avatar or account deletion. — [WAIMAKERS compliance guide [3P]](https://www.waimakers.com/en/resources/ai-data-security/heygen)
- **Training use, conflicting third-party readings:**
  - WAIMAKERS: the general privacy policy lets user input be used to train and improve models, with an email opt-out, while Enterprise content is not used for training. — [WAIMAKERS [3P]](https://www.waimakers.com/en/resources/ai-data-security/heygen)
  - aifoxx: biometric data for custom avatars is excluded from AI training by default. — [aifoxx trust page [3P]](https://aifoxx.com/trust/heygen)
- **Deletion:** account deletion is under Settings → Account tab → Delete Account. It "cannot be undone", and "all your personal data and associated information will be permanently removed from our system". — [How to manage/delete your HeyGen account [official]](https://help.heygen.com/en/articles/8300888-how-to-delete-your-account-on-heygen)
- **Free accounts:** the terms let HeyGen delete a Free Plan account after six months of inactivity, on notice. — [HeyGen Terms [official]](https://www.heygen.com/terms)
- **Unsourced claim:** a third-party blog says cancelled accounts keep generated videos for about 30–90 days and custom avatar models are deleted; it gives no source. — [Flowith FAQ [3P]](https://flowith.io/blog/heygen-faq-custom-avatar-api-limits-commercial-rights/)
- **Compliance claims:** HeyGen publishes a GDPR compliance statement; a third-party trust page lists SOC 2 and GDPR. — [HeyGen GDPR statement [official]](https://www.heygen.com/gdpr-compliant); [aifoxx [3P]](https://aifoxx.com/trust/heygen)
- **Not HeyGen:** heygen.site's "privacy policy" appears to belong to a different product and should be ignored.

### Inferences
- A privacy-minded user should, after the experiment: delete the photo avatar or twin and the uploaded assets, either via API delete endpoints (if they exist; unverified) or in the web app; then delete the account. The user should also email HeyGen to opt out of training use, given the conflicting readings.
- Because uploaded API assets, voice clones and rendered videos have no stated retention period, assume they persist until deleted.

### Gaps
- The privacy policy's retention table and training clause were not read directly; only excerpts and third-party summaries were.
- Retention of `/v3/assets` uploads, voice-clone samples and rendered `video_url` files, and whether API delete endpoints exist for avatars, assets and voices, were not verified.

## 9. Tips for best results from one photo vs a short selfie video

### Takeaway
For one photo, HeyGen's help center recommends:
- a clear, front-facing, close-up or half-body image with the face filling much of the frame;
- a subtle expression (a wide smile can cause an oversized mouth);
- no accessories covering the face;
- a sharp, well-lit image (blurry, dark, small or blocked faces get rejected).

Avatar IV can take angled photos, but the front-facing advice is safer, and a motion prompt or expressiveness setting can add movement. For the selfie-video route (Avatar V), about 15 s of footage plus a webcam consent clip by the same person is needed.

### Cited Findings
- **Photo choice:**
  - "For the best results, we recommend using a clear, front-facing image with a natural posture and visible hands, if applicable."
  - Use a close-up or half-body image, keep the face clearly visible, use a subtle expression, and avoid large accessories that cover the face.
  - Use a subtle smile, not a wide "cheese" smile, which can produce an oversized mouth.
  - "The character should take up a larger portion of the image."
  - — [How to Get Started with Photo Avatars [official]](https://help.heygen.com/en/articles/10034438-how-to-get-started-with-photo-avatars); [Avatar & Voice FAQ [official]](https://help.heygen.com/en/articles/15544929-avatar-voice-faq-troubleshooting-best-practices-and-credits)
- **Upload rejections:** common causes are an unsupported format, a corrupt file, no detectable face, a face that is too small or blocked, or an image that is blurry or too dark. — [Avatar & Voice FAQ [official]](https://help.heygen.com/en/articles/15544929-avatar-voice-faq-troubleshooting-best-practices-and-credits)
- **Angled photos:** "Unlike earlier models, Avatar IV can generate avatars from tilted heads, profiles, and angled poses." This is marketing and conflicts with the help center's front-facing advice. — [Avatar IV page [official]](https://www.heygen.com/avatars/avatar-iv)
- **Adding motion:** a custom motion prompt such as "talks excitedly" helps add movement on Photo/Avatar IV looks. — [Avatar & Voice FAQ [official]](https://help.heygen.com/en/articles/15544929-avatar-voice-faq-troubleshooting-best-practices-and-credits). The API's "expressiveness" option for Avatar IV photo avatars defaults to low. — [Photo Avatar API [official]](https://developers.heygen.com/photo-avatar)
- **Multi-photo looks:** for photo-avatar "looks" built from several images, HeyGen recommends "a mix of close-up and full-body images, captured from different angles and with varied expressions". Another page suggests uploading 10–15 high-quality images. — [HeyGen Academy: avatar from photos [official]](https://www.heygen.com/academy/avatars/how-to-create-an-avatar-using-image)
- **Resolution:** no minimum pixel count was found for Avatar IV photos. HeyGen's guide for its different real-time product (LiveAvatar) asks for at least 1080p footage, because "lower resolution images result in a blurry or pixelated avatar". — [LiveAvatar creation guide [official]](https://help.heygen.com/en/articles/9612935-liveavatar-custom-liveavatar-creation-guide)
- **Selfie-video route:** Avatar V builds an identity-consistent twin from about a 15-second recording. — [Releasebot [3P]](https://releasebot.io/updates/heygen); [MindStudio [3P]](https://www.mindstudio.ai/blog/what-is-heygen-avatar-v-digital-twin-explained). The consent clip must show the same person, and screen recordings or AI-generated clips fail. — [MindStudio [3P]](https://www.mindstudio.ai/blog/what-is-heygen-avatar-v-digital-twin-explained); [Recording your Consent Video [official]](https://help.heygen.com/en/articles/12092609-recording-your-consent-video)
- **Audio input:** MP3 or WAV up to 32 MB; the video length follows the audio. — [Audio to Video [official]](https://developers.heygen.com/audio-to-video). Lip-sync reportedly breaks with fast speech or heavy accents. — [pjirc forum [user]](https://pjirc.com/t/heygen-ai-review-realistic-ai-avatars-or-not/2288)

### Inferences
- **Practical recipe for the photo path:**
  - The newest, sharpest, high-resolution, front-facing, chest-up photo available.
  - Even, soft light and a neutral or slight-smile expression, with the mouth and eyes clearly visible.
  - No glasses glare and nothing covering the face.
  - Your own audio recorded in a quiet room at moderate pace, exported as WAV or MP3.
  - Optionally, moderate expressiveness or a motion prompt to reduce stiffness.
- Because single-photo clips get uncanny beyond about 15 s, a 45–60 s test is a fair stress test. If realism matters most, spend part of the budget on the 15 s selfie video → Avatar V route.

### Gaps
- No HeyGen guidance was retrieved on lighting, background or framing for the Avatar V or digital-twin recording itself, or on audio quality for voice cloning (search budget ran out).
- No independent, practitioner-tested tips were found; Reddit and YouTube were not accessible or not covered.
