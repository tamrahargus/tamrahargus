# AI talking avatars from one photo or a short selfie video: tool-agnostic comparisons, giveaways, and input best practices (state as of 23 Oct 2026)

**How this was researched (read first).** No web page could be opened directly. The sandbox egress proxy returned 403 for every general host tried (reddit.com, news.ycombinator.com, youtube.com, arxiv.org, huggingface.co, wikipedia.org, artificialanalysis.ai, venturebeat.com, invideo.io, longcatai.org, versely.studio). WebFetch also failed DNS lookup for every URL, including fal.ai and help.heygen.com. So **every finding below comes from search-engine result summaries and snippets** (about 25 searches), not from reading the full pages. Short quoted fragments are as they appeared in those snippets. Partway through, the shared per-turn search budget ran out. That stopped the planned searches on photo, video and audio input best practices, AI "tells", voice-clone APIs, post-processing and named press outlets, so Q4 and Q5 are thinner than Q1–Q3 and Q6. **No Reddit or Hacker News thread surfaced in any search result.** The "community consensus" below is built from blogs, one forum, review sites, X posts and reseller tests, not from Reddit or HN.

**Source labels:**
- [INDEPENDENT]: no evident commercial stake.
- [VENDOR]: the publisher makes one of the tools it compares.
- [RESELLER]: the publisher sells API access to several of the compared models. This covers WaveSpeed, PiAPI, fal, Atlas Cloud, Fuser, Segmind and OpenArt.
- [SEO/AFFILIATE]: a "best of" or "tested" listicle with a likely affiliate or lead-generation motive.
- [SELF-REPORTED]: the model developer's own evaluation.
- [ANECDOTE]: a single person's account.
- [OLD]: older than about 6 months (before late April 2026). Treat it as possibly outdated, because rankings move monthly.

## 1. Are there public leaderboards, arenas or human-eval benchmarks for talking-avatar / lip-sync quality in 2026, and what do they rank top?

### Takeaway
As of October 2026 there is no established, independent public leaderboard for photo-to-talking-head or digital-twin realism. Three things come closest:
- **OpenArt Arena's Lip Sync board.** It launched 15 Sep 2026 and uses blind, expert-weighted voting, but it is run by a model-hosting platform, and its current leader could not be retrieved.
- **Artificial Analysis.** Its video arenas rank general text-to-video and image-to-video models, not identity-preserving talking heads. Its separate cloned-voice TTS arena put HeyGen Voice at #1 on 9 Oct 2026.
- **Developer technical reports with human-preference studies.** LongCat-Video-Avatar 1.5 and KlingAvatar 2.0 each rank their own model first. In the more detailed one (LongCat), HeyGen, OmniHuman 1.5, Kling Avatar 2.0 and the open-source InfiniteTalk sit in a tight top cluster.

### Cited Findings
**OpenArt Arena (Lip Sync board)** [RESELLER-run arena]
- Launched 15 Sep 2026. Video boards are split by job: Ads, Film, Animation, Motion Design, Editing and Lip Sync. The Lip Sync board covers matching visible speech or singing to audio. — [OpenArt: What is OpenArt Arena](https://openart.ai/blog/what-is-openart-arena/); [OpenArt: AI model leaderboard](https://openart.ai/blog/ai-model-leaderboard/); [Jerrod Lew on X, 15 Sep 2026](https://x.com/jerrod_lew/status/2099944544892821737)
- Method is blind pairwise judging: "Creative pros judge image and video outputs blind. No logos, no model names, just two outputs and a vote." — [Min Choi on X, 15 Sep 2026](https://x.com/minchoi/status/2099907680890417178)
- Reported panel is 28 expert judges plus 1,003 "Tastemakers". Scores come from a Bradley–Terry model with published confidence intervals, expert votes count more than Tastemaker votes, and scores are meant to be compared only within one board. — [OpenArt blog](https://openart.ai/blog/what-is-openart-arena/); [Creators Toolbox](https://creatorstoolbox.com/blog/openart-openart-arena-leaderboard-for-creative-intelligence)
- VentureBeat gives a different panel size: OpenArt's handpicked creative-professional users and outside experts, "numbering more than 800". This does not reconcile with the 28 + 1,003 figure above. — [VentureBeat](https://venturebeat.com/orchestration/whats-the-best-ai-model-for-graphic-design-video-ads-lip-sync-and-more-openarts-new-arena-offers-leaderboards-for-different-media-jobs)
- One creator called it "a useful AI leaderboard" because it ranks models per job. [practitioner opinion, 16 Sep 2026] — [Aria Westcott on X](https://x.com/AriaWestcott/status/2100163156668534786)
- No snippet showed which models lead the Lip Sync board (see Gaps).

**Artificial Analysis (AA)** [INDEPENDENT benchmarker; site blocked, so data comes via secondary snippets]
- No AA lip-sync, avatar or talking-head leaderboard turned up. AA runs separate Video Arena Elo pools for text-to-video, image-to-video and video editing, with splits for models that generate synchronized audio. — [invideo, "Best AI Video Model in August 2026"](https://invideo.io/blog/best-ai-video-model/) [VENDOR-adjacent: invideo is a video-creation product]; [AlphaSignal: AA launches a Video Editing Arena pitting 6 frontier models](https://alphasignal.ai/news/artificial-analysis-launches-a-video-editing-arena-pitting-6-frontier-models)
- General-video standings (not talking-head-specific; sources disagree):
  - An August 2026 guide lists Gemini Omni Flash leading AA text-to-video-with-audio at 1245 Elo, three points ahead of MiniMax-H3 at 1242. — [invideo, Aug 2026](https://invideo.io/blog/best-ai-video-model/)
  - A reseller calls HappyHorse-1.0 "the mystery #1 AI video model". — [WaveSpeed blog](https://wavespeed.ai/blog/posts/what-is-happyhorse-1-0-ai-video-model/) [RESELLER]
- **AA Controlled Voice TTS Arena.** Announced 8 Jul 2026, it tests every TTS model on the same 8 cloned voices, so cloning quality is separated from which voice a model happens to have. — [Artificial Analysis on X, 8 Jul 2026](https://x.com/ArtificialAnlys/status/2074886571166462405?lang=en)
- **HeyGen Voice #1 for cloned voices, 9 Oct 2026.** AA wrote: "HeyGen Voice takes the #1 spot on the Artificial Analysis Controlled Voice TTS Arena Leaderboard, ahead of Alibaba's Qwen-Audio-3.1-TTS-Plus and ElevenLabs' Eleven v4 Turbo". It is HeyGen's first TTS model evaluated there. The search summary gives Elo 1,201 across 1,468 arena appearances. Separate coverage is headlined "HeyGen's Voice Turbo Tops Speech Leaderboard at 87% Less Cost" (not confirmed to be the same board). — [Artificial Analysis on X, 9 Oct 2026](https://x.com/ArtificialAnlys/status/2108608255387935199); [AlphaSignal](https://alphasignal.ai/news/heygen-s-voice-turbo-tops-speech-leaderboard-at-87-less-cost)
- AA added multilingual TTS arenas for 9 non-English languages on 22 Sep 2026, noting that TTS performance varies significantly by language. — [Artificial Analysis on X, 22 Sep 2026](https://x.com/ArtificialAnlys/status/2102490340678856997)

**Developer technical reports with human evaluation** [SELF-REPORTED]
- **LongCat-Video-Avatar 1.5** (Meituan, open-source, arXiv 2605.26486, May 2026):
  - User-preference win rates for LongCat 1.5: **65.9% vs Kling Avatar 2.0, 61.1% vs OmniHuman 1.5, 54.3% vs HeyGen.** — [LongCat model page](https://www.longcatai.org/models/video-avatar); [AIbase](https://news.aibase.com/news/28241)
  - Scale: more than 500 test samples across varied audio-visual complexity, scenarios and languages, and more than 13,240 individual judgments. — [arXiv HTML](https://arxiv.org/html/2605.26486v1). The launch page cites 770 evaluators. — [LongCat news](https://www.longcatai.org/news/video-avatar-1.5)
  - Single-person result: "the top three methods—LC-video-avatar 1.5, LC-video-avatar 1.0, and InfiniteTalk—demonstrate comparable leading performance, which is closely followed by Heygen and OmniHuman-1.5". — [arXiv HTML](https://arxiv.org/html/2605.26486v1)
  - Multi-person human-likeness: 2.730 vs InfiniteTalk's 2.339. — [arXiv HTML](https://arxiv.org/html/2605.26486v1)
  - The authors concede "audio-visual harmony remains an open challenge across the entire field". — [arXiv HTML](https://arxiv.org/html/2605.26486v1)
- An independent review criticizes the LongCat paper. It says no details are given on benchmark construction, sampling, prompt distribution or the human-study protocol ("blinding, rating scales, number of raters, inter-rater reliability statistics"). It also says the closed-source comparators ran with uncontrolled inference settings. — [Pith review](https://pith.science/paper/2605.26486)
- **KlingAvatar 2.0** Technical Report (arXiv 2512.13313, Dec 2025) [OLD]. It claims to beat OmniHuman 1.5, an earlier Kling avatar model and HeyGen on visual quality, camera movement, lip-sync accuracy and "fine-grained lip-teeth detail preservation". — [arXiv](https://arxiv.org/html/2512.13313v1)

**Academic benchmarks** (methods-focused; mostly research models, not the commercial tools)
- **THEval** (arXiv 2511.04520, revised Mar 2026) [OLD]: benchmarks 17 audio- and video-driven talking-head methods. Its user study found that **existing automatic metrics correlate poorly with human ratings**. — [arXiv](https://arxiv.org/html/2511.04520v3)
- **"Temporally-Aligned Evaluation for Audio-Driven Talking Head Generation"** (arXiv 2606.01031, 31 May 2026): covers 20 methods across seven datasets. Snippets did not show whether it includes a human-preference study. — [arXiv](https://arxiv.org/abs/2606.01031)
- **TalkingHeadBench** (arXiv 2505.24866, rev. Jan 2026) [OLD] benchmarks deepfake detection, not quality. — [arXiv](https://arxiv.org/html/2505.24866v3)
- **MTAVG-Bench** (arXiv 2602.00607, early 2026) [OLD] covers multi-talker dialogue audio-video generation. — [arXiv](https://arxiv.org/html/2602.00607v1)
- A curated GitHub list names "AVAPrintDB", a 2026 benchmark for talking-head avatar fingerprinting and photorealism. Not verified beyond the listing. — [Awesome-Talking-Head-Synthesis](https://github.com/Kedreamix/Awesome-Talking-Head-Synthesis)

### Inferences
- The only multi-model human-preference numbers come from developers who rank themselves first, so the defensible reading is the cluster, not the order. As of mid-2026, HeyGen, OmniHuman 1.5, Kling Avatar 2.0, InfiniteTalk and LongCat are all top tier for a single person talking. LongCat's own 54.3% against HeyGen is close to a coin flip.
- The general video-arena leaders (Gemini Omni Flash, MiniMax-H3, HappyHorse, Wan, Seedance) are judged on prompt-to-video quality, not on preserving a specific real face. They are not a proxy for "looks like me".
- For the voice half, AA's Controlled Voice arena (cloned voices, 9 Oct 2026) is the best independent evidence found. It ranks HeyGen Voice above ElevenLabs Eleven v4 Turbo, which suggests a HeyGen-only pipeline could be competitive on both face and voice. This is an inference: TTS arena listeners judge naturalness, not resemblance to a specific person.
- THEval's finding means vendor "lip-sync accuracy %" claims (such as the "96%" in Q2) are weak evidence of perceived realism. A human side-by-side view is the meaningful test.

### Gaps
- Current OpenArt Arena Lip Sync rankings: which models are on the board and which lead it. No snippet had them, and openart.ai/arena could not be opened.
- Whether AA has added any lip-sync or avatar arena. The site was blocked and searches found none.
- No Hugging Face arena for talking heads or lip sync surfaced.
- Which methods THEval and the May 2026 temporal-alignment paper rank top, and whether either includes commercial tools.
- Conflicting AA general-video claims could not be traced to a specific page and stay unverified: one snippet said Wan 3.0 is #1 on AA text-to-video with audio (1,156 Elo), and another said AA moved to a v2.0 board with a pinned Elo scale.

## 2. Independent shootouts (YouTube creators, journalists, Reddit/HN) comparing multiple tools side by side in 2025–2026: what did they conclude, on what inputs?

### Takeaway
Truly independent, same-input, multi-tool shootouts are scarce. Nearly every 2025–2026 "head-to-head" found came from one of two kinds of publisher:
- **A vendor of one contestant:** VEED, ByteDance's Dreamina, HeyGen, Synthesia, Creatify or PixVerse.
- **An API reseller hosting all contestants:** WaveSpeed, PiAPI or Fuser.

These tests usually use one clip or a handful. No multi-tool shootout from The Verge, Wired, Tom's Guide or PCMag surfaced; press coverage is first-person, single-tool clone stories. Even so, the biased tests repeat the same verdicts:

| Tool | Recurring verdict |
|---|---|
| Kling AI Avatar | Most precise mouth and lip sync, very stable, but stiff with little movement |
| OmniHuman (1.5) | Most expressive body and gestures; poor value and short clips (30 s per call) |
| InfiniteTalk | Most natural, dynamic motion; slightly weaker on some phonemes |
| HeyGen Avatar IV | Recommended default for a still portrait |
| Hedra Character-3 | Cheaper and character-oriented, with good raw lip sync |

### Cited Findings
**Reseller same-input tests** [RESELLER]
- **WaveSpeedAI, 16 Sep 2025** [OLD]. Tested InfiniteTalk, Kling v1 and OmniHuman "using the same video". Sample size was not stated and appears to be one clip. The quotes below are each from either the X post or the blog; which page carries which quote is unverified. — [WaveSpeedAI on X](https://x.com/wavespeed_ai/status/1967888266797125769); [WaveSpeed blog: The 2026 AI Digital Human Crown](https://wavespeed.ai/blog/posts/the-2026-ai-digital-human-crown/)
  - InfiniteTalk "achieves the best balance of naturalness and stability in facial expressions, pose details, and overall look and feel".
  - For lip-sync consistency, "OmniHuman leads, Kling follows, and InfiniteTalk lags slightly on certain phonemes and linked speech".
  - Kling was very stable but had stiff expressions (snippet paraphrase).
- **PiAPI, 2026** (PiAPI resells both models). In a neutral-speech test, OmniHuman 1.5 and Kling AI Avatar were closely matched on head motion, but "Kling AI Avatar demonstrated stronger lip-sync accuracy and clearer mouth articulation". — [PiAPI blog](https://piapi.ai/blogs/omnihuman-1-5-vs-kling-ai-avatar)
- **Fuser, 2026** [RESELLER]. Ran one 6.3-second voice line through four models (n=1). — [Fuser](https://fuser.studio/articles/best-ai-lip-sync-tools)
  - Recommends LatentSync for editing words into existing video, because it changes only the mouth.
  - Recommends the HeyGen Avatar IV node for a still portrait; it animates the head, face and hands to the audio.
  - Recommends MiniMax H3 for generating a whole shot around a voice file.
  - Seedance 2.5 re-voiced the line instead of using the recording and "refused the photoreal face".
- **Videomaker.me** (date unknown; publisher's commercial interest unverified). Compared Kling AI Avatar, Hedra and InfiniteTalk. — [Videomaker.me](https://videomaker.me/blog-kling-ai-avatar-vs-hedra-vs-infinitetalk-best-ai-avatar-tool-54935)
  - Kling "offers the best realism and lip-syncing, though it lacks movement compared to others".
  - InfiniteTalk "provides the most dynamic motion and solid lip-sync but is more expensive".

**Vendor-run comparisons** [VENDOR]
- VEED tested its own Fabric 1.0 against others. It claims Fabric leads on lip-sync accuracy and speed and that HeyGen and Hedra lag on speed and quality. — [VEED](https://www.veed.io/learn/best-lipsync-api)
- ByteDance's Dreamina (maker of OmniHuman) compares it with Kling: "OmniHuman AI is ideal for professional video, as it can create full-body realistic animation, emotive movements, and photorealistic graphics". — [Dreamina/CapCut](https://dreamina.capcut.com/resource/omnihuman-vs-kling-ai)
- HeyGen, Synthesia, Creatify and PixVerse each publish "tested" best-of lists that put themselves at or near the top. — [HeyGen](https://www.heygen.com/blog/best-ai-avatar-generators); [Synthesia](https://www.synthesia.io/post/best-ai-avatar-generator); [Creatify](https://creatify.ai/blog/best-ai-avatar-generators-and-tools); [PixVerse](https://pixverse.ai/en/blog/best-ai-avatar-video-generator-2026)

**Scenario reviews and listicles** [SEO/AFFILIATE or interest unclear]
- **Versely, 2026** (its commercial interest and sample size are not verified). Says OmniHuman 1.5 wins "zero scenarios" against Kling V2 Pro, HeyGen, Creatify Aurora and Hedra at current pricing. — [Versely](https://www.versely.studio/blog/omnihuman-1-5-review-2026)
  - Concedes that OmniHuman's identity and gesture consistency across a whole generation is a real technical advance.
  - Notes OmniHuman has no published self-serve pricing.
  - For lip-sync-first jobs (mouth accuracy, dubbing, UGC talking heads), the alternatives "already have clearer pricing and workflow fit".
- A "Hedra alternatives" roundup says Hedra Character-3 has the edge on raw lip-sync precision, while HeyGen Avatar IV is stronger on full-body motion and micro-expressions. — [Morphed](https://morphed.app/blog/hedra-alternatives)
- **Roundups claiming hands-on tests** (Venture Harbour's "I Tested the 7 Best AI Avatar Video Generators Head-to-Head", Techsy, Max-Productive). Which page made which claim could not be verified, because the pages couldn't be opened. Together they say: — [Venture Harbour](https://ventureharbour.com/best-ai-avatar-software/); [Techsy](https://techsy.io/en/blog/best-ai-avatar-generators-2026); [Max-Productive](https://max-productive.ai/blog/best-ai-avatar-generators/)
  - HeyGen is best overall, for language support and the fastest avatar setup; one reviewer reports "over 96% lip-sync accuracy".
  - Synthesia showed "the most convincing body language" in one test, and its Express-3 avatars have "closed the realism gap with HeyGen".
  - Hedra Character-3 "handled a still photo better than we expected".
  - Entry prices are about $29/month for HeyGen, $29/month for Synthesia and $15/month for Hedra.
- Weak methodology in other lists:
  - AIToolChooser says it did not run a shared hands-on test across its six tools. — [AIToolChooser](https://aitoolchooser.com/best-ai-lip-sync-tools/)
  - Pixazo's open-source ranking (Wav2Lip and Sync 1.9 top for sync accuracy, LatentSync top for visual fidelity) is a ratings table, not a described test. — [Pixazo](https://www.pixazo.ai/blog/best-open-source-ai-lip-sync-models)
  - Other lists name MuseTalk as the best free option and LatentSync 1.6 as the best modern open-source option. — [Crazyrouter](https://crazyrouter.com/en/blog/ai-lip-sync-tools-comparison-2026); [Meaningfussion](https://meaningfussion.com/best-ai-lip-sync-tools-2026/)

**YouTube** (titles and line-ups only; conclusions could not be retrieved)
- "I Compared Top 4 AI Talking Avatar Video Generator, So You Don't Have To": HeyGen Avatar IV vs Creatify Aurora vs VEED Fabric 1.0 vs OmniHuman. The snippet says "OmniHuman 2.5", probably meaning 1.5 (unverified). It was about 90 days old when indexed, so roughly July 2026. — [YouTube](https://www.youtube.com/watch?v=ybxN6BmszEI)
- "AI Singing Lip Sync Test: OmniHuman 1.5 vs Kling Avatar 2.0 vs Kling Motion Control" uses singing as a stress test. — [YouTube](https://www.youtube.com/watch?v=foZvnCpIrYg)
- "HeyGen Avatar 5 & Seedance Review — I Built My AI Digital Twin". — [YouTube](https://www.youtube.com/watch?v=he9llVz0GJM)
- A Substack creator who retested 20+ AI video generators in 2026 concluded that all-in-one tools improved, that speed now matters more than realism, and that confusing credit systems hurt rankings (snippet paraphrase). — [Anangsha, Substack](https://anangsha.substack.com/p/i-tested-every-ai-video-generator)

**Press and first-person clone stories** (single tool each)
- **Globe and Mail** [INDEPENDENT; OLD, pre-2026]. Reporter Joe Castaldo built "Fake Joe" with HeyGen by recording about 90 seconds of talking, plus sitting still and active-listening gestures. The build took about 24 hours. The clone was jittery at first and "more stoic" after a second attempt. — [Globe and Mail](https://www.theglobeandmail.com/business/article-digital-clone-ai-avatar-meeting-efficiency/)
- **TechCrunch, 26 Sep 2026** [INDEPENDENT]. A journalist created an interactive digital twin with Synthesia, the first avatar Synthesia had made for a journalist. The snippet reports no friends-and-family test. — [TechCrunch](https://techcrunch.com/2026/09/26/i-created-an-interactive-digital-avatar-of-myself-and-you-can-talk-to-it/)
- **Unite.ai HeyGen review** [likely AFFILIATE; date unknown]. The author's AI clone fooled the author's own mother on a test call. — [Unite.ai](https://www.unite.ai/heygen-review/)

**Reddit and Hacker News**
- No Reddit or HN threads appeared for any query, and both sites were blocked for direct fetching. See Gaps.

### Inferences
- The biased tests are internally consistent and match the self-reported LongCat cluster from Q1 (the verdict table above).
- Seedance 2.5 refusing a photoreal face (Fuser) suggests some general-purpose video models now block real-person photos. For a real person, dedicated avatar or lip-sync models are the practical route.
- Shootout inputs are tiny, often one clip of 6–30 s. None shows how the tools hold up across a 45–60 s monologue, which is the user's case.

### Gaps
- No multi-tool avatar shootout from The Verge, Wired, Tom's Guide or PCMag surfaced. A targeted search per outlet could not run because the search budget was exhausted.
- The YouTube comparisons' conclusions could not be retrieved; no transcripts were reachable.
- Reddit and HN consensus could not be read at all. This is the largest limitation for the community-opinion part of the brief.
- Sample sizes for the WaveSpeed, PiAPI, Versely and Videomaker tests are not stated in the snippets.
- A 2026 comparison of Hedra, HeyGen and Captions for UGC ads exists, but its findings were not retrieved. — [EvolveAMZ](https://evolveamz.com/ai-ugc-video-ads-hedra-heygen-captions-2026/)

## 3. Recurring community consensus: which tool wins for one still photo, which for a selfie-video "digital twin", best value, overhyped, and how fast rankings shifted in 2025–2026

### Takeaway
**Selfie-video digital twin.** HeyGen's Avatar V (launched 8 Apr 2026, trained on about 15 s of footage) is the most-cited realism leader. Hands-on reviewers praise its identity consistency and less plastic skin, but flag teeth, eye and voice issues. Synthesia is the enterprise alternative, but its best "Studio" avatars need a professional shoot.

**Single photo.** There is no single winner:

| Tool | Where it stands |
|---|---|
| HeyGen Avatar IV photo avatar | Most-named well-rounded pick |
| Kling AI Avatar v2 | Best mouth precision and cheapest via API, but stiff |
| OmniHuman | 1.5 is expressive but widely called poor value; 2.0 launched 15 Oct 2026 and is untested independently |
| InfiniteTalk | Open model, natural motion, good for longer clips |
| Hedra Character-3 | Cheap, character-oriented |
| D-ID | Older, still-photo style with limited motion |

**Best value via API.** Kling AI Avatar v2 Standard, Hedra at 720p, HeyGen's API and OmniHuman 2.0 all cost about $0.04–0.07 per second, roughly $2.50–4.20 for a 60 s clip.

**Overhyped.** OmniHuman 1.5 at its price, cloned voices, and vendor accuracy percentages.

**Pace of change.** Rankings turned over several times in 12 months.

### Cited Findings
**Selfie-video twin: HeyGen Avatar V**
- Launched 8 Apr 2026 (borderline [OLD], about 6.5 months ago). It builds a digital twin from about 15 seconds of footage. Its skin rendering is said to remove most of the "plastic" look of older HeyGen models. [vendor-friendly press] — [Stork.ai](https://www.stork.ai/blog/this-ai-avatar-just-stole-a-youtubers-job)
- A hands-on test scored it 9/10. It reports a "0.840 face similarity" score (metric unspecified), 175+ languages and $29/month. The reviewer says it shows "no identity drift", which was Avatar IV's biggest weakness. — [The Planet Tools](https://theplanettools.ai/blog/heygen-avatar-v-tested-hands-on-review-2026)
- Language count conflicts: HeyGen claims 175+, while MindStudio says the avatar can speak 40+ languages. — [MindStudio](https://www.mindstudio.ai/blog/what-is-heygen-avatar-v-digital-twin-explained)
- Another review calls it HeyGen's premium engine for realistic human twins. It says the illusion gets less reliable "when the scene demands full-body movement, prop interaction", and that premium engines plus failed attempts raise the real cost. — [DIY AI](https://diyai.io/ai-tools/video-generation/reviews/heygen-review/)
- [ANECDOTE] Hands-on owner: the avatar copied the reviewer's posture and head tilts, but the voice sounded AI-generated, the teeth were slightly off, and the avatar wore a wedding ring the reviewer does not own. — [brisk.vision Substack](https://lucijatomsic.substack.com/p/avatar)
- [ANECDOTE] A user who compared an AI twin with stock avatars (19 Aug 2026) found the twin more convincing. — [aiavatar blog](https://aiavatar.tech.blog/2026/08/19/i-tried-ai-avatars-vs-ai-twins-which-one-is-better/)

**Synthesia**
- Its Studio Avatar needs a professional filming session, several days of processing and a $1,000/year add-on. One comparison calls this the opposite of HeyGen's approach. (Attribution to this page is uncertain.) — [JorgeP](https://jorgep.com/blog/ai-avatars-digital-twins-value-tools-and-options/)
- Roundups say Synthesia's Express-3 avatars "closed the realism gap with HeyGen". — [Venture Harbour](https://ventureharbour.com/best-ai-avatar-software/) (within-set attribution uncertain)

**Single photo**
- Fuser's one-line test recommends HeyGen Avatar IV for a still portrait. — [Fuser](https://fuser.studio/articles/best-ai-lip-sync-tools)
- A May 2026 "most realistic" roundup names HeyGen, Synthesia, Creatify, D-ID and Hour One. — [Resident, 21 May 2026](https://resident.com/technology-and-digital-resources/2026/05/21/5-most-realistic-ai-avatar-tools-in-2026)
- Related photo-avatar roundups [SEO/AFFILIATE] say: — [Resident](https://resident.com/technology-and-digital-resources/2026/05/21/5-most-realistic-ai-avatar-tools-in-2026); [Zoice](https://zoice.com/blog/best-ai-avatar-generator-from-photo/); [Pose.ai](https://pose.ai/blog/best-ai-talking-avatar-generator-2026) (per-page attribution uncertain)
  - Avatar IV leads on lip sync and micro-expressions.
  - HeyGen's custom (video) avatars traditionally needed 2–5 minutes of self-shot footage.
  - D-ID is the main single-photo option, from about $5.90/month.
- D-ID animates a headshot instantly, but the result stays a still-image avatar rather than a full one. — [DIGEN roundup](https://resource.digen.ai/best-ai-avatar-makers-2026/) (attribution uncertain)
- **Kling AI Avatar:** best lip sync and stability, but stiff, with little movement. — [Videomaker.me](https://videomaker.me/blog-kling-ai-avatar-vs-hedra-vs-infinitetalk-best-ai-avatar-tool-54935); [PiAPI](https://piapi.ai/blogs/omnihuman-1-5-vs-kling-ai-avatar); [WaveSpeed (Sep 2025, OLD)](https://x.com/wavespeed_ai/status/1967888266797125769)
- **OmniHuman 2.0** went live on BytePlus on 15 Oct 2026 at $0.07 per second. [vendor, plus one secondary source] — [BytePlus](https://www.byteplus.com/en/product/OmniHuman); [Supermaker](https://supermaker.ai/blog/omnihuman-2-0-launch/)
  - Added camera movement, stronger emotional expression and tighter lip sync.
  - "Strictly image-sourced": it cannot be driven by a reference video.
  - Region-locked at launch, so broad hands-on testing wasn't yet possible; ByteDance says it will come to Dreamina, with no timeline. — [MindStudio, ~16 Oct 2026](https://www.mindstudio.ai/blog/bytedance-omnihuman-2-avatar-video)
- **InfiniteTalk** (open weights, built on Wan 2.1) is praised for natural, dynamic motion. — [Videomaker.me](https://videomaker.me/blog-kling-ai-avatar-vs-hedra-vs-infinitetalk-best-ai-avatar-tool-54935)
  - A ComfyUI hands-on tester found "the actual mouth movement and synchronization are excellent. The phoneme shapes are accurate and the timing is spot-on." — [Zanno.se](https://zanno.se/lets-talk-multitalk-infinitetalk-wan-s2v/)
  - LongCat's own paper puts it in the top three for a single speaker. — [arXiv](https://arxiv.org/html/2605.26486v1)
- **Hedra:** builds a character you design; HeyGen instead casts from presenters (1,100+ stock) or your twin. Hedra also hosts OmniHuman 1.5 as a third-party model. — [NovoAds](https://novoads.ai/en/blog/hedra-vs-heygen)
  - Entry plan about $8–10/month vs HeyGen's about $29/month, so Hedra is cheaper for occasional use. — [PicassoIA](https://blog.picassoia.com/hedra-vs-heygen-best-ai-avatar-generator)
  - Character-3 handled a still photo "better than we expected". — [Venture Harbour](https://ventureharbour.com/best-ai-avatar-software/)
- **Other photo-to-avatar contenders** in 2026 comparisons: Creatify Aurora, VEED Fabric 1.0, LongCat-Video-Avatar 1.5 (open), and daVinci-MagiHuman (15B, Apache 2.0, from Sand.ai and SII GAIR Lab). One blog calls daVinci-MagiHuman "the current open-weight ceiling" for generating a person rather than animating a photo; the publisher sells GPU cloud. — [YouTube comparison](https://www.youtube.com/watch?v=ybxN6BmszEI); [Spheron](https://www.spheron.network/blog/self-host-ai-avatar-generator-heygen-alternative-2026/)

**Overhyped / disappointing**
- OmniHuman 1.5: "zero scenarios it wins" at current pricing. — [Versely](https://www.versely.studio/blog/omnihuman-1-5-review-2026). Counterpoint: WaveSpeed's Sep 2025 test [OLD] rated OmniHuman best on lip-sync consistency, and LongCat's paper puts OmniHuman 1.5 just behind the leaders. — [WaveSpeed](https://x.com/wavespeed_ai/status/1967888266797125769); [arXiv](https://arxiv.org/html/2605.26486v1)
- Cloned voices: the voice "sounded AI-generated" even when the visuals convinced. — [brisk.vision Substack](https://lucijatomsic.substack.com/p/avatar)
- Forum user on HeyGen: fine for neutral content, but the eyes look "dead" in long or emotional scripts. — [PJIRC forum](https://pjirc.com/t/heygen-ai-review-realistic-ai-avatars-or-not/2288)

**How fast rankings moved** (dated milestones)
- 1 Apr 2025 [OLD]: OmniHuman became publicly usable ("VERY slow and costs 192 credits but it's GOOD. This is from 1 image + sound!"). — [Alex Volkov on X](https://x.com/altryne/status/1907173680456794187)
- 16 Sep 2025 [OLD]: WaveSpeed test of InfiniteTalk vs Kling v1 vs OmniHuman. — [X](https://x.com/wavespeed_ai/status/1967888266797125769)
- Dec 2025 [OLD]: KlingAvatar 2.0 report. — [arXiv](https://arxiv.org/html/2512.13313v1)
- Early 2026 [OLD]: HeyGen moved its API to pay-as-you-go, and free API credits ended in Feb 2026. — [Magic Hour](https://magichour.ai/blog/heygen-pricing); [CrixPix](https://crixpix.com/heygen-pricing/)
- 8 Apr 2026: HeyGen Avatar V. — [Stork.ai](https://www.stork.ai/blog/this-ai-avatar-just-stole-a-youtubers-job)
- May 2026: LongCat-Video-Avatar 1.5. — [arXiv](https://arxiv.org/html/2605.26486v1)
- 26 May 2026: Avaturn AVTR-1, an open-weights real-time avatar model driven by a single photo. — [NatLawReview press release](https://natlawreview.com/press-releases/avaturn-releases-avtr-1-first-open-weights-ai-avatar-duplex-model)
- 15 Sep 2026: OpenArt Arena Lip Sync board. — [X](https://x.com/minchoi/status/2099907680890417178)
- 25 Sep 2026: Google's conversational "Live Avatar", enterprise allowlist only. — [MediaPost](https://www.mediapost.com/publications/article/418288/google-launches-conversational-avatar.html)
- 9 Oct 2026: HeyGen Voice #1 on AA's cloned-voice arena. — [X](https://x.com/ArtificialAnlys/status/2108608255387935199)
- 15 Oct 2026: OmniHuman 2.0 on BytePlus. — [Supermaker](https://supermaker.ai/blog/omnihuman-2-0-launch/)
- About 22 Oct 2026: OmniHuman 2 on Atlas Cloud at $0.056 per second. — [Atlas Cloud](https://www.atlascloud.ai/blog/tips/omnihuman-2-talking-head-ip-system)

### Inferences
- For the user's two input options, the recurring opinion maps as follows:
  - **Short selfie video:** HeyGen Avatar V is the consensus realism pick, and it is API-reachable (see Q6).
  - **One photo:** HeyGen Avatar IV photo avatar is the safe all-rounder. Kling AI Avatar v2 is the precise-mouth value pick. OmniHuman 2.0 is the newest contender, but nobody has tested it independently yet.
- Any recommendation that names a single-photo winner should be re-checked. The field changed within the last 8 days (OmniHuman 2.0), and the main arena board's leader is unknown.
- "Best value" for a one-off 60 s experiment matters less than "best per attempt". Several API options cost about $2.50–4.20 per 60 s attempt, so the $30 budget allows multiple tools or retakes (cost math in Q6).

### Gaps
- No Reddit, HN or Product Hunt consensus could be read directly.
- No independent tests of OmniHuman 2.0 yet; it is only 8 days old.
- Whether Hedra has shipped a model newer than Character-3. A 2026 title mentions "Omnia", but details were not retrieved. — [Magic Hour Hedra guide](https://magichour.ai/blog/guide-to-hedra-ai)
- Captions (Mirage), Sora 2 "cameo"-style self-insertion, Google Veo-based avatars, VEED Fabric and Creatify Aurora did not get dedicated searches, so they could not be assessed.

## 4. What gives AI talking heads away, which tools handle each issue best, and how people test "does it look like me"

### Takeaway
The giveaways most often reported in 2026 hands-on accounts are:
- dead or unfocused eyes in long or emotional delivery
- teeth and mouth-interior errors
- lip sync breaking on fast speech or jargon
- stiffness or too little head and body movement (Kling, D-ID)
- identity drift over a clip (HeyGen Avatar IV; reportedly fixed in Avatar V)
- plastic-looking skin (older HeyGen)
- invented details, such as a wedding ring the person doesn't own
- jitter
- a cloned voice that sounds synthetic, which several users found more telling than the face

Body movement and handling props are still unreliable. How the tools split on these issues:
- **Mouth precision:** Kling, on a self-reported benchmark plus one reseller test.
- **Natural motion:** InfiniteTalk and OmniHuman.
- **Identity consistency and skin:** HeyGen Avatar V.

People test resemblance informally, by showing family, colleagues or an audience. One review used a face-similarity score. Research shows automated metrics track human judgment poorly, so a side-by-side human viewing is the meaningful test.

### Cited Findings
- Teeth "slightly off", an AI-sounding voice and a hallucinated wedding ring in a HeyGen Avatar V twin. [ANECDOTE] — [brisk.vision Substack](https://lucijatomsic.substack.com/p/avatar)
- Eyes look "dead" in long or emotional scripts, and fast speech or jargon breaks lip sync (HeyGen, marketing use; HeyGen version not stated). [ANECDOTE, forum] — [PJIRC](https://pjirc.com/t/heygen-ai-review-realistic-ai-avatars-or-not/2288)
- The avatar inherits its creator's own on-camera stiffness. Trainees in a corporate pilot did not realize the trainer's avatar was AI. [Capterra review, cited secondhand] — [Smart Remote Gigs](https://smartremotegigs.com/software/heygen/)
- Identity drift was Avatar IV's biggest weakness; Avatar V is reported to have none. — [The Planet Tools](https://theplanettools.ai/blog/heygen-avatar-v-tested-hands-on-review-2026)
- Avatar V's skin rendering removes most of the plastic look of older models (vendor-friendly claim). — [Stork.ai](https://www.stork.ai/blog/this-ai-avatar-just-stole-a-youtubers-job)
- The illusion fails on full-body movement and prop interaction. — [DIY AI](https://diyai.io/ai-tools/video-generation/reviews/heygen-review/)
- Jittery first clone, "more stoic" after a second try (HeyGen). [OLD] — [Globe and Mail](https://www.theglobeandmail.com/business/article-digital-clone-ai-avatar-meeting-efficiency/)
- **Mouth and teeth:**
  - KlingAvatar 2.0 claims the best "fine-grained lip-teeth detail preservation" against OmniHuman 1.5 and HeyGen. [SELF-REPORTED, OLD] — [arXiv](https://arxiv.org/html/2512.13313v1)
  - PiAPI saw "clearer mouth articulation" from Kling than OmniHuman 1.5. [RESELLER] — [PiAPI](https://piapi.ai/blogs/omnihuman-1-5-vs-kling-ai-avatar)
  - Hedra Character-3 has the edge on raw lip-sync precision. — [Morphed](https://morphed.app/blog/hedra-alternatives)
- **Stiffness and motion:**
  - Kling was very stable but had stiff expressions (snippet paraphrase). [OLD] — [WaveSpeed](https://x.com/wavespeed_ai/status/1967888266797125769)
  - Kling "lacks movement"; InfiniteTalk is the "most dynamic". — [Videomaker.me](https://videomaker.me/blog-kling-ai-avatar-vs-hedra-vs-infinitetalk-best-ai-avatar-tool-54935)
  - HeyGen Avatar IV is stronger on full-body motion and micro-expressions. — [Morphed](https://morphed.app/blog/hedra-alternatives)
  - D-ID output "stays a still-image avatar". — [DIGEN](https://resource.digen.ai/best-ai-avatar-makers-2026/) (attribution uncertain)
- InfiniteTalk "lags slightly on certain phonemes and linked speech". [OLD] — [WaveSpeed](https://x.com/wavespeed_ai/status/1967888266797125769)
- **Consistency over long clips:**
  - InfiniteTalk uses sparse-frame processing and a rolling 81-frame context window to keep extended sequences consistent. Its README claims fewer hand and body distortions and better lip sync than MultiTalk. [SELF-REPORTED] — [InfiniteTalk README (HF Space mirror)](https://huggingface.co/spaces/kyboface/MyInfiniteTal/blob/main/README.md); [Zanno.se](https://zanno.se/lets-talk-multitalk-infinitetalk-wan-s2v/)
  - OmniHuman 1.5 keeps identity and gestures consistent across a whole generation. — [Versely](https://www.versely.studio/blog/omnihuman-1-5-review-2026)
- "Audio-visual harmony remains an open challenge across the entire field." [SELF-REPORTED paper's own admission] — [arXiv](https://arxiv.org/html/2605.26486v1)
- **How resemblance gets tested:**
  - A clone fooled the author's mother on a test call. — [Unite.ai](https://www.unite.ai/heygen-review/)
  - A creator claims their audience didn't notice a week of avatar-made posts. [ANECDOTE, unverified] — [Medium](https://medium.com/@realtalkonly/i-replaced-myself-with-an-ai-avatar-for-7-days-my-audience-couldnt-tell-and-that-terrified-me-0134d634b35e)
  - A reviewer reports a "0.840 face similarity" score for Avatar V. — [The Planet Tools](https://theplanettools.ai/blog/heygen-avatar-v-tested-hands-on-review-2026)
  - Automatic metrics correlate poorly with human ratings. — [THEval, arXiv](https://arxiv.org/html/2511.04520v3)
- A deepfake-detection benchmark specific to talking heads exists. It is relevant if the user wants to check whether detectors flag the clip. — [TalkingHeadBench](https://arxiv.org/html/2505.24866v3)

### Inferences
- For a 45–60 s talking-to-camera clip, the biggest risks are eye "deadness" and drift over time, plus the voice, rather than lip sync on any single phrase. That favours models with long-context consistency (HeyGen Avatar V, InfiniteTalk) or splitting the clip into shorter segments joined by cuts.
- A practical self-test the report could recommend: watch the AI clip next to real footage of the user, at full screen and at phone size. Then show it to one or two people without saying which is which. Separately, check the mouth on open-vowel and "f/v/th" sounds. This is an inference built from the anecdotes and THEval's metric finding; no source prescribes this exact protocol.
- Because the voice was repeatedly the weakest element, recording one's own voice reading the script is the likely way to get "sounds like me". This is an inference; no source directly compared own-recording against a clone for avatars.

### Gaps
- Searches dedicated to blinking rate, tongue rendering, gaze behaviour, neck stiffness, hand artifacts and audio-visual lag could not run because the search budget was exhausted. No source found compares tools on these specific tells.
- No systematic friends-and-family blind test with a stated sample size was found.

## 5. Best-practice inputs: source photo, selfie video for a twin, audio, script length and coherence, post-processing

### Takeaway
Sourced specifics are thin; the targeted searches were cut off by the exhausted budget. What the gathered sources support:
- **Photo:** a frontal, neutral-expression, photographic (not stylized) portrait in ordinary lighting.
- **Video twin:**
  - About 15 s of phone footage for HeyGen Avatar V. Older twin flows wanted 2–5 minutes, or about 90 s of talking plus still and "listening" segments.
  - Be animated in the training footage, because the avatar copies your posture, tilts and stiffness.
- **Script:** neutral delivery at moderate speed, without jargon or big emotional swings. Long or emotional scripts expose dead eyes, and fast speech breaks lip sync.
- **Length limits per generation:** OmniHuman takes up to 30 s of audio per call and MultiTalk caps at 15 s. InfiniteTalk and HeyGen are built for longer clips. A 45–60 s clip on OmniHuman therefore needs 2–3 segments.
- **Audio:** clean audio fed correctly into the model; in ComfyUI, the way audio is loaded changes sync quality. Synthetic cloned voices are the most-reported giveaway.
- **Re-dubbing real footage:** mouth-only lip-sync models such as LatentSync can put new words into real footage.

### Cited Findings
- **Photo:** frontal portraits with neutral expressions work best for single-photo animation (D-ID); side angles, unusual lighting or stylised images expose weaknesses. — [Resident](https://resident.com/technology-and-digital-resources/2026/05/21/5-most-realistic-ai-avatar-tools-in-2026); [Zoice](https://zoice.com/blog/best-ai-avatar-generator-from-photo/) (per-page attribution uncertain)
- OmniHuman 2.0 accepts only an image as the identity source, not a driving video. — [MindStudio](https://www.mindstudio.ai/blog/bytedance-omnihuman-2-avatar-video)
- **Twin footage:**
  - HeyGen Avatar V needs about 15 seconds of footage (a "15-second phone clip"). — [The Planet Tools](https://theplanettools.ai/blog/heygen-avatar-v-tested-hands-on-review-2026); [Stork.ai](https://www.stork.ai/blog/this-ai-avatar-just-stole-a-youtubers-job); [Segmind](https://www.segmind.com/models/heygen-avatar-v)
  - Earlier HeyGen custom avatars used 2–5 minutes of self-shot footage. — [Resident](https://resident.com/technology-and-digital-resources/2026/05/21/5-most-realistic-ai-avatar-tools-in-2026) (attribution uncertain)
  - Globe and Mail [OLD]: about 90 s of talking plus sitting still and active-listening gestures. — [Globe and Mail](https://www.theglobeandmail.com/business/article-digital-clone-ai-avatar-meeting-efficiency/)
- The twin copies posture and head tilts. — [brisk.vision](https://lucijatomsic.substack.com/p/avatar). It inherits the creator's on-camera stiffness. — [Smart Remote Gigs/Capterra](https://smartremotegigs.com/software/heygen/)
- Reviewers agree output quality depends heavily on the source recording and the script. [synthesis of hands-on accounts] — [brisk.vision](https://lucijatomsic.substack.com/p/avatar); [PJIRC](https://pjirc.com/t/heygen-ai-review-realistic-ai-avatars-or-not/2288); [Smart Remote Gigs](https://smartremotegigs.com/software/heygen/)
- **Script:** neutral content holds up; long or emotional scripts produce "dead" eyes; fast speech or jargon breaks lip sync. — [PJIRC](https://pjirc.com/t/heygen-ai-review-realistic-ai-avatars-or-not/2288)
- **Clip-length limits:**
  - OmniHuman on fal has a 30-second maximum audio length. Its hosted workflow is "best treated as a short-clip model: one audio file, up to about 30 seconds". — [fal OmniHuman](https://fal.ai/models/fal-ai/bytedance/omnihuman); [Z.Tools](https://z.tools/blog/ai-talking-head-video-models)
  - MultiTalk "is a sprinter, not a marathon runner. The model has a hard cap at 15 sec of video." — [Zanno.se](https://zanno.se/lets-talk-multitalk-infinitetalk-wan-s2v/)
  - InfiniteTalk's rolling 81-frame context window targets extended sequences. — [InfiniteTalk README mirror](https://huggingface.co/spaces/kyboface/MyInfiniteTal/blob/main/README.md)
- **Audio handling (open-source):** with MultiTalk, feeding audio by file path gave muffled sound and poor lip sync, while the node's direct audio_upload widget gave "crystal-clear audio and far more accurate lip-sync". — [Zanno.se](https://zanno.se/lets-talk-multitalk-infinitetalk-wan-s2v/)
- **Voice:** in at least one hands-on test, the cloned voice was the least convincing element. — [brisk.vision](https://lucijatomsic.substack.com/p/avatar). The leading cloned-voice TTS on AA's arena was HeyGen Voice as of 9 Oct 2026, ahead of Qwen-Audio-3.1-TTS-Plus and ElevenLabs Eleven v4 Turbo. — [AA on X](https://x.com/ArtificialAnlys/status/2108608255387935199)
- **Post-production / re-dub path:** LatentSync is recommended for editing words into an existing video because it changes only the mouth. — [Fuser](https://fuser.studio/articles/best-ai-lip-sync-tools)
- **Output resolution and cost:**
  - Hedra's Character-3 API is priced in 540p, 720p and 1080p tiers. — [Magic Hour Hedra guide](https://magichour.ai/blog/guide-to-hedra-ai)
  - HeyGen's API charges more for 4K than 720p/1080p ($4 vs $3 per minute for a photo avatar). — [Magic Hour HeyGen pricing](https://magichour.ai/blog/heygen-pricing)

### Inferences
- A concrete input kit the report can recommend. This is inference stitched from the findings above, not a single source's checklist:
  - **(a) Photo:** a recent, sharp, front-facing head-and-shoulders photo; neutral or relaxed expression; even soft light on the face; plain background; no stylisation or filters.
  - **(b) Video (for an Avatar V–type twin):** at least 15 s, ideally 30–60 s, of the user talking naturally to a phone camera at eye level. Use steady framing and good light, and keep normal head movement and expression, since the twin copies stiffness.
  - **(c) Audio:** the user's own voice reading the 45–60 s script in a quiet, soft-furnished room, recorded at a natural, unhurried pace, with no music, saved as WAV or high-bitrate audio.
  - **(d) Script:** plain conversational language without jargon and with moderate emotion, broken into 2–4 sentence chunks so it can be split into segments of 30 s or less if needed.
- Re-dub alternative: record a real selfie video, then lip-sync only the mouth to new audio (LatentSync-style). This probably gives the most realistic look because head motion, eyes and skin stay real. But it is less of an "AI made me" test and needs the user to film themselves anyway.
- For OmniHuman (fal), splitting at sentence boundaries into 2–3 calls and joining with hard cuts or a slight zoom change between segments is a common way to hide joins. This is an inference; no source in these notes documents it.

### Gaps
- No sourced specifics were retrieved on: minimum photo resolution; mouth open versus closed or smiling with teeth; glasses, hair over the face or earrings; background complexity; shooting distance and focal length; lighting setups; HeyGen's official Avatar V recording guidelines (the help-center page was unreachable); consent or verification video requirements for twins of real people; or how many seconds of reference audio voice cloning needs.
- Microphone and room recommendations, ElevenLabs instant versus professional cloning requirements, and the trade-off between own recording and cloned TTS were not searched (budget exhausted).
- Post-processing practices were not retrieved: upscaling (for example Topaz or other AI upscalers), adding grain or background blur, B-roll cut-aways.

## 6. End-to-end pipelines practitioners use, and which can be fully automated via HTTP APIs (no GPU, budget under $30)

### Takeaway
Every top-tier option can be driven by HTTP API with a key and no local GPU:
- **HeyGen's own API.** A pay-as-you-go wallet with a $5 minimum, separate from web plans. An Avatar IV photo avatar costs about $3/min and a digital twin about $4/min, billed per second.
- **HeyGen Avatar V through fal.ai and Segmind.** Includes a reported one-shot "create a twin from a 15-second video_url" endpoint.
- **fal.ai.** Kling AI Avatar v2 Standard ($0.0562/s) and Pro ($0.115/s); OmniHuman v1 ($0.14/s, 30 s cap) and 1.5 ($0.16/s).
- **BytePlus.** OmniHuman 2.0 at $0.07/s, launched 15 Oct 2026, with region availability unclear.
- **Atlas Cloud.** OmniHuman 2 at $0.056/s and InfiniteTalk at $0.06/s.
- **WaveSpeed.** InfiniteTalk and OmniHuman.
- **Hedra's API.** A prepaid wallet with no free tier; Character-3 at about $0.05/s for 720p.

The typical pipeline is: get audio (own recording, or a cloned-voice TTS), then call an audio-driven avatar API, then optionally join segments and upscale. A 60 s clip costs roughly $2.50–$9.60 per attempt depending on the model, so $30 covers several attempts or a two- or three-tool bake-off. Web subscriptions ($29–30/month) would use the whole budget on one tool.

### Cited Findings
**HeyGen API** (third-party pricing summaries; HeyGen's own pricing page was not reached)
- Moved to pay-as-you-go in early 2026, using a prepaid USD wallet with a $5 minimum that is separate from web-plan credits. — [Magic Hour](https://magichour.ai/blog/heygen-pricing) [VENDOR-competitor]; [Anam](https://anam.ai/blog/heygen-pricing) [VENDOR-competitor]; [Spatius](https://www.spatius.ai/blog/heygen-pricing-2026/); [DIY AI](https://diyai.io/ai-tools/video-generation/heygen-pricing/); [CrixPix ("Verified Sept" 2026)](https://crixpix.com/heygen-pricing/)
- Per-minute rates: Avatar IV Photo Avatar $3/min at 720p/1080p and $4/min at 4K; Digital Twin and Studio Avatar $4/min at 720p/1080p and $5/min at 4K. — [Magic Hour](https://magichour.ai/blog/heygen-pricing); [Nemo Video](https://www.nemovideo.com/blog/heygen-pricing); [CrixPix](https://crixpix.com/heygen-pricing/)
- Charges accrue per second generated. Funds expire after 12 months. Self-serve accounts can run up to 10 jobs at once. Free API credits ended in Feb 2026. — [Sume](https://sume.com/blog/heygen-api-pricing); [Spatius](https://www.spatius.ai/blog/heygen-pricing-2026/); [CrixPix](https://crixpix.com/heygen-pricing/) (per-claim attribution within this set uncertain)
- Outlier: one source lists $2.31/min with no explanation. — [Sume](https://sume.com/blog/heygen-api-pricing)
- HeyGen's own comparison blog lists Avatar V API access at $0.05 per second, which matches $3/min. — [HeyGen blog: Photo vs Digital Twin vs Avatar V](https://www.heygen.com/blog/photo-avatar-vs-digital-twin-vs-avatar-v-vs-instant-avatar) [VENDOR]
- On fal.ai, the Avatar V endpoint `fal-ai/heygen/avatar5/digital-twin` takes an avatar ID plus a script and returns a finished video. — [fal HeyGen Avatar](https://fal.ai/heygen-avatar) [RESELLER]
- Segmind lists a companion `heygen-avatar-v-create` endpoint that trains a twin from a 15-second reference clip in one shot via `video_url`. Not confirmed against HeyGen's official docs. — [Segmind](https://www.segmind.com/models/heygen-avatar-v) [RESELLER]
- HeyGen web plans start around $29/month. — [Omid Saffari](https://omidsaffari.com/blog/heygen-pricing); [The Planet Tools](https://theplanettools.ai/blog/heygen-avatar-v-tested-hands-on-review-2026)

**fal.ai** [RESELLER]
- Kling AI Avatar v2 is $0.0562/s (Standard) and $0.115/s (Pro). — [fal Standard](https://fal.ai/models/fal-ai/kling-video/ai-avatar/v2/standard); [fal Pro](https://fal.ai/models/fal-ai/kling-video/ai-avatar/v2/pro). A third-party calculator lists Standard at $0.042/s in Oct 2026. — [CostGoat](https://costgoat.com/pricing/kling)
- OmniHuman (v1) is $0.14/s with a 30 s maximum audio length. — [fal OmniHuman](https://fal.ai/models/fal-ai/bytedance/omnihuman). OmniHuman 1.5 is $0.16/s. — [fal OmniHuman 1.5 guide](https://fal.ai/learn/devs/omnihuman-15-user-guide). Docs: [fal OmniHuman API reference](https://fal.ai/docs/model-api-reference/video-generation-api/bytedance-omnihuman)
- fal keeps a curated "best avatar models" page. — [fal Explore](https://fal.ai/explore/best-avatar-models)

**OmniHuman 2.0**
- Official BytePlus API at $0.07/s, live 15 Oct 2026. — [BytePlus](https://www.byteplus.com/en/product/OmniHuman); [Supermaker](https://supermaker.ai/blog/omnihuman-2-0-launch/)
- Region-locked at launch. — [MindStudio](https://www.mindstudio.ai/blog/bytedance-omnihuman-2-avatar-video)
- Atlas Cloud lists it at $0.056/s, against OmniHuman 1.5 at $0.12/s, and InfiniteTalk at $0.06/s. Its blog walks through a talking-head channel pipeline driven by Claude Opus 5.5 and a "Remix skill" (vendor tutorial). — [Atlas Cloud](https://www.atlascloud.ai/blog/tips/omnihuman-2-talking-head-ip-system) [RESELLER]
- Older-model resale prices: AIML API $0.182/s and WaveSpeed $0.12/s for OmniHuman (pre-2.0). — [AIML API](https://aimlapi.com/models/bytedance-omnihuman); [WaveSpeed](https://wavespeed.ai/models/bytedance/avatar-omni-human)

**InfiniteTalk (hosted)**
- WaveSpeed lists it at "$0.15+ per 5 sec". — [WaveSpeed avatar/lipsync collection](https://wavespeed.ai/collections/avatar-lipsync); [MindStudio model page](https://www.mindstudio.ai/models/wavespeed-ai-infinitetalk) [RESELLER]

**Hedra API**
- Billed from a prepaid dollar wallet separate from studio credits, with no free API tier. One source says generations made through MCP draw on studio credits instead. Which page made which claim is uncertain. — [DailyAIFixs](https://dailyaifixs.com/blog/hedra-pricing-2026-credits-burn-by-the-second); [Heyper AI](https://heyperai.com/blog/hedra-pricing)
- Character-3 API rates: $0.025/s at 540p, $0.05/s at 720p, $0.0625/s at 1080p. Sources broadly agree but were captured on different dates. — [Magic Hour](https://magichour.ai/blog/guide-to-hedra-ai) [VENDOR-competitor]; [Lokesh Kapoor](https://lokeshkapoor.com/blog/hedra-pricing)
- Studio plans: Basic $15/month (1,500 credits), Creator $30/month (5,400), Professional $75/month (14,400). Character-3 reportedly uses 3–6 credits per second depending on resolution. Attribution uncertain. — [Heyper AI](https://heyperai.com/blog/hedra-pricing); [DailyAIFixs](https://dailyaifixs.com/blog/hedra-pricing-2026-credits-burn-by-the-second)
- Conflict: one comparison lists Hedra API access as absent. — [LipSync.com](https://lipsync.com/compare/heygen-vs-hedra)

**Other API notes**
- VEED's "Best Lip-Sync API" page promotes its own Fabric 1.0 model, which implies API access (not verified). [VENDOR] — [VEED](https://www.veed.io/learn/best-lipsync-api)
- D-ID web plans start around $5.90/month; API pricing was not retrieved. — [Resident](https://resident.com/technology-and-digital-resources/2026/05/21/5-most-realistic-ai-avatar-tools-in-2026)
- Open-weight models need a GPU to self-host and are out of scope for a no-GPU sandbox unless hosted: InfiniteTalk, MultiTalk, LongCat-Video-Avatar 1.5, daVinci-MagiHuman, LatentSync, MuseTalk, Wav2Lip, Avaturn AVTR-1. InfiniteTalk is hosted by WaveSpeed and Atlas Cloud, and LatentSync is available inside Fuser. — [Spheron](https://www.spheron.network/blog/self-host-ai-avatar-generator-heygen-alternative-2026/); [Atlas Cloud](https://www.atlascloud.ai/blog/tips/omnihuman-2-talking-head-ip-system); [Fuser](https://fuser.studio/articles/best-ai-lip-sync-tools)

### Inferences
**Per-attempt cost for 60 s of output**, computed from the cited per-second prices (not quoted by any source):

| Model and host | Cost per 60 s attempt |
|---|---|
| Kling AI Avatar v2 Standard (fal) | $2.52–3.37 |
| Kling AI Avatar v2 Pro (fal) | $6.90 |
| OmniHuman 2.0 | $4.20 (BytePlus) / $3.36 (Atlas) |
| OmniHuman 1.5 (fal) | $9.60, plus at least 2 calls because of the 30 s cap |
| InfiniteTalk (Atlas) | $3.60 |
| Hedra Character-3 | $3.00 (720p) / $3.75 (1080p) |
| HeyGen API photo avatar (Avatar IV) | about $3.00 |
| HeyGen API digital twin / Avatar V | $3.00–4.00, with a $5 wallet minimum |

Under $30, a sensible plan is one HeyGen route plus one or two fal or Atlas routes, with one or two retakes each.

Candidate fully automatable pipelines (curl or Python, key in an environment variable):
- **Path A, highest consensus realism with a short selfie video:** upload the selfie clip, create an Avatar V twin (Segmind create endpoint or HeyGen API), then generate with the user's own recorded audio (or a script plus voice) and download the MP4.
- **Path B, one photo:** take the photo plus the user's own recorded audio. Call Kling AI Avatar v2 (fal) and/or OmniHuman 2.0 (BytePlus or Atlas) and/or HeyGen Avatar IV photo avatar (HeyGen API). For 30 s-capped models, split the audio into ≤30 s chunks, then join the pieces with ffmpeg in the sandbox (CPU only).

Recording the user's own voice avoids the voice-clone weak spot. It also removes a paid TTS step and keeps the "sounds like me" goal intact.

Web-only subscriptions (HeyGen Creator about $29/month, Hedra Creator $30/month) would consume the whole budget on a single tool and are not agent-friendly. API pay-as-you-go fits the constraints better.

### Gaps
- Whether HeyGen's own public API exposes Avatar V twin creation from an uploaded video (versus only via fal or Segmind), and whether it requires a consent or verification recording of the user. Not retrieved, but critical for an agent-driven flow.
- Whether BytePlus OmniHuman 2.0 can be used by a US individual account (region lock at launch).
- Whether fal or Segmind pass through HeyGen's consent requirements for real-person twins.
- Voice-clone API costs and requirements (ElevenLabs, HeyGen Voice via API) were not retrieved.
- Max output duration per call for Kling AI Avatar v2 and HeyGen photo avatars was not retrieved.
- No source documented an upscaling step (API-based upscalers and their prices) for talking-head output.
- All prices come from third-party snippets captured on different dates; confirm them on the live pricing pages before running.
