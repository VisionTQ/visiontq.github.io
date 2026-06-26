---
title: "Best Free Speech-to-Text AI: Whisper AI"
date: 2026-04-09
author: tnebula
description: A clean guide to using OpenAI Whisper in Google Colab to transcribe audio and video for free.
image: /assets/whisper-ai/whisper-thumbnail.png
tags:
  - openai
  - whisper
  - speech-to-text
  - transcription
  - colab
  - ai
categories:
  - AI
  - Tutorials
---
## Before You Begin

OpenAI Whisper is one of the easiest free tools for turning audio or video into text. In this guide, I will show you how to use Whisper online with Google Colab, so you do not need to install anything on your computer.

### My Personal Use Cases

I use the online version because my hardware is weak, and local transcription takes too long.

Here are the ways I use it:

- Transcribe audio in another language, then send the text to another AI tool for translation.
- I also Transcribe TikTok or YouTube audio into text so I can summarize it or ask questions about it.

### What You'll Need

1. A Google account
2. An audio or video file to transcribe

## Step 1: Open Google Colab

If you have never added Colab to Google Drive before:

1. Go to [Google Drive](https://drive.google.com/).
2. Click `+ New` -> `More` -> `Connect more apps`.

![Google Drive New menu](/assets/whisper-ai/google-drive-new-menu.png){: .w-75 .shadow .rounded-10 }

3. Click the search icon and search for `Colaboratory`.

![Search for Colaboratory](/assets/whisper-ai/search-colaboratory.png){: .w-75 .shadow .rounded-10 }

After you do this once, you will not need to repeat it again.

The next time you want to use Whisper:

1. Go to [Google Drive](https://drive.google.com/).
2. Click `+ New` -> `More` -> `Google Colab`.

![Google Colab in the New menu](/assets/whisper-ai/google-colab-menu.png){: .w-75 .shadow .rounded-10 }

## Step 2: Enable GPU

Your screen should look similar to this:

![Google Colab notebook screen](/assets/whisper-ai/colab-notebook-screen.png){: .w-75 .shadow .rounded-10 }

Then:

1. Open `Runtime > Change runtime type`.
2. Set `Hardware accelerator` to `GPU`.
3. Save the change.

> Whisper runs much faster on a GPU than on a CPU in Colab.
{: .prompt-info }

## Step 3: Install Whisper and FFmpeg

Paste this into the first cell and run it:

```
# Install Whisper
!pip install -q -U openai-whisper

# Install ffmpeg
!apt-get -qq update
!apt-get -qq install ffmpeg

print("Setup complete")
```

This installs Whisper and FFmpeg, which Colab uses to read common audio and video formats.

Wait until everything finishes installing.

## Step 4: Upload Your File

1. Create a new code cell.
2. Click the folder icon in the left sidebar.

![Colab folder icon in sidebar](/assets/whisper-ai/colab-folder-sidebar.png){: .w-75 .shadow .rounded-10 }

3. Upload the audio or video file you want to transcribe.
4. Note the exact filename, such as `interview.mp3` or `lecture.mp4`.

![Upload file in Colab](/assets/whisper-ai/upload-file.png){: .w-75 .shadow .rounded-10 }

## Step 5: Run Whisper

Paste this into a new cell:

```bash
!whisper "your-file-name.mp3" --model medium.en
```

Replace `your-file-name.mp3` with your actual filename.

Example:

![Whisper command example](/assets/whisper-ai/whisper-command-example.png){: .w-75 .shadow .rounded-10 }

### Model Options

- `tiny`: fastest, lowest accuracy
- `base`: slightly better accuracy
- `small`: good balance for quick jobs
- `medium`: better accuracy, slower
- `large`: best quality, slowest and heaviest

If your audio is not in English, use `small`, `medium`, or `large` instead of an `.en` model, and pass `--language` to skip auto-detection:

```
!whisper "your-file-name.mp3" --model medium --language Arabic
!whisper "your-file-name.mp3" --model medium --language Japanese
!whisper "your-file-name.mp3" --model medium --language French
!whisper "your-file-name.mp3" --model medium --language Spanish
!whisper "your-file-name.mp3" --model medium --language Chinese
```
Whisper supports many languages — see the full list [here](https://github.com/openai/whisper#available-models-and-languages).

If you only want `.txt` output:

```
!whisper "your-file-name.mp3" --model medium --language Arabic --output_format txt
```

## Output Files

After the command finishes, Whisper usually creates:

- `your-file-name.txt` for plain text
- `your-file-name.srt` for subtitles
- `your-file-name.vtt` for web captions

You can download them from the file browser in the left sidebar.

## Common Issues

### The Filename Does Not Work

Make sure the filename matches exactly.

### Transcription Is Slow

Use GPU runtime and try a smaller model like `base.en` or `small.en`.

## Final Thoughts

Whisper is one of the best speech-to-text tools I have used. I mainly use it for audio in languages I do not understand, and it saves me a lot of time.

If you have any questions or suggestions, let me know.

## Resources

- [OpenAI Whisper GitHub repository](https://github.com/openai/whisper)
- [Google Colab](https://colab.research.google.com/)
- [FFmpeg](https://ffmpeg.org/)
- [Kevin Stratvert reference guide](https://kevinstratvert.com/2023/01/19/best-free-speech-to-text-ai-whisper-ai/)

![Not AI](/assets/img/Written-By-Humans-Not-By-AI-Badge-black.png){: .right }