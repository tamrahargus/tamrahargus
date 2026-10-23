# AI voice cloning of the user's own voice for a ~45–60 s clip (state as of 23 Oct 2026)

*Method note: no page could be read in full in this session. WebFetch returned DNS errors (ENOTFOUND) for every domain tried. The sandbox egress proxy refused direct connections to elevenlabs.io and artificialanalysis.ai. The shared web-search budget ran out after about 45 searches. So every finding below comes from search-engine result summaries and snippets of the cited pages, not from full-page reads. No Reddit or Hacker News thread came up in any search. Source labels: [Vendor] = the company's own page; [Competitor] = written by a rival vendor; [3rd-party] = review, affiliate or aggregator site; [News]; [Arena] = Artificial Analysis leaderboards; [Practitioner] = an individual user's hands-on account. "Possibly outdated" means older than about 6 months (before roughly late April 2026).*

## 1. ElevenLabs (Oct 2026): cheapest cloning plan, credits, Instant vs Professional cloning, verification, API, cancellation complaints, quality

### Takeaway
Starter is the cheapest plan that includes Instant Voice Cloning (IVC). It costs $6/month (it was $5 until about April 2026) and gives 30,000 credits a month with API access. IVC wants about 1–2 minutes of clean audio, although 30 s can work and the new Eleven v4 reportedly clones from about 10 s. IVC asks only for a consent self-attestation. Professional Voice Cloning (PVC) needs the Creator plan ($22/month) or higher, at least 30 minutes of audio, and a read-aloud "voice captcha" check, and it works only for your own voice. That is far more than a one-off needs. ElevenLabs models are still at or near the top of the arenas, but on the arena that uses cloned voices it now trails HeyGen Voice and Qwen. Trustpilot shows a recurring pattern of renewal and cancellation complaints, so plan to cancel right after the test.

### Cited Findings
**Plans and price**
- Starter is listed at $6/month with 30,000 credits and is the lowest tier with IVC. PVC starts at Creator, $22/month. Free and Starter have no PVC slot. Annual billing works out to about $5/month ($60/year, "10 monthly payments"). These guides were checked June–Sept 2026. [3rd-party]: [Magic Hour](https://magichour.ai/blog/elevenlabs-pricing), [Rinzara](https://rinzara.com/elevenlabs-pricing), [SmartAIToolsReview](https://smartaitoolsreview.com/blog/elevenlabs-voice-cloning-plans-2026), [Comparedge](https://comparedge.com/tools/elevenlabs/pricing), [Gradually.ai](https://www.gradually.ai/en/elevenlabs-pricing/). Note: Magic Hour sells AI video tools, so it partly competes with ElevenLabs.
- **Price change:** PricingSaaS's changelog records a repricing of paid plans between its 13 Apr and 20 Apr 2026 snapshots, with Starter going from $5 to $6/month — [PricingSaaS diff 2026W17](https://pricingsaas.com/companies/elevenlabs/diffs/2026W17), [PricingSaaS history](https://pricingsaas.com/companies/elevenlabs). [3rd-party]
- One 2026 guide says Starter includes "30,000 credits/month, 2 instant voice clones, commercial license", and one guide in the same results says it read ElevenLabs' pricing page on 10 Oct 2026. I could not tell which page made each claim, and the clone-slot count is unverified — [HappyRobot](https://www.happyrobot.ai/hub/elevenlabs-pricing), [Dupple](https://dupple.com/learn/is-elevenlabs-free), [CASRAI](https://casrai.org/guides/elevenlabs-pricing). [3rd-party]
- Deal sites show temporary promotions, such as 50% off the first period and a seasonal $1 first month. Tom's Guide once reported "free for the first two months" for Black Friday (undated, possibly outdated) — [EliteContentMarketer](https://www.elitecontentmarketer.com/deals/elevenlabs-promo-code/), [Tom's Guide](https://www.tomsguide.com/ai/elevenlabs-is-free-for-the-first-two-months-in-black-friday-deal-create-ai-sound-for-less). [3rd-party/News]
- A reviewer warns that a paid plan "unlocks the clone button, not the legal right to use it" — [Rinzara](https://rinzara.com/elevenlabs-pricing). [3rd-party]
- ModelsLab says unused credits roll over for up to two months (capped at 2x the monthly quota) and lists Starter at "60,000 API characters" against 30,000 credits. ModelsLab is a competing API aggregator; this is unverified — [ModelsLab](https://modelslab.com/elevenlabs-api-pricing). [Competitor]

**API rates and access**
- Third-party pages put Multilingual v2 and Eleven v3 at $0.10 per 1K characters and Flash/Turbo at $0.05 per 1K. One page estimates about 900 characters per spoken minute, or about $0.09/min, for v3. Activepieces gives conflicting figures ($0.04 for Flash, $0.17 for Multilingual v2). Pages checked Jul–Oct 2026 — [Puter](https://developer.puter.com/tutorials/elevenlabs-api-pricing/), [HappyRobot](https://www.happyrobot.ai/hub/elevenlabs-pricing), [Invideo, Aug 2026](https://invideo.io/blog/ai-voice-model-pricing/), [Activepieces](https://www.activepieces.com/blog/elevenlabs-pricing-2026-plans-credits-and-costs). [3rd-party]
- **Eleven v4 and v4 Turbo** launched on 28 Sept 2026; OpenRouter dates it 7 Oct 2026, with the model ID suffix 20260930. Reported details:
  - "Entirely new architecture" and "most emotive" model.
  - v4 Turbo has about 100 ms median latency.
  - "Voice cloning with just 10 seconds of audio."
  - 90+ languages and a 10,000-character request limit.
  - Available immediately through ElevenAPI, with access on the free tier.

  Sources: [Unite.AI](https://unite.ai/elevenlabs-launches-eleven-v4-with-low-latency-turbo-variant), [ProPakistani, 29 Sept 2026](https://propakistani.pk/2026/09/29/elevenlabs-unveils-its-fastest-most-expressive-voice-ai-models-yet/amp/), [VKTR](https://www.vktr.com/ai-platforms/elevenlabs-launches-eleven-v4-and-v4-turbo/), [ElevenLabs blog](https://elevenlabs.io/de/blog/eleven-v4) [Vendor], [OpenRouter](https://openrouter.ai/elevenlabs/eleven-v4). [News/3rd-party]
- ElevenLabs' API requires a consent attestation for every clone. It says it embeds SynthID watermarking (built with Google DeepMind) in every generation and that all audio can be traced back to the user who generated it — [ElevenLabs voice-cloning API blog](https://elevenlabs.io/blog/voice-cloning-api). [Vendor; surfaced only as a snippet, unverified]

**Instant Voice Cloning (IVC)**
- Official guidance: about 1–2 minutes of good audio. Avoid going past 3 minutes, which "will yield little improvement and can, in some cases, even be detrimental." Only the total runtime matters, not the number of clips. Use consistent, high-quality clips. MP3 at 192 kbps or higher is recommended, and WAV usually doesn't help; another page says 128 kbps is enough. Target RMS is −23 to −18 dB with true peak at −3 dB. The docs say 30-second samples have given excellent results while some 10-minute uploads did worse. Undated docs, current as indexed — [ElevenLabs IVC docs](https://elevenlabs.io/docs/eleven-creative/voices/voice-cloning/instant-voice-cloning), [Help: how many samples](https://elevenlabs.io/docs/help-center/product/voices/voice-cloning/how-many-voice-samples-should-i-upload-for-instant-voice-cloning.md). [Vendor]
- IVC "may struggle with uncommon accents or unique voices"; the docs suggest PVC for those cases. "The AI will attempt to mimic everything it hears… speed… inflections… accent, tonality." Inconsistent delivery makes the clone unstable — [ElevenLabs IVC docs](https://elevenlabs.io/docs/eleven-creative/voices/voice-cloning/instant-voice-cloning). [Vendor]
- A 2026 guide says IVC uses 1–5 minutes of audio, which conflicts with the official "avoid >3 min" — [TechJack Solutions](https://techjacksolutions.com/ai-tools/elevenlabs/). [3rd-party]

**Professional Voice Cloning (PVC) and verification**
- PVC needs at least 30 minutes of clean single-speaker audio; another page recommends 30 minutes to 3 hours. Fine-tuning typically takes 3–6 hours. Only your own voice can be a PVC, even if another person consents. Creator plan or higher — [ElevenLabs IVC vs PVC blog](https://elevenlabs.io/blog/instant-vs-professional-voice-cloning), [PVC docs](https://elevenlabs.io/docs/eleven-creative/voices/voice-cloning/professional-voice-cloning). [Vendor]
- **Verification ("voice captcha"):** you read a displayed prompt aloud, and ElevenLabs compares that recording with the uploaded data. Use the same or similar recording equipment and read each line only once. After a failure, wait 24 hours or contact support. The help article is about 905 days old, so possibly outdated — [Help: failed PVC verification](https://help.elevenlabs.io/hc/en-us/articles/23743577775889-What-can-I-do-if-I-failed-to-verify-my-Professional-Voice-Clone-PVC). [Vendor]
- One guide says the read-aloud has a 10-second window and you get 4 attempts (undated, unverified) — [TechJack Solutions cloning guide](https://techjacksolutions.com/ai-tools/elevenlabs/elevenlabs-voice-cloning/). [3rd-party]
- The PVC language count is 32+ on one ElevenLabs page and 90+ in the current PVC docs. The newer docs are probably right — [PVC docs](https://elevenlabs.io/docs/eleven-creative/voices/voice-cloning/professional-voice-cloning). [Vendor]

**Cancellation and auto-renewal complaints**
- Trustpilot's auto-generated summaries for ElevenLabs (about 917–934 reviews, depending on crawl date) cite "problems with automatic renewals and trouble canceling" and "lost credits after downgrading plans." Two examples:
  - Dec 2025: a reviewer called cancellation confusing.
  - Jan 2026: a reviewer says a cancellation and refund request was ignored, they were asked to "verify" the cancellation, and they were charged again the next month.

  These are self-selected reviews, and the Dec/Jan examples are possibly outdated — [Trustpilot p.4](https://www.trustpilot.com/review/elevenlabs.io?page=4), [p.2](https://www.trustpilot.com/review/elevenlabs.io?page=2), [p.7](https://www.trustpilot.com/review/elevenlabs.io?page=7), [p.9](https://www.trustpilot.com/review/elevenlabs.io?page=9). [Practitioner/aggregated]

**Quality opinions**
- A Tom's Guide reviewer who cloned their own voice said it "sounds so much like me it was disturbing" (date not shown, likely older) — [Tom's Guide](https://tomsguide.com/ai/i-cloned-my-voice-with-elevenlabs-ai-and-the-results-are-so-accurate-its-scary). [News/Practitioner, n=1]
- A Substack writer found the instant clone impressive "but still robotic" and said a professional clone is more realistic (undated) — [Andrew VH Substack](https://andrewvh.substack.com/p/how-i-used-elevenlabs-to-clone-my). [Practitioner, n=1]
- **Provider Voice Arena (each model uses its own stock voices, so it is not a cloning test):** an undated Artificial Analysis snapshot lists Eleven v4 Turbo at 1335, Eleven v4 at 1329, Qwen-Audio-3.1-TTS-Plus at 1301, Cartesia Sonic 3.6 at 1289 and Gemini 3.8 Flash TTS at 1278 — [AA provider-voice leaderboard](https://artificialanalysis.ai/text-to-speech/leaderboard/provider-voice). [Arena]
- ElevenLabs itself says v4 ranked first on that arena in Sept 2026 — [Unite.AI](https://unite.ai/elevenlabs-launches-eleven-v4-with-low-latency-turbo-variant). [Company claim]
- Speechify, a competitor, reports Sonic 3.6 on top at 1,273 on 23 Sept and its own Simba 3.2 at 1,244 on 13 Oct — [Speechify](https://speechify.ai/blog/simba-3-tops-artificial-analysis-tts-leaderboard). [Competitor]
- **Controlled Voice Arena (all models use the same 8 cloned voices):**
  - At its July 2026 launch, Eleven v3 was second (1,088), behind Cartesia Sonic 3.5 (1,122) — [Wes Roth on X](https://x.com/WesRoth/status/2075248621797384271), [AA on X](https://x.com/ArtificialAnlys/status/2074886571166462405?lang=en). [Arena]
  - By early October 2026, Eleven v4 Turbo was third, behind HeyGen Voice and Qwen-Audio-3.1-TTS-Plus — [AA on X](https://x.com/ArtificialAnlys/status/2108608255387935199). [Arena]
  - As of 22 Oct 2026, HeyGen Voice Turbo leads — see section 2.

### Inferences
- A 45–60 s talking-to-camera script is about 110–150 words, or roughly 650–900 characters. That rate (about 150 words/min at about 6 characters/word) is my assumption; it matches the third-party estimate of about 900 characters per minute. At an assumed 1 credit per character, Starter's 30,000 credits cover about 30 full takes of a 60 s script. So $6 for one month covers the voice side of this test many times over.
- For the user's case, IVC is the right ElevenLabs tier. Eleven v4's reported 10 s cloning suggests a short selfie-video audio track might be enough, but the docs' 1–2 minutes is still the safer target. PVC needs 30+ minutes of audio and the Creator plan, which doesn't fit a one-off.
- Because of the complaint pattern, an agent-driven plan should be: subscribe to Starter, generate, delete the cloned voice, then cancel in account settings the same day. Promotions can drop the first month to $1–3.
- ElevenLabs' strongest point for this use case may be its pronunciation dictionaries with phoneme tags (see section 4), which help with EDA jargon. Many cheaper rivals offer no comparable feature, or none surfaced in these searches.

### Gaps
- I could not read elevenlabs.io/pricing (proxy-blocked, WebFetch DNS failure). The $6 price and 30,000 credits rest on several consistent 2026 third-party guides and the PricingSaaS changelog. The IVC slot count on Starter ("2") is unverified.
- Credits per character for Eleven v4 and v4 Turbo were not confirmed. Historically Multilingual v2/v3 used 1 credit per character and Flash/Turbo less, but that comes from prior knowledge, not this session.
- The IVC API endpoint path and fields were not confirmed (historically a multipart POST to `/v1/voices/add`). Confirm against the current API reference.
- No current text was found on whether IVC now has any technical speaker verification beyond the self-attestation that Consumer Reports found in March 2025 (section 6).
- No Reddit (r/ElevenLabs) threads were retrievable, so there is no larger-sample practitioner opinion on v4 clones.

## 2. Alternatives: cheapest way to clone and generate 60 s via API, sample length needed, quality vs ElevenLabs (practitioners and arenas)

### Takeaway
For a 60 s clip, several API alternatives cost cents rather than dollars:
- **HeyGen Voice Turbo:** new #1 on the cloned-voice arena (22 Oct 2026), about $0.004 per 1K characters on fal.ai, with a free tier reported through 30 Nov 2026.
- **Fish Audio:** $15 per million UTF-8 bytes, so about $0.014 per minute of English.
- **Inworld:** $5–10 per million characters, with free zero-shot cloning.
- **Resemble:** first clone free.
- **Cartesia:** about $4–5/month Pro plan, led the July cloned-voice arena.

PlayHT is gone. It was bought by Meta in July 2025 and shut down at the end of 2025. Azure Personal Voice is gated behind Microsoft approval, and OpenAI still offers no public cloning from audio. The arenas measure listener *preference*, not *similarity to the real speaker*. Only the Controlled Voice Arena even uses cloned voices, and those come from 1–2 minute samples.

### Cited Findings
**Arena context**
- Artificial Analysis Elo is a blind preference score. Listeners hear two clips of the same text and pick the one they prefer — [AA methodology](https://artificialanalysis.ai/methodology/text-to-speech), [Speechify explainer](https://speechify.ai/blog/artificial-analysis-tts-leaderboard-elo-explained). [Arena/Competitor]
- The Controlled Voice Arena launched on 8 July 2026. It uses 8 voices (2 US male, 2 US female, 2 UK male, 2 UK female), each cloned from the same 1–2 minute recordings for every model, which separates voice preference from model quality.
  - July results: Cartesia Sonic 3.5 1,122; Eleven v3 1,088; Inworld Realtime TTS-2 Research Preview 1,070. Sonic 3.5 also led both the US-accent and UK-accent categories. Open-weights leaders: Fish Audio S2 Pro 1,034; Mistral Voxtral TTS 1,024; Resemble Chatterbox 930.
  - Sources: [Wes Roth on X](https://x.com/WesRoth/status/2075248621797384271), [AA on X](https://x.com/ArtificialAnlys/status/2074886571166462405?lang=en). [Arena]
- **Current standings as of 22 Oct 2026:** HeyGen Voice Turbo 1,202 ±19; HeyGen Voice about 1,195 ±15; Qwen-Audio-3.1-TTS-Plus 1,185. The top two overlap within their confidence intervals — [AA controlled-voice leaderboard](https://artificialanalysis.ai/text-to-speech/leaderboard/controlled-voice), [AA on X](https://x.com/ArtificialAnlys/status/2112961069526249973). [Arena]

**HeyGen Voice / Voice Turbo (new in Oct 2026)**
- HeyGen Voice Turbo launched in October 2026. One source dates it 13 Oct; another says it went live on the API on 21 Oct as `heygen-voice-1-turbo`. Artificial Analysis lists $4 per 1M characters, a figure it normalizes from HeyGen's credit pricing. An X post says HeyGen lists $7.50 per 1M. fal.ai lists $0.004 per 1K characters and offers "library voices and instant cloning from a reference clip" — [fal.ai model page](https://fal.ai/models/heygen/heygen-voice/turbo), [OpenRouter](https://openrouter.ai/heygen/heygen-voice-1-turbo), [Respan](https://www.respan.ai/models/heygen-voice-1-turbo), [AGTP on X](https://x.com/AGTPinsights/status/2113135273169362972), [OrcaRouter](https://www.orcarouter.ai/blog/heygen-voice-turbo-tops-controlled-voice-arena), [AlphaSignal](https://alphasignal.ai/news/heygen-s-voice-turbo-tops-speech-leaderboard-at-87-less-cost). [3rd-party/resellers]
- A free model ID, `heygen-voice-1-turbo-free`, reportedly speaks public voices and instant clones without a credit balance through 30 Nov 2026. It runs on shared capacity with no guarantees and can return 429 (rate-limit) errors. This comes from model-directory listings and is unverified — [OpenRouter](https://openrouter.ai/heygen/heygen-voice-1-turbo), [Respan](https://www.respan.ai/models/heygen-voice-1-turbo). [3rd-party]
- OrcaRouter compares HeyGen Voice Turbo with Inworld Realtime TTS-2: "57 Elo, 50 ms" — [OrcaRouter](https://www.orcarouter.ai/blog/heygen-voice-turbo-vs-inworld-realtime-tts-2). [3rd-party/reseller]

**Cartesia**
- Official pricing, as seen in a search snippet:
  - Pro: $4/month, 100K credits/month and $5 of prepaid agent usage. Adds a commercial license and instant voice cloning.
  - Startup: $39/month, 1.25M credits, adds pro voice cloning.
  - Scale: $239/month, 8M credits.

  Source: [Cartesia pricing](https://www.cartesia.ai/pricing). [Vendor]
- Fish Audio's comparison page lists Pro at $48/year (the same as $4/month if billed annually, so the $4 may be the annual rate). It says the Free tier has 20K credits with no IVC and that credits roughly equal characters — [fish.audio vs Cartesia](https://fish.audio/vs/pricing/cartesia-ai/). [Competitor]
- Cartesia says it can "clone a voice with just 3 seconds of audio." A third-party guide in the same results recommends 5–10 s, but I couldn't tell which page said that — [Cartesia voice cloning](https://cartesia.ai/product/voice-cloning), [Codesota](https://codesota.com/speech/best-for-voice-cloning). [Vendor/3rd-party]
- Sonic 3.5 led the July 2026 Controlled Voice Arena (see above). Sonic 3.6 sits about 4th on the undated Provider Voice snapshot (1289) — [AA provider-voice leaderboard](https://artificialanalysis.ai/text-to-speech/leaderboard/provider-voice). [Arena]

**Fish Audio**
- Official API docs list speech-1.5, speech-1.6 and s1 at $15.00 per million UTF-8 bytes of input text — [Fish Audio API pricing docs](https://docs.fish.audio/docs/models-pricing/pricing-and-rate-limits). [Vendor]
- A review dated 28 Aug 2026 lists S2.1 Pro at the same $15 per million bytes, a free S2.1 Pro tier at $0, and "no subscription fees or monthly minimums for API access." Non-Latin scripts use 3–4 bytes per character. Smallest.ai is a competing TTS vendor — [Smallest.ai](https://smallest.ai/blog/fish-audio-pricing-plans-api-billing-commercial-use-in-2026). [Competitor]
- On the hosted service, an instant clone needs about 10 s of reference audio. Professional cloning uses 10–180 minutes — [OpenClaw docs](https://docs.openclaw.ai/providers/fish-audio.md). [3rd-party]
- The open-weights S2 Pro led open models in the July Controlled Voice Arena (1,034). On the Provider Voice open-weights board, "Fish Audio Drama 3 Preview" is first at 1,248 ±15 and S2 Pro is 4th at 1,112 — [AA open-weights board](https://artificialanalysis.ai/text-to-speech/leaderboard/provider-voice/open-weights). [Arena]

**Resemble AI**
- Changelog dated 8 May 2026: the first voice clone is free and each later clone costs $2. A card is only requested after the free clone — [Resemble changelog](https://www.resemble.ai/changelogs/voice-cloning-pricing-first-clone-free-then-2-each-2026). [Vendor]
- Voiceflow's review (updated 30 June 2026) says Resemble dropped consumer subscriptions in 2025. It now uses pay-per-use "Flex" pricing: TTS at $0.0005 per second of output, credits that never expire, and full API access from day one, including cloning. Toolradar (May 2026) instead lists $0.006 per second, about 12 times more — [Voiceflow](https://www.voiceflow.com/articles/resemble-ai), [Toolradar](https://toolradar.com/tools/resemble-ai/pricing). [3rd-party; conflicting]
- A review citing Resemble's April 2026 pricing page lists "rapid voice clones $2/voice/month, pro $5/voice/month." That conflicts with the one-time $2 in the changelog, and the April date makes it possibly outdated — [CASRAI](https://casrai.org/guides/lovo-ai-and-resemble-ai-pricing-compared). [3rd-party]
- Resemble's open-source Chatterbox is covered in section 3.

**PlayHT (status)**
- Meta acquired PlayAI, the company behind PlayHT, in July 2025; one source says about 35 staff joined Meta's Superintelligence Labs. The API went offline on 26 July 2025, sign-ups stopped in August 2025, and the service shut down permanently on 31 Dec 2025. Accounts, voice clones and audio were reportedly deleted with no export. These sources are mostly alternative-vendor blogs, and infrabase.ai misdates the deal; no primary Meta/PlayAI notice surfaced — [AnySpeech](https://anyspeech.io/playht-alternatives), [CognitiveFuture](https://cognitivefuture.ai/elevenlabs-vs-playht-alternatives/), [TextToLab](https://texttolab.com/blog/play-ht-shutdown-alternatives), [AIWiki](https://www.aiwiki.ai/wiki/playht). [Competitor/3rd-party]

**Hume (Octave)**
- Plans run from Free to Business ($500/month), plus Enterprise. One summary lists Free $0, Starter $3, Creator $7–14, Pro $70, Scale $200 and Business $500. Free includes 10,000 TTS characters a month and Creator 140,000. Overage is $0.15 per 1K characters on lower tiers and $0.05 per 1K on Business. Free is for non-commercial use only — [Hume pricing](https://hume.ai/pricing), [CostBench](https://costbench.com/software/voice-apis/hume-ai/), [UsagePricing](https://usagepricing.com/blueprint/hume-ai). [Vendor/3rd-party]
- One source says cheaper Octave 2 rates of $0.075–0.025 per 1K characters arrived in June 2026. Unconfirmed — [AnotherWrapper](https://anotherwrapper.com/tools/llm-pricing/speech-models/octave-2). [3rd-party]
- Sources conflict on cloning. Some say Free and Starter can only create clones, with full use from Creator. Speechify (July 2026) says cloning is unlimited on every tier, including Free — [Speechify Hume alternatives](https://speechify.ai/alternatives/hume), [eesel](https://www.eesel.ai/blog/hume-ai-pricing). [Competitor/3rd-party]

**MiniMax Speech**
- Cloning costs $1.50 per voice, charged once at first use; previews are billed separately. A third-party page in the results gives a 10 s minimum and 5 min maximum for source audio. Speech HD costs about $100 per 1M characters and Turbo about $60. Voice Design (a different product) is $3 per voice. Sources dated Aug–Oct 2026 — [Gradually.ai Speech 2.8](https://www.gradually.ai/en/ai-models/minimax-speech-2-8/), [Invideo MiniMax family](https://invideo.io/blog/minimax-ai-voice-models/), [Invideo pricing comparison](https://invideo.io/blog/ai-voice-model-pricing/), [MuAPI](https://muapi.ai/comparison/minimax-voice-clone). [3rd-party]
- It is also hosted on Replicate as `minimax/speech-2.6-turbo` — [Replicate](https://replicate.com/minimax/speech-2.6-turbo). [3rd-party host]

**Microsoft Azure Personal Voice**
- Personal Voice is a limited-access feature for "certain pre-approved use cases only," and you must apply. Synthesis is billed per 1M characters, voice creation is free, and profile storage is billed per 1,000 profiles a month. The dollar amounts were masked in the snippet — [Azure Speech pricing](https://azure.microsoft.com/en-us/pricing/details/speech/). [Vendor]
- Consent: you need a recording of the speaker reading a locale-specific consent statement, in the same language as the voice data. The current docs say the audio prompt should be a clean sample of 5–90 seconds; an older preview page said 1 minute — [Personal voice: create consent](https://learn.microsoft.com/el-gr/azure/ai-services/speech-service/personal-voice-create-consent), [Personal voice: create voice](https://learn.microsoft.com/en-my/Azure/ai-services/speech-service/personal-voice-create-voice), [Overview](https://learn.microsoft.com/azure/ai-services/speech-service/personal-voice-overview). [Vendor]

**OpenAI**
- Voice Engine, OpenAI's 15-second cloning tool previewed in March 2024, reportedly remains a limited preview in 2026 and is not a standard developer API — [TechCrunch, 29 Mar 2024](https://techcrunch.com/2024/03/29/openai-custom-voice-engine-preview/), [Fora Soft 2026 guide](https://www.forasoft.com/blog/article/openai-realtime-api-voice-agent-production-guide-2026), [Gradium (TTS vendor)](https://gradium.ai/content/best-voice-cloning-apis-2026). [News/3rd-party/Competitor]
- On 16 Oct 2026, OpenAI reportedly opened prompt-to-voice to all API customers. It creates a custom voice from a text description, costs nothing to create, and needs no reference recording, but the voices run only in GPT-Live and not in the TTS API. It is not a clone of a real voice — [Digital Applied](https://www.digitalapplied.com/blog/openai-prompt-to-voice-custom-gpt-live-voices), [TechTimes, 19 Oct 2026](https://www.techtimes.com/articles/329184/20261019/gpt-live-adds-prompt-voice-real-time-action-selection-no-recording-required.htm). [News]

**Inworld**
- The official billing page lists TTS-1.5-Max at $10 per 1M characters and TTS-1.5-Mini at $5 per 1M, billed on characters synthesized in the Playground and API. The TTS docs list "free instant (zero-shot) voice cloning." A Gradium comparison gives $35 and $25 per 1M, which is likely outdated — [Inworld billing docs](https://docs.inworld.ai/stt/resources/billing), [Inworld TTS docs](https://docs.inworld.ai/docs/tts/tts), [Gradium](https://gradium.ai/content/how-to-compare-tts-pricing-across-providers-2026). [Vendor/Competitor]
- Inworld Realtime TTS-2 Research Preview was third in the July Controlled Voice Arena (1,070) — [Wes Roth on X](https://x.com/WesRoth/status/2075248621797384271). [Arena]

**Other 2026 models the arenas rate highly**
- Qwen-Audio-3.1-TTS-Plus, an Alibaba API model, ranks third on the Controlled Voice Arena (1,185) and on the Provider Voice snapshot (1301) — [AA controlled-voice](https://artificialanalysis.ai/text-to-speech/leaderboard/controlled-voice), [AA provider-voice](https://artificialanalysis.ai/text-to-speech/leaderboard/provider-voice). [Arena]
- Mistral Voxtral TTS (open weights, March 2026) is second among open models on the Controlled Voice Arena — section 3.

### Inferences
Estimated voice cost to produce one 60 s take, assuming about 900 characters of English (my estimates from the cited rates):

| Option | Clone sample (reported) | Cheapest path | ~Cost for 60 s | Agent-drivable via HTTP API? |
|---|---|---|---|---|
| Record yourself | n/a | phone or USB mic | $0 | n/a (upload audio to the avatar API) |
| HeyGen Voice Turbo | "reference clip" (HeyGen's in-app clone: 30 s minimum, 1–3 min ideal) | fal.ai $0.004/1K, or the free model ID until 30 Nov 2026 | ~$0.004 (~$0.007 at the $7.50/M figure) | Yes (fal.ai or HeyGen API) |
| Fish Audio | ~10 s | pay-as-you-go $15/M bytes | ~$0.014 | Yes |
| Inworld | zero-shot (length not verified) | Mini $5/M, Max $10/M | ~$0.005–0.009 | Yes |
| Resemble | not verified | first clone free + Flex | ~$0.03 (or ~$0.36 at $0.006/s) | Yes |
| fal.ai Chatterbox / F5-TTS | ~7–20 s | $0.025/1K / $0.05/1K | ~$0.02 / ~$0.045 | Yes |
| Cartesia | 3 s (vendor), 5–10 s suggested | Pro $4–5/month | $4–5 | Yes |
| ElevenLabs | 1–2 min (v4: 10 s reported) | Starter $6/month | $6 | Yes |
| MiniMax | 10 s – 5 min | $1.50 per clone + HD/Turbo per character | ~$1.55–1.60 | Yes |
| Hume | not verified | Free 10K characters (if Free allows clone use) | $0–3 | Yes |
| Azure Personal Voice | 5–90 s + consent statement | needs Microsoft approval | n/a in practice | Gated |
| OpenAI | no audio cloning | — | — | No |
| PlayHT | — | shut down | — | No |

- On cost alone, every option fits easily inside a $30 budget, so pick on quality, friction and data handling. Unknown minimum prepaid top-ups (fal.ai, Fish, Inworld, HeyGen) are the main budget uncertainty.
- On arena evidence for *cloned* voices (1–2 min samples), the strongest candidates as of late Oct 2026 are HeyGen Voice Turbo, Qwen-Audio-3.1-TTS-Plus, Eleven v4 Turbo and Cartesia Sonic. Arena preference does not equal resemblance to *your* voice, so the practical way to choose is to run the same sample and script through 2–3 cheap APIs and compare.
- HeyGen Voice is attractive if HeyGen is also the avatar tool, since voice and avatar would sit in one ecosystem. That is worth checking against the parallel avatar-tool research.

### Gaps
- No vendor page could be read in full. Cartesia's $4 vs $5 monthly price, Fish Audio's and fal.ai's minimum top-ups, and HeyGen Voice's official per-character price and consent flow are all unverified.
- No independent, practitioner-level comparison of clone *similarity* (as opposed to preference) between these vendors surfaced. Reddit could not be searched.
- The minimum sample lengths for Hume, Inworld and Resemble clones were not found.
- I could not confirm whether the Controlled Voice Arena shows listeners the original reference voice or measures similarity in any way. As described, it is a pairwise preference vote.

## 3. Open-source: best similarity from a 10–60 s sample, hardware, CPU feasibility, hosted options and cost, licenses

### Takeaway
On the July 2026 Controlled Voice Arena (cloned voices), the best open-weight models were Fish Audio S2 Pro (research and non-commercial license), Mistral Voxtral TTS (CC BY-NC 4.0) and Resemble's MIT-licensed Chatterbox. All three trailed the top commercial models by roughly 90–190 Elo. Most strong open models need a GPU, from about 6 GB of VRAM (Zonos) to 24 GB (Higgs Audio). On a CPU-only Linux sandbox, Kyutai's Pocket TTS (and possibly NeuTTS Air) is the realistic local option. Otherwise, use hosted endpoints: fal.ai runs Chatterbox at $0.025 per 1K characters and F5-TTS at $0.05 per 1K, and Replicate bills per second of GPU time. Licenses vary a lot, but for a private, non-commercial experiment even non-commercial licenses are workable.

### Cited Findings
**Arena results for open models**
- Controlled Voice Arena, July 2026: Fish Audio S2 Pro 1,034, Voxtral TTS 1,024, Chatterbox 930. For comparison, Sonic 3.5 scored 1,122 and Eleven v3 1,088 — [Wes Roth on X](https://x.com/WesRoth/status/2075248621797384271). [Arena]
- A third-party blog reports Voxtral at 1,010 and Breeze TTS 2 at 1,002 on the same arena. Those numbers don't match the July figures, probably because they were captured on a different date — [Pinggy](https://pinggy.io/blog/best_open_source_self_hosted_text_to_speech_models/). [3rd-party]
- Provider Voice open-weights board (models use their own voices, so this is not a cloning test): Fish Audio Drama 3 Preview 1,248 ±15, Breeze TTS 2 1,225 ±14, Ming-3.0-tts 1,190 ±14, Fish S2 Pro 1,112 ±12 — [AA open-weights board](https://artificialanalysis.ai/text-to-speech/leaderboard/provider-voice/open-weights). [Arena]

**Models: licenses, reference length, hardware**
- **Fish Audio S2 Pro:** released under the Fish Audio Research License. Personal, research and non-commercial use are allowed; commercial use needs a separate license. Fish's developer page says its open models ship as open weights with a paid commercial license — [OpenClaw docs](https://docs.openclaw.ai/providers/fish-audio.md), [fish.audio developers](https://fish.audio/en/developers/). [3rd-party/Vendor]
  - A community mirror says it typically needs a 10–30 s reference — [HF mirror](https://huggingface.co/jashansinghTT/s2-pro-blackhole).
  - Zero-shot cloning needs a "reference clip + its transcript" — [vLLM recipe](https://recipes.vllm.ai/fishaudio/s2-pro).
- **Mistral Voxtral TTS:** released 26 Mar 2026 under CC BY-NC 4.0 (non-commercial). Reported to clone from about 3 s and to keep the speaker's accent across languages — [InsiderLLM](https://insiderllm.com/guides/mistral-voxtral-tts-local-voice-ai/), [NYU Shanghai RITS](https://rits.shanghai.nyu.edu/ai/voxtral-tts-mistrals-open-weight-text-to-speech-model-rivals-elevenlabs/), [MindStudio](https://www.mindstudio.ai/blog/mistral-open-weight-tts-voice-cloning-local). [3rd-party]
- **Qwen3-TTS:** Apache 2.0, so commercial use is allowed. Its two base models support zero-shot cloning and fine-tuning — [NYU Shanghai RITS](https://rits.shanghai.nyu.edu/ai/%F0%9F%93%A2-qwen3%E2%80%91tts-open%E2%80%91source-text%E2%80%91to%E2%80%91speech-tts-family/), [LetsDataScience](https://letsdatascience.com/news/qwen3-tts-releases-open-source-voice-cloning-and-generation-37ef2448), [Duarte O. Carmo Substack](https://duarteocarmo.substack.com/p/tts-doesnt-suck-anymore). [3rd-party]
- **Chatterbox / Chatterbox-Turbo (Resemble AI):** MIT license. Turbo has 350M parameters, paralinguistic tags and is English-only. It runs on a GPU or Apple MPS; one comparison says only a smaller "Nano" variant runs on CPU — [Yaps.ai](https://www.yaps.ai/blog/best-local-tts-models), [OpenVox](https://openvoxai.com/blog/best-free-local-tts-models-2026), [ModelsLab chatterbox-turbo README](https://huggingface.co/ModelsLab/chatterbox-turbo/blob/main/README.md). [3rd-party]
  - Resemble's own blind test, run through Podonos: 63.75% of evaluators preferred Chatterbox over ElevenLabs (38.75% strongly, 25.00% somewhat; 8.75% no preference; 27.5% preferred ElevenLabs). Both systems used the same 7–20 s reference clips, zero-shot. The number of evaluators wasn't shown, and the test predates Eleven v4 — [Resemble Chatterbox page](https://www.resemble.ai/learn/models/chatterbox). [Vendor]
  - PromptQuorum notes that this claim was "not an independent study" — [PromptQuorum](https://www.promptquorum.com/power-local-llm/chatterbox-vs-elevenlabs). [3rd-party]
  - A newer Podonos study (Chatterbox Turbo vs ElevenLabs Turbo v2.5, 50 evaluators per model) exists, but its results didn't surface — [Podonos](https://www.podonos.com/resembleai/chatterbox-turbo-vs-elevenlabs-turbo?t=o).
- **F5-TTS:** code is MIT, but the weights are CC BY-NC 4.0 (non-commercial). One GitHub-hosted hands-on comparison rated F5's cloning "easily the best clone quality" it tested, and the fastest, but with limited emotion control — [Cartesia "open-source TTS by license" (written by a commercial competitor)](https://www.cartesia.ai/learn/open-source-tts), [mirfahimanwar/TTS-Model-Comparison-Chart](https://github.com/mirfahimanwar/TTS-Model-Comparison-Chart/), [5uck1ess/tts-bench](https://github.com/5uck1ess/tts-bench). The search summary didn't make clear which of the two repos holds the reviewer quote. [Competitor/Practitioner]
- **IndexTTS2:** the same reviewer says it "clones the original speaker well" but is "not recommendable" for cloning because of problems with non-word text, and it needs about 14 GB of VRAM — same repos as above. [Practitioner]
  - The license is disputed. tts-bench lists a bilibili Model License, and OpenVox lists IndexTTS 2.5 as "commercial use not allowed." Only vibevoice.info, a less authoritative site, claims Apache 2.0 — [tts-bench](https://github.com/5uck1ess/tts-bench), [OpenVox](https://openvoxai.com/blog/best-tts-models-local-cloud-2026), [vibevoice.info](https://vibevoice.info/indextts2). [3rd-party; conflicting]
- **Higgs Audio (Boson AI):** v2 is reported as Apache 2.0; v3 is under a research and non-commercial license. The reviewer recommends 24 GB of VRAM (16 GB minimum) — same repos, plus [Cartesia learn page](https://www.cartesia.ai/learn/open-source-tts). [Practitioner/Competitor]
- **Zonos (Zyphra):** v0.1 is Apache 2.0, and Zonos2 (June 2026) is also listed as Apache 2.0. It has the lowest VRAM need of the cloning models compared, about 6 GB — [Cartesia learn page](https://www.cartesia.ai/learn/open-source-tts), [tts-bench](https://github.com/5uck1ess/tts-bench). [Competitor/3rd-party]
- **VibeVoice (Microsoft):** MIT-licensed but restricted by its model cards to research use. Microsoft pulled the original inference code on 5 Sept 2025 because of misuse; the 1.5B weights remain available. Possibly outdated — [OpenVox](https://openvoxai.com/blog/best-tts-models-local-cloud-2026), [Cartesia learn page](https://www.cartesia.ai/learn/open-source-tts). [3rd-party/Competitor]
- **XTTS-v2 (Coqui):** a packaged wrapper describes zero-shot cloning from 6–10 s of reference audio — [Docker Hub demod-voice](https://hub.docker.com/r/alh477/demod-voice). [3rd-party]
- **OpenVoice v2:** it has powered cloning on myshell.ai since May 2023; no similarity comparison surfaced — [HF OpenVoice-v2 mirror](https://huggingface.co/flopml/OpenVoice-v2/commit/88fdff2f768ab7f45b20155e9698cddbb3ea92b6). [3rd-party]
- **Older options:** Llasa-3B (Jan 2025) clones from "a couple seconds" — [HF blog](https://huggingface.co/blog/srinivasbilla/llasa-tts). Nari Labs' Dia-1.6B is dialogue-focused with cloning — [DEV Community](https://dev.to/aibyamdad/how-to-run-dia-16b-locally-your-ultimate-guide-to-open-source-tts-freedom-3ej1). [3rd-party; possibly outdated]

**CPU feasibility**
- **Kyutai Pocket TTS:** CPU-first, about 100M parameters (one post says 82M), zero-shot cloning from a short clip in six languages. It runs at about 6x real time on a MacBook Air M4 using 2 CPU cores. The license is reported as MIT in one place and CC BY 4.0 with a gated Hugging Face repo in another. A C++/ONNX runtime with an HTTP server exists — [OSTechNix](https://ostechnix.com/pocket-tts-local-text-to-speech-no-gpu/), [Medium](https://medium.com/@bytefer/pocket-tts-high-quality-voice-cloning-thats-fast-lightweight-fully-open-source-bcd596f9db54), [ScriptByAI](https://www.scriptbyai.com/cpu-tts-voice-cloning-pocket/), [PocketTTS.cpp](https://github.com/VolgaGerm/PocketTTS.cpp). [3rd-party]
- **NeuTTS Air (Neuphonic):** 0.5B LLM backbone in GGUF format, real-time on CPUs. Its current license and benchmarks were not verified — [BentoML](https://www.bentoml.com/blog/exploring-the-world-of-open-source-text-to-speech-models). [3rd-party]
- Kokoro-82M (Apache 2.0) and Supertonic 3 run on CPU but can't clone voices — [Yaps.ai](https://www.yaps.ai/blog/best-local-tts-models). [3rd-party]

**Hosted options and cost**
- **fal.ai:** F5-TTS costs about $0.05 per 1K characters ("20 generations per dollar") — [fal F5-TTS](https://fal.ai/models/fal-ai/f5-tts). Chatterbox costs $0.025 per 1K characters, and fal advertises pay-as-you-go with "no subscriptions or minimums" — [fal TTS explore](https://fal.ai/explore/text-to-speech-apis). HeyGen Voice Turbo is $0.004 per 1K — [fal](https://fal.ai/models/heygen/heygen-voice/turbo). [Host]
- **Replicate:** bills per second, by hardware. Examples: T4 at $0.000225/s, A40 (Large) at $0.000725/s, A100 80GB at about $5.04/hour. The per-model cost appears under "Run time and cost" on each model page. No Chatterbox-specific figure surfaced — [Replicate pricing](https://replicate.com/pricing). [Host]
- MuAPI, a competitor, claims Replicate charges about $0.85 per clone generation. Unverified — [MuAPI](https://muapi.ai/comparison/minimax-voice-clone). [Competitor]
- **Hugging Face Spaces:** community demo Spaces exist, such as E2-F5-TTS — [HF Space](https://huggingface.co/spaces/emilalvaro/E2-F5-TTS/blob/96269ddb27a5e86e0a708cf6f59ab915050a1f4c/README.md). Quotas and costs were not verified. [3rd-party]

### Inferences
- With no GPU, local open-source cloning is realistic only with Pocket TTS or NeuTTS Air. Their clone quality has no arena data I could find, and small CPU-first models are probably below the arena leaders. Running locally does have one real advantage: the voice sample never leaves the sandbox.
- Hosted open models (fal Chatterbox or F5) cost about the same as the cheapest commercial APIs and ranked lower on the cloned-voice arena (Chatterbox 930 vs HeyGen Voice Turbo 1,202). For this one-off, the best reason to pick open source is privacy, not quality or cost.
- Non-commercial licenses (F5 weights, Voxtral, Fish S2 Pro, Higgs v3) shouldn't block a private, unpublished personal experiment. They would matter if the clip were later used commercially.
- IndexTTS2's reported "non-word text issues" are a warning sign for scripts full of identifiers like `fc_shell`.

### Gaps
- No full model cards could be read. XTTS-v2's license (historically the non-commercial Coqui Public Model License, after Coqui shut down in early 2024) and OpenVoice v2's license come from prior knowledge, not this session.
- No r/LocalLLaMA or r/StableDiffusion threads surfaced, so there is no larger-sample community verdict on which open model sounds most like the reference speaker from 10–60 s.
- Hugging Face ZeroGPU quotas, programmatic (Gradio client) access, and fal.ai/Replicate minimum top-ups were not verified.
- "Breeze TTS 2", "Ming-3.0-tts" and "Fish Audio Drama 3" appear on the arena, but I found no details on their cloning ability or licenses.

## 4. Practitioner opinions: how close clones sound to the real person, common tells (prosody, accent drift, technical jargon such as EDA terms), and tips for recording a good sample

### Takeaway
Hands-on reviewers often describe their own clones as uncannily close in timbre ("disturbing"). The recurring tells are:
- flattened, less varied delivery, especially from short samples;
- accent or language drift in longer generations, and trouble with uncommon accents;
- stilted handling of unusual phrasing and technical vocabulary.

Nothing EDA-specific (`fc_shell`, PrimeTime, Tcl) surfaced. The generic fixes are respelling terms in the script, alias rules, or phoneme tags; ElevenLabs supports phoneme tags on v3, v4 and Flash v2. For the sample itself: 1–2 minutes of clean, single-speaker, consistently delivered speech, recorded the way you want the output to sound.

### Cited Findings
**How close clones sound**
- A Tom's Guide reviewer said their ElevenLabs clone "sounds so much like me it was disturbing" — [Tom's Guide](https://tomsguide.com/ai/i-cloned-my-voice-with-elevenlabs-ai-and-the-results-are-so-accurate-its-scary). A Substack writer found the instant clone "impressive but still robotic" — [Andrew VH](https://andrewvh.substack.com/p/how-i-used-elevenlabs-to-clone-my). Another guide says cloning "needs good source audio or it sounds off" — [Daily Build Substack](https://dailybuild.substack.com/p/ai-cloned-my-voice). All n=1 and undated, so possibly outdated. [Practitioner]
- A write-up on HeyGen Avatar 5 says a voice cloned from short samples "captures your general tone and timbre, but it may flatten out some of the natural variation in your real delivery. Unusual phrasing, technical vocabulary, or languages you don't natively speak can produce stilted-sounding output" — [MindStudio](https://www.mindstudio.ai/blog/what-is-heygen-avatar-5). [3rd-party, 2026]
- An academic paper in JASA (vol. 159 no. 4, 2026) is titled "Voice clones are easier to understand in noise than their human originals: The voice cloning intelligibility benefit." Only the title and abstract listing surfaced — [JASA](https://pubs.aip.org/asa/jasa/article/159/4/3476/3387364/Voice-clones-are-easier-to-understand-in-noise). [Academic]

**Accent drift and instability**
- ElevenLabs' troubleshooting page says the AI "can sometimes switch languages or accents throughout a single generation, especially if that generation is longer," and that the company is working on it — [ElevenLabs troubleshooting](https://elevenlabs.io/docs/eleven-creative/troubleshooting). [Vendor]
- IVC "may struggle with uncommon accents or unique voices." It copies everything in the sample, including pace, inflection, accent and tone, and inconsistent delivery makes it unstable — [ElevenLabs IVC docs](https://elevenlabs.io/docs/eleven-creative/voices/voice-cloning/instant-voice-cloning). [Vendor]
- You cannot change a clone's accent or tone after creating it; you have to change the input samples. The help article is about 560 days old, so possibly outdated — [ElevenLabs help](https://help.elevenlabs.io/hc/en-us/articles/13434263477137-Why-does-my-voice-or-accent-not-sound-correct-after-cloning). [Vendor]

**Technical jargon and pronunciation**
- TTS engines guess pronunciations from spelling (grapheme-to-phoneme conversion), and the guess fails on rare vocabulary, acronyms and jargon. Workarounds, roughly in order of effort:
  - respell the term phonetically in the script ("SCSI" becomes "scuzzy");
  - space out the letters ("S Q L");
  - search-and-replace before generation;
  - pronunciation dictionaries or PLS lexicons;
  - IPA/ARPAbet phoneme tags.

  Sources: [Gradium (TTS vendor)](https://gradium.ai/content/how-to-fix-tts-mispronouncing-names-acronyms-technical-terms), [Deepgram (TTS vendor)](https://deepgram.com/learn/developers-guide-fixing-tts-pronunciation-errors), [DEV Community](https://dev.to/stanlymt/fix-ai-mispronunciations-before-you-export-3o7), [Picovoice (vendor)](https://picovoice.ai/blog/custom-pronunciation-in-tts/). [Competitor/3rd-party]
- A forum user with hundreds of textbook acronyms proposed swapping each one for a similar-sounding word before generation. They noted this is practical mainly for small documents — [lemm.ee thread](https://lemm.ee/comment/14028421). [Practitioner, n=1]
- **ElevenLabs pronunciation dictionaries** support phoneme rules (IPA or CMU Arpabet) and alias rules (substitute spellings). Details:
  - The dictionary is checked from start to end and only the first match is used.
  - Upload as TXT or PLS; multiple dictionaries are allowed.
  - Add separate entries for capitalized and lowercase forms.
  - Phoneme tags "only work with eleven_v4, eleven_flash_v2 and eleven_v3"; other models ignore them. Older pages list Turbo v2 / English v1 instead.
  - IPA/CMU phonemes work for English; for other languages, use v4 or v3.

  Sources: [ElevenLabs pronunciation dictionaries](https://elevenlabs.io/docs/eleven-agents/customization/voice/pronunciation-dictionary), [ElevenLabs prompting: pronunciation](https://elevenlabs.io/docs/product/prompting/pronunciation), [ElevenLabs best practices](https://elevenlabs.io/docs/overview/capabilities/text-to-speech/best-practices), [ElevenLabs Python SDK guide](https://www.mintlify.com/elevenlabs/elevenlabs-python/guides/pronunciation-dictionaries). [Vendor]
- One hands-on reviewer says IndexTTS2 has "non-word text issues" — [TTS-Model-Comparison-Chart](https://github.com/mirfahimanwar/TTS-Model-Comparison-Chart/) / [tts-bench](https://github.com/5uck1ess/tts-bench). [Practitioner]

**Recording tips (vendor guidance)**
- ElevenLabs: 1–2 minutes total; avoid more than 3 minutes. One speaker, no background noise or room reverb, consistent volume and tone, few long silences. MP3 at 192 kbps or higher; RMS −23 to −18 dB with true peak at −3 dB. A noise remover can help — [ElevenLabs IVC docs](https://elevenlabs.io/docs/eleven-creative/voices/voice-cloning/instant-voice-cloning). [Vendor]
- HeyGen clone, as described by a wrapper: a 30 s clear sample is enough, 1–3 minutes is ideal, and only the first 3 minutes are used. MP3 or WAV; no music, extra speakers or heavy reverb. Set similarity to "Max" if you want it to sound like you — [Wireflow HeyGen voice clone node](https://www.wireflow.ai/docs/nodes/audio--heygen_voice_clone), [Segmind](https://www.segmind.com/models/heygen-voice-clone). [3rd-party]
- A HeyGen reviewer advises recording the clone sample "with natural changes in pace, emphasis, and emotion" — [DIY AI HeyGen review](https://diyai.io/ai-tools/video-generation/reviews/heygen-review/). [3rd-party, 2026]

### Inferences
- For EDA jargon, preprocess the script before TTS. My suggestions, adjusted to how the user actually says each term:
  - `fc_shell` → "F C shell" (an underscore may otherwise be read as "underscore" or skipped);
  - "PrimeTime" → "Prime Time";
  - "Tcl" → "tickle", which is how its community usually says it, or "T C L" if that's the user's habit.

  With ElevenLabs, these can live in an alias dictionary, with IPA phoneme rules on v3, v4 or Flash v2. Test each term alone before rendering the full clip.
- In zero-shot models the reference audio mostly carries timbre and prosody, and pronunciation comes from the text front end. Saying the jargon in your sample probably won't teach the model how to pronounce it; respelling the script is the dependable fix.
- To reduce flat prosody, record the sample in the same energetic, explanatory "talking to camera" register as the target clip. Keep the generated clip short (45–60 s) to limit drift, and generate 2–3 takes to pick from.
- The audio of the user's planned selfie video can double as the clone sample (extract it with ffmpeg), as long as it is clean and at least about 30–60 s long.

### Gaps
- No Reddit or Hacker News threads were retrievable, so there are no larger-sample reports of friends or family being fooled, or not, by clones.
- No sources on how TTS handles EDA terms (`fc_shell`, PrimeTime, Tcl) specifically.
- No practitioner comparison of accent fidelity for non-US/UK accents between vendors.

## 5. Lip-synced avatar video: does a real recording give better-looking lip sync than TTS, and is recording yourself the better choice for a one-off test?

### Takeaway
I found no controlled comparison showing that real recordings lip-sync *more accurately* than TTS. Avatar vendors accept both. But reviewers say the audio's delivery drives the avatar's whole performance, and flat narration makes avatars look stiff. A real recording of the user is free, guaranteed to sound like them, and has natural prosody and correct jargon pronunciation, so it is the better *first* experiment. A cloned-voice version can then be an A/B test with the same script.

### Cited Findings
- A 2026 review of HeyGen Avatar V says the engine "uses the audio delivery as a major motion signal. Flat narration can make the visual performance feel stiff even when the avatar image is strong." It adds that a dedicated voice clone recorded with natural variation gives the engine more to work with than audio captured during avatar training — [DIY AI HeyGen review](https://diyai.io/ai-tools/video-generation/reviews/heygen-review/). [3rd-party]
- HeyGen's own pages say both work: "Upload clean, noise-free audio or use HeyGen's text-to-speech for accurate syncing." They pitch TTS for easy edits ("changing the text, not re-recording") — [HeyGen lip-sync tool](https://www.heygen.com/en-in/tool/create-ai-lip-sync-videos), [HeyGen TTS avatar](https://www.heygen.com/tool/text-to-speech-avatar). [Vendor]
- One hands-on tester found HeyGen's avatar lip sync "doesn't look quite right" and not yet good enough to pass as natural on social media. The search summary called this an older test and didn't make clear which page it came from — [AIToolsSME](https://www.aitoolssme.com/blogs/elevenlabs-heygen-ai-voice-cloning) or [Morphed (which sells a competing product)](https://morphed.app/blog/heygen-ai-video-generator). [Practitioner/Competitor; possibly outdated]
- Short-sample clones may "flatten out" natural variation and make technical vocabulary sound stilted — [MindStudio](https://www.mindstudio.ai/blog/what-is-heygen-avatar-5). [3rd-party]
- Built-in voice cloning in avatar tools, per third-party sites with conflicting prices:
  - **HeyGen:** instant voice clone from about 30 s of audio, unlimited on Creator ($29/month) and above, one clone on Free. API access reportedly needs Business ($149/month plus $20/seat) — [Arcade](https://www.arcade.software/post/heygen-pricing), [Creatify (HeyGen competitor)](https://creatify.ai/review/heygen-ai).
  - **Hedra:** voice cloning on Creator ($30/month, 5,400 credits) and above. Other plans: Basic $15 (1,500 credits), Professional $75 (14,400 credits). Has a public API — [ToolQuestor](https://toolquestor.com/vs/hedra-vs-heygen), [Magic Hour Hedra guide (competitor)](https://magichour.ai/blog/guide-to-hedra-ai), [Hedra voice cloning page](https://mkt.hedra.com/uses/ai-voice-cloning).
  - **D-ID:** only an "Advanced $196/mo with API" mention surfaced — [Fluxnote](https://fluxnote.io/best/best-talking-avatar-generators).

  [3rd-party/Competitor/Vendor]

### Inferences
- For a private one-off test of "does this look like me," recording the script yourself is the better default:
  - it costs $0;
  - the voice is 100% you;
  - prosody is natural, which reviewers say drives better facial and head motion;
  - EDA jargon is pronounced correctly;
  - no voice clone is stored with a vendor.

  This assumes the chosen avatar API accepts uploaded audio, which HeyGen's pages indicate. It also isolates the video question from the voice question.
- If the goal also covers "can AI fake me saying something I didn't record," run a second pass: the same script through one cheap clone (HeyGen Voice Turbo, Fish, or ElevenLabs Starter) into the same avatar pipeline, then compare the two. The incremental cost is cents to $6.
- Using the avatar vendor's own clone (for example HeyGen Voice) keeps everything in one API. Standalone voice APIs can feed any avatar tool that accepts audio.

### Gaps
- No controlled test (blind ratings or sync metrics) of real vs TTS audio driving the same avatar model was found, for HeyGen, Hedra, D-ID or open-source lip-sync models.
- Whether HeyGen's, Hedra's and D-ID's *API* tiers (as opposed to web plans) include voice cloning, and at what cost, was not verified. The parallel avatar-tool research may cover this.

## 6. Consent/verification rules, voice-data retention and deletion at the main vendors, and the security risk of having a voice clone on file

### Takeaway
Most instant-clone services still rely on a checkbox or self-attestation. Exceptions: ElevenLabs PVC (read-aloud voice captcha), Azure Personal Voice (recorded consent statement plus Microsoft approval), Descript (spoken consent statement), and Resemble (live recording, easily bypassed per Consumer Reports, March 2025). Cloning your own voice satisfies every one of these. ElevenLabs lets you delete your account and its voice data, but sets no fixed retention period, and zero-retention mode reportedly excludes cloning. PlayHT's shutdown shows clones can disappear, or change hands, in an acquisition. Voiceprint authentication at banks is widely considered broken; OpenAI's CEO said in July 2025 that AI has "fully defeated" it. A stored clone adds modest extra risk compared with public audio of you that already exists. Delete it after the test, and don't rely on bank voice ID.

### Cited Findings
**Consent and verification**
- **Consumer Reports, March 2025** (possibly outdated), testing 6 companies: ElevenLabs, Speechify, PlayHT and Lovo "required only that researchers check a box confirming that they had the legal right to clone the voice or make a similar self-attestation." Resemble required real-time recording, which testers got around by playing a recording from a computer. Descript required a specific spoken consent statement, the most effective check. CR urged technical consent verification — [Consumer Reports](https://innovation.consumerreports.org/new-report-do-these-6-ai-voice-cloning-companies-do-enough-to-prevent-misuse/), [The Register, 10 Mar 2025](https://www.theregister.com/2025/03/10/ai_voice_cloning_safeguards/), [NBC News](https://www.nbcnews.com/tech/security/ai-voice-cloning-software-flimsy-guardrails-report-finds-rcna195131). [News/Independent]
- **ElevenLabs** today:
  - consent attestation for every API clone (vendor claim);
  - PVC voice-captcha verification, own voice only — [PVC docs](https://elevenlabs.io/docs/eleven-creative/voices/voice-cloning/professional-voice-cloning);
  - celebrity and high-risk voices blocked — [ElevenLabs help: restrictions](https://help.elevenlabs.io/hc/en-us/articles/13313778519057), [TechJack Solutions](https://techjacksolutions.com/ai-tools/elevenlabs/);
  - claimed traceability and SynthID watermarking — [ElevenLabs blog](https://elevenlabs.io/blog/voice-cloning-api).

  [Vendor/3rd-party]
- **Azure Personal Voice:** explicit verbal consent statement, plus an application for limited access — [MS Learn consent](https://learn.microsoft.com/el-gr/azure/ai-services/speech-service/personal-voice-create-consent), [Azure pricing footnote](https://azure.microsoft.com/en-us/pricing/details/speech/). [Vendor]
- **HeyGen voice clone**, via a third-party wrapper: a checkbox, "I own this voice or have permission to clone it." Pictory, a different avatar vendor, requires a recorded consent sentence for its avatar and voice clones — [Wireflow](https://www.wireflow.ai/docs/nodes/audio--heygen_voice_clone), [Pictory KB](https://kb.pictory.ai/en/articles/14297997-what-is-the-consent-footage-needed-to-create-an-avatar-clone-or-a-voice-clone). [3rd-party/Vendor]
- **Fish Audio:** requires that you have the right to clone the voice and publishes consent guidance. No technical verification surfaced — [Bitdoze](https://www.bitdoze.com/fish-audio-clone-voice/), [Kingy.ai](https://kingy.ai/ai/fish-audio-a-comprehensive-review-of-its-features-voice-cloning-and-value-proposition/). [3rd-party]
- **MiniMax:** its public docs reportedly describe no consent-verification mechanism as of Aug 2026 — [Invideo pricing comparison](https://invideo.io/blog/ai-voice-model-pricing/). [3rd-party]
- **Cartesia:** no consent policy surfaced. Third-party commentary cites Tennessee's ELVIS Act and California AB 1836 / AB 2602 as laws requiring verified consent of the voice owner — [RapidDevelopers](https://rapidevelopers.com/ai-implementation/ai-based-voice-cloning-tool-ai-white-label). [3rd-party]
- A May 2026 article discusses ElevenLabs cloning alongside the US NO FAKES Act; only its title surfaced — [Fora Soft, 31 May 2026](https://www.forasoft.com/learn/ai-for-video-engineering/articles-ai/elevenlabs-pricing-voice-cloning-no-fakes-act). [3rd-party]

**Retention and deletion**
- **ElevenLabs CCPA notice:** users can request deletion of "all Personal Information we maintain about you including your account and the Voice Data associated with your account" (or anonymization where the law allows), and can close the account from settings — [ElevenLabs CCPA notice](https://elevenlabs.io/ccpa-notice-at-collection). [Vendor]
- Its general privacy policy says data is kept "as long as necessary to provide… the Services and as required by applicable law," with no fixed period — [Conduct Atlas](https://conductatlas.com/platform/elevenlabs/elevenlabs-privacy-policy/data-retention/). [3rd-party]
- ElevenLabs agent conversations are kept 2 years by default (configurable from 0 to unlimited). This applies to the agents product, not TTS — [ElevenLabs retention docs](https://elevenlabs.io/docs/eleven-agents/customization/privacy/retention). [Vendor]
- Deepgram, a competitor, says ElevenLabs' Zero Retention Mode is Enterprise-only and "voice cloning workflows are excluded from Zero Retention Mode entirely." It also says the privacy policy treats voice data as possibly biometric and cites a 30-day post-deletion backup window. Unverified — [Deepgram](https://deepgram.com/learn/how-elevenlabs-uses-your-audio-data). [Competitor]
- PlayHT users' clones and audio were reportedly deleted with no export when the service shut down at the end of 2025 — [TextToLab](https://texttolab.com/blog/play-ht-shutdown-alternatives), [AnySpeech](https://anyspeech.io/playht-alternatives). [Competitor]

**Security risk**
- On 22 July 2025, at a Federal Reserve conference, OpenAI CEO Sam Altman warned of a "significant impending fraud crisis." He said AI has "fully defeated" voiceprint authentication, which some banks still use for large transactions — [AP via Local10](https://www.local10.com/business/2025/07/22/openais-sam-altman-warns-of-ai-voice-fraud-crisis-in-banking), [Benzinga](https://www.benzinga.com/markets/tech/25/07/46571546/sam-altman-warns-of-impending-fraud-crisis-as-banks-still-use-voiceprints-for-big-transactions-a-thing), [eWeek](https://www.eweek.com/de/news/openai-sam-altman-ai-voice-cloning-fraud-warning/). [News; possibly outdated]
- A BBC journalist used a voice clone to get into her accounts at Santander and Halifax, both of which used voice ID (Nov 2024) — [CX Today](https://www.cxtoday.com/contact-center/voice-cloning-tech-is-breaking-customer-authentication-systems/). [News; possibly outdated]
- A reporter got into a Lloyds Voice ID account with a clone, and Senator Sherrod Brown wrote to six large US bank CEOs about voice authentication — [Vice](https://vice.com/en/article/n7enqd/senator-asks-banks-stop-ai-cloned-voices). [News; 2023, possibly outdated]
- ITIF (May 2024) recommended that regulators bar financial institutions from relying *solely* on voice authentication — [ITIF](https://itif.org/publications/2024/05/20/to-do-ban-financial-institutions-from-relying-solely-on-voice-authentication/). [Think tank; possibly outdated]
- OpenAI (Apr 2024) urged businesses to phase out voice-based authentication — [CX Today](https://www.cxtoday.com/contact-center/openai-warns-businesses-to-phase-out-voice-based-authentication-stalls-the-release-of-its-voice-cloning-tool), [GovInfoSecurity](https://www.govinfosecurity.com/cloned-voice-tech-coming-for-bank-accounts-a-24850). [News; possibly outdated]

### Inferences
- Cloning your own voice clears every vendor's consent bar. The only real friction is Azure's approval gate, which rules it out for a quick personal test, and ElevenLabs PVC's voice captcha, which is unnecessary here.
- Most services need only seconds to a minute of audio and a checkbox. So anyone with a short public recording of the user can already clone them; storing a clone yourself adds limited new exposure. The extra risks are account or API-key compromise (someone generating speech as you from your account) and the vendor's retention, breach or acquisition (as with PlayHT).
- Mitigations, which are my suggestions and not sourced in this session:
  - store the API key only as an environment variable and revoke it after the test;
  - delete the cloned voice, and the account if you're done (ElevenLabs CCPA deletion);
  - prefer a local CPU model (Pocket TTS) if keeping the voice off third-party servers matters;
  - opt out of bank voice-ID where offered;
  - agree a family "safe word" against voice-clone scams.

### Gaps
- Voice-data retention and deletion terms for Cartesia, Fish Audio, HeyGen Voice, Inworld, MiniMax, Hume and fal.ai/Replicate inputs were not found.
- ElevenLabs' current biometric-consent language (for example under Illinois BIPA) and how long it keeps a deleted clone's model were not confirmed from the primary policy.
- No 2026 reports surfaced of US banks dropping voice ID, or of FTC/FBI guidance; the bank-related sources are from 2023–2025.
- Consumer Reports' assessment is from March 2025. I found no 2026 re-test of vendor safeguards.
