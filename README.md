# Chime TTS
[![hacs_badge](https://img.shields.io/badge/HACS-Default-41BDF5.svg)](https://github.com/hacs/integration)
![version](https://img.shields.io/github/v/release/nimroddolev/chime_tts)
[![Community Forum][forum-shield]][forum]
<a href="https://www.buymeacoffee.com/nimroddolev"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" height="20px"></a>

Chime TTS is a Home Assistant integration that eliminates the audio lag between playing a chime/notification sound effect before a TTS audio notification.


![Chime TTS](https://raw.githubusercontent.com/nimroddolev/chime_tts/main/icon.png)

- [What is Chime TTS?](https://github.com/nimroddolev/chime_tts/wiki/#what-is-chime-tts)
- [Features](https://github.com/nimroddolev/chime_tts/wiki/#features)
- [Quick Start](https://github.com/nimroddolev/chime_tts/wiki/#quick-start)
- [How Do I Use It?](https://github.com/nimroddolev/chime_tts/wiki/#how-do-i-use-it)
- [Discussion](https://github.com/nimroddolev/chime_tts/wiki/#support-and-discussion)
- [Show Your Support](https://github.com/nimroddolev/chime_tts/wiki/#show-your-support)

---

## What is Chime TTS?

### The Problem:

<source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/nimroddolev/chime_tts/main/images/wiki/home/no_chime_tts-dark.png">
<source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/nimroddolev/chime_tts/main/images/wiki/home/no_chime_tts-light.png">
<img alt="Latency is introduced between the notification chime and the TTS audio" src="https://raw.githubusercontent.com/nimroddolev/chime_tts/main/images/wiki/home/no_chime_tts-dark.png">

Home Assistant allows audio files and Text-To-Speech (TTS) audio messages to be played on speakers around your home. While TTS messages are a great way to provide real-time updates, by the time you realize a message is playing, you've missed the start of the message.

It makes sense to add a notification chime before the TTS audio, but in practice this introduces a delay between the two, caused by latency from network requests to the cloud TTS platform and latency from audio processing & networking before playback begins on the speakers.

### The Solution:

<source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/nimroddolev/chime_tts/main/images/wiki/home/wuth_chime_tts-dark.png">
<source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/nimroddolev/chime_tts/main/images/wiki/home/with_chime_tts-light.png">
<img alt="Chime TTS removes the latency between the notification chime and the TTS audio" src="https://raw.githubusercontent.com/nimroddolev/chime_tts/main/images/wiki/home/with_chime_tts-dark.png">

Chime TTS is a custom Home Assistant integration that solves this issue by stitching these audio files together. Chime TTS generates a single audio file locally on your Home Assistant device, and plays it to your speakers in a single event, eliminating any lag.

***

##  Features

Chime TTS offers various features that enhance TTS audio playback experience:

- **No lag or timing issues:** Precise timing between audio files without cloud TTS delays.
- **Customizable audio cues:** Play preset or custom audio before and after TTS messages.
- **Flexible TTS platform selection:** Supports various [TTS platform integrations](https://www.home-assistant.io/integrations/#text-to-speech).
- **Easy service invocation:** Use the 'chime_tts.say' service in automations and scripts.
- **Set media player notification volume:** Restore volume after playback.
- **Configurable TTS playback speed:** Set the TTS audio speed anywhere from 100-200%.
- **Configurable delay:** Set custom delays between audio and TTS.
- **Caching:** Cache audio for faster playback.
- **Speaker Groups:** Group speakers for simultaneous playback.

***

## Quick Start

Follow these easy steps to get started with Chime TTS:

1. [Installation](https://github.com/nimroddolev/chime_tts/wiki/Installation) - Quickly install Chime TTS via HACS or manually.
2. [Add the Integration](https://github.com/nimroddolev/chime_tts/wiki/Installation#2-add-the-chime-tts-integration) - Add Chime TTS to your Home Assistant instance.

***

## How Do I Use It?

Chime TTS adds two new services to your Home Assistant instance: `chime_tts.say` and `chime_tts.clear_cache`. Discover how you can use these services and the features they offer:

- [chime_tts.say](https://github.com/nimroddolev/chime_tts/wiki/chime_tts.say): Play audio and TTS messages with various settings.
- [chime_tts.clear_cache](https://github.com/nimroddolev/chime_tts/wiki/chime_tts.clear_cache): Clear generated audio cache.

***

## Support and Discussion

For questions, suggestions, and community discussion about Chime TTS, visit our [Community Forum](https://community.home-assistant.io/t/chime-tts-play-audio-before-after-tts-audio-lag-free/578430).

***

## Show Your Support

If you find Chime TTS useful, consider showing your support:
<a href="https://www.buymeacoffee.com/nimroddolev" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 30px !important;width: 140px !important;" ></a>

[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg?style=popout
[forum]: https://community.home-assistant.io/t/chime-tts-play-audio-before-after-tts-audio-lag-free/578430
