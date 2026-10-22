---
title: I Tested Free ElevenLabs Alternatives, Then Went Back to ElevenLabs
date: 2026-10-22 12:00:00 +0300
author: tnebula
categories:
  - AI
  - TTS
tags:
  - elevenlabs
  - chatterbox
  - qwen3-tts
  - voice-cloning
description: I tested Chatterbox and Qwen3-TTS as free ElevenLabs alternatives, then went back to the ElevenLabs Reader for listening to EPUB books.
---

I wanted a free alternative to ElevenLabs for voice cloning, so I tried two open source demos: Chatterbox and Qwen3-TTS.

## Reference Voice

{% include embed/audio.html src='/assets/voice-cloning/reference-voice.flac' %}

### Reference Text

Transcript of the reference audio:

> That place in the distance, it's huge and dedicated to Lady Shah. It can only mean one thing. I have a hidden place close to the cloister where night all kids bloom.

## Chatterbox TTS Demo

<https://huggingface.co/spaces/ResembleAI/Chatterbox>

{% include embed/audio.html src='/assets/voice-cloning/chatterbox-demo.wav' %}

![Chatterbox TTS interface](/assets/voice-cloning/chatterbox-ui.png){: .shadow }

## Qwen3-TTS Demo

<https://huggingface.co/spaces/Qwen/Qwen3-TTS>

![Qwen3-TTS interface](/assets/voice-cloning/qwen3-tts-ui.png){: .shadow }

Model size: 1.6B parameters, English language.

### Target Text

Text to synthesize with the cloned voice:

> Now let's make my mum's favourite. So three mars bars into the pan. Then we add the tuna and just stir for a bit, just let the chocolate and fish infuse. A sprinkle of olive oil and some tomato ketchup. Now smell that. Oh boy this is going to be incredible.

{% include embed/audio.html src='/assets/voice-cloning/qwen3-tts-demo.wav' %}

## Why I Went Back to ElevenLabs

I gave up on this since I found the ElevenLabs Reader. It seems better because I can just upload the EPUB from z-lib.gd. I used the ElevenLabs Reader, and right now I'm using it to listen to *Fluent Forever*. I tried to listen to it on Spotify, but it seems region locked or something. Anyway, if you are looking to listen to books, get them from z-lib.gd and listen to the audiobook using ElevenLabs by uploading the book from z-lib.gd as an EPUB file.

![Not AI](/assets/img/Written-By-Humans-Not-By-AI-Badge-black.png){: .right }
