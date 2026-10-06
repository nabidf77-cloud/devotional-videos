# Full Video Prompts (with Voice) — God-Editor-Style Batch 2

Complete generation recipe per video: visual prompt + Bengali voiceover + audio mix.
Voice: `avocado_v2:MAI_03` (current default), `--language bn`.
Output: 10s, 720×1280 vertical 9:16, 24fps, H.264 + AAC, faststart.

**Pipeline per video:**
1. Generate video from the VISUAL PROMPT (10s, 9:16, silent).
2. Synthesize the VOICEOVER SCRIPT with TTS (`--voice avocado_v2:MAI_03 --language bn`).
3. Fit narration to 10s: if narration > 10s, apply `atempo=D/9.96` with NO adelay;
   otherwise `adelay=500|500` lead-in.
4. Mix: narration + subtle brown-noise ambience bed
   (`anoisesrc=color=brown, lowpass=f=450, volume=0.05`, 1.2s fades in/out). No music.
5. Mux: `-c:v libx264 -preset slow -crf 18 -r 24 -pix_fmt yuv420p -c:a aac -b:a 128k -t 10 -movflags +faststart`.

---

## 1. Hanuman 🐒 — `godstyle2-hanuman-voice-devotional.mp4`

**VISUAL PROMPT:**
```
Create a 10-second vertical 9:16 hyper-realistic AI devotional art video, one continuous shot, no cuts.
Mighty Lord Hanuman flying through dramatic monsoon clouds carrying a glowing mountain of healing herbs in one hand and a golden mace (gada) in the other. Orange dhoti flowing, sacred thread across his chest, determined divine expression, lightning softly illuminating the clouds behind him.
CAMERA: 50mm cinematic lens, slow smooth tracking shot following his flight, shallow depth of field, no shake.
AUDIO: Silent video - audio will be added separately.
Negative prompt: no cuts, no text, no subtitles, no watermark, no distorted face, no malformed hands, no extra limbs, no cartoon, no artificial CGI look.
```

**VOICEOVER SCRIPT (Bengali):**
```
পবনপুত্র হনুমানের আশীর্বাদে আপনার জীবনে আসুক অসীম শক্তি ও সাহস। সংকটমোচন দূর করুন সব বাধা। ভিডিওটি শেয়ার করুন, কমেন্টে লিখুন জয় বজরংবলী।
```

---

## 2. Vishnu 🐚 — `godstyle2-vishnu-voice-devotional.mp4`

**VISUAL PROMPT:**
```
Create a 10-second vertical 9:16 hyper-realistic AI devotional art video, one continuous shot, no cuts.
Lord Vishnu standing majestically on the cosmic ocean — deep blue skin, golden crown and jewelry, holding the conch (shankh) and discus (chakra), a soft divine halo behind his head. Gentle cosmic waves with floating lotus flowers, stars and nebula colors in the sky above.
CAMERA: 50mm cinematic lens, very slow push-in toward the deity, shallow depth of field, no shake.
AUDIO: Silent video - audio will be added separately.
Negative prompt: no cuts, no text, no subtitles, no watermark, no distorted face, no malformed hands, no extra limbs, no cartoon, no artificial CGI look.
```

**VOICEOVER SCRIPT (Bengali):**
```
ভগবান বিষ্ণুর কৃপায় আপনার জীবনে আসুক শান্তি ও সমৃদ্ধি। জগতের পালনকর্তা রক্ষা করুন আপনাকে। শেয়ার করুন, কমেন্টে লিখুন ওম নমো নারায়ণ।
```

---

## 3. Krishna's Flute 🎶 — `godstyle2-krishna-flute-voice-devotional.mp4`

**VISUAL PROMPT:**
```
Create a 10-second vertical 9:16 hyper-realistic AI devotional art video, one continuous shot, no cuts.
Close artistic view of blue-skinned Krishna playing a bamboo flute under soft moonlight — peacock feather crown, gentle smile, fingers graceful on the flute. Musical notes seem to float as glowing particles in the air. Flowering trees softly blurred around, fireflies drifting.
CAMERA: 50mm cinematic lens, slow gentle orbital drift around the flutist, shallow depth of field, no shake.
AUDIO: Silent video - audio will be added separately.
Negative prompt: no cuts, no text, no subtitles, no watermark, no distorted face, no malformed hands, no extra fingers, no cartoon, no artificial CGI look.
```

**VOICEOVER SCRIPT (Bengali):**
```
শ্রীকৃষ্ণের বাঁশির সুরের মতোই মধুর হোক আপনার জীবন। তাঁর আশীর্বাদে ভরে উঠুক মন আনন্দে। শেয়ার করুন, কমেন্টে লিখুন হরে কৃষ্ণ।
```

---

## 4. Parvati 🌸 — `godstyle2-parvati-voice-devotional.mp4`

**VISUAL PROMPT:**
```
Create a 10-second vertical 9:16 hyper-realistic AI devotional art video, one continuous shot, no cuts.
Goddess Parvati in an elegant white and gold saree with delicate jewelry, meditating gracefully among Himalayan wildflowers at dawn. Soft golden sunlight breaking over snow peaks behind her, gentle flower petals drifting in the mountain breeze, a serene divine glow around her.
CAMERA: 50mm cinematic lens, slow smooth cinematic drift, shallow depth of field, no shake.
AUDIO: Silent video - audio will be added separately.
Negative prompt: no cuts, no text, no subtitles, no watermark, no distorted face, no malformed hands, no extra limbs, no cartoon, no artificial CGI look.
```

**VOICEOVER SCRIPT (Bengali):**
```
মা পার্বতীর আশীর্বাদে আপনার জীবনে আসুক সুখ ও সৌভাগ্য। মায়ের কৃপায় পূর্ণ হোক মনোবাঞ্ছা। শেয়ার করুন, কমেন্টে লিখুন জয় মা পার্বতী।
```

---

## 5. Kartik (Murugan) 🦚 — `godstyle2-kartik-voice-devotional.mp4`

**VISUAL PROMPT:**
```
Create a 10-second vertical 9:16 hyper-realistic AI devotional art video, one continuous shot, no cuts.
Lord Kartik (Murugan) standing heroically with his divine spear (vel) beside a majestic peacock with fully spread iridescent tail feathers. Traditional South Indian temple gopuram softly blurred behind, marigold and jasmine garlands, warm festive lighting with floating flower petals.
CAMERA: 50mm cinematic lens, slow smooth orbital movement, shallow depth of field, no shake.
AUDIO: Silent video - audio will be added separately.
Negative prompt: no cuts, no text, no subtitles, no watermark, no distorted face, no malformed hands, no extra limbs, no cartoon, no artificial CGI look.
```

**VOICEOVER SCRIPT (Bengali):**
```
ভগবান কার্তিকের আশীর্বাদে আপনার জীবনে আসুক বিজয় ও সাহস। তাঁর বেল দূর করুক সব অশুভ শক্তি। শেয়ার করুন, কমেন্টে লিখুন জয় মুরুগান।
```
