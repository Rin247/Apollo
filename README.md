# Apollo — Modular Media Player, System-Wide EQ, Transcoder & Tag Editor

Apollo is an enthusiast-grade, cross-platform media player, system-wide audio processing engine, transcoder, and metadata tag editor inspired by foobar2000, Poweramp, and MX Player. Built with Jetpack Compose & Media3 for Android and Qt 6 / C++20 for Desktop (with a **Vulkan 1.3 & DirectX 12_1** rendering architecture), Apollo is designed for audiophiles and power users seeking total audio control without telemetry or proprietary locks.

---

## ⚡ Core Subsystems & Status Matrix

| Subsystem | Features & Capabilities | Status / Roadmap |
|---|---|---|
| **Graphics Engine** | **Vulkan 1.3 & DirectX 12_1** desktop viewport | Active |
| **Audio Playback** | 32-bit float engine, gapless playback, FLAC/ALAC/WAV/AAC/MP3/Opus decoding | Active |
| **Audiophile Output** | Bit-perfect USB DAC passthrough, DSD / DoP native decoding, ReplayGain 2.0 | Roadmap |
| **DSP & Equalizer** | Parametric EQ, multi-band graphic EQ, spatializer, AutoEQ 10,000+ headphone presets | Active / Expanding |
| **System-Wide Audio** | System-wide global audio processing hook, convolution reverb, tube preamp | Roadmap |
| **Video Playback** | Hardware-accelerated video decoding, multi-track audio, ASS/SSA subtitle engine | Active |
| **Video Processing** | Custom shader post-processing, HDR10 tone mapping, PiP mode | Roadmap |
| **Tag Editor** | TagLib-backed ID3v2/Vorbis/FLAC editing, MusicBrainz/Discogs auto-tagging | Active / Expanding |
| **Transcoder** | FFmpeg batch audio/video converter, optical CD ripping engine | Active / Expanding |

---

## 🎵 Key Features & Module Breakdown

### 🎧 Audio Playback Engine (`player`)
- **Current**: High-fidelity gapless audio playback powered by Jetpack Media3, custom FFmpeg decoders, FLAC/ALAC/WAV/AAC/MP3/Opus format support, and 32-bit float audio pipeline.
- **Planned / Roadmap**: Bit-perfect USB DAC passthrough, DSD / DoP decoding, ReplayGain 2.0 automatic gain adjustment, and crossfade / gapless mixing engine.

### 🎛️ Equalizer & DSP Effects (`dsp`)
- **Current**: Parametric EQ, multi-band graphic equalizer, spatializer, and bass boost/virtualizer.
- **Planned / Roadmap**: System-wide global audio processing hook, AutoEQ headphone preset integration (10,000+ headphone models), convolution reverb, and tube preamp emulation.

### 🎬 Video Player (`video`)
- **Current**: Hardware-accelerated video playback with multi-track audio selection, subtitle rendering (ASS/SSA/SRT), and gesture-based playback controls.
- **Planned / Roadmap**: Picture-in-Picture (PiP), custom shader video post-processing, network stream playback (HLS/DASH/SMB), and HDR10 tone mapping.

### 🏷️ Tag Editor & Library Manager (`taglib`)
- **Current**: Fast ID3v2, Vorbis Comment, MP4, and FLAC metadata tag editing backed by TagLib.
- **Planned / Roadmap**: Batch tag editing, MusicBrainz / Discogs automated metadata lookup, embedded lyrics editor, and cover art downloader.

### 🔄 Transcoder & Converter (`transcoder`)
- **Current**: Local media format converter utilizing FFmpeg backend.
- **Planned / Roadmap**: High-speed batch audio/video transcoding preset manager, optical disc / CD ripping interface, and lossy-to-lossless format validator.

---

## 🏗️ Architecture & Technology Stack

- **Graphics APIs**: Vulkan 1.3 & DirectX 12_1.
- **Android App**: Kotlin, Jetpack Compose, Material 3, Hilt, Jetpack Media3, FFmpeg Kit, TagLib.
- **Desktop Shell**: C++20, Qt 6.12, QML, CMake.
- **Audio Engine**: Shared C++ DSP pipeline with low-latency audio buffers.
- **Licensing**: AGPL-3.0 copyleft protection.

---

## 🛠️ Building & Running

### Desktop (Windows)
```bat
build.bat Release
run.bat
```

### Android
```bash
./gradlew assembleDebug
```

---

## 📜 License

Apollo is released under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [`LICENSE`](LICENSE) for details.
