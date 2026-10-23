# General-purpose AI video models and lip-sync services: one photo (or selfie video) plus audio to a talking clip, state as of Oct 23, 2026

Scope: ByteDance OmniHuman (and Seedance), Kling, Runway, Pika, Higgsfield, Google Veo 3.x / Gemini Omni, OpenAI Sora 2, MiniMax/Hailuo, Alibaba Wan S2V / Animate, Sync Labs (sync.so). Dedicated avatar platforms (HeyGen, Hedra, D-ID, Synthesia) and self-hosted open models are out of scope; they appear only where a source compares against them.

Source-type labels used below: [official] = the vendor's own docs or pricing; [host] = an API host or reseller that sells the model (fal.ai, Replicate, WaveSpeed, PiAPI, Kie.ai, etc.), which has a commercial interest; [competitor] = written by a company selling a rival product; [blog] = SEO or affiliate blog of unclear independence; [press] = journalism; [paper] = the model authors' own paper. Dates are the source's date where the search tool showed one. Otherwise they're marked "undated (retrieved Oct 23, 2026)". Anything older than about 6 months (before roughly late April 2026) is flagged **[>6 mo]**.

## 1. Which are reachable through a self-serve HTTP API, what is the pricing basis, and what would one 45–60 s talking clip cost (Oct 2026)?

### Takeaway
The cheapest options that take your own audio, can be driven over an API, and render 45–60 s in one pass are Kling AI Avatar 2.0 via fal.ai (about $2.50–$6.90 per clip) and ByteDance OmniHuman 1.5 via fal.ai (about $7.20–$9.60, single pass at 720p). Re-dubbing an existing selfie video with sync.so costs about $3–$8 per clip, plus a $5/month plan if you buy direct. OmniHuman 2.0 on BytePlus is listed at about $0.07/s (about $4.20/min), but it launched Oct 15, 2026 and reportedly with region locks. OpenAI's Sora 2 API no longer exists (removed Sept 24, 2026). Google Veo 3.1 can't take your own audio, and Gemini Omni Flash reportedly refuses still-photo-plus-audio lip sync.

### Cited Findings

#### ByteDance OmniHuman (1.0 / 1.5 / 2.0)
- **OmniHuman 1.5 on fal.ai, $0.16 per second of output.** The fal v1.5 model page reads "Your request will cost $0.16 per second" [host, undated] — [fal OmniHuman v1.5](https://fal.ai/models/fal-ai/bytedance/omnihuman/v1.5). A fal user guide from **January 2026 [>6 mo]** also gives $0.16/s — [fal user guide](https://fal.ai/learn/devs/omnihuman-15-user-guide).
- **Conflicting older fal figure.** An older fal page for the original OmniHuman says v1.5 costs "the same $0.14 per second" as v1.0. The search tool judged that page out of date [host, undated] — [fal OmniHuman (v1)](https://fal.ai/models/fal-ai/bytedance/omnihuman).
- **Billing basis on fal.** "Both models charge based on the duration field in the response, which matches input audio length" [host] — [fal OmniHuman 1.5 vs 1.0](https://fal.ai/learn/biz/omnihuman-15-vs-omnihuman-comparison).
- **Other resellers (OmniHuman 1.5), all [host], undated:**
  - Muapi: $0.045/s (720p) and $0.060/s (1080p) — [Muapi](https://muapi.ai/comparison/omnihuman-1-5)
  - AIMLAPI: $0.182–$0.208/s — [AIMLAPI](https://aimlapi.com/models/omnihuman-v1-5)
  - ModelsLab: $0.14/s — [ModelsLab](https://modelslab.com/models/byteplus/omni-human-1.5)
  - Pixazo: $0.16/s — [Pixazo](https://www.pixazo.ai/models/omnihuman)
- **OmniHuman 2.0 on BytePlus (official API).** The BytePlus product page lists about **$0.07 per second**, and a **$0.12** figure also appears on the page; the search tool couldn't say which applies to what — [BytePlus OmniHuman 2.0](https://www.byteplus.com/en/product/OmniHuman). A SuperMaker article dated **Oct 15, 2026** says 2.0 went live that day at $0.07/s [blog] — [SuperMaker](https://supermaker.ai/blog/omnihuman-2-0-launch/).
- **OmniHuman 2.0 availability caveats.**
  - A MindStudio piece from about mid-Oct 2026 says 2.0 was shown publicly but was **region-locked at launch**, with no firm public release timeline [blog] — [MindStudio](https://www.mindstudio.ai/blog/bytedance-omnihuman-2-avatar-video).
  - Atlas Cloud says it could not confirm a public 2.0 playground, detailed input limits, or an Atlas endpoint. The BytePlus documentation it could verify covered v1.5 only [host] — [Atlas Cloud](https://www.atlascloud.ai/blog/tips/omnihuman-2.0-full-body-gesture-generation).
  - No fal.ai or Replicate listing for OmniHuman 2.0 turned up — (search result set above).
- **Estimated cost for one clip:**

  | Version and host | Rate | 45 s | 60 s |
  |---|---|---|---|
  | 1.5 on fal | $0.16/s | **$7.20** | **$9.60** |
  | 1.0 on fal | $0.14/s | $6.30 | $8.40 |
  | 2.0 on BytePlus | $0.07/s | $3.15 | $4.20 |
  | 2.0 on BytePlus, if the $0.12 figure applies | $0.12/s | $5.40 | $7.20 |

  These are my arithmetic on the rates cited above.

#### Kling AI (Kuaishou): AI Avatar 2.0, Lip Sync, official API
- **Official credit rates (Kling app).** Avatar 2.0 Standard costs 4 credits/s and Professional 8 credits/s, with a 2-second minimum per generation. Maximum length is 5 minutes [blog, undated] — [The Rundown](https://www.therundown.ai/tools/kling-avatar-2-0).
- **fal.ai.** Avatar v2 Standard is about **$0.0562/s** and Pro **$0.115/s** [host, undated] — [fal Kling AI Avatar v2 Pro](https://fal.ai/models/fal-ai/kling-video/ai-avatar/v2/pro).
- **Other resellers, all [host], undated:**
  - PiAPI: Standard $0.052/s and Pro $0.26/s on its pricing list — [PiAPI Kling Avatar](https://piapi.ai/kling-ai-avatar). PiAPI's own guide gives Pro as $0.104/s, so its figures conflict — [PiAPI guide](https://piapi.ai/blogs/kling-ai-avatar-guide-standard-vs-pro).
  - WaveSpeed Pro: billed on audio duration with a 5 s minimum; a 10 s clip costs $1.12, i.e. about $0.112/s — [WaveSpeed](https://wavespeed.ai/docs/docs-api/kwaivgi/kwaivgi-kling-v2-ai-avatar-pro).
  - Kie.ai: about $0.04/s for 720p (Standard) and about $0.08/s for 1080p (Pro), up to 300 s per generation — [Kie.ai](https://kie.ai/kling-ai-avatar).
- **useapi.net (unofficial wrapper that drives your own Kling web account).** It lists Avatar 2.0 Std at 4 credits/s (about $0.04) and Pro at 8 credits/s (about $0.09). Kling's separate **LipSync** endpoint (video plus audio) costs about $0.06 per 5 s clip there [host, undated] — [useapi.net Kling](https://useapi.net/docs/api-kling-v1). The same page title mentions Kling "v3, O3" models.
- **Official Kling developer API.**
  - The [official] pricing page lists Avatar and Lip Sync among its API features. Its snippet shows **Kling 4.0** at 1.0 unit/s (720p) and 1.5 units/s (1080p) without video input — [Kling dev pricing](https://kling.ai/dev/pricing).
  - Third-party cost guides read the official page as **Avatar 720p = 0.4 units/s (about $0.056/s)** and **1080p = 0.8 units/s (about $0.112/s)**, at a **$0.14/unit** list price — [CostGoat (Oct 2026)](https://costgoat.com/pricing/kling); [Costbench](https://costbench.com/software/ai-media-apis/kling-api/). The search tool did not isolate which of these pages gave the avatar rows.
- **Official API minimum purchase.**
  - A **$9.80 trial package of 100 units** (30-day validity, 5 concurrent tasks) — [Atlas Cloud](https://www.atlascloud.ai/blog/tips/kling-ai-api-pricing). FrameSurfer says it can be bought up to 5 times — [FrameSurfer](https://framesurfer.com/blogs/kling-ai-pricing). Camclo3d reports a 30% first-purchase discount — [camclo3d](https://camclo3d.com/blog/kling-ai-pricing). Agentgid notes it saw the trial price only in a snippet — [agentgid](https://agentgid.com/assets/kling/).
  - The smallest standard package is **$700 for 5,000 units** (180 days) — [ToolColumn](https://www.toolcolumn.com/pricing/kling-ai-pricing).
  - API units are a separate budget from web-subscription credits — [ToolColumn](https://www.toolcolumn.com/pricing/kling-ai-pricing).
  - Conflict: one page in the same result set claims the official API starts at $4,200/month with a 3-month commitment. The tool did not isolate which page, and it contradicts the prepaid-package model.
- **Kling 3.0 with native audio (generates its own sound; not driven by your audio).** About $0.126/s at 720p and $0.168/s at 1080p, from a third-party table at $0.14/unit. The page wasn't isolated; the $0.168 figure matches Costbench's headline range — [Costbench](https://costbench.com/software/ai-media-apis/kling-api/).
- **Estimated cost for one clip (my arithmetic):**
  - Kling Avatar 2.0 on fal: Standard **$2.53 (45 s) / $3.37 (60 s)**; Pro **$5.18 / $6.90**.
  - Official API at 0.4 units/s: 18 units (45 s) or 24 units (60 s) at 720p, which is $2.52 / $3.36 at list price. A 60 s 1080p clip takes 48 units. So the $9.80 trial package (100 units) covers about four 60 s attempts at 720p or two at 1080p.

#### Sync Labs (sync.so): video plus new audio re-dubbing
- **lipsync-2-pro, official.** About **$0.067–$0.083 per second** at 25 fps, charged per processed output second [official] — [sync.so lipsync models](https://sync.so/docs/models/lipsync); [sync.so billing](https://sync.so/docs/product/billing).
- **The rate depends on plan tier.** Entry tiers pay $0.08325/s and the top tier $0.06675/s. The same pricing page's FAQ says all models cost $0.05/s, which conflicts with its own table and may be stale [official] — [sync.so pricing](https://sync.so/pricing).
- **sync-3 (newest flagship), official.** **$0.107–$0.133/s** at 25 fps. Maximum video duration depends on plan, "from 1 minute on Hobbyist up to 30 minutes on Scale+" [official] — [sync-3 docs](https://sync.so/docs/models/sync-3).
- **Plans [official].**

  | Plan | Price | Max duration |
  |---|---|---|
  | Hobbyist | $5/mo | 1 min |
  | Creator | $19/mo | 5 min |
  | Growth | $49/mo | 10 min |
  | Scale | $249/mo | 30 min |

  Source: [sync.so billing](https://sync.so/docs/product/billing).
- **Free trial [official].** One sync-3 generation per month, 15 s maximum — [sync.so free trial](https://sync.so/docs/free-trial).
- **react-1.** Described as the model for "expressive lip sync with emotions on short clips". No price or duration cap was found [official] — [sync.so lipsync models](https://sync.so/docs/models/lipsync).
- **Hosted versions:**
  - fal.ai: lipsync-2 at about $0.05/s ($3/min) and lipsync-2-pro at **$5/min** (1.67x standard), with five audio/video duration-mismatch modes (e.g. cut_off, loop, silence) [host] — [fal sync-lipsync v2](https://fal.ai/models/fal-ai/sync-lipsync/v2); [fal blog](https://blog.fal.ai/sync-labs-lipsync-2-0-model-now-available-on-fal/).
  - WaveSpeed: lipsync-2-pro at $0.084 per billable second (rounded up) — [WaveSpeed lipsync-2-pro](https://wavespeed.ai/models/sync/lipsync-2-pro). "Lipsync 3" at $0.135/s, capped at 300 s billable ($40.50) — [WaveSpeed lipsync-3](https://wavespeed.ai/models/sync/lipsync-3).
  - Versely's headline claims "Sync Labs $0.04/sec", which conflicts with the official rates [blog / possible competitor] — [Versely](https://www.versely.studio/blog/best-lip-sync-api-2026).
- **Estimated cost for one clip (my arithmetic):**
  - Direct lipsync-2-pro: $3.00–$3.75 (45 s) or $4.02–$5.00 (60 s), plus the $5 Hobbyist plan, so about **$10 all-in for 60 s**.
  - Direct sync-3: $4.82–$5.99 (45 s) or $6.42–$7.98 (60 s), plus the plan.
  - fal lipsync-2-pro: **$3.75 / $5.00**. fal lipsync-2: $2.25 / $3.00.

#### Alibaba Wan 2.2-S2V (speech-to-video) and Wan Animate
- **Alibaba Cloud Model Studio (first-party).** wan2.2-s2v costs **$0.071677/s at 480P** and **$0.129018/s at 720P**. Only successfully generated seconds are billed; failed calls are free [official, undated] — [Alibaba Cloud wan-s2v API](https://www.alibabacloud.com/help/en/model-studio/wan-s2v-api).
- **fal.ai.** $0.20 per video-second at 720p, $0.15 at 580p and $0.10 at 480p, with "video seconds" calculated at 16 fps. The page is about a year old **[>6 mo]** [host] — [fal Wan 2.2 S2V](https://fal.ai/models/fal-ai/wan/v2.2-14b/speech-to-video).
- **Other hosts, all [host], undated:**
  - WaveSpeed: $0.15 per 5 s at 480p and $0.30 per 5 s at 720p, 3 s minimum — [WaveSpeed Wan S2V](https://wavespeed.ai/models/wavespeed-ai/wan-2.2/speech-to-video).
  - Kie.ai: about $0.12/s at 720p, $0.09 at 580p, $0.06 at 480p — [Kie.ai Wan S2V](https://kie.ai/wan-speech-to-video-turbo).
- **Estimated cost for one clip (my arithmetic).** Alibaba 720P: $5.81 (45 s) or $7.74 (60 s); 480P: $3.23 / $4.30. fal 720p: $9.00 / $12.00.

#### Google Veo 3.1 and Gemini Omni Flash
- **Veo 3.1 Gemini API rates, from Sept–Oct 2026 sources.** Per generated second, audio included:

  | Tier | 720p | 1080p | 4K |
  |---|---|---|---|
  | Standard | $0.40 | $0.40 | $0.60 |
  | Fast | $0.10 | $0.12 | $0.30 |
  | Lite | $0.05 | $0.08 | none |

  Only successful generations are billed [blog]. The search tool attributed these rates to "one source" without isolating which of these pages it was: [BenchLM Veo pricing](https://benchlm.ai/media-pricing/veo); [Magic Hour](https://magichour.ai/blog/veo-3-pricing) (Magic Hour sells competing tools); [CloudZero](https://www.cloudzero.com/blog/veo-3-pricing/).
- **Older Veo rates.** Fast $0.15/s, Standard $0.40/s and Veo 3.0 $0.75/s as of **Dec 2025 [>6 mo]** — [AIFreeAPI](https://www.aifreeapi.com/en/posts/veo-3-1-pricing-per-second-gemini-api).
- **Possible retirement of Veo 3.1 preview IDs (unverified).** A source in the Veo pricing result set says Google lists **Oct 22, 2026** as the earliest shutdown date for the three Veo 3.1 *preview* model IDs on the Gemini API, with `gemini-omni-1.1-flash` named as the replacement. I couldn't open Google's page to confirm.
- **Gemini Omni Flash pricing.**
  - Video output is token-billed at 5,792 tokens per second of 720p × $17.50 per 1M tokens, which is about **$0.10/s at 720p**. A single source gives about $0.152/s at 1080p and $0.304/s at 4K [blog] — [eesel Omni Flash pricing](https://www.eesel.ai/blog/gemini-omni-flash-pricing).
  - Gemini Omni 1.1 Flash went to preview on **Aug 27, 2026**, model ID `gemini-omni-flash-preview` [blog] — [eesel Omni 1.1](https://www.eesel.ai/blog/gemini-omni-1-1-flash-pricing).
- **Estimated cost for one clip (my arithmetic; needs stitching, and neither can use your own audio).**
  - Veo: 48 s (6 × 8 s) is $19.20 on Standard or $4.80 on Fast; 64 s (8 × 8 s) is $25.60 on Standard or $6.40 on Fast.
  - Omni: about $6 for 60 s at 720p if a usable workflow existed (see section 3).

#### OpenAI Sora 2
- **The API is gone.** OpenAI's deprecations page says developers were notified on **Mar 24, 2026** that the Videos API and the Sora 2 aliases and snapshots would be removed on **Sept 24, 2026** [official] — [OpenAI deprecations](https://developers.openai.com/api/docs/deprecations). Secondary reports say the shutdown happened, with no recommended replacement — [TechJack Solutions](https://techjacksolutions.com/ai-brief/openai-videos-api-sora-2-deprecated-september-2026/); [AI Watch](https://ai-watch-blog.vercel.app/en/posts/2026-09-24-sora-api-shutdown-effective/); [AF.net](https://af.net/realtime/openai-to-shut-down-sora-api-on-september-24-2026-with-no-replacement-announced/).
- **The app is gone too (secondary sources only).** The consumer Sora app and web experience reportedly closed **Apr 26, 2026**, with export via sora.chatgpt.com/sunset [blog] — [VideoCreate](https://videocreate.org/guides/sora-shutdown). I didn't find the OpenAI help article for this date.
- **Historical prices, no longer purchasable.** sora-2 cost $0.10/s (720p). sora-2-pro cost $0.30/s (720p), $0.50/s (1024p) and $0.70/s (1080p) — [eesel](https://www.eesel.ai/blog/sora-2-in-the-api-pricing); [Sume](https://www.sume.com/blog/sora-2-api-pricing).

#### Runway
- **Act-Two on the API.** **5 credits/s, which is $0.05/s** at $0.01 per credit, with a $10 minimum initial purchase. API credits are separate from subscription credits [blog] — [VideoMake](https://videomake.ai/blog/runway-ml-pricing); [FairStack](https://fairstack.ai/blog/runway-pricing); [The Rundown, Runway Dev](https://www.therundown.ai/tools/runway-dev). The reseller CometAPI lists $0.04/s [host] — [CometAPI](https://www.cometapi.com/models/runway/act-two/).
- **Act-Two in the app.** 3 s minimum and up to 30 s per generation (search summary of the Runway pricing result set).
- **Runway Characters.**
  - Launched **Mar 9, 2026 [>6 mo]** as a real-time video agent API for conversational characters, built on the GWM-1 world model and creating personas "from a single image with no fine-tuning" [official] — [Runway: Introducing Characters](https://runway.com/news/introducing-runway-characters); [Runway changelog](https://runway.com/changelog).
  - Runway Dev launched **Jul 8, 2026**, and Characters are "only available on Runway Dev" [official] — [Runway Dev](https://runwayml.com/news/introducing-runway-dev).
  - Third-party billing figure: 2 credits upfront plus 2 credits per 6 s — [The Rundown](https://www.therundown.ai/tools/runway-dev). Unverified.
- I found no audio-file-driven lip-sync product or price from Runway in 2026 sources (see Gaps).

#### Pika (Pikaformance)
- **Credit cost.** **3 credits per second of audio** on every plan; free clips are capped at 10 s and paid at 30 s; output is 720p. 10 s costs 30 credits and 30 s costs 90 [blog] — [eesel Pika pricing](https://www.eesel.ai/blog/pika-ai-pricing); [WhatAIDoINeed](https://whataidoineed.com/tool/pika-labs).
- **Dollar estimate.** One third-party guide puts 10 s at $1.50 and 30 s at $4.50 on the Standard plan, but plan prices conflict across sources ($8–$10 vs $35/mo for 700 credits) [blog] — (same result set).
- **API access is unconfirmed.** One aggregator lists the API as **"Not available"** for Pikaformance — [SOTA2](https://www.sota2.com/products/pika-pikaformance). A Pika "API Club" ($10/mo with a $10 usage credit) is mentioned elsewhere, but nothing confirms Pikaformance is on it.
- **Caution.** Several result domains (pika-labs.org, pikaais.com, pikaslabs.com) look like unofficial lookalike sites, not Pika's own (pika.art), so I didn't rely on them.
- **Estimated cost for one clip.** 60 s = 180 credits (two 30 s runs), or about $9 at the third-party $1.50 per 10 s figure.

#### Higgsfield (Speak / Lipsync Studio)
- **Segmind hosts "Higgsfield Speech 2 Video" (Speak v2).** It takes an image plus MP3 audio, offers high or mid quality, and makes 5, 10 or 15 s clips. The price section showed no figure, and the page is about 13 months old **[>6 mo]** [host] — [Segmind](https://www.segmind.com/models/higgsfield-speech2video).
- **Synthesys cost tests (checked Oct 13, 2026; Synthesys sells rival avatar products) [competitor]** — [Synthesys](https://synthesys.io/blog/higgsfield-vs-heygen/):
  - Speak 2.0 at 720p is about 168 credits/min, about **$8.26/min on the Plus plan**.
  - Its own Speak 2.0 High test cost about $2.75 for 13 s.
  - "Kling Speak" inside Higgsfield is about $2.95/min, and "Avatar V" about $2.32/min on Creator.
- **Plan prices conflict.** Sources give $49/mo for 1,000 credits, $59/mo for 1,200, and an older $29/mo listing — [Aliteq](https://aliteq.com/ai-talking-avatar-with-higgsfield-2026); [Synthesys](https://synthesys.io/blog/higgsfield-vs-heygen/).
- **Lipsync Studio [official marketing].** It bundles several lip-sync engines, and cost ranges "from $0.50 for a short clip to $9.65 for long-form" — [Higgsfield AI Talking Avatar](https://higgsfield.ai/ai-talking-avatar); [Higgsfield lipsync blog](https://higgsfield.ai/blog/make-ai-lipsync-videos).
- **No official metered Higgsfield API was found.** The only API-like listing was the Segmind one above.

#### Cost summary for one 45–60 s clip (Oct 2026, my arithmetic on the rates above)

| Option | Uses your audio? | 45 s | 60 s | One pass for 60 s? | Self-serve API |
|---|---|---|---|---|---|
| Kling AI Avatar 2.0, fal Std / Pro | Yes (photo + audio) | $2.53 / $5.18 | $3.37 / $6.90 | Yes (up to 5 min) | fal |
| Kling Avatar, official API (720p / 1080p) | Yes | ≈$2.52 / $5.04 | ≈$3.36 / $6.72 | Yes | Kling dev API; $9.80 trial package |
| OmniHuman 1.5, fal | Yes | $7.20 | $9.60 | Yes at 720p (60 s cap); 1080p caps at 30 s | fal |
| OmniHuman 2.0, BytePlus | Yes (+ prompt) | $3.15–$5.40 | $4.20–$7.20 | Yes (4–300 s audio) | BytePlus; region-lock reported |
| sync.so lipsync-2-pro (selfie video + audio) | Yes | $3.00–$3.75 + $5 plan | $4.02–$5.00 + $5 plan | Yes (Hobbyist 1-min cap) | sync.so; fal $3.75 / $5.00 |
| sync.so sync-3 | Yes | $4.82–$5.99 + plan | $6.42–$7.98 + plan | Yes | sync.so |
| Wan 2.2-S2V, Alibaba 720P / fal 720p | Yes | $5.81 / $9.00 | $7.74 / $12.00 | Unknown (max audio not found) | Alibaba Model Studio; fal |
| Runway Act-Two | No (driven by a performance video) | $2.25 | $3.00 (2 × 30 s) | No | Runway API |
| Pikaformance | Yes | ≈135 credits | ≈180 credits (≈$9) | No (30 s cap) | API not confirmed |
| Higgsfield Speak 2.0 | Yes | — | ≈$8.26 + subscription | Unknown | No official API found |
| Veo 3.1 Std / Fast | No (makes its own voice) | $19.20 / $4.80 (48 s) | $25.60 / $6.40 (64 s) | No (8 s clips) | Gemini API |
| Gemini Omni Flash | Audio input yes, but photo + audio lip sync refused | — | ≈$6 if allowed | No (10 s cap) | Gemini API (preview) |
| Sora 2 | No | — | — | — | Removed Sept 24, 2026 |

### Inferences
- The leading API-drivable candidates for this use case are Kling AI Avatar 2.0 via fal, OmniHuman 1.5 via fal, and (for the selfie-video path) sync.so lipsync-2-pro or sync-3. A full 60 s clip from any of them costs under $10, so a $30 budget allows roughly 3–8 attempts depending on the tool.
- OmniHuman 2.0 at $0.07/s would be the best value if a US user can actually get BytePlus access. Its Oct 15, 2026 launch and reported region lock make it a "check, don't count on it" option.
- Kling's official API is affordable only through the $9.80 trial package. The next tier ($700) is far over budget, so fal or another host is the practical route.
- For sync.so, buying direct adds a $5/month plan, so fal's per-minute pricing ($5/min for lipsync-2-pro) is cheaper for a one-off clip. Direct is the only route I found to sync-3 apart from resellers like WaveSpeed.

### Gaps
- **Research limitations (apply to every section).**
  - WebFetch failed with DNS errors (`getaddrinfo ENOTFOUND`) for fal.ai, sync.so, platform.openai.com and replicate.com.
  - Direct curl through the session proxy got 403 CONNECT policy denials for replicate.com, byteplus.com, docs.byteplus.com, sync.so, reddit.com, ai.google.dev, developers.openai.com, docs.dev.runwayml.com, app.klingai.com and alibabacloud.com.
  - The shared per-turn WebSearch budget ran out after about 25 searches.
  - So **every finding here comes from search-engine result summaries and snippets, not full-page reads**. Prices quoted "from" fal, sync.so, Kling, OpenAI, BytePlus and Google pages are as the search tool summarized them and may be cached or stale. They should be re-checked on the live pages before any spend.
- **Replicate.** Pricing and availability for OmniHuman, Kling Avatar/Lip Sync, sync lipsync and Wan S2V on Replicate weren't retrieved.
- **Dreamina/CapCut.** OmniHuman access, credit costs and limits there weren't researched (budget exhausted).
- **OmniHuman on fal.** Whether the fal v1.5 price differs at 1080p is unconfirmed. The maximum audio length for OmniHuman 1.0 on fal wasn't found.
- **Kling official avatar rates.** The 0.4 / 0.8 units/s figures are third-party readings of the official page and weren't seen directly. Whether a US individual can buy the $9.80 trial self-serve wasn't confirmed.
- **Account and access requirements.** BytePlus account and verification requirements, KYC, and US eligibility for OmniHuman 2.0 are unknown. Whether an individual US user can sign up for Alibaba Model Studio international is unconfirmed.
- **fal.ai minimum credit top-up** wasn't retrieved.
- **MiniMax/Hailuo.** Nothing was retrieved on any talking-avatar or audio-driven lip-sync product or API (budget exhausted). I can't say whether one exists.
- **Wan 2.2 Animate.** Pricing and limits on fal, Replicate or Alibaba weren't retrieved. Nor was whether newer Wan versions (2.5 and later) take an input audio track.

## 2. Does each accept a user-supplied audio track for lip sync? Max duration per generation, resolution, render time, and how people stitch longer clips

### Takeaway
OmniHuman, Kling AI Avatar, Wan 2.2-S2V, Pikaformance, Higgsfield Speak and sync.so all take your audio. Veo 3.1 and the late Sora 2 generate their own speech and won't lip-sync to a supplied file. Gemini Omni takes audio but reportedly refuses the photo-plus-audio lip-sync combination. Runway Act-Two is driven by a performance video, not audio. A 45–60 s clip can be made in **one pass** with OmniHuman 1.5 (720p, 60 s cap), OmniHuman 2.0 (300 s), Kling Avatar 2.0 (5 min) and sync.so (plan cap of 1 min or more), which avoids stitching.

### Cited Findings

#### Audio-driven, user-supplied audio
- **OmniHuman 1.5 on fal.** Takes an image plus audio; billed on input audio length — [fal comparison](https://fal.ai/learn/biz/omnihuman-15-vs-omnihuman-comparison). "720p for faster, higher-quality output (up to 60s audio) or 1080p for higher resolution (up to 30s)" (Jan 2026 **[>6 mo]**) — [fal user guide](https://fal.ai/learn/devs/omnihuman-15-user-guide).
- **OmniHuman 2.0 on BytePlus.** Takes "a single image, audio, and text prompt" [official] — [BytePlus](https://www.byteplus.com/en/product/OmniHuman). Audio runs **4–300 s** (WAV/MP3 under 15 MB) — [SuperMaker, Oct 15, 2026](https://supermaker.ai/blog/omnihuman-2-0-launch/). Sources attribute up to 5 minutes in one continuous shot to BytePlus. The search summary didn't isolate which page said it; candidates are [MindStudio](https://www.mindstudio.ai/blog/bytedance-omnihuman-2-avatar-video) and [Atlas Cloud](https://www.atlascloud.ai/blog/tips/omnihuman-2.0-full-body-gesture-generation). Atlas Cloud itself says it couldn't verify 2.0 input limits.
- **Kling AI Avatar 2.0.** Animates the mouth to match uploaded or generated speech, including singing. Maximum is 5 minutes, with a 2 s minimum — [The Rundown](https://www.therundown.ai/tools/kling-avatar-2-0). Kie.ai lists 720p (Standard) and 1080p (Pro), up to 300 s per generation — [Kie.ai](https://kie.ai/kling-ai-avatar). Works across humans, animals and cartoons [host] — [fal Kling Avatar v2 developer guide](https://fal.ai/learn/devs/kling-avatar-v2-developer-guide); [fal v2 vs v1](https://fal.ai/learn/devs/kling-avatar-v2-vs-v1-evolution-ai-powered-avatar-generation).
- **Kling Lip Sync (video plus audio).** A separate endpoint, about $0.06 per 5 s on useapi.net — [useapi.net](https://useapi.net/docs/api-kling-v1). Its maximum length wasn't found.
- **sync.so.** Takes video plus audio. Maximum duration is by plan (1 min Hobbyist to 30 min Scale+), and the free trial is 15 s — [sync.so lipsync models](https://sync.so/docs/models/lipsync); [billing](https://sync.so/docs/product/billing); [free trial](https://sync.so/docs/free-trial). On fal you choose how to handle audio and video length mismatches (cut_off, loop, silence, etc.) — [fal sync v2](https://fal.ai/models/fal-ai/sync-lipsync/v2).
- **Wan 2.2-S2V.** Takes image plus audio. Resolutions are 480P and 720P on Alibaba — [Alibaba Cloud](https://www.alibabacloud.com/help/en/model-studio/wan-s2v-api) — and 480p, 580p and 720p on fal, billed at 16 fps "video seconds" — [fal Wan S2V](https://fal.ai/models/fal-ai/wan/v2.2-14b/speech-to-video).
- **Pikaformance.** Audio-driven at 720p, with a 10 s cap on free and 30 s on paid — [eesel](https://www.eesel.ai/blog/pika-ai-pricing).
- **Higgsfield.**
  - Speak v2 via Segmind takes an image plus MP3 and makes 5, 10 or 15 s clips **[>6 mo]** — [Segmind](https://www.segmind.com/models/higgsfield-speech2video).
  - Lipsync Studio takes a photo plus a script or audio — [Higgsfield](https://higgsfield.ai/ai-talking-avatar).
  - Higgsfield also markets photo-plus-voice lip sync using Gemini Omni Flash ("lip sync driven by the audio") [official marketing; contradicted below] — [Higgsfield blog](https://higgsfield.ai/blog/how-to-use-gemini-omni-flash-multi-shot-video).

#### Not driven by your audio
- **Veo 3.1.** Generates its own dialogue, sound effects and music; "Veo doesn't accept audio as input" [blog] — [Opus Clip comparison](https://www.opus.pro/blog/gemini-omni-vs-veo-3-which-google-ai-video-model); [Picsart](https://picsart.com/blog/google-omni-vs-veo-3/). A secondary source citing Google's docs says 1080p and 4K work only at 8 s (Veo pricing result set). Google's docs list an "Extension" feature (personGeneration "allow_all" for text-to-video and Extension) — [Gemini API Veo docs](https://ai.google.dev/gemini-api/docs/veo).
- **Gemini Omni Flash.**
  - It *does* accept audio as an input ("provide an audio clip and instruct Gemini Omni to synchronize specific visual events to it") — [Artlist](https://artlist.io/blog/veo-3-1-vs-gemini-omni-flash-how-google-just-changed-the-way-you-edit-video/); [Opus Clip](https://www.opus.pro/blog/gemini-omni-vs-veo-3-which-google-ai-video-model).
  - Output is up to 720p (1080p and 4K upscale "still to come"), in **3–10 s clips** [blog] — (same result set).
  - VentureBeat reports clips cap at 10 s and that the model **refuses a still photo of a person combined with an audio clip for lip sync**. It will, however, translate a recording of someone talking into another language [press] — [VentureBeat](https://venturebeat.com/technology/googles-gemini-omni-flash-hits-the-api-turning-enterprise-video-production-into-a-conversation).
- **Sora 2.** Was text/image-to-video with its own generated audio. It is now removed from the API (section 1). No user-audio support was found in any source.
- **Runway Act-Two.** "Performance capture: record yourself acting and drive a character with your movement and expression" (head position, facial expressions, hand and upper-body gestures from a reference video). The app takes 3–30 s per generation [blog] — [VideoMake](https://videomake.ai/blog/runway-ml-pricing); [FairStack](https://fairstack.ai/blog/runway-pricing). The sources mention no audio-driven mode.
- **Runway Characters.** A real-time conversational avatar (voice, tool calling, knowledge base) made from a single image [official, Mar 2026 **[>6 mo]**] — [Runway](https://runway.com/news/introducing-runway-characters). It is not described as lip-syncing a supplied audio file.

#### Render time
- No render-time figures were retrieved for any tool (see Gaps).

#### Stitching longer clips
- The only drift-and-length note found: an inference-platform page says OmniHuman 1.5 generations "approaching the 30-second maximum can accumulate drift" [host] — [inference.sh](https://inference.sh/apps/bytedance/omnihuman-1-5).
- Gemini Omni lip sync "holds up until about 6 to 7 seconds before it begins to drop off" for a single speaker [competitor/aggregator test] — [invideo Omni Flash review](https://invideo.io/blog/gemini-omni-flash-review/). That alone argues against assembling a 60 s monologue from Omni segments.

### Inferences
- For a 45–60 s monologue, stitching is avoidable. OmniHuman 1.5 at 720p (60 s cap), OmniHuman 2.0 (300 s), Kling Avatar 2.0 (300 s) and sync.so (Hobbyist 1 min cap) each fit the whole clip in one generation. Veo (8 s), Omni (≤10 s), Pikaformance (30 s), Higgsfield Speak v2 (≤15 s) and OmniHuman 1.5 at 1080p (30 s) would need 2–8 joined segments.
- One cited host note says OmniHuman 1.5 drifts on long runs. If that holds, splitting the audio at sentence boundaries into about 20–30 s chunks, regenerating each from the same source photo, and hard-cutting or crossfading may preserve identity better than one long run, at the same per-second cost. This is untested reasoning, not a sourced practitioner technique.
- Veo and Sora-style models that write their own speech can't give "your words in your voice" without separate re-dubbing, for example running sync.so over the Veo output. That doubles cost and processing steps.

### Gaps
- No render or queue times were retrieved for OmniHuman (fal/BytePlus), Kling Avatar, sync.so, Wan S2V or Pikaformance.
- Maximum audio length per call wasn't found for Wan 2.2-S2V (Alibaba or fal), Kling Lip Sync, or OmniHuman 1.0.
- No practitioner write-ups on stitching technique (last-frame chaining, audio chunking, crossfades, consistency across segments) were retrieved. Reddit and YouTube were unreachable and the search budget ran out.
- Whether Gemini Omni's "translate a recording of someone talking" mode can take a user-supplied target audio file (rather than generating translated speech) is unknown.
- It's unconfirmed whether Act-Two keeps the driving video's audio in the output, and whether Runway Characters can be fed a pre-recorded audio file.

## 3. Policies: do they refuse or restrict photorealistic real-person images or likenesses? Is self-likeness allowed with verification?

### Takeaway
The strictest are ByteDance Seedance 2.0/2.5 (real faces blocked unless identity-verified or authorized), Google Gemini Omni (photo plus audio lip sync refused as an anti-deepfake measure), Veo (image-to-video of people allowed only with personGeneration "allow_adult", plus reported face-detection and region refusals) and Sora (dead; its API rejected human faces, and self-likeness ran only through the in-app verified Cameo flow). For OmniHuman, Kling, sync.so, Wan and fal/Replicate hosting, no real-person upload restriction turned up in the sources retrieved. That is a gap, not evidence of permissiveness.

### Cited Findings

#### ByteDance Seedance 2.0 / 2.5 (relevant because BytePlus also sells OmniHuman)
- **Feb 10, 2026 [>6 mo].** ByteDance "urgently suspended" a Seedance 2.0 feature that produced voice characteristics from facial photos. Jimeng (the Chinese platform) operators said they "will not allow real-human-like photos or videos to be used as reference subjects" [press] — [TechNode](https://technode.com/2026/02/10/bytedance-suspends-seedance-2-0-feature-that-turns-facial-photos-into-personal-voices-over-potential-risks/).
- **ModelArk/BytePlus documentation, as quoted by third parties.** "Seedance 2.5 and Seedance 2.0 series models do not support directly uploading reference images/videos that contain real human faces." A specific real person requires identity verification or prior legal authorization. These are vendor blogs selling workarounds — [SeedRouter](https://seedrouter.ai/blog/seedance-real-person-error); [Sume](https://www.sume.com/blog/seedance-real-human-face-reference-images-rejected-2-5-and-2-0-what-to-do-on-sume); [Yingtu](https://yingtu.ai/en/blog/seedance-2-0-human-face).
- **The whole model was not suspended.** Specific real-person reference workflows were restricted, per one of the same blogs — [GlobalGPT](https://www.glbgpt.com/hub/seedance-2-0-face-to-voice-suspended-privacy-risks/). A "Portrait" tier said to bypass the block couldn't be confirmed officially.

#### OpenAI Sora 2 (historical; product now shut down)
- **API face rejection.** A developer forum post from the Sora 2 API preview (**about Oct 2025 [>6 mo]**) says "input images with faces of humans are currently rejected", and that real people, including public figures, cannot be generated. The only API option was a reference image or video, which moderation blocks if it contains a person — [OpenAI Developer Community](https://community.openai.com/t/sora-2-api-are-the-cameo-features-coming-to-the-api/1361267).
- **Cameo consent was app-only.** OpenAI can't generate anyone from a prompt or photo unless they've submitted a verified cameo [press] — [Implicator](https://www.implicator.ai/openai-wants-your-face-on-its-feed/).
- **Further tightening (secondary).** 2026 guides say face uploads for character creation were fully banned from Feb 2026, and that the API never supported Cameo embedding [blog **[>6 mo]**] — [APIYI](https://help.apiyi.com/en/sora-2-character-face-restriction-policy-2026-en.html); [Wentuo](https://blog.wentuo.ai/en/sora-2-character-consistency-cameo-api-guide-2026-en.html).

#### Google Veo 3.1 and Gemini Omni
- **Gemini API Veo docs [official].** personGeneration for "Text-to-video & Extension" is `"allow_all"` only; for "Image-to-video, Interpolation, & Reference images" it is `"allow_adult"` only. Reference images take "up to three asset images of a single person, character, or product", and safety filters cover "uploaded photos" — [Gemini API Veo docs](https://ai.google.dev/gemini-api/docs/veo).
- **Developer forum reports (dates not shown).**
  - "Veo 3.1 image-to-video rejects documented personGeneration=allow_adult" — [Forum thread 181139](https://discuss.ai.google.dev/t/veo-3-1-image-to-video-rejects-documented-persongeneration-allow-adult/181139).
  - Errors "when human like face/model detected" — [Forum thread 109707](https://discuss.ai.google.dev/t/veo3-1-giving-error-in-generation-from-image-when-human-like-face-model-detected/109707).
  - A UK user blocked from "images of realistic people because i am in england" — [Forum thread 98350](https://discuss.ai.google.dev/t/so-google-veo-wont-let-me-use-images-of-realistic-people-because-i-am-in-england-even-though-the-images-are-generated-using-an-ai-so-they-are-not-real-people/98350).
  - A non-celebrity got the refusal "we can't create videos from input images containing celebrity or their likenesses" (per the search summary of these threads).
- **Consumer photo-to-video.** It launched in the Gemini app for AI Pro and Ultra subscribers **[>6 mo, 2025]** — [TechRadar](https://www.techradar.com/computing/artificial-intelligence/google-releases-photo-to-video-gemini-veo-3-capabilities-and-it-might-just-blow-your-mind).
- **Gemini Omni Flash.** It "refuses a still photo of a person combined with an audio clip for lip-sync", described as a deliberate anti-deepfake measure [press] — [VentureBeat](https://venturebeat.com/technology/googles-gemini-omni-flash-hits-the-api-turning-enterprise-video-production-into-a-conversation). Third-party sellers advertise photo-plus-voice lip sync on Omni anyway, which is unverified and possibly via their own wrappers — [Higgsfield](https://higgsfield.ai/blog/how-to-use-gemini-omni-flash-multi-shot-video); [omni-flash.net](https://omni-flash.net/lip-sync).

#### Runway
- Runway published a safety post on building interactive AI characters responsibly. Its content wasn't retrieved [official] — [Runway safety](https://runway.com/news/safety/building-interactive-ai-characters-responsibly).

### Inferences
- A private self-likeness experiment is most likely to be blocked on Google (Omni refuses photo plus audio; Veo face and region filters are inconsistent) and ByteDance Seedance (verification or authorization needed). Sora is moot.
- No real-face block turned up in the sources for OmniHuman 1.5 via fal, Kling Avatar via fal or Kling, sync.so, or Wan S2V. These audio-driven "digital human" products exist to animate a supplied portrait, so a ban like Seedance's would defeat their purpose. Expect terms that require you to own or have consent for the likeness, rather than technical face blocks. This is inference, not verified policy text.
- Seedance's real-face block (BytePlus docs) and OmniHuman 2.0 come from the same vendor. Whether BytePlus applies a similar face check or verification to OmniHuman 2.0 needs checking before relying on it.

### Gaps
- No acceptable-use or likeness clauses were retrieved for fal.ai, Replicate, BytePlus OmniHuman, Kling (app or API), sync.so, Alibaba Model Studio, Pika, Higgsfield or Runway Act-Two.
- Whether BytePlus offers a self-service "real person authorization" or identity-verification flow (for Seedance or OmniHuman) usable by a US individual is unknown.
- No official Google statement on uploading a photo of *yourself* to Veo in Flow or the Gemini app was found.
- Dreamina/CapCut policies on real-face uploads for OmniHuman weren't researched.

## 4. Practitioner opinions: realism, lip-sync accuracy, identity preservation, motion, artifacts, consistency across stitched segments; comparisons with HeyGen/Hedra/each other

### Takeaway
Independent practitioner evidence is **thin in what I could retrieve**. No Reddit, Hacker News, X or YouTube threads came through, and the available comparisons are mostly from hosts, resellers or competitors. Their rough consensus: OmniHuman is strongest for expressive, gesture-aware, full-body motion but less consistent on complex shots, with possible drift near 30 s. Kling Avatar is versatile and cheap. HeyGen Avatar IV (out of scope) was rated highest for pure talking-head realism in at least one 2026 test. Gemini Omni's lip sync degrades after about 6–7 s.

### Cited Findings

#### OmniHuman
- **PiAPI head-to-head with Kling AI Avatar.** PiAPI is an API reseller (it sells Kling access — [PiAPI Kling API](https://piapi.ai/kling-api)), so it isn't independent. One sample: OmniHuman 1.5's avatar "occasionally introduced a subtle head tilt that appeared slightly unnatural relative to the speech delivery" — [PiAPI](https://piapi.ai/blogs/omnihuman-1-5-vs-kling-ai-avatar).
- **Search-tool summary of 2026 comparison pages.** OmniHuman "is built around expressive full-body and gesture-aware motion, but it can be less consistent depending on shot complexity", and is described as strong on "realism and motion quality, especially for creators experimenting with cinematic AI video". The exact page wasn't isolated among [invideo, Aug 2026](https://invideo.io/blog/ai-lipsync-models/), [Blue Lightning TV, May 27, 2026](https://bluelightningtv.com/2026/05/27/best-ai-avatar-generator-in-artlist-heygen-avatar-4-vs-omnihuman-1-5-vs-fabric-1-0-vs-aurora/) and [Artlist](https://artlist.io/blog/best-ai-avatar-generator-platforms/). invideo and Artlist sell access to multiple models.
- **Drift near the length cap.** Longer generations "approaching the 30-second maximum can accumulate drift" [host] — [inference.sh](https://inference.sh/apps/bytedance/omnihuman-1-5).
- **Versely 2026 review.** It argues "none of the tested scenarios favor OmniHuman 1.5 at current pricing", while saying full-body consistency across a long shoot is still worth testing. Versely runs an AI video platform, so it may be a competitor; sample size not shown — [Versely](https://www.versely.studio/blog/omnihuman-1-5-review-2026).
- **The vendor's own paper (Aug 2025 [>6 mo]).** It claims the reasoning module "maintains or slightly improves lip-sync consistency". Its "pseudo last frame" technique is credited by blogs with reducing identity drift — vendor framing, not independent testing — [arXiv 2508.19209](https://arxiv.org/html/2508.19209v1); [Moonlight review](https://www.themoonlight.io/en/review/omnihuman-15-instilling-an-active-mind-in-avatars-via-cognitive-simulation).

#### Kling AI Avatar
- Its main differentiator is range: v2 works across humans, animals and cartoons [host] — [fal developer guide](https://fal.ai/learn/devs/kling-avatar-v2-developer-guide).
- In the PiAPI head-to-head above, Kling was not the model flagged for unnatural head tilt — [PiAPI](https://piapi.ai/blogs/omnihuman-1-5-vs-kling-ai-avatar). That is one test by a reseller.

#### Against HeyGen (out-of-scope platform, cited only as the comparison baseline)
- "For talking-head realism with facial micro-expressions and gesture control, HeyGen's Avatar IV scores highest in my testing", per one 2026 review in the result set. The page wasn't isolated between [Blue Lightning TV, May 27, 2026](https://bluelightningtv.com/2026/05/27/best-ai-avatar-generator-in-artlist-heygen-avatar-4-vs-omnihuman-1-5-vs-fabric-1-0-vs-aurora/) (tests inside Artlist) and HeyGen's own blog, which would make it a competitor source — [HeyGen blog](https://www.heygen.com/blog/best-ai-avatar-generators).
- The search tool's synthesis: HeyGen for polished presenter-style realism, OmniHuman for full-body or gesture-heavy shots, Kling Avatar for non-human characters and flexibility. Mostly vendor or affiliate sources.

#### Gemini Omni Flash
- "For a single person talking, the lip sync holds up until about 6 to 7 seconds before it begins to drop off". Multiple speakers in one frame remain "a major weakness across current AI models" [aggregator/competitor, own tests] — [invideo Omni review](https://invideo.io/blog/gemini-omni-flash-review/).
- Veo versus Omni dialogue: one side-by-side found both lip-synced, Omni word for word and Veo with an extra word inserted. Another source says Veo 3 has the edge on dialogue lip sync, so the sources conflict [blog; the search summary didn't tie each claim to a specific page, most likely these two] — [SkyStudio "4 Tests"](https://skystudioai.com/en/guides/veo-3-1-vs-gemini-omni-flash/); [Opus Clip](https://www.opus.pro/blog/gemini-omni-vs-veo-3-which-google-ai-video-model). Opus Clip and SkyStudio sell video tools; sample size of one test set.

#### Higgsfield Speak
- Synthesys's hands-on cost test of Speak 2.0 High was about $2.75 for 13 s. Synthesys sells a rival product and published no quality verdict in the snippet — [Synthesys](https://synthesys.io/blog/higgsfield-vs-heygen/).

### Inferences
- There is no retrievable independent consensus. The pattern across vendor-adjacent sources is that OmniHuman wins on expressive motion and Kling Avatar on price and flexibility. Long-run identity drift is a concern for OmniHuman 1.5 near its length cap. Any single-model verdict should be treated as low-confidence until confirmed by community threads.
- Since practitioner evidence is weak, the user's own A/B test of Kling Avatar (cheap) against OmniHuman 1.5 (pricier) on 10–15 s of the same audio and photo is the most reliable way to choose. A 10 s pair costs about $2.16 ($0.56 + $1.60) and a 15 s pair about $3.24 ($0.84 + $2.40), by arithmetic on the fal rates above.

### Gaps
- **No Reddit** (r/aivideo, r/StableDiffusion, r/KlingAI_Videos, r/runwayml, r/singularity, r/ChatGPT, r/OpenAI, r/Bard), **Hacker News, X or YouTube** practitioner content was retrieved. Reddit and other hosts were blocked at the proxy, and the search budget ran out before I could try snippet-based searches of those sites. Sample sizes for all cited comparisons are unknown.
- No practitioner reports were found on Pikaformance quality, Wan 2.2-S2V realism or identity hold, Runway Act-Two with real faces, or Kling Avatar identity preservation over 30–60 s.
- No direct comparisons were found against Hedra.
- No evidence was found on consistency across stitched segments for any tool.

## 5. The "selfie video + new audio" path (sync.so and similar): quality, cost, and whether it beats animating a still photo

### Takeaway
sync.so is the main API-drivable re-dubbing option. lipsync-2-pro costs about $0.067–$0.083/s direct (about $4–$5 for 60 s plus a $5/month plan) or $5/min on fal. The newer sync-3 costs $0.107–$0.133/s. Vendor and review sources position lipsync-2-pro for clean close-up talking-head footage and rate sync-3 highly. No independent practitioner comparison of re-dubbing against photo animation was retrieved. Structurally, though, re-dubbing keeps your real face, head motion and lighting and changes only the mouth region.

### Cited Findings

#### sync.so options and pricing
- **Model line-up and rates [official].**
  - lipsync-2-pro: $0.067–$0.083/s
  - sync-3: $0.107–$0.133/s
  - react-1: "expressive lip sync with emotions on short clips"
  - Billing is per processed output second at 25 fps.
  - Sources: [sync.so lipsync models](https://sync.so/docs/models/lipsync); [sync-3](https://sync.so/docs/models/sync-3); [billing](https://sync.so/docs/product/billing).
- **Plans and caps [official].** Hobbyist is $5/mo with a 1 min maximum, enough for a 45–60 s selfie. The free trial gives one 15 s sync-3 generation per month — [billing](https://sync.so/docs/product/billing); [free trial](https://sync.so/docs/free-trial).
- **fal.ai [host].** lipsync-2 at $3/min and lipsync-2-pro at $5/min, with duration-mismatch modes — [fal sync v2](https://fal.ai/models/fal-ai/sync-lipsync/v2); [fal blog](https://blog.fal.ai/sync-labs-lipsync-2-0-model-now-available-on-fal/).

#### Quality claims (no independent tests)
- **Artlist [reseller marketing].** Lipsync 2 Pro is "built for realistic lip sync in clean video setups, especially talking-head videos, close-ups, interviews, presenter footage, and high-detail shots" — [Artlist](https://artlist.io/ai/models/sync-lipsync).
- **Kompozy 2026 review [review site; methodology unconfirmed].** Centers on sync-3 and scores lip-sync accuracy and dubbing highly — [Kompozy](https://kompozy.io/reviews/sync).
- **Picassoia [blog].** Calls Lipsync 2 Pro the high-accuracy option and advises audio "with clear consonants and minimal background noise" — [Picassoia](https://blog.picassoia.com/best-lipsync-tools-for-video-dubbing).

#### Other re-dub routes
- **Kling Lip Sync** (video plus audio): about $0.06 per 5 s via useapi.net, an unofficial wrapper — [useapi.net](https://useapi.net/docs/api-kling-v1).
- **Gemini Omni Flash** will "take a recording of someone talking and translate it into another language" (10 s cap) [press] — [VentureBeat](https://venturebeat.com/technology/googles-gemini-omni-flash-hits-the-api-turning-enterprise-video-production-into-a-conversation). It isn't clear whether you can supply the new audio yourself.

### Inferences
- **Why re-dubbing should look more like the user** (structural, not practitioner-sourced). The output keeps the real person's actual face, skin texture, head and body motion, blinks and background. Identity drift, which photo-animation sources flag for OmniHuman near 30 s, mostly doesn't arise, and artifacts are confined to the mouth and jaw.
- **The trade-off.** Mouth movements that don't match the original head motion or expression can look "dubbed". Clean, front-facing, well-lit selfie footage with little head turning and no hand-over-mouth should help, consistent with Artlist's "clean video setups" framing.
- **Cost.** Within budget either way: about $5 on fal or about $10 direct (lipsync-2-pro, 60 s plus plan), versus about $3.40–$9.60 for photo animation via Kling or OmniHuman on fal.
- **Best of both under $30.** Record a 45–60 s selfie of yourself talking naturally (any words), then re-sync it to the target audio with sync.so lipsync-2-pro or sync-3. In parallel, run Kling Avatar Std on the same audio from a still frame as a comparison.

### Gaps
- No independent practitioner (Reddit, YouTube, HN) assessments of sync.so on handheld or phone selfie footage were retrieved. The question "does re-dubbing beat photo animation?" has no direct practitioner evidence in these notes.
- No react-1 price or limits were found. Whether sync-3 is available on fal (rather than only direct or on WaveSpeed) wasn't confirmed.
- No sync.so render-time figures were found.
- Comparable re-dub services (Kling Lip Sync official API limits, Pika or Higgsfield "lipsync on video") weren't evaluated for quality.

## 6. Which do practitioners consider the most realistic photo-to-talking option in 2026, and is it practical under a $30 budget?

### Takeaway
No independent consensus was retrievable. Among in-scope tools, vendor-adjacent 2026 comparisons point to OmniHuman (1.5 now; 2.0 newly launched) as the most expressive and realistic photo-plus-audio model, with Kling AI Avatar 2.0 as the cheaper, flexible runner-up. HeyGen Avatar IV (out of scope) was rated highest for pure talking-head realism in at least one test. All the leading in-scope options are practical under $30 via fal.ai: about $9.60 for 60 s with OmniHuman 1.5, $3.37–$6.90 with Kling Avatar, and about $5 for sync.so re-dubbing. That leaves room for several attempts.

### Cited Findings
- OmniHuman's positioning is "realism and motion quality" and "expressive full-body and gesture-aware motion", with the caveat "less consistent depending on shot complexity". From the search summary of 2026 comparison pages; page not isolated — [invideo, Aug 2026](https://invideo.io/blog/ai-lipsync-models/); [Blue Lightning TV, May 27, 2026](https://bluelightningtv.com/2026/05/27/best-ai-avatar-generator-in-artlist-heygen-avatar-4-vs-omnihuman-1-5-vs-fabric-1-0-vs-aurora/).
- HeyGen Avatar IV was rated top for talking-head realism "in my testing"; possibly from HeyGen's own blog (competitor) — [Blue Lightning TV](https://bluelightningtv.com/2026/05/27/best-ai-avatar-generator-in-artlist-heygen-avatar-4-vs-omnihuman-1-5-vs-fabric-1-0-vs-aurora/); [HeyGen blog](https://www.heygen.com/blog/best-ai-avatar-generators).
- A contrarian view: "none of the tested scenarios favor OmniHuman 1.5 at current pricing" [possible competitor] — [Versely](https://www.versely.studio/blog/omnihuman-1-5-review-2026).
- OmniHuman 2.0 launched Oct 15, 2026 at about $0.07/s with up to 300 s audio. It is too new for practitioner reviews, and region-locked at launch per one source — [SuperMaker](https://supermaker.ai/blog/omnihuman-2-0-launch/); [MindStudio](https://www.mindstudio.ai/blog/bytedance-omnihuman-2-avatar-video).
- **Budget facts (section 1).** OmniHuman 1.5 on fal costs $0.16/s, i.e. $9.60 for 60 s — [fal](https://fal.ai/models/fal-ai/bytedance/omnihuman/v1.5). Kling Avatar v2 on fal costs $0.0562 / $0.115 per second — [fal](https://fal.ai/models/fal-ai/kling-video/ai-avatar/v2/pro). fal lipsync-2-pro is $5/min — [fal](https://fal.ai/models/fal-ai/sync-lipsync/v2). The Kling official trial is $9.80 for 100 units — [Atlas Cloud](https://www.atlascloud.ai/blog/tips/kling-ai-api-pricing).
- **Ruled out, or poor fits, for the user's goal:**
  - Sora 2: API removed Sept 24, 2026 — [OpenAI deprecations](https://developers.openai.com/api/docs/deprecations).
  - Gemini Omni: refuses photo plus audio lip sync — [VentureBeat](https://venturebeat.com/technology/googles-gemini-omni-flash-hits-the-api-turning-enterprise-video-production-into-a-conversation).
  - Veo 3.1: no audio input, and allow_adult and face filters apply — [Gemini API Veo docs](https://ai.google.dev/gemini-api/docs/veo).
  - Seedance 2.x: real faces blocked without verification — [SeedRouter](https://seedrouter.ai/blog/seedance-real-person-error).
  - Runway Act-Two: needs a driving performance video, not audio — [VideoMake](https://videomake.ai/blog/runway-ml-pricing).
  - Pikaformance: 30 s cap, and API not confirmed — [eesel](https://www.eesel.ai/blog/pika-ai-pricing); [SOTA2](https://www.sota2.com/products/pika-pikaformance).
  - Higgsfield: subscription-priced, with no official metered API found — [Synthesys](https://synthesys.io/blog/higgsfield-vs-heygen/).

### Inferences
- **A plausible, fully API-driven plan under $30, run from a no-GPU Linux sandbox with a `FAL_KEY` env var** (the arithmetic is mine; the endpoints are the fal model pages cited above):
  1. Kling AI Avatar v2 Standard, about $3.37 per 60 s, and/or a 15 s Pro test, about $1.73.
  2. OmniHuman 1.5 at 720p, one 60 s run for about $9.60, or two 30 s halves for the same total.
  3. Optionally, sync.so lipsync-2-pro on a 60 s selfie video, about $5 on fal.

  Total is about $18–$20, leaving margin for one retry.
- **Fallbacks.** If fal is inaccessible, Kling's $9.80 official trial package covers about four 60 s Avatar attempts at 720p. OmniHuman 2.0 via BytePlus ($4.20 per 60 s) is worth checking if US sign-up works.
- **Voice.** Every audio-driven option above lip-syncs whatever audio you supply, so "sounds like them" depends entirely on the user's own recording or a separate voice-clone step. Of the ByteDance tools, the only one that generated a voice from a face (Seedance 2.0) had that feature suspended — [TechNode](https://technode.com/2026/02/10/bytedance-suspends-seedance-2-0-feature-that-turns-facial-photos-into-personal-voices-over-potential-risks/).

### Gaps
- No independent ranking (Reddit or YouTube creator blind tests, sample sizes) of OmniHuman vs Kling Avatar vs Wan S2V vs sync re-dub for *real-person* identity fidelity in 2026 was retrieved, so "most realistic" remains low-confidence.
- No practitioner reviews of OmniHuman 2.0 exist yet in what was retrieved; it launched 8 days before these notes.
- Whether fal.ai or Replicate account policies or minimum top-ups affect a $30 one-off budget wasn't verified.
