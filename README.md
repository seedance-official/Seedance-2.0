# Seedance 2.0

Seedance 2.0 is ByteDance's video generation model with native audio, multi-shot storytelling and image, video and audio references.

> **Try Seedance 2.0 online →** [https://seedance-2.us](https://seedance-2.us?utm_source=github&utm_medium=ugc&utm_campaign=seedance-official&utm_content=readme-top&utm_term=tier-b)

Seedance is the video generation model family from ByteDance's Seed research team, the same group behind the Seedream image models and the Doubao language models. Seedance 1.0 arrived in June 2025 and immediately placed at the top of the Artificial Analysis text-to-video and image-to-video leaderboards, largely on the strength of its multi-shot narrative generation, prompt adherence and stable 1080p motion. Seedance 1.5 pro followed in December 2025 with jointly generated audio, including lip-synced dialogue. Seedance 2.0, announced in February 2026, is the current flagship.

The defining feature of Seedance 2.0 is multimodal referencing. Instead of a single starting frame, a generation can be steered by a set of uploaded assets, up to 9 images, 3 video clips and 3 audio files, which the prompt addresses by name. A reference image can fix a character's face or a product, a reference video can supply camera motion, choreography or an editing rhythm, and a reference audio track can drive lip movement or set the beat for cuts. Together with native sound (dialogue, effects and music generated in the same pass as the pixels) and multi-shot output that keeps subjects consistent across cuts, this pushes the model from clip generation toward short-form production.

Its nearest competitors are Google's Veo 3.1, Kuaishou's Kling, OpenAI's Sora 2 and MiniMax's Hailuo. Seedance 2.0 competes on reference flexibility, motion realism and cost, and it is distributed through ByteDance's own consumer apps (Jimeng and Doubao in China, Dreamina and CapCut internationally) as well as the Volcano Engine and BytePlus cloud APIs. Its launch also drew scrutiny from Hollywood studios over generated clips featuring copyrighted characters, and ByteDance said it would tighten safeguards before wider international rollout.

## Contents

- [What Seedance 2.0 can do](#what-seedance-2-0-can-do)
- [Versions](#versions)
- [How to access Seedance 2.0](#how-to-access-seedance-2-0)
- [Prompt examples](#prompt-examples)
- [Seedance 2.0 vs alternatives](#seedance-2-0-vs-alternatives)
- [Pricing](#pricing)
- [FAQ](#faq)
- [Links](#links)

## What Seedance 2.0 can do

- Text-to-video and image-to-video generation, with first-frame and first-plus-last-frame control for image inputs.
- Multimodal references: up to 9 images, 3 video clips and 3 audio files per generation, referenced in the prompt so each asset plays a defined role (character, product, camera move, motion, voice, music).
- Native audio generated together with the video: lip-synced dialogue in multiple languages, ambient sound, effects and music.
- Multi-shot output: a single prompt can produce a sequence of cuts with consistent characters, wardrobe and setting.
- Clips from roughly 4 to 15 seconds, at 480p and 720p with 1080p output on the higher tiers, 24 fps.
- Video-to-video editing and extension: restyle an existing clip, swap a subject, continue a shot, or match a reference video's motion.
- Camera language in prompts: pans, dolly moves, orbit, rack focus and handheld are followed reliably, as are film and animation styles.
- Strong physical motion for sports, dance, fabric, fluids and crowds, which is where the 1.x series first stood out.

Known limitations: Seedance 2.0 launched first in China and the international rollout on Dreamina and CapCut has been staged, so features, resolution options and clip lengths differ by platform and date. Outputs top out around 1080p and 15 seconds; longer pieces must be stitched. Content filters block real public figures and many copyrighted characters, especially after the February 2026 studio complaints, and the reference system works best with clean, well-lit assets. Text inside the video frame is still unreliable, and the audio track is good for dialogue and effects but not a substitute for a produced music track.

## Versions

| Version | Released | Notes |
|---|---|---|
| Seedance 1.0 (Lite and Pro) | 2025-06 | First release; 1080p, 5 to 10 second clips, multi-shot narrative generation, no native audio. Topped Artificial Analysis T2V and I2V leaderboards at launch. |
| Seedance 1.0 Pro Fast | 2025-08 | Faster, cheaper variant of 1.0 Pro on Volcano Engine and BytePlus for high-volume use. |
| Seedance 1.5 pro | 2025-12 | Adds joint audio-video generation with lip-synced multilingual dialogue and sound effects; 480p and 720p at launch. |
| Seedance 2.0 | 2026-02 | Multimodal references (images, videos, audio), native audio, longer clips up to 15 seconds, video-to-video editing. Launched in Jimeng and Doubao, then Dreamina and CapCut internationally. |

## How to access Seedance 2.0

Seedance 2.0 is a closed model hosted by ByteDance. Official access paths:

- Consumer apps: Jimeng (即梦) and Doubao in mainland China; Dreamina (dreamina.capcut.com) and CapCut internationally, both on a credit or subscription basis. International availability was rolled out in stages after the Chinese launch.
- API: Volcano Engine (火山引擎, ByteDance's China cloud) and BytePlus ModelArk for customers outside China. Seedance models are exposed as Doubao-Seedance endpoints with per-token or per-second billing and require a verified cloud account.
- Third-party hosts such as fal.ai, Replicate, WaveSpeed and Kie resell Seedance endpoints once ByteDance makes a version available on ModelArk; the 1.x models are widely mirrored, and 2.0 availability depends on the host.

Region and tier restrictions apply: the China-side apps need a Chinese phone number, Dreamina and CapCut gate the newest model behind paid tiers and daily caps, and ModelArk requires business verification. If you want to try the model without a waitlist, a ByteDance cloud account or a monthly plan, [Seedance 2.0](https://seedance-2.us) offers pay-per-generation access.

**Fastest way to try it:** [Try Seedance 2.0 online](https://seedance-2.us?utm_source=github&utm_medium=ugc&utm_campaign=seedance-official&utm_content=readme-access&utm_term=tier-b) — no waitlist, runs in the browser.

## Prompt examples

**Multi-shot product film**

```text
Three-shot sequence, 12 seconds, 16:9. Shot 1: slow dolly-in on a matte black wireless speaker on a walnut desk, morning light through blinds. Shot 2: close-up of a finger tapping the top button, LED ring lights up. Shot 3: wide shot of a loft apartment as music fills the room, camera slowly orbits. Warm soft ambient sound, subtle bass when the speaker turns on.
```

**Reference-driven character dialogue**

```text
@image1 is the actor, @image2 is the rain-soaked alley location, @audio1 is the voice line. Generate a 9 second night scene where the actor from @image1 stands in the alley from @image2 and delivers @audio1 to camera with accurate lip sync. Neon reflections on wet asphalt, handheld camera, shallow depth of field, light rain audible.
```

**Motion transfer from video**

```text
@video1 shows a dancer doing a spin and drop. @image1 is a cartoon fox in a tracksuit. Make the fox perform exactly the motion in @video1 on a rooftop at sunset, 3D animated style, 8 seconds, upbeat electronic music that matches the movement.
```

**Physical realism**

```text
A cyclist descends a wet mountain road in a downpour, 10 seconds, tracking shot from a chase car. Water spray from the tires, jacket flapping in the wind, brake lights reflected on the road, realistic rain and wind sound with the hiss of tires.
```

**First and last frame transition**

```text
Start frame: a paper airplane on a school desk. End frame: a real jet airliner above the clouds. 8 seconds, seamless morph as the paper plane lifts off the desk, flies out of the window and turns into the airliner, orchestral swell, 16:9.
```

## Seedance 2.0 vs alternatives

| Model | Max resolution / duration | Native audio | Editing / references | Access | Price tier |
|---|---|---|---|---|---|
| Seedance 2.0 (ByteDance) | 1080p, up to 15 s | Yes, dialogue with lip sync | Up to 9 images, 3 videos, 3 audio; video-to-video | Jimeng, Dreamina, CapCut, Volcano Engine / BytePlus API | Low-medium |
| Veo 3.1 (Google) | 1080p, 4K upscale, 8 s (extendable) | Yes | Up to 3 reference images, first/last frame, extend | Gemini app, Flow, Gemini API, Vertex AI | Medium-high |
| Kling 2.6 (Kuaishou) | 1080p, 5 to 10 s | Yes | Elements references, first/last frame, motion control | Kling app, Kling API, fal | Medium |
| Sora 2 (OpenAI) | 1080p (Pro), up to 15 s | Yes | Remix, cameo characters | Sora app, ChatGPT, OpenAI API | Medium-high |
| Hailuo 2.3 (MiniMax) | 1080p, 6 or 10 s | No | First/last frame, subject reference | Hailuo app, MiniMax API | Low |

Seedance 2.0 is the most flexible of the group on references, being the only one that accepts video and audio inputs alongside images, and it is priced below Veo and Sora. Veo 3.1 still leads on cinematic polish and audio quality, Kling has the broadest third-party availability, and Sora 2 has the strongest consumer app. Seedance's weaker points are the staged international rollout and the stricter content filters introduced after its launch.

## Pricing

As of the last public information, ByteDance prices Seedance on Volcano Engine and BytePlus ModelArk per generated video, computed from resolution and duration (the 1.x Pro models cost on the order of a few tenths of a US dollar for a 5 second 1080p clip, with Lite and Fast variants cheaper), and Seedance 2.0 sits above the 1.x tiers. Consumer access through Dreamina and CapCut uses credits, with free daily allowances on the older models and paid plans for Seedance 2.0 and higher resolutions. Exact per-second rates and credit costs have changed with each release, so treat any specific number as a snapshot and check the ModelArk or Dreamina pricing pages.

For occasional use, [Seedance 2.0](https://seedance-2.us) offers pay-per-generation access with no subscription or cloud account required.

## FAQ

**What is Seedance 2.0?**

Seedance 2.0 is ByteDance's flagship video generation model, released in February 2026. It produces clips with native audio, keeps characters consistent across multi-shot sequences, and can be steered by reference images, videos and audio files.

**Is Seedance 2.0 free?**

Not in general. Dreamina, CapCut, Jimeng and Doubao give limited free credits, mostly on older Seedance versions, and put Seedance 2.0 and higher resolutions behind paid tiers. The Volcano Engine and BytePlus APIs are pay-as-you-go.

**Is there a Seedance 2.0 API?**

Yes. Seedance models are served as Doubao-Seedance endpoints on Volcano Engine in China and BytePlus ModelArk internationally, and third-party hosts such as fal.ai and Replicate mirror the versions ByteDance releases.

**Does Seedance 2.0 have an official GitHub repository?**

No. Seedance is a closed, hosted model and ByteDance has not published weights or an official repository; only a technical report exists for Seedance 1.0. This page collects publicly available information.

**How do I try Seedance 2.0 online?**

Use Dreamina or CapCut internationally, or Jimeng and Doubao in China. For pay-per-generation access without a waitlist or account on a ByteDance platform, use https://seedance-2.us.

**What are the limits of Seedance 2.0?**

Clips are capped at roughly 15 seconds and 1080p, the international rollout has been staged so features vary by platform, content filters block public figures and many copyrighted characters, and in-frame text is unreliable.

**What can Seedance 2.0 use as a reference?**

Up to 9 images, 3 video clips and 3 audio files in one generation. Images fix characters, products or scenes, videos supply motion or camera movement, and audio drives lip sync or sets the rhythm of cuts.

## Links

- [Seedance (ByteDance Seed, official)](https://seed.bytedance.com/en/seedance)
- [Dreamina by CapCut](https://dreamina.capcut.com/)
- [BytePlus ModelArk](https://www.byteplus.com/en/product/modelark)
- [Try Seedance 2.0 online](https://seedance-2.us)

---

*This is an independent, community-maintained information repository about Seedance 2.0. It is not affiliated with, endorsed by, or sponsored by ByteDance (Seed). All trademarks belong to their respective owners. Corrections welcome via issues.*


_Last reviewed: 2026-09-22_
