# Consent, privacy, data retention, legal and personal-security issues of making a talking AI replica of yourself (US, as of October 2026, with EU notes)

> **How this was researched (read first).** Compiled Oct 23, 2026. WebFetch could not resolve any host, and the session proxy refused direct connections to vendor, government and news sites. So **no primary page was opened directly**. Every finding below comes from search-engine result summaries and snippets of the linked pages: 36 searches before the shared search budget ran out. Quoted wording is as it appeared in those snippets, so spot-check it against the live page before the report quotes it. Tags: **[P]** = primary source (statute or bill text, government page, the vendor's own policy or docs); **[S]** = secondary (law-firm alert, news, third-party policy analysis, blog). "Possibly outdated" = dated before about April 2026, more than about 6 months old. This is not legal advice.

## 1. What the main vendors require before you can create a likeness of yourself: consent videos, ID or liveness checks, voice captchas, still photos, web app vs API

### Takeaway
Products that build a "digital twin" or replica from video gate creation behind a recorded, spoken consent statement or passcode. That covers HeyGen digital twins, Tavus personal replicas, D-ID V3 Instant Avatars and Synthesia custom avatars. ElevenLabs' Professional Voice Clone requires a read-aloud "voice captcha". No source found in this research describes a government-ID or KYC check for individual self-cloning users.

The single-photo routes most relevant to this experiment rely on policy or Terms of Service attestations, not technical verification: HeyGen "photo" avatars via API, Tavus image-based replicas, Hedra, Dreamina/OmniHuman and the Captions/Mirage AI Twin. Instant voice clones at ElevenLabs needed only a checkbox in Consumer Reports' March 2025 test. Sora cameos are no longer available: the Sora app shut down in April 2026.

### Cited Findings

#### HeyGen (developer docs and help center; page dates not captured, so check the live pages)
- [P] The API docs require consent only for "digital twin" avatars: "Photo avatars (type: "photo") and prompt-to-avatar characters (type: "prompt") depict no real, identifiable person and do not require consent." — [HeyGen developer docs: Avatar consent](https://developers.heygen.com/docs/avatar-consent)
- [P] Default API flow: the person being cloned records a consent statement by webcam on a page HeyGen hosts. Uploading a pre-recorded consent video is limited to whitelisted enterprise accounts ("contact sales"). Consent collection is waived for accounts that have signed an indemnity agreement. — [HeyGen developer docs](https://developers.heygen.com/docs/avatar-consent)
- [P] The API checks the consent statement "semantically", so small differences in wording are accepted. — [HeyGen developer docs](https://developers.heygen.com/docs/avatar-consent)
- [P] The web app help center gives stricter rules:
  - read the provided script exactly as written;
  - keep the consent video under 30 seconds;
  - the person on camera must match the avatar footage;
  - record and submit the consent video at the same time as the avatar training footage.
  — [HeyGen Help Center, article 12092609](https://help.heygen.com/en/articles/12092609)
- [S] The two HeyGen sources conflict: semantic check in the developer docs versus exact script in the help center. — [HeyGen developer docs](https://developers.heygen.com/docs/avatar-consent); [HeyGen Help Center](https://help.heygen.com/en/articles/12092609)
- [S] Wikipedia describes an older flow: verbal consent plus a spoken password. This probably predates the current process. — [Wikipedia: HeyGen](https://en.wikipedia.org/wiki/HeyGen)
- [P] HeyGen also has a blog post on consent and brand controls, but no details from it surfaced. — [HeyGen blog](https://www.heygen.com/blog/ai-avatar-consent-brand-controls)

#### ElevenLabs
- [P] Professional Voice Clone (PVC): "Before training can begin, a verification step is required to ensure you have permission to use the voice." The flow works through the API:
  - you request a captcha, which returns an image with several lines of text;
  - the voice owner reads the text aloud and records it;
  - the recording is submitted to a verify endpoint.

  Manual verification through support is a slower fallback, for example when the voice owner is visually impaired. Page date not captured. — [ElevenLabs PVC quickstart](https://elevenlabs.io/docs/eleven-api/guides/how-to/voices/professional-voice-cloning)
- [S] Instant voice cloning, from Consumer Reports' study published March 2025 (possibly outdated):
  - ElevenLabs, Speechify, PlayHT and Lovo required only a checkbox confirming the user had the legal right to clone the voice;
  - Descript required the user to read and record a consent statement;
  - Resemble AI required the first clone to be made from audio recorded in real time.

  — [Consumer Reports Innovation Lab](https://innovation.consumerreports.org/new-report-do-these-6-ai-voice-cloning-companies-do-enough-to-prevent-misuse/); [CO/AI summary](https://getcoai.com/news/ai-voice-cloning-risks-exposed-by-consumer-reports-descript-more-secure-than-elevenlabs/); [The Register, Mar 10 2025](https://www.theregister.com/2025/03/10/ai_voice_cloning_safeguards/)
- [S] For four of the six products, CR researchers could "easily create" a voice clone from publicly available audio. — [Axios, Mar 15 2025](https://www.axios.com/2025/03/15/ai-voice-cloning-consumer-scams)
- [S] Coverage of the study differs on the count. CR says four of six lacked meaningful safeguards. TechCrunch reports that only two, Descript and Resemble AI, took steps against misuse. — [CR](https://innovation.consumerreports.org/new-report-do-these-6-ai-voice-cloning-companies-do-enough-to-prevent-misuse/); [TechCrunch](https://techcrunch.com/?p=2977855)

#### Hedra
- [P] Acceptable Use Policy (version dated July 31, 2024; possibly outdated):
  - users may not create output containing personal information about anyone other than themselves, including photos, videos or other media of other people;
  - the one exception is people who died at least 100 years ago;
  - users may not impersonate real entities or create fake personas (deepfakes) to mislead without consent or legal right;
  - violations can lead to suspension or termination.

  The current, unversioned AUP page leaves out the 100-year exception. — [Hedra AUP 2024-07-31 (PDF)](https://hedra.com/legal/acceptable_use_2024_07_31.pdf); [Hedra AUP (current page)](https://www.hedra.com/acceptable-use)
- No consent video, liveness check or ID check for Hedra appeared in any search result. This is absence of evidence, not proof.

#### D-ID
- [P] API "V3 Instant Avatars" require consent verification. The system issues a passcode script that the person reads aloud on video, and the consent window closes after 30 minutes. The avatar can be created only after the consent status shows as completed. Page date not captured. — [D-ID docs: V3 Instant Avatars](https://docs.d-id.com/docs/v3-instant-avatars)
- [S] In a case study it submitted itself, D-ID says it obtained the families' consent before using the likenesses of deceased domestic-violence victims in an awareness video. — [Partnership on AI case study](https://partnershiponai.org/d-id-framework-case-study/)

#### Synthesia
- [S] Personal avatar flow, from a 2024 Decrypt review (possibly outdated):
  - before generation, the user consents to the collection, use, storage and disclosure of their video and audio recordings, "to authenticate" the avatar submission;
  - requests are screened before anything is generated;
  - Synthesia's Alexandru Voica said the company will never create an AI avatar without someone's clear consent.

  — [Decrypt](https://decrypt.co/243795/ai-video-avatars-synthesia-review)
- [P, via search summary only] Synthesia's help article on photo avatars reportedly requires a recorded consent video for photo avatars. Not independently verified. — [Synthesia Help: Photo avatars content moderation](https://help.synthesia.io/en/articles/13846500-photo-avatars-content-moderation)
- [S] A third-party reading of Synthesia's Terms of Service says the customer is contractually responsible for getting "free and informed consent" from anyone whose voice or likeness is used for a Custom Avatar. — [ConductAtlas: Synthesia ToS](https://conductatlas.com/platform/synthesia/synthesia-terms-of-service/custom-avatar-consent-requirement/)
- No source describing a formal KYC or government-ID check for Synthesia personal avatars was found. — [Decrypt](https://decrypt.co/243795/ai-video-avatars-synthesia-review)

#### Tavus (docs; page dates not captured)
- [P] A personal replica made from real footage needs a verbal consent statement spoken by the person being cloned. It goes at the start of the training video, or in a separate consent video. It must use the exact statement shown on the platform. Training videos without it are not processed. — [Tavus docs: Consent statement](https://docs.tavus.io/sections/troubleshooting/consent-statement); [Tavus API: Create replica](https://docs.tavus.io/api-reference/phoenix-replica-model/create-replica.md); [Tavus: Replica training](https://docs.tavus.io/sections/replica/replica-training)
- [P] No consent video is needed for a synthetic (AI-generated) training video or for a replica built from an uploaded image. Replicas of famous or deceased people are allowed only from fully synthetic footage; real footage of those people is not permitted. — [Tavus: Replica training](https://docs.tavus.io/sections/replica/replica-training); [Tavus: Personal replicas](https://docs.tavus.io/sections/replicas/personal-replicas)
- [P] Recording specs:
  - one continuous shot: about 1 minute of talking and about 1 minute of silence after the statement;
  - at least 25 fps;
  - mp4 (H.264 video, AAC audio) or webm;
  - 750 MB maximum;
  - minimum resolution: the docs conflict (1080p on one page, 720p on another).

  — [Tavus: Replica training](https://docs.tavus.io/sections/replica/replica-training); [Tavus Replica FAQs](https://docs.tavus.io/sections/replica/replica-faqs)

#### Captions (renamed Mirage)
- [S] Captions has been renamed Mirage (reported Sept 2025). — [Design Compass, Sept 25 2025](https://designcompass.org/2025/09/25/mirage-dream-like-ai-video-tool/)
- [P] AI Twin flow in the help docs:
  - take a selfie, choose a voice, and pick from generated variants;
  - no consent step is mentioned;
  - available on Pro, Max and Scale plans, on iOS;
  - up to 30 AI Twins;
  - delete one with "Delete actor".

  — [Captions help: AI Twin](https://captions.ai/help/docs/project/ai-twin.md); [Captions help (Portuguese)](https://captions.ai/help/docs/pt/project/ai-twin.md)
- [P] Moderation: content that violates the policies "may be blocked, removed, or prevented from being generated". Suspected violations go to hello@captions.ai. — [Mirage moderation](https://captions.ai/help/mirage/account-management/mirage-moderation)

#### ByteDance (Dreamina / OmniHuman / CapCut)
- [P, marketing pages] Dreamina's OmniHuman pages:
  - an avatar can be made from "a script and a photo";
  - the user can upload an image of themselves, or an AI image from Seedream 4.5, plus a voice recording;
  - the upload can be a portrait, upper-body or full-body image of a "human, animal, or animated character".

  None of these pages mention a consent step, ID verification or a "yourself only" rule. — [Dreamina: OmniHuman AI](https://dreamina.capcut.com/resource/omnihuman-ai); [Dreamina AI human generator (Spanish)](https://dreamina.capcut.com/es-es/tools/ai-human-generator); [Dreamina VTuber AI](https://dreamina.capcut.com/resource/vtuber-ai)
- [P] Dreamina is served from a CapCut subdomain (dreamina.capcut.com), so it sits inside the CapCut web platform. — [Dreamina](https://dreamina.capcut.com/resource/omnihuman-ai)

#### Kling (Kuaishou)
- No consent or verification process was found (see Gaps).

#### Runway
- [S] Third-party summaries of Runway's Usage and Content policies say:
  - users may not use any image, video or audio of a real person, as input or in output, without that person's permission;
  - permission must be affirmative (failing to object is not enough);
  - the policy doesn't say what form the permission must take;
  - violations can lead to suspension;
  - the rule applies whether or not the output is shared publicly.

  No verification step specific to Act-Two was found. — [ConductAtlas: Runway real-person likeness](https://conductatlas.com/platform/runway/runway-usage-policy/prohibition-on-real-person-likeness-without-permission/); [ConductAtlas: personal media](https://conductatlas.com/platform/runway/runway-usage-policy/provision/CA-P-060865/prohibition-on-unauthorized-use-of-personal-media/); [ConductAtlas: another person's image/video/audio](https://conductatlas.com/platform/runway/runway-usage-policy/use-of-another-persons-image-video-or-audio-without-permission/)
- [S] For comparison, Pika's AUP requires express consent before uploading any real person's likeness. — [ConductAtlas: Pika AUP](https://conductatlas.com/platform/pika/pika-acceptable-use-policy/prohibition-on-uploading-photos-without-express-consent/)

#### OpenAI Sora cameos (discontinued)
- [S] At launch (Sept 30, 2025):
  - creating a cameo required a short video and audio recording made in the app, validated with audio challenges to prevent impersonation;
  - the owner chose who could use the cameo: only themselves, approved people, mutuals or everyone;
  - the owner could revoke access and delete videos featuring their likeness, including drafts made by others.

  — [VentureBeat](https://venturebeat.com/ai/openai-debuts-sora-2-ai-video-generator-app-with-sound-and-self-insertion); [Axios, Sept 30 2025](https://www.axios.com/2025/09/30/openai-sora-app-social-ai); [Zilliz FAQ](https://zilliz.com/ai-faq/how-does-the-cameo-feature-work-in-sora-2-and-what-controls-do-users-have-over-their-likeness)
- [S] "Character cameos" were for objects and animals only, not real people. — [eWeek](https://www.eweek.com/news/openai-sora-character-cameos/)
- [P] Current status: OpenAI announced the discontinuation on March 24, 2026. The Sora web and app experiences closed on April 26, 2026, and the Sora API was set to close on September 24, 2026. — [OpenAI Help Center: Sora discontinuation](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation?so=1); [The Decoder](https://the-decoder.com/openai-sets-two-stage-sora-shutdown-with-app-closing-april-2026-and-api-following-in-september/); [Engadget](https://engadget.com/ai/openai-is-shutting-down-its-sora-video-generation-app-211023358.html)

### Inferences
- **No verification on the one-photo routes.** The likely one-photo paths appear to involve no technical identity or consent verification, only a Terms of Service attestation. That covers HeyGen photo avatars via API, Hedra, Tavus image-based replicas, Dreamina/OmniHuman and the Captions/Mirage AI Twin. The user is unlikely to be asked for ID or a liveness check. The flip side: anyone with a photo of the user could do the same.
- **The selfie-video route adds a short consent recording.** At HeyGen, Tavus and D-ID it triggers a recorded consent statement or passcode, plus a face match against the training footage in HeyGen's web flow. This is trivial when the person being cloned is the user.
- **API vs web.** Self-serve API users should expect the same consent steps as the web app, not fewer. HeyGen's API keeps the consent requirement via its hosted webcam page; only enterprise accounts get uploaded consent videos or indemnity-based waivers. D-ID and Tavus enforce consent inside the API flow, and ElevenLabs exposes PVC verification as API endpoints.
- **Voice.** At ElevenLabs, the instant clone route historically needed only a checkbox, while the professional route needs a read-aloud captcha. Neither asked for ID in any source found.
- **Vendor consent checks don't stop others cloning you.** HeyGen's indemnity waiver for enterprise accounts, plus the unverified photo and instant-voice routes, mean these checks give limited protection against third parties making a clone of the user from public photos or audio.

### Gaps
- **ElevenLabs instant clones.** Couldn't check whether ElevenLabs has added a captcha or other verification for instant clones since CR's March 2025 test. The search budget ran out before this was done.
- **Missing verification details for several vendors:**
  - Kling: no source on consent or verification flows.
  - Dreamina/OmniHuman/CapCut: only marketing pages surfaced; no terms or community guidelines.
  - Runway: nothing specific to Act-Two.
  - D-ID: nothing on its classic photo-to-talking-head route, only the V3 Instant Avatars API.
- **HeyGen photo avatars.** Not confirmed whether HeyGen's web app applies moderation or face matching to photo avatars made from a real photo. The API doc's statement that photo avatars "depict no real, identifiable person" is odd and should be checked against the live page.
- **Hedra.** Only 2024 documents surfaced; any verification added in 2025–26 is unknown.
- **Synthesia photo avatars.** The consent-video requirement rests on a search summary only.
- **Sora 2 inside ChatGPT.** One secondary source in the results claimed the Sora 2 model is still available for a fee inside ChatGPT; this is unverified. Cameo creation was reportedly mobile-only (third-party guide; source not pinned down).
- **Page dates.** Dates for the HeyGen, ElevenLabs, Tavus, D-ID and Captions docs were not captured, so their current accuracy is unknown.

## 2. What vendors do with face and voice data: retention, training use, deletion, sharing, breaches, output ownership, data location

### Takeaway
Terms vary widely between vendors:

- **Synthesia:** deletes avatar, video and voice data within 90 days of a request and confirms in writing.
- **HeyGen:** its biometric notice reportedly destroys US users' face geometry once the purpose is met, or within 3 years of last interaction (per a third-party summary).
- **ElevenLabs:** offers a training opt-out toggle and CCPA deletion rights. Commentators read its Terms of Service as granting a perpetual, irrevocable license over voice models.
- **Hedra:** the consumer terms grant it a perpetual, irrevocable sublicense, and the API/enterprise terms let it train on customer content.
- **CapCut:** its June 2025 terms were widely read as a perpetual license covering face and voice that survives account deletion.

Two of the listed services have Chinese owners: Kling (Kuaishou) and Dreamina/OmniHuman/CapCut (ByteDance). HeyGen was founded in Shenzhen but is now headquartered in Los Angeles, and its Chinese investors sold their stakes.

### Cited Findings

#### HeyGen
- [P] Biometric Information Privacy Notice:
  - HeyGen mainly collects face geometry and may collect voiceprints;
  - collection happens only when a user creates a custom avatar;
  - the stated purpose is avatar creation;
  - consent is requested before collection.

  — [HeyGen Biometric Information Privacy Notice](https://www.heygen.com/biometric-privacy-notice)
- [S] Retention, from a third-party summary not checked against the notice:
  - EEA/UK/Swiss users: face geometry is kept while the associated avatar stays active;
  - US/Illinois users: destroyed once the purpose is met or within three years of last interaction, whichever comes first;
  - deletion on request.

  — [Waimakers HeyGen assessment](https://www.waimakers.com/en/resources/ai-data-security/heygen)
- [P/S] HeyGen's general privacy policy says it may use inputs to train its models. Per Waimakers, users outside Enterprise plans must contact support to opt out. — [HeyGen Privacy Policy](https://www.heygen.com/policy); [Waimakers](https://www.waimakers.com/en/resources/ai-data-security/heygen)
- [S] Corporate history:
  - founded in 2020 in Shenzhen as "Surreal", later renamed Movio;
  - moved its headquarters to Los Angeles in 2022, then rebranded as HeyGen;
  - founders: Joshua Xu and Wayne Liang.

  — [Wikipedia](https://en.wikipedia.org/wiki/HeyGen); [SCMP](https://scmp.com/tech/tech-trends/article/3267861/ai-start-heygen-raises-us60-million-after-pivoting-away-mainland-china-investors)
- [S] Chinese investors:
  - after scrutiny from US lawmakers, HeyGen asked its Chinese investors (IDG Capital, Baidu Ventures, HongShan, ZhenFund) to sell their shares to US firms;
  - HongShan gave up its board seat in November 2023;
  - a $60M Series A led by Benchmark followed in June 2024, at a valuation of $440M per The Information or $500M per SCMP/Bloomberg (conflicting);
  - HeyGen reportedly dissolved its Shenzhen entity.

  — [SCMP](https://scmp.com/tech/tech-trends/article/3267861/ai-start-heygen-raises-us60-million-after-pivoting-away-mainland-china-investors); [DealStreetAsia](https://dealstreetasia.com/stories/heygen-funding-401368); [The Decoder](https://the-decoder.com/ai-video-startup-heygen-raises-60-million-at-440-million-valuation/?amp=1)

#### ElevenLabs
- [P] CCPA Notice at Collection: users can ask for their personal information to be deleted, "including your account and the Voice Data associated with your account". Where applicable law provides for it, the user may instead request that personal information be anonymized rather than deleted. — [ElevenLabs CCPA Notice at Collection](https://elevenlabs.io/ccpa-notice-at-collection)
- [S] A third-party rating site quotes the privacy policy as saying:
  - users can "opt out of our use of your Personal Data for training at any time";
  - ElevenLabs will "not keep data it generates about your voice longer than 3 years after your last interaction".

  The same site flags that the policy gives no deletion timeline after an account is closed. — [VerifyWise: ElevenLabs](https://verifywise.ai/ai-trust-index/elevenlabs)
- [S] Training defaults, from a blog by Deepgram (a speech-AI vendor and potential competitor; its plan names may not match ElevenLabs' current tiers):
  - free and lower-tier users are opted in to training by default;
  - the opt-out toggle applies only going forward;
  - it does not stop security monitoring, analytics or metadata handling;
  - Enterprise is the reverse: training off by default, plus DPAs, BAAs and "Zero Retention Mode".

  — [Deepgram blog](https://deepgram.com/learn/how-elevenlabs-uses-your-audio-data)
- [S] The training opt-out sits in the "Data use" menu of the account settings. — [LicenseOrg guide](https://licenseorg.com/blog/elevenlabs-licensing-guide-ai-voices)
- [S] Terms of Service license, as read by secondary sources:
  - a "perpetual, irrevocable, non-exclusive, royalty-free, worldwide, sub-licensable" license covering creating a voice model and using it to provide and improve services;
  - a forum post quoting the terms says ElevenLabs may develop new services and products with user voice models;
  - ElevenLabs says it won't commercialize a user's voice on a standalone basis without permission.

  — [LicenseOrg](https://licenseorg.com/blog/elevenlabs-licensing-guide-ai-voices); [Terms.law](https://terms.law/ai-output-rights/elevenlabs/); [Creative COW forum](https://creativecow.net/forums/thread/elevenlabs-credits-ai-audio-sodftware/)
- [S] Unverified secondary claim: raw voice recordings are deleted after 3 years of inactivity, but models and derivatives made from them are kept permanently. This conflicts with the CCPA notice's deletion of "Voice Data". — [LicenseOrg: AI voice licensing](https://licenseorg.com/blog/ai-voice-licensing-elevenlabs)
- [S] Output ownership: paid-plan users generally get commercial rights to their output; the free tier does not. — [LicenseOrg](https://licenseorg.com/blog/elevenlabs-licensing-guide-ai-voices); [Terms.law](https://terms.law/ai-output-rights/elevenlabs/)
- [S] A governance analysis says the policy makes training use subject to account settings and to consent choices that vary by jurisdiction, and that the policy text alone can't show whether the consent mechanism is adequate. — [ConductAtlas: ElevenLabs privacy](https://conductatlas.com/platform/elevenlabs/elevenlabs-privacy-policy/voice-data-collection-and-ai-model-training/)

#### Hedra (2024 documents; possibly outdated)
- [P] Consumer Terms of Use: the user keeps ownership of their content but grants Hedra a "perpetual, irrevocable, royalty-free" sublicense, "subject to any applicable Account settings". Its stated purpose is operating and providing the Service "to you and to our other users". — [Hedra Terms of Use](https://hedra.com/terms)
- [P] API and enterprise terms: Hedra "is entitled to use Customer Content to provide and improve the Solution, including improving and training any algorithmic models", and may share content with third-party AI services as needed. — [Hedra API Terms](https://hedra.com/api-terms); [Hedra Enterprise API License](https://www.hedra.com/enterprise-lite-api-terms)
- [P] Privacy Policy (effective Oct 25, 2024): lists user-uploaded prompts, inputs and outputs as personal information. It directs residents of Illinois, Texas and Washington to a separate Biometric Data Privacy Policy. — [Hedra Privacy Policy 2024-10-25 (PDF)](https://www.hedra.com/legal/privacy_2024_10_25.pdf); [Hedra Privacy](https://www.hedra.com/privacy)

#### Synthesia
- [P] Deletion: avatar, video and voice data are "permanently" removed within 90 days of a deletion request, and Synthesia confirms in writing. If an account is terminated without a request, the data is deleted automatically within 90 days. — [Synthesia Help 9490158](https://help.synthesia.io/en/articles/9490158-what-is-the-time-frame-for-complete-deletion-of-an-avatar)
- [S] A third-party reading of the privacy policy says custom-avatar biometric data is kept for the life of the account unless the user asks for earlier deletion, and that no concrete retention period is given per data type. — [ConductAtlas: Synthesia retention](https://conductatlas.com/platform/synthesia/synthesia-privacy-policy/data-retention/); [ConductAtlas: Synthesia ToS deletion](https://conductatlas.com/platform/synthesia/synthesia-terms-of-service/data-portability-and-deletion/)
- [P] Avatars in a company workspace stay after the user leaves unless an owner or admin deletes them. — [Synthesia Help: Avatar policy foundation](https://help.synthesia.io/en/articles/15453102-avatar-policy-foundation)

#### D-ID
- No privacy or retention text surfaced (see Gaps).
- [P, background] An EU CORDIS project page describes D-ID's earlier technology as face-image privacy protection. It notes that the GDPR treats face images as sensitive personal information. — [CORDIS project 854762](https://cordis.europa.eu/project/id/854762/reporting/de)

#### Captions/Mirage
- [P] A twin can be deleted with "Delete actor". No retention or training terms surfaced. — [Captions help: AI Twin](https://captions.ai/help/docs/project/ai-twin.md)

#### OpenAI Sora
- [P] OpenAI's shutdown notice says that after the shutdown and any final export window, OpenAI "will permanently delete any data associated with your use of Sora". Users were told to export their content as soon as possible. If a final export window is offered, users will be notified by email. The surfaced excerpts don't say how cameos specifically were handled. — [OpenAI Help Center: Sora discontinuation](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation?so=1)

#### Kling (owned by Kuaishou)
- [P] The privacy policy was last updated April 21, 2026 (about 6 months old). It names Kling AI Pte. Ltd., a Singapore-registered entity, as the operator of the Kling apps and websites. — [Kling AI Privacy Policy](https://kling.ai/docs/privacy-policy)
- [S] Kling is owned by the Chinese company Kuaishou. — [VerifyWise: Kling AI](https://verifywise.ai/ai-trust-index/kling-ai); [ConductAtlas: Kling](https://conductatlas.com/platform/kling-ai/)
- [S] Third-party analyses conflict on biometrics. One says the face-reference and virtual try-on features process biometric and photographic data without any disclosed consent mechanism, retention limit or opt-out. Another rates Kling as not processing biometrics. — [ConductAtlas: Kling](https://conductatlas.com/platform/kling-ai/); [VerifyWise](https://verifywise.ai/ai-trust-index/kling-ai)
- [S] No retention period was found. Other claims from third-party reviews:
  - the policy references GDPR and CCPA;
  - data in transit is encrypted with HTTPS/TLS;
  - Kling does not sell personal information.

  One analysis suggests China's PIPL "may apply"; this is speculative. — [Zoftware analysis](https://zoftwarehub.com/en-bh/products/klingai/zoftware-analysis); [VerifyWise](https://verifywise.ai/ai-trust-index/kling-ai)

#### ByteDance: CapCut (and Dreamina, which is hosted on capcut.com)
- [S] CapCut's Terms of Service update of June 12, 2025 set off a viral backlash, including a TikTok video with more than 7 million views. Commentators read the new license as:
  - covering footage, audio and unpublished drafts;
  - reaching facial features and voice, usable in promotional material;
  - perpetual, and surviving account deletion;
  - accepted simply by using the app, with no opt-out.

  — [TechTrendsKE, June 19 2025](https://techtrendske.co.ke/2025/06/19/capcut-terms-of-service-concerns/); [2B Advice, July 4 2025](https://2b-advice.com/en/2025/07/04/capcut-trouble-over-new-terms-of-service-legal-risks-lurk-here/); [Techloy](https://www.techloy.com/capcuts-latest-terms-of-service-raises-big-questions-about-content-ownership/); [HelloPartner](https://hellopartner.com/claudia-sandino-capcuts-new-update-could-cost-creators-and-marketers-their-video-content-rights/)
- [S] Counterpoints:
  - TechRadar's headline framed the change as "all is well";
  - others note that TikTok, YouTube, Instagram and Adobe have similar clauses;
  - Podcastle, a competitor, says the terms never mention using voice beyond the service.

  — [TechRadar](https://www.techradar.com/pro/popular-video-editing-app-capcut-wants-to-use-any-content-you-produce-for-free-forever-heres-what-you-should-know); [Podcastle](https://podcastle.ai/blog/capcut-terms-of-service)

#### Runway
- No data-handling information surfaced (see Gaps).

#### Breaches involving these vendors
- No confirmed breach of face or voice data at the named vendors was found (details in Q3).

### Inferences
- **Deleting is not the same as revoking.** Hedra's consumer terms, and ElevenLabs' and CapCut's terms as commentators read them, grant perpetual, irrevocable licenses. Deleting an avatar or voice may remove the stored files without ending the vendor's license over content already submitted, or undoing models already trained.
- **Opt out before uploading.** If training opt-outs only apply going forward, as Deepgram says of ElevenLabs, they only help if set before the first upload.
- **Most concrete deletion commitment.** Of the vendors researched, Synthesia's public 90-day deletion with written confirmation is the most concrete. If HeyGen's 3-year outer limit for US users is accurate, face geometry could persist long after the experiment unless the user asks for deletion.
- **State of residence matters.** HeyGen and Hedra give specific biometric notices or terms to residents of Illinois, Texas and Washington, so the disclosures and consents the user sees depend on their state.
- **Chinese-owned services.** Kling (Kuaishou) and Dreamina/CapCut (ByteDance) are the two Chinese-owned options. Beyond Kling's Singapore operating entity, this research could not verify which entity contracts with US users, where their data is stored, or which law governs. The report should say so rather than speculate. HeyGen is now US-headquartered, and its Chinese investors sold their stakes in 2023–24.

### Gaps
- Retention periods, training use and output ownership for D-ID, Tavus, Captions/Mirage, Runway, Kling and Dreamina were not found.
- Unknown whether ElevenLabs' deletion also removes trained voice models, derived embeddings and backups. Also unknown whether its current 2026 Terms of Service still contain the perpetual-license wording, which is reported from early-2025 readings.
- Where CapCut/Dreamina store US users' data, and the current CapCut terms after June 2025, were not researched (budget).
- HeyGen's biometric notice retention clause was not read directly; it rests on the Waimakers summary.
- Output ownership terms for HeyGen, D-ID, Synthesia, Tavus, Captions, Kling, Runway and Dreamina were not captured.

## 3. Known incidents and controversies, 2024–2026: breaches, misuse, enforcement, lawsuits, policy changes

### Takeaway
The best-documented incidents involve misuse of other people's cloned voices. The main one is the January 2024 Biden robocall, made with ElevenLabs: it led to a $6M FCC fine for the consultant behind it and a $1M settlement by the phone carrier. The other main thread is lawsuits against companies that built voice models from recordings without valid consent:

- Lehrman v. Lovo (Southern District of New York, July 2025), where right-of-publicity claims were allowed to proceed;
- a wave of Illinois BIPA voice-training suits filed in May 2026, reportedly naming ElevenLabs among nine defendants.

Sora 2 went through likeness controversies in October 2025, then shut down in April 2026. Two Terms of Service controversies were about licenses over user voices and faces: ElevenLabs in early 2025 and CapCut in June 2025. No confirmed breach exposing users' face or voice data at the named vendors was found.

### Cited Findings
- [S] **Biden robocall (January 2024, New Hampshire primary).**
  - Consultant Steve Kramer hired a New Orleans magician, who made the recording with ElevenLabs; the magician said he didn't know Kramer's plans.
  - The FCC fined Kramer $6M in September 2024 under the Truth in Caller ID Act.
  - The carrier, Lingo Telecom, settled for $1M (the FCC had sought $2M) and agreed to caller-ID authentication commitments.
  - Kramer also faced 13 felony voter-suppression counts and 13 misdemeanor impersonation counts in New Hampshire.
  - No action against ElevenLabs was reported.

  — [Nextgov, Sept 2024](https://nextgov.com/artificial-intelligence/2024/09/mastermind-behind-biden-ai-robocalls-fined-6m-fcc/399857); [KSL/AP](https://www.ksl.com/article/news/business/company-that-sent-ai-calls-mimicking-joe-biden-to-voters-agrees-to-pay-1m-fine/51106394); [Boston Globe, Sept 26 2024](https://www.bostonglobe.com/2024/09/26/business/biden-robocalls-fcc-fine/); [Maginative](https://www.maginative.com/article/lingo-telecom-fined-1-million-for-biden-deepfake-robocall/)
- [S] **Lehrman v. Lovo (SDNY, Judge J. Paul Oetken, July 2025).**
  - Voice actors allege Lovo used recordings they made through Fiverr, which they were told were for internal or academic research, to sell AI voice clones.
  - Claims allowed to proceed: right of publicity under New York Civil Rights Law §§50–51, New York consumer protection, and breach of contract.
  - Dismissed: federal trademark claims, most copyright claims, and other common-law claims. The court reasoned that voices as abstract concepts are not copyrightable.
  - This was the motion-to-dismiss stage only, not a final ruling.

  — [Loeb & Loeb, July 2025](https://www.loeb.com/en/insights/publications/2025/07/lehrman-v-lovo-inc); [Volokh Conspiracy, July 10 2025](https://reason.com/volokh/2025/07/10/begun-the-clone-war-has-here-as-to-cloning-of-voice-over-actors-voices/); [Mondaq](https://www.mondaq.com/unitedstates/trademark/1655160/lehrman-v-lovo-inc)
- [S] **Illinois BIPA voice-training suits (May 2026).**
  - Illinois voice actors, podcasters and journalists filed suits in the Northern District of Illinois between May 13 and 19, 2026.
  - Reported defendants: Apple, Amazon, Meta, Microsoft, Nvidia, Samsung, Alphabet, Adobe and ElevenLabs.
  - They allege that voiceprints were extracted from their recordings to train AI voice models without consent or retention safeguards.
  - Plaintiffs' counsel is Loevy & Loevy. Defendants argue the plaintiffs show no concrete harm.
  - BIPA damages are reported at $1,000 per negligent violation and $5,000 per intentional or reckless violation.
  - No rulings on the merits were found.

  — [Bloomberg Law](https://news.bloomberglaw.com/ip-law/nvidia-sued-by-journalists-podcasters-over-ai-biometric-claims); [Loevy & Loevy](https://www.loevy.com/bipa-ai-class-action/); [Crypto Briefing](https://cryptobriefing.com/tech-giants-lawsuit-ai-voice-training-bipa/); [ZwillGen](https://zwillgen.com/litigation/old-statutes-new-targets-plaintiffs-using-existing-privacy-consumer-laws-against-ai-companies); [ABA Litigation newsletter](https://www.americanbar.org/groups/litigation/resources/newsletters/class-actions-derivative-suits/voiceprints-ai-bipa-new-trends-biometric-privacy-litigation/)
- [S] **Criticism of ElevenLabs.** Voice actors criticized ElevenLabs in January 2024, claiming it used samples of their voices without consent. Its Terms of Service license language caused controversy in early 2025, and the platform Kukarella reportedly ended its ElevenLabs partnership over it (secondary source). — [TechCrunch, Jan 22 2024](https://techcrunch.com/2024/01/22/voice-cloning-startup-elevenlabs-lands-80m-achieves-unicorn-status); [LicenseOrg](https://licenseorg.com/blog/elevenlabs-licensing-guide-ai-voices)
- [S] **Sora 2 likeness controversies (launched Sept 30, 2025).**
  - It launched letting celebrities opt out; after backlash, OpenAI switched to opt-in.
  - The Martin Luther King Jr. estate and OpenAI blocked videos of King.
  - Bryan Cranston's likeness was generated despite his opt-out. OpenAI and SAG-AFTRA issued a joint statement in which OpenAI expressed regret for "unintentional generations"; in October OpenAI blocked videos of living celebrities.
  - NewsGuard found Sora 2 produced realistic videos of false claims 80% of the time when asked.
  - Public Citizen urged OpenAI to take the tool offline.

  — [Tom's Guide](https://www.tomsguide.com/ai/openai-tightens-guardrails-around-celebrity-deepfakes-after-pressure-from-bryan-cranston-and-sag-aftra-heres-everything-you-need-to-know); [ITdaily](https://itdaily.com/news/security/openai-adjusts-sora-2-policy-deepfake); [Decrypt](https://decrypt.co/345296/sora-2-fabricate-convincing-deepfakes-on-command-study-finds?amp=1); [Common Dreams/Public Citizen](https://www.commondreams.org/news/openai-sora-public-citizen)
- [P/S] **Sora shutdown.** Announced March 24, 2026; the app closed April 26, 2026; the API closed September 24, 2026. A $1B Disney partnership announced in December 2025 collapsed. — [OpenAI Help Center](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation?so=1); [Engadget](https://engadget.com/ai/openai-is-shutting-down-its-sora-video-generation-app-211023358.html); [Hackernoon](https://hackernoon.com/openai-killed-sora-and-took-a-%241b-disney-deal-with-it-heres-the-lesson-for-ai-filmmakers?source=rss)
- [S] **Cutout.Pro breach (February 2024), an AI photo and video editing tool.**
  - About 20M users' emails, IP addresses, names and hashed, salted passwords leaked (5.93 GB of CSV files).
  - The company called the leak a "scam", but Troy Hunt and BleepingComputer validated the data.
  - No face or voice data was reported in the leak.

  — [Bitdefender](https://www.bitdefender.com/en-us/blog/hotforsecurity/hacker-leaks-records-of-20-million-users-of-ai-visual-creation-platform-online); [TechRadar](https://www.techradar.com/pro/security/top-ai-service-hit-by-massive-data-breach-20-million-cutoutpro-users-have-personal-info-leaked-so-change-passwords-now); [Hackread](https://www.hackread.com/hacker-cutout-pro-ai-tool-data-breach/)
- [S] **Synthesia breach listing (unverified).** A single breach-tracker entry lists Synthesia as a May 2025 breach victim, with the size unknown. No corroboration was found. — [Breachsense](https://www.breachsense.com/breaches/synthesia-data-breach/)
- [S] **FTC impersonation rule.**
  - The Government and Business Impersonation Rule took effect in April 2024, with civil penalties of up to $53,088 per violation and redress.
  - A February 2024 supplemental proposal would extend it to impersonation of individuals. It also asked whether AI platforms that knowingly enable impersonation should be liable.
  - The FTC filed five enforcement actions under the rule in its first year and runs "Operation AI Comply".
  - Whether the extension to individuals was ever finalized is not confirmed.

  — [The Record](https://therecord.media/ftc-crack-down-ai-impersonation); [Vixio](https://www.vixio.com/insights/pc-us-ftc-proposes-extending-ban-impersonation-scams); [FTC](https://www.ftc.gov/node/82618)
- [S] **FTC enforcement of the TAKE IT DOWN Act.**
  - May 20, 2026: warning letters to 12 "nudify" sites that appeared to lack a removal process.
  - Earlier, Chairman Ferguson wrote to large platforms: Alphabet, Amazon, Apple, Meta, Microsoft, Reddit, Snapchat, TikTok and X.

  — [JD Supra](https://www.jdsupra.com/legalnews/ftc-sends-warning-letters-to-companies-1534409/); [Fox 7 Austin](https://www.fox7austin.com/news/ftc-chairman-companies-take-down-act)
- [S] **Texas Attorney General biometric settlements under CUBI.**
  - Meta: $1.4B, July 2024.
  - Google: $1.375B, announced May 9, 2025 and executed Oct 31, 2025 per Bracewell. The claims included voiceprints and face geometry collected through Google Photos, Google Assistant and Nest Hub Max.

  — [Bracewell, Nov 10 2025](https://www.bracewell.com/resources/google-agrees-to-1-375-billion-settlement-as-texas-attorney-general-continues-data-privacy-push/); [CSLR](https://www.cslawreport.com/21169961/texas-ags-billiondollar-settlement-with-google-highlights-biometric-data-use-compliance-considerations.thtml)

### Inferences
- The Lovo case and the May 2026 BIPA suits target vendors that collect voices without valid consent or retention schedules. That puts vendors' retention and consent practices under active legal scrutiny. For a user cloning themselves with consent, the practical relevance is that vendors may change these practices, or be compelled to disclose them.
- Finding no confirmed face or voice breach at these vendors does not mean the risk is low. Breach reporting on small AI startups is thin, and the Cutout.Pro case shows account data at AI media services does leak.

### Gaps
- Outcome of the New Hampshire criminal case against Kramer, and whether he paid the FCC fine; not verified in this session.
- Whether ElevenLabs is definitely a named defendant in the May 2026 BIPA suits; reported by aggregators and not checked against court dockets. Case numbers were not captured.
- Status of Vacker v. ElevenLabs, the 2024 suit by audiobook narrators; not researched (budget).
- No FTC action against an AI avatar or voice-clone vendor was found. No BIPA suit over face geometry in an AI avatar product surfaced.
- Whether the Synthesia "breach" listing is genuine.

## 4. US law as of October 2026 on creating or holding a digital replica of yourself, plus EU AI Act Article 50; private experiment vs publishing or impersonating others

### Takeaway
None of the laws found makes it unlawful to privately create, keep or view a non-intimate talking replica of yourself that you consented to. The laws apply to other activities:

- **intimate deepfakes:** the federal TAKE IT DOWN Act; FTC enforcement of the platform 48-hour takedown duty began May 19, 2026;
- **using another person's voice or likeness without authorization, or tools built for that:** Tennessee's ELVIS Act, New York Civil Rights Law §§50–51, Illinois and California digital-replica laws;
- **how vendors handle biometric data:** Illinois BIPA (private lawsuits), Texas CUBI and Washington's RCW 19.375 (attorney-general enforcement);
- **AI voices in robocalls:** the FCC's February 2024 TCPA ruling;
- **labeling deepfakes that are published in the EU:** AI Act Article 50, in force since August 2, 2026.

The federal NO FAKES Act is not law. It was reintroduced in May 2026 and cleared the Senate Judiciary Committee on June 18, 2026, then stalled after Sen. Cruz objected on October 7, 2026.

### Cited Findings

#### TAKE IT DOWN Act (federal; enacted May 2025)
- [P/S] **Criminal provisions.** It is a federal crime to knowingly publish, through an interactive computer service, a "digital forgery" of an identifiable person without consent, where publication is meant to cause harm or does cause psychological, financial or reputational harm.
  - A "digital forgery" is an intimate visual depiction created or altered with software, machine learning, AI or other technology that a reasonable person would find indistinguishable from an authentic one.
  - The Act creates seven offenses, with penalties of up to 2 years in prison for adult victims and 3 years for minors.
  - The Act doesn't define "knowingly" or "publish".

  — [Enrolled bill S.146 (govinfo)](https://www.govinfo.gov/content/pkg/BILLS-119s146enr/html/BILLS-119s146enr.htm); [CRS Legal Sidebar LSB11314](https://www.everycrsreport.com/reports/LSB11314.html); [NAAG](https://naag.org/attorney-general-journal/congresss-attempt-to-criminalize-nonconsensual-intimate-imagery-the-benefits-and-potential-shortcomings-of-the-take-it-down-act)
- [S] **Platform duties.** Covered platforms had one year after enactment to set up a notice-and-removal process. They must post clear notice of it and remove reported content, plus known identical copies, within 48 hours of a valid request. FTC enforcement began May 19, 2026, with penalties of up to $53,088 per violation. — [Wiley alert](https://www.wiley.law/alert-May-19-Deadline-for-TAKE-IT-DOWN-Act-Compliance-Is-Your-Company-Prepared); [National Law Review](https://natlawreview.com/article/what-platforms-need-know-about-compliance-ftc-take-it-down-act); [JD Supra](https://www.jdsupra.com/legalnews/ftc-sends-warning-letters-to-companies-1534409/)

#### NO FAKES Act (federal bill, not enacted)
- [S] Reintroduced May 20, 2026 with revisions, including a counter-notice procedure for challenging takedowns. The search summary gave the bill numbers as S. 4591 / H.R. 8915; verify these on congress.gov. — [Manatt](https://manatt.com/insights/newsletters/client-alert/congress-reintroduces-the-no-fakes-act-what-s-new-in-the-2026-bill); [Digital Music News, May 20 2026](https://www.digitalmusicnews.com/2026/05/20/the-no-fakes-act-2026/); [RightsTech, May 2026](https://rightstech.com/2026/05/the-no-fakes-act-is-back-can-a-2026-version-pass-in-congress/)
- [P] The Senate Judiciary Committee advanced it unanimously on June 18, 2026. — [Sen. Blackburn press release, June 2026](https://www.blackburn.senate.gov/2026/6/blackburn-coons-bipartisan-bill-to-protect-individuals-and-creators-from-deepfakes-passes-senate-judiciary-committee); [LA Mag](https://lamag.com/general/the-no-fakes-act-passed-the-senate-judiciary-committee-paving-the-way-for-increased-protections-against-deepfakes/)
- [S] On October 7, 2026, Sen. Cruz objected to a unanimous-consent request, and the bill is reported "dead for now". A search summary attributes to a law-firm analysis that it is stalled until at least November; that source was not pinned down. — [Daily Journal](https://www.dailyjournal.com/article/395055-no-fakes-act-dead-for-now-as-cruz-objects-to-unanimous-consent-request)

#### Tennessee ELVIS Act (signed March 21, 2024; effective July 1, 2024)
- [S] The Act:
  - adds voice, whether actual or simulated, if readily identifiable, to Tennessee's Personal Rights Protection Act;
  - creates liability for publishing or making available someone's voice or likeness while knowing that person did not authorize it;
  - creates liability for distributing an algorithm, software or tool whose "primary purpose or function" is producing a person's photograph, voice or likeness without authorization;
  - keeps fair-use and First Amendment exceptions;
  - requires parental consent for minors and protects deceased people's voices.

  — [Latham & Watkins](https://www.lw.com/admin/upload/SiteAttachments/The-ELVIS-Act-Tennessee-Shakes-Up-Its-Right-of-Publicity-Law-and-Takes-On-Generative-AI.pdf); [Manatt](https://www.manatt.com/insights/newsletters/client-alert/tennessees-elvis-act-expands-publicity-rights-for); [Frankfurt Kurnit](https://advertisinglaw.fkks.com/post/102j3ju/tennessees-new-elvis-act-governs-use-of-persona-and-ai); [Proskauer](https://www.proskauer.com/blog/the-king-is-back-in-the-digital-era-the-elvis-act-generative-ai-and-right-of-publicity)

#### California AB 2602 and AB 1836 (signed Sept 17, 2024; effective Jan 1, 2025; possibly outdated)
- [S] AB 2602 adds Labor Code §927. It makes contract terms that let a digital replica stand in for work a person would otherwise do in person unenforceable under certain conditions. Law firms disagree on whether a specific description of uses and representation by a lawyer or union are both required.
- [S] AB 1836 gives estates control over deceased people's digital replicas for up to 70 years after death.
- [S] Both use the same definition of a digital replica: a computer-generated, highly realistic electronic representation readily identifiable as a person's voice or visual likeness.

  — [Perkins Coie](https://perkinscoie.com/insights/update/single-day-california-enacts-five-bills-tackling-digital-replicas-and-deepfakes); [Cozen O'Connor](https://www.cozen.com/news-resources/publications/2024/new-california-ai-laws-protect-against-unauthorized-use-of-ai-replicas); [Skadden (PDF)](https://www.skadden.com/-/media/files/publications/2024/09/california_enacts_host_of_airelated_bills_designed_to_protect_individuals.pdf); [Manatt](https://www.manatt.com/insights/newsletters/client-alert/california-enacts-a-host-of-new-ai-and-digital-rep)

#### New York
- [S/P] **Synthetic performer disclosure law** (S.8420-A/A.8887-B, amending General Business Law §396-b), signed Dec 11, 2025:
  - an ad must carry a conspicuous disclosure when the advertiser has actual knowledge that it uses a synthetic performer;
  - penalties: $1,000 for a first violation, $5,000 for each later one;
  - it excludes ads for expressive works and applies to ads distributed to New York audiences;
  - the governor's office announced in June 2026 that it is in effect.

  — [Cooley, Jan 29 2026](https://www.cooley.com/news/insight/2026/2026-01-29-new-york-enacts-synthetic-performer-disclosure-law-for-advertisements-including-those-using-generative-ai); [Loeb, Dec 2025](https://www.loeb.com/fr/insights/passle/2025/12/new-york-enacts-ai-advertising-disclosure-law-focused-on-synthetic-performers); [NY Governor](https://www.governor.ny.gov/news/governor-hochul-announces-first-nation-law-requiring-disclosure-when-advertisements-include-ai); [WBNG, June 10 2026](https://www.wbng.com/2026/06/10/hochul-says-first-in-the-nation-ai-ad-disclosure-law-is-now-effect/)
- [S] **Post-mortem companion law** (S.8391/A.8882): expands the post-mortem right of publicity in Civil Rights Law §50-f to cover digital replicas, so heirs or executors must consent. Effective immediately on Dec 11, 2025. — [Lowenstein Sandler](https://www.lowenstein.com/news-insights/publications/articles/new-york-legislation-requires-disclosure-on-ai-generated-performers-in-advertising-and-strengthens-post-mortem-publicity-rights-savare-sterba-tijani); [Skadden, Jan 2026](https://www.skadden.com/insights/publications/2026/01/two-newly-enacted-new-york-laws-will-regulate)
- [S] **Existing right of publicity.** New York Civil Rights Law §§50–51 bars unauthorized commercial use of a person's name, portrait, picture or voice. The court applied it to AI voice clones in Lehrman v. Lovo (July 2025). — [Loeb](https://www.loeb.com/en/insights/publications/2025/07/lehrman-v-lovo-inc)

#### Illinois
- [S] **BIPA** gives individuals a private right to sue, with statutory damages reported as $1,000 per negligent violation and $5,000 per intentional or reckless violation. — [ABA](https://www.americanbar.org/groups/litigation/resources/newsletters/class-actions-derivative-suits/voiceprints-ai-bipa-new-trends-biometric-privacy-litigation/); [Crypto Briefing](https://cryptobriefing.com/tech-giants-lawsuit-ai-voice-training-bipa/)
- [P] **Digital Voice and Likeness Protection Act** (HB 4762, Public Act 103-0830, Aug 9, 2024). A term in a personal or professional services agreement is unenforceable if all of these apply:
  - it allows a digital replica of the person's voice or likeness to replace work they would do in person;
  - it doesn't clearly define the intended uses;
  - the person had no counsel negotiating in writing and no union representation.

  It defines a digital replica as a newly created electronic representation of a real person's identity made with AI or other technology. — [ILGA bill status](https://www.ilga.gov/ftp/legislation/103/BillStatus/HTML/10300HB4762.html); [Public Act 103-0830](https://ilga.gov/Legislation/publicacts/view/103-0830)
- [S] **HB 4875** amends Illinois' Right of Publicity Act to cover unauthorized digital replicas, effective Jan 1, 2025 (from the search summary). — [Workplace Privacy Report](https://www.workplaceprivacyreport.com/?p=6777)

#### Texas CUBI
- [S] Enforced only by the attorney general, with up to $25,000 per violation. It was the basis for the Google ($1.375B) and Meta ($1.4B) settlements over voiceprints and face geometry. — [Bracewell](https://www.bracewell.com/resources/google-agrees-to-1-375-billion-settlement-as-texas-attorney-general-continues-data-privacy-push/); [CSLR](https://www.cslawreport.com/21169961/texas-ags-billiondollar-settlement-with-google-highlights-biometric-data-use-compliance-considerations.thtml); [ITECS (vendor guide)](https://itecsonline.com/post/texas-biometric-identifier-act-cubi-a-compliance-guide-for-businesses-capturing-fingerprints-faces-or-voices)

#### Washington
- [P/S] **RCW 19.375** bars enrolling a biometric identifier in a database for a commercial purpose without notice, consent, or a mechanism to prevent later commercial use. The term "biometric identifier" excludes "a physical or digital photograph, video or audio recording or data generated therefrom". It is enforced by the attorney general under the Consumer Protection Act; individuals have no private right to sue. — [RCW 19.375 (WA Legislature)](https://lawfilesext.leg.wa.gov/Law/RCW/RCW%20%2019%20%20TITLE/RCW%20%2019%20.375%20%20CHAPTER/RCW%20%2019%20.375%20%20CHAPTER.htm); [CaseGuard](https://caseguard.com/articles/washington-revised-code-ann-19375020/); [Eduverse summary](https://edlaw.eduverse.com/docs/jurisdiction/nat/us/state/wa/biometric-identifiers)
- [S] **My Health My Data Act (RCW 19.373)** defines biometric data more broadly, within "consumer health data", and does give individuals a right to sue through the Consumer Protection Act. — [BakerHostetler](https://www.bakerlaw.com/insights/examining-the-likely-impact-of-washingtons-my-health-my-data-act-on-class-action-litigation-involving-biometric-data)

#### FCC
- [S] In February 2024 the FCC issued a declaratory ruling making AI-generated voices in robocalls illegal under the TCPA's rules on "artificial" voices, as reported by AP. — [KSL/AP](https://www.ksl.com/article/news/business/company-that-sent-ai-calls-mimicking-joe-biden-to-voters-agrees-to-pay-1m-fine/51106394); [The Record](https://therecord.media/ftc-crack-down-ai-impersonation)

#### EU AI Act Article 50 (relevant to US users of EU-facing services)
- [S] **Deepfake disclosure (Article 50(4)), applicable from August 2, 2026.** A deployer who uses AI to generate or manipulate images, audio or video resembling real people that would falsely appear authentic must disclose that the content is AI-generated or manipulated. For evidently artistic, creative, satirical or fictional work, the disclosure can be made "in an appropriate manner that does not hamper the display or enjoyment of the work". — [Cloud Security Alliance research note, July 29 2026 (AI-assisted, not CSA-reviewed)](https://labs.cloudsecurityalliance.org/research/csa-research-note-eu-ai-act-article-50-transparency-20260729/); [Dastra](https://www.dastra.eu/en/blog/ai-act-transparency-rules-what-changes-august-2-2026/60164); [Reed Smith](https://www.reedsmith.com/our-insights/blogs/viewpoints/102nfqg/always-read-the-label-eu-ai-transparency-rules-and-questions-that-remain-unanswe/)
- [S] **Digital Omnibus did not delay Article 50.**
  - It deferred the Annex III high-risk obligations from August 2026 to December 2027, but left Article 50 on schedule.
  - Machine-readable marking of AI output (Article 50(2)) has a grace period to December 2, 2026, only for systems already on the market before August 2, 2026.
  - The Commission published its final Article 50 Guidelines on July 20, 2026.

  — [CSA](https://labs.cloudsecurityalliance.org/research/csa-research-note-eu-ai-act-article-50-transparency-20260729/); [Dastra](https://www.dastra.eu/en/blog/ai-act-transparency-rules-what-changes-august-2-2026/60164); [GDPR Local](https://gdprlocal.com/eu-ai-act-article-50/)

### Inferences
- **A private experiment with your own likeness.** None of the statutes above prohibits creating, keeping or privately viewing a consented, non-intimate replica of yourself (uncertain; not legal advice):
  - ELVIS, New York §§50–51 and the Illinois and California replica and publicity laws protect the depicted person against unauthorized use. Here the user is the person giving authorization.
  - California AB 2602 and the Illinois Digital Voice and Likeness Protection Act target personal or professional services contracts that replace in-person work. A consumer software subscription's Terms of Service probably isn't such a contract.
  - The TAKE IT DOWN Act covers intimate imagery only.
  - NO FAKES is not law.
- **The user's legal leverage runs against the vendors.** The user's main legal interests are the rights they hold as a data subject:
  - Illinois: BIPA notice, consent, retention-schedule and destruction duties, with a private right to sue. This is the strongest lever.
  - California: CCPA/CPRA deletion rights; ElevenLabs' CCPA notice offers deletion of "Voice Data".
  - Texas (CUBI) and Washington (RCW 19.375): attorney-general enforcement only.
  - Washington: My Health My Data adds a private right of action.

  These are the levers for getting avatars and voice clones deleted.
- **Where the legal lines are:**
  - publishing the clip in a way that misleads people;
  - impersonating a business or government agency (FTC Impersonation Rule);
  - using the cloned voice in automated calls (FCC/TCPA);
  - using anyone else's face or voice, including family members', without consent (vendor policies; ELVIS; New York; Illinois; California for deceased people);
  - using a synthetic performer in ads shown in New York (disclosure required);
  - any intimate content (TAKE IT DOWN).
- **EU.** EU deployer duties to label deepfakes apply when content is published. Separately, outputs from vendors serving the EU may carry machine-readable marks by December 2026 under Article 50(2), which could affect a US user's files.
- **Washington's photo exclusion.** RCW 19.375 excludes photos, video and audio "or data generated therefrom", which may leave face templates derived from a photo outside that statute, unlike BIPA. My Health My Data could still apply. This reading is uncertain.

### Gaps
- California's 2025–2026 follow-on laws were not researched: for example, changes to the AI Transparency Act (SB 942) effective date, and any new digital-replica bills.
- New York's 2024 digital-replica contract law (believed to be S.7676-B, effective Jan 1, 2025) was not verified in this session.
- The 2024 BIPA amendment (believed to be SB 2979, limiting per-person damages) was not verified. Current BIPA damages calculations may differ from aggregator wording ("per victim and per subsection").
- Texas TRAIGA (HB 149, believed effective Jan 1, 2026) was not verified.
- Status of FCC follow-on rulemaking on AI-call disclosure, and of the FTC's extension of the impersonation rule to individuals: not verified.
- EU AI Act Article 3(4): the "personal non-professional activity" carve-out from the definition of "deployer" is believed to exempt purely personal use from Article 50(4). It was not verified in this session.
- TAKE IT DOWN criminal provisions: believed to have taken effect on enactment, May 19, 2025; not confirmed in the snippets.
- Detailed NO FAKES 2026 provisions were not captured: scope of the right, limits on license length, preemption of state laws, safe harbors, and whether the bill numbers are correct.
- Other states' 2025–26 deepfake and right-of-publicity laws were not researched.

## 5. Personal security risks of having your face and voice clone on a vendor's servers or in circulation, and how to minimise them

### Takeaway
The main practical risks from a face-and-voice clone are:

- voice-based fraud: family "emergency" scams and social engineering of banks or employers;
- account takeover wherever a voiceprint is still used for authentication;
- reputational misuse if the files leak.

The FBI advises agreeing a family code word and limiting how much of your voice and image you post. Sam Altman said in July 2025 that AI "has fully defeated" voiceprint authentication. A secondary source says Wells Fargo disabled its voiceprint service.

Cloning someone from public audio or a single photo is already easy (CR 2025; the unverified photo routes in Q1). So the extra risk the experiment adds lies mostly in how vendors retain and license the data, how secure the user's account is, and where the outputs end up.

### Cited Findings
- [S] **FBI warning on generative-AI fraud** (PSA I-120324-PSA, December 2024; possibly outdated). Criminals use generative AI to commit fraud "on a larger scale". Cloned voices of public figures or people close to the victim are used to get bank access or fraudulent transfers. The FBI recommends:
  - agreeing a secret word or phrase with family;
  - limiting the images and voice recordings you post online;
  - listening for tone and word choice;
  - looking for imperfections in images and video.

  — [TechTarget](https://www.techtarget.com/searchsecurity/news/366616605/FBI-Criminals-using-AI-to-commit-fraud-on-a-larger-scale); [Bitdefender](https://www.bitdefender.com/en-us/blog/hotforsecurity/fbi-alarm-ai-scams); [CO/AI](https://getcoai.com/news/how-to-protect-your-family-from-ai-voice-clones-claiming-to-be-you)
- [S] At a Federal Reserve conference in July 2025, Sam Altman criticized banks that still accept voiceprints ("AI has fully defeated that") and warned of a coming fraud crisis. — [Local10/AP, July 22 2025](https://www.local10.com/business/2025/07/22/openais-sam-altman-warns-of-ai-voice-fraud-crisis-in-banking); [Storyboard18](https://www.storyboard18.com/digital/ai-can-fool-banks-and-wipe-out-jobs-warns-openai-ceo-sam-altman-76574.htm)
- [S] An undated secondary blog says Wells Fargo told customers it disabled its voiceprint service. Not verified with the bank. No other bank discontinuations were found. — [KnowBe4 blog](https://blog.knowbe4.com/voice-cloning-bank-voice-authentication)
- [S] In 2023 a journalist used a cloned voice to get into a UK Lloyds Bank account. The same year, Sen. Sherrod Brown wrote to the CEOs of six large US banks about the security of voice authentication. — [AI Incident Database report 2740](https://incidentdatabase.ai/reports/2740); [Vice](https://vice.com/en/article/n7enqd/senator-asks-banks-stop-ai-cloned-voices); [BankInfoSecurity](https://www.bankinfosecurity.com/cloned-voice-tech-coming-for-bank-accounts-a-24850)
- [S] CR researchers could easily clone a voice from public audio on four of six services (March 2025). — [Axios](https://www.axios.com/2025/03/15/ai-voice-cloning-consumer-scams)
- [S] NewsGuard found Sora 2 produced realistic videos of false claims 80% of the time when asked (October 2025). — [Decrypt](https://decrypt.co/345296/sora-2-fabricate-convincing-deepfakes-on-command-study-finds?amp=1)
- [P/S] **Controls vendors offer:**
  - ElevenLabs: a training opt-out ("Data use" settings) and CCPA deletion of the account plus its "Voice Data".
  - Synthesia: deletion within 90 days, confirmed in writing.
  - Captions: "Delete actor".
  - HeyGen: deletion on request and a training opt-out through support (per Waimakers).
  - Sora: permanent deletion after the shutdown.

  — [LicenseOrg](https://licenseorg.com/blog/elevenlabs-licensing-guide-ai-voices); [ElevenLabs CCPA notice](https://elevenlabs.io/ccpa-notice-at-collection); [Synthesia Help](https://help.synthesia.io/en/articles/9490158-what-is-the-time-frame-for-complete-deletion-of-an-avatar); [Captions help](https://captions.ai/help/docs/project/ai-twin.md); [Waimakers](https://www.waimakers.com/en/resources/ai-data-security/heygen); [OpenAI Help](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation?so=1)
- [S] The Cutout.Pro breach shows that account data at AI media services (emails, names, hashed passwords) does leak. — [TechRadar](https://www.techradar.com/pro/security/top-ai-service-hit-by-massive-data-breach-20-million-cutoutpro-users-have-personal-info-leaked-so-change-passwords-now)

### Inferences (a mitigation checklist for the report, drawn from the findings above; not itself sourced)
1. **Before uploading,** set training opt-outs (ElevenLabs "Data use"; HeyGen through support). Opt-outs may only apply going forward. Read the license clause too: avoid services whose terms give a perpetual, irrevocable license over your face or voice (CapCut, as read by commentators; Hedra's consumer terms) if that matters to you.
2. **Use a dedicated account:** a separate email, a unique password and MFA. Keep API keys secret and rotate or revoke them afterwards. An API key plus an avatar or voice ID lets whoever holds them generate content as you.
3. **Upload as little as possible:** one photo or a short selfie clip, and a short voice sample. Don't upload government ID; no source found any of these vendors requiring ID for a self-clone. Don't say sensitive things in samples or scripts: passphrases like "my voice is my password", PINs, birthdates or account numbers.
4. **Prefer vendors with concrete deletion commitments,** such as Synthesia's 90 days. After the experiment:
   - delete the avatar and voice in the app;
   - send a formal deletion request, citing CCPA or BIPA where they apply;
   - keep the confirmation.
5. **Keep outputs private.** Store them locally, don't post them, and don't post long clean recordings of your voice. If you ever share a clip, label it as AI.
6. **Agree a family safe word** (per the FBI) and tell close family the experiment exists.
7. **Turn off voiceprint authentication** at banks, brokerages and phone carriers if you have it, and use app-based MFA instead. Don't "test" your bank's voice ID with the clone: it could breach the bank's terms or raise fraud concerns.
8. **Chinese-owned services** (Kling, Dreamina/CapCut): the factual position is that their terms, operating entities and ownership differ from the US vendors. Read their terms before uploading biometric data. Data-location specifics were not verified.

### Gaps
- No authoritative list of which US banks still use voiceprints or have dropped them; only the Wells Fargo claim from a secondary blog. Schwab, Chase, HSBC, Vanguard and others were not checked.
- No quantitative data on family-emergency or impersonation scam losses (for example, FTC Consumer Sentinel for 2025) was gathered before the search budget ran out.
- No source assessed actual misuse of self-uploaded clones held on vendor servers, whether by insiders or through account compromise.

## 6. Practitioner and journalist commentary: Reddit, Hacker News, security researchers, consumer advocates (EFF, Consumer Reports)

### Takeaway
Consumer advocates and journalists make three recurring points:

- self-serve voice-cloning safeguards are weak (CR's "slapdash" findings in 2025);
- platform likeness policies were reactive, as Sora 2's reversals showed;
- broad Terms of Service licenses are the hidden cost of uploading a face or voice (ElevenLabs in early 2025, CapCut in June 2025).

Reddit, Hacker News and EFF commentary could not be gathered before the shared search budget ran out.

### Cited Findings
- [S] The Register's coverage of CR's March 2025 report described voice-cloning safeguards as "slapdash". — [The Register](https://www.theregister.com/2025/03/10/ai_voice_cloning_safeguards/)
- [S] CR policy analyst Grace Gedye argued that some voice-cloning offerings may violate Section 5 of the FTC Act. CR recommended technical consent checks, better AI-audio detection, and supervised rather than self-service cloning. — [Consumer Reports](https://innovation.consumerreports.org/new-report-do-these-6-ai-voice-cloning-companies-do-enough-to-prevent-misuse/); [CO/AI](https://getcoai.com/news/ai-voice-cloning-risks-exposed-by-consumer-reports-descript-more-secure-than-elevenlabs/)
- [S] Public Citizen pressed OpenAI to take Sora offline. Critics said OpenAI's October 2025 guardrail changes still allowed realistic, disruptive deepfakes. — [Common Dreams](https://www.commondreams.org/news/openai-sora-public-citizen); [Tom's Guide](https://www.tomsguide.com/ai/openai-tightens-guardrails-around-celebrity-deepfakes-after-pressure-from-bryan-cranston-and-sag-aftra-heres-everything-you-need-to-know)
- [S] Eugene Volokh on Lehrman v. Lovo: "Begun the Clone War Has." — [Volokh Conspiracy](https://reason.com/volokh/2025/07/10/begun-the-clone-war-has-here-as-to-cloning-of-voice-over-actors-voices/)
- [S] On CapCut's terms, legal experts said users may unknowingly waive right-of-publicity protections. TechRadar was less alarmed. — [Central Florida Lifestyle](https://www.centralfloridalifestyle.com/tech/capcuts-updated-terms-raise-concerns-over-content-ownership-and-user-rights/amp/); [TechRadar](https://www.techradar.com/pro/popular-video-editing-app-capcut-wants-to-use-any-content-you-produce-for-free-forever-heres-what-you-should-know)
- [S] Policy-monitoring site ConductAtlas notes that following Runway's policy does not by itself meet legal consent or disclosure requirements, and that right-of-publicity laws, BIPA and the GDPR may apply independently. Reliability caveat: the same summaries refer to "California's ELVIS Act", but the ELVIS Act is a Tennessee law. — [ConductAtlas: Runway impersonation](https://conductatlas.com/platform/runway/runway-usage-policy/prohibition-on-impersonation-and-misleading-content/)
- [S] Law-firm commentary on the BIPA voice suits: they may open a new route to class-wide claims over AI training, but people outside Illinois may have no remedy unless new private rights of action are created. — [ZwillGen](https://zwillgen.com/litigation/old-statutes-new-targets-plaintiffs-using-existing-privacy-consumer-laws-against-ai-companies)
- [S] Bloomberg Government reports that state privacy laws are poised to be used against unauthorized voice cloning. — [Bloomberg Government](https://news.bgov.com/in-house-counsel/state-privacy-laws-poised-to-fight-unauthorized-voice-cloning)
- [S] OpenAI CEO Sam Altman on voiceprints: "AI has fully defeated that" (July 2025). — [Local10/AP](https://www.local10.com/business/2025/07/22/openais-sam-altman-warns-of-ai-voice-fraud-crisis-in-banking)

### Inferences
- The commentary agrees that the technical barrier to cloning anyone is low. For someone cloning themselves, the risks they can actually control are the vendor's terms, its retention and deletion practices, and the security of their account and API keys.
- Some of the third-party policy-analysis sites used here make errors (ConductAtlas's "California's ELVIS Act"; the conflicting Kling biometrics ratings). The report should prefer vendor documents and statutes where they conflict.

### Gaps
- Reddit, Hacker News and EFF commentary was not gathered (search budget exhausted). EFF's position on NO FAKES, believed to be critical on free-speech grounds in 2024–25, was not verified in this session.
- No security-researcher studies on bypassing consent or liveness checks at HeyGen, ElevenLabs, Tavus or D-ID were found.
- Whether Consumer Reports published a 2026 follow-up on voice cloning was not checked.
