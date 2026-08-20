# Awesome Natural Speech2Speech (STS) [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated collection of state-of-the-art resources, models, and tools for building **natural, expressive, and ultra-low latency Speech-to-Speech (STS)** applications.

[STS (Speech-to-Speech)](#speech-to-speech-sts) · [STT (Speech-to-Text)](#speech-to-text-stt) · [TTS (Text-to-Speech)](#text-to-speech-tts) · [Voice Cloning](#voice-cloning) · [Audio Processing](#audio-processing--speech-enhancement) · [Quick Start](#quick-start) · [Use Cases](#use-cases--applications) · [Apps & Products](#apps--products) · [Tooling](#tooling--infrastructure) · [Datasets](#datasets) · [Learning](#learning-resources)

---

### The Evolution to Natural Speech-to-Speech (STS)
Historically, voice interfaces relied on **cascaded pipelines** (STT ➔ LLM ➔ TTS). While highly functional, this introduces significant latency (often >1.5s) and strips away the rich paralinguistic features of human voice—like tone, laughter, emotion, and interruptions. 

The state-of-the-art is rapidly evolving toward **native end-to-end Speech-to-Speech (STS)**, where multimodal models ingest audio tokens directly and output audio in real time. This repository serves as a developer map for navigating this landscape—bringing together both native end-to-end models and highly-optimized cascaded stacks to help developers build voice agents that feel completely natural, empathic, and human-like.

---

## Speech-to-Text (STT)

In a cascaded Speech-to-Speech pipeline, STT is the critical sensory input. To make the interaction feel natural, the transcription engine must be ultra-fast (sub-100ms first-chunk latency), resilient to background noise and varied accents, and support features like word-level timestamps or voice activity alignment.

### Open-Source Models

| Project | Architecture | Parameters | Languages | License |
|---------|-------------|------------|-----------|---------|
| [Whisper Large V3 (OpenAI)](https://github.com/openai/whisper) | Encoder-decoder Transformer | 1.55B | 99+ | MIT |
| [Whisper Large V3 Turbo](https://github.com/openai/whisper) | Reduced decoder layers | 809M | 99+ | MIT |
| [Faster-Whisper](https://github.com/SYSTRAN/faster-whisper) | CTranslate2-optimized Whisper | — | 99+ | MIT |
| [Distil-Whisper](https://github.com/huggingface/distil-whisper) | Distilled Whisper encoder-decoder | 756M | EN | MIT |
| [WhisperX](https://github.com/m-bain/whisperX) | Whisper + wav2vec2 alignment | — | Multi | BSD 2-Clause |
| [Parakeet TDT 0.6B (NVIDIA)](https://huggingface.co/nvidia/parakeet-tdt-0.6b-v2) | RNN Transducer | 600M | EN | — |
| [Parakeet TDT 1.1B (NVIDIA)](https://huggingface.co/nvidia/parakeet-tdt-1.1b) | RNN Transducer | 1.1B | EN | — |
| [NeMo (NVIDIA)](https://github.com/NVIDIA/NeMo) | Multi (Conformer-CTC, RNN-T) | — | Multi | Apache 2.0 |
| [Canary Qwen 2.5B (NVIDIA)](https://huggingface.co/nvidia/canary-qwen-2.5b) | SALM (Speech-Augmented LM) | 2.5B | EN | — |
| [Microsoft MAI-Transcribe-1](https://microsoft.ai/news/state-of-the-art-speech-recognition-with-mai-transcribe-1/) | — | — | Multi | — |
| [Cohere Transcribe](https://huggingface.co/CohereLabs/cohere-transcribe-03-2026) | Fast-Conformer + X-attention | 2B | 14 | Apache 2.0 |
| [IBM Granite Speech 3.3](https://huggingface.co/ibm-granite/granite-speech-3.3-8b) | — | 8B | EN, FR, DE, ES + JP/ZH translation | — |
| [SenseVoice](https://github.com/FunAudioLLM/SenseVoice) | — | — | Multi | MIT |
| [FunASR](https://github.com/modelscope/FunASR) | Paraformer, Conformer | — | Multi | MIT |
| [ESPnet](https://github.com/espnet/espnet) | Multi (Conformer, Transformer) | — | Multi | Apache 2.0 |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | Multi (Conformer, ECAPA) | — | Multi | Apache 2.0 |
| [Wav2Vec 2.0 XLSR (Meta)](https://github.com/facebookresearch/fairseq) | Self-supervised CNN-Transformer | — | 53+ | MIT |
| [Kaldi](https://github.com/kaldi-asr/kaldi) | HMM-DNN (C++) | — | Multi | Apache 2.0 |
| [k2 / Icefall](https://github.com/k2-fsa/icefall) | FSA-based recipes | — | Multi | Apache 2.0 |
| [Vosk](https://github.com/alphacep/vosk-api) | Kaldi-based | — | 20+ | Apache 2.0 |
| [Moonshine](https://github.com/usefulsensors/moonshine) | — | 27M | Edge-optimized | Apache 2.0 |
| [Silero Models](https://github.com/snakers4/silero-models) | — | — | Multi | — |
| [Coqui STT](https://github.com/coqui-ai/STT) | DeepSpeech (CTC) | — | Multi | MPL 2.0 |

### Cloud & Commercial APIs

| Service | Languages | Features | Pricing |
|---------|-----------|----------|---------|
| [Google Cloud Speech-to-Text](https://cloud.google.com/speech-to-text) | 125+ | Custom models, real-time/batch | $0.006/15s |
| [Azure Speech Service](https://azure.microsoft.com/products/ai-services/ai-speech/) | 100+ | Custom models, speaker ID | $1/hr |
| [Amazon Transcribe](https://aws.amazon.com/transcribe/) | 100+ | PII redaction, custom vocab | $0.024/min |
| [OpenAI Whisper API](https://platform.openai.com/docs/guides/speech-to-text) | 99+ | Transcription, translation | $0.006/min |
| [Deepgram](https://deepgram.com/) | 30+ | Custom models, summarization, PII redaction | $0.0043/min |
| [AssemblyAI](https://www.assemblyai.com/) | 18+ | Summarization, PII redaction, LLM integration | $0.00025/sec |
| [Speechmatics](https://www.speechmatics.com/) | 30+ | Diarization, real-time streaming | Custom |
| [Rev AI](https://www.rev.ai/) | 30+ | AI + human transcription | $0.005/sec |
| [Gladia Solaria](https://www.gladia.io/) | Multi | Universal model, real-time | Pay-per-char |
| [Gradium](https://gradium.ai/) | 5 | Real-time streaming, translation | Freemium |

### Architecture Reference

| Category | Models / Approaches |
|----------|-------------------|
| **Encoder-Decoder** | Whisper, Canary, Transformer-ASR, Listen Attend Spell |
| **CTC-based** | DeepSpeech, Jasper, QuartzNet, Conformer-CTC, Wav2Vec 2.0 |
| **RNN-T** | Transducer-based end-to-end, Emformer-RNNT, Parakeet TDT |
| **Hybrid** | HMM-DNN, Wav2Vec + CTC, HuBERT |
| **Streaming** | Emformer-RNNT, ContextNet, Chunk-based Conformer |

---

## Text-to-Speech (TTS)

TTS is the voice, emotion, and identity of the agent. Achieving a truly natural conversational experience requires synthesis engines that go beyond robotic readings. Modern TTS systems leverage flow matching or diffusion to support dynamic prosody, realistic breathing, contextual laughter, and ultra-low streaming latency.

### Open-Source Models

| Project | Architecture | Parameters | Languages | License |
|---------|-------------|------------|-----------|---------|
| [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) | Flow matching + LLM | — | 50+ | Apache 2.0 |
| [F5-TTS](https://github.com/SWivid/F5-TTS) | Flow matching | — | Multi | MIT |
| [Qwen3-TTS](https://github.com/QwenLM/Qwen3-TTS) | — | 0.6B, 1.7B | 10 | Apache 2.0 |
| [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) | GPT + VITS | — | Multi | MIT |
| [Fish Speech](https://github.com/fishaudio/fish-speech) | — | — | Multi | CC BY-NC-SA 4.0 |
| [Bark (Suno)](https://github.com/suno-ai/bark) | Transformer | — | Multi | MIT |
| [ChatTTS](https://github.com/2noise/ChatTTS) | Autoregressive | — | EN, ZH | CC BY-NC 4.0 |
| [StyleTTS 2](https://github.com/yl4579/StyleTTS2) | Style diffusion + GAN | — | EN | MIT |
| [VITS](https://github.com/jaywalnut310/vits) | VAE + GAN | — | Multi | MIT |
| [Piper](https://github.com/rhasspy/piper) | VITS-based | — | Multi | MIT |
| [MeloTTS](https://github.com/myshell-ai/MeloTTS) | — | — | EN, ES, FR, ZH, JP, KR | MIT |
| [Kokoro](https://github.com/hexgrad/kokoro) | — | 82M | EN | Apache 2.0 |
| [MetaVoice-1B](https://github.com/metavoiceio/metavoice-src) | Transformer | 1.2B | EN | Apache 2.0 |
| [Mistral Voxtral TTS](https://huggingface.co/mistralai/Voxtral-4B-TTS-2603) | — | 4B | Multi | Apache 2.0 |
| [Chatterbox (Resemble AI)](https://github.com/resemble-ai/chatterbox) | — | — | 23+ | MIT |
| [Tortoise-TTS](https://github.com/neonbjb/tortoise-tts) | Autoregressive + diffusion | — | EN | Apache 2.0 |
| [Sesame CSM](https://github.com/SesameAILabs/csm) | — | — | EN | — |
| [Hume TADA](https://github.com/HumeAI/tada) | LLM-based | — | Multi | — |
| [IndexTTS 2](https://github.com/index-tts/index-tts) | — | — | EN, ZH | Apache 2.0 |
| [KaniTTS2](https://github.com/rhasspy/kani) | — | 400M | EN | — |
| [Silma TTS](https://github.com/SILMA-AI/silma-tts) | — | — | EN, ES | Apache 2.0 |
| [VoxCPM](https://github.com/OpenBMB/VoxCPM) | — | — | Multi | MIT |
| [MOSS-TTS](https://github.com/OpenMOSS/MOSS-TTS) | — | — | Multi | — |
| [Ming-omni-tts](https://github.com/inclusionAI/Ming-omni-tts) | — | — | Multi | — |
| [OpenVoice](https://github.com/myshell-ai/OpenVoice) | — | — | Multi | MIT |
| [Parler-TTS](https://github.com/huggingface/parler-tts) | — | — | EN | Apache 2.0 |
| [OmniVoice](https://github.com/k2-fsa/OmniVoice) | Diffusion language model | — | 600+ | Apache 2.0 |

### API Wrappers & Related Projects

| Project | Description |
|---------|-------------|
| [Edge-TTS](https://github.com/rany2/edge-tts) | Free Microsoft Edge TTS API wrapper, no API key required |
| [tortoise-tts-fast](https://github.com/152334H/tortoise-tts-fast) | Faster inference for Tortoise-TTS with optimized pipelines |
| [xTTS](https://github.com/daswer123/xtts-api-server) | REST API server for Coqui XTTS with streaming support |

### Cloud & Commercial APIs

| Service | Languages | Voice Cloning | Streaming | Pricing |
|---------|-----------|--------------|-----------|---------|
| [ElevenLabs](https://elevenlabs.io/) | 70+ | Yes (3min sample) | Yes (~200ms) | $0.10/min |
| [Cartesia Sonic-3](https://cartesia.ai/) | 40+ | Yes (15s sample) | Yes (40ms) | Pay-per-char |
| [OpenAI TTS](https://platform.openai.com/docs/guides/text-to-speech) | Multi | No | Yes (~300ms) | Pay-per-char |
| [Google Cloud TTS](https://cloud.google.com/text-to-speech) | 220+ | No | Yes (~200ms) | Pay-per-char |
| [Azure AI Speech](https://azure.microsoft.com/products/ai-services/ai-speech/) | 100+ | Yes (Personal Voice) | Yes | Pay-per-char |
| [Amazon Polly](https://aws.amazon.com/polly/) | 50+ | Yes (Neural) | Yes | $4-100/1M chars |
| [Fish Audio](https://fish.audio/) | Multi | Yes (10-30s) | Yes (~250ms) | Freemium |
| [PlayHT](https://play.ht/) | 142 | Yes (instant) | Yes (~300ms) | $39-99/mo |
| [Deepgram Aura-2](https://deepgram.com/) | 7 + 40 English accents | No | Yes (90ms) | $0.03/1k chars |
| [Resemble AI](https://www.resemble.ai/) | Multi | Yes (10s sample) | Yes (~200ms) | Enterprise |
| [Gradium](https://gradium.ai/) | 5 | Yes (instant) | Yes (158ms P50) | Freemium |

### Architecture Reference

| Category | Models / Approaches |
|----------|-------------------|
| **Autoregressive** | Tacotron, Tacotron2, VITS, Bark, WaveNet, Tortoise-TTS |
| **Non-Autoregressive** | FastSpeech, FastSpeech 2, ParaNet, FastPitch, Aligner TTS |
| **Flow-based** | Glow-TTS, Flowtron, F5-TTS, CosyVoice 2 |
| **GAN-based** | HiFi-GAN, MelGAN, BigVGAN, UnivNet |
| **Diffusion** | StyleTTS 2, OmniVoice, CosyVoice 2, Tortoise-TTS |
| **Vocoders** | WaveNet, WaveRNN, HiFi-GAN, MelGAN, Parallel WaveGAN, LPCNet, BigVGAN |
| **Formant Synthesis** | eSpeak NG, Festival |

---

## Speech-to-Speech (STS)

Speech-to-Speech (or Speech2Speech) is the ultimate frontier of conversational AI. This section highlights native end-to-end audio models (direct audio-to-audio mapping), real-time voice conversion tools, and the orchestrators and platforms needed to coordinate real-time full-duplex dialogues.

### Open-Source Models

| Project | Architecture | Parameters | Key Features | License |
|---------|-------------|------------|--------------|---------|
| [GLM-4-Voice](https://github.com/THUDM/GLM-4-Voice) | Whisper + GLM + CosyVoice | 9B | End-to-end bilingual conversational, emotional control | Apache 2.0 |
| [Moshi (Kyutai)](https://github.com/kyutai-labs/moshi) | Mimi audio codec + Helium LLM | — | Full-duplex conversational, expressive inner monologue | CC-BY-4.0 |
| [Mini-Omni](https://github.com/gpt-omni/mini-omni) | Text-instructed speech LLM | — | Low-latency speech-to-speech, parallel streaming | MIT |
| [Ultravox](https://github.com/fixie-ai/ultravox) | Multimodal projector + Llama/Gemma | — | Real-time speech tokenization, direct audio input | Apache 2.0 |
| [WhisperSpeech](https://github.com/WhisperSpeech/WhisperSpeech) | Audio-to-audio Transformer | — | End-to-end speech-to-speech translation | MIT |

### Voice Conversion

| Tool | Description | License |
|------|-------------|---------|
| [RVC](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) | Retrieval-based voice conversion with GUI | MIT |
| [FreeVC](https://github.com/jjery2243542/FreeVC) | High-quality text-free one-shot voice conversion | MIT |
| [so-vits-svc](https://github.com/svc-develop-team/so-vits-svc) | Singing voice conversion using VITS | MIT |
| [MetaVoice STS](https://github.com/metavoiceio/metavoice-src) | Speech-to-speech with tone color preservation | Apache 2.0 |

### Cloud & Commercial APIs

| Service | Latency | Features | Pricing |
|---------|---------|----------|---------|
| [Gemini Multimodal Live API](https://ai.google.dev/api/live) | Low (<300ms) | Native audio/text input & output, multi-turn dialogue | Pay-per-token |
| [OpenAI Realtime API](https://platform.openai.com/docs/guides/realtime) | Low (~300ms) | Multimodal speech-to-speech, function calling | $0.06/min input, $0.24/min output |
| [Hume EVI](https://hume.ai/) | Ultra-low (~200ms) | Empathic voice interface, emotion detection | $0.072/min |
| [Gradium Live Translation](https://gradium.ai/) | Low (streaming) | Live speech-to-speech translation across en/fr/de/es/pt | 45k credits free, ~$0.10/min |

### AI Voice Agent Platforms

| Platform | Type | Description |
|----------|------|-------------|
| [LiveKit Agents](https://github.com/livekit/agents) | Open-Source | Framework and WebRTC infrastructure for real-time voice agents |
| [Vapi](https://vapi.ai/) | Commercial | Inbound/outbound conversational voice agent platform |
| [Retell AI](https://www.retellai.com/) | Commercial | High-performance conversational voice agent API |
| [Bland AI](https://www.bland.ai/) | Commercial | Enterprise API for outbound/inbound phone agents |
| [Play AI](https://play.ai/) | Commercial | Platform for building conversational voice agents |
| [Synthflow AI](https://synthflow.ai/) | Commercial | No-code voice agent builder for SMBs |

---

## Voice Cloning

Custom personalities and emotional resonance make speech interactions feel truly personal. Modern voice cloning allows you to replicate a voice persona—retaining accent, tone, and vocal texture—from reference clips as short as three seconds.

| Tool | Clone From | Languages | License |
|------|-----------|-----------|---------|
| [OpenVoice V2](https://github.com/myshell-ai/OpenVoice) | ~5 seconds | Multi | MIT |
| [Chatterbox](https://github.com/resemble-ai/chatterbox) | 5 seconds | 23+ | MIT |
| [Qwen3-TTS](https://github.com/QwenLM/Qwen3-TTS) | 3 seconds | 10 | Apache 2.0 |
| [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) | 3-10 seconds | 50+ | Apache 2.0 |
| [F5-TTS](https://github.com/SWivid/F5-TTS) | ~10 seconds | Multi | MIT |
| [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) | ~10 seconds | Multi | MIT |
| [Fish Speech V1.5](https://github.com/fishaudio/fish-speech) | 10-30 seconds | Multi | CC BY-NC-SA 4.0 |
| [IndexTTS 2](https://github.com/index-tts/index-tts) | ~10 seconds | EN, ZH | Apache 2.0 |
| [XTTS-v2 (Coqui)](https://github.com/coqui-ai/TTS) | 6 seconds | 16+ | MPL 2.0 |
| [Tortoise-TTS](https://github.com/neonbjb/tortoise-tts) | ~30 seconds | EN | Apache 2.0 |
| [ElevenLabs](https://elevenlabs.io/) | 3 minutes | 70+ | Proprietary |

---

## Audio Processing & Speech Enhancement

Real-world voice interactions happen in noisy environments. The tools below are crucial for filtering out ambient noise, detecting when a user starts/stops speaking (Voice Activity Detection), and identifying different speakers (Diarization) to ensure natural, seamless turn-taking.

### Noise Suppression & Enhancement

| Tool | Description | License |
|------|-------------|---------|
| [AudioSep](https://github.com/Audio-AGI/AudioSep) | Separate audio with natural language queries | — |
| [DeepFilterNet](https://github.com/Rikorose/DeepFilterNet) | Speech enhancement using deep filtering | Apache 2.0 |
| [Demucs (Meta)](https://github.com/facebookresearch/demucs) | Music/source separation | MIT |
| [RNNoise](https://github.com/xiph/rnnoise) | Recurrent neural network noise reduction | BSD |
| [Spleeter (Deezer)](https://github.com/deezer/spleeter) | Source separation with pretrained models | MIT |
| [VoiceFixer](https://github.com/haoheliu/voicefixer) | Speech quality restoration | MIT |

### Voice Activity Detection (VAD)

| Tool | Description | License |
|------|-------------|---------|
| [Silero VAD](https://github.com/snakers4/silero-vad) | Pretrained VAD model | MIT |
| [WebRTC VAD](https://github.com/wiseman/py-webrtcvad) | VAD from WebRTC project | BSD |
| [PyAnnote VAD](https://github.com/pyannote/pyannote-audio) | Neural VAD as part of pyannote ecosystem | MIT |

### Speaker Diarization

| Tool | Description | License |
|------|-------------|---------|
| [pyannote.audio](https://github.com/pyannote/pyannote-audio) | Speaker diarization toolkit (v3.1) | MIT |
| [WhisperX](https://github.com/m-bain/whisperX) | Diarization via wav2vec2 alignment | BSD 2-Clause |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | Built-in diarization module | Apache 2.0 |
| [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) | MSDD (Multi-scale Diarization Decoder) | Apache 2.0 |

---

## Quick Start Guides

Building a natural speech-to-speech application typically requires choosing between an **Online-First (API-driven)** or **Offline-First (Self-hosted)** architecture. Below are the recommended minimal and optimal setups to achieve ultra-low latency and maximum naturalness.

### Summary of Recommended Architectures

| Architecture | Tier | STT Component | LLM Component | TTS Component | Key Characteristics |
|--------------|------|---------------|---------------|---------------|---------------------|
| **Online-First** | **Minimal (Cascaded)** | [Deepgram Nova-2](https://deepgram.com) | [Gemini Flash](https://ai.google.dev/) or [GPT-4o-mini](https://openai.com) | [Cartesia Sonic](https://cartesia.ai) or [ElevenLabs](https://elevenlabs.io) | Low latency, stateless APIs, highest quality, zero host hosting requirements |
| | **Optimal (Real-time STS)** | [OpenAI Realtime](https://openai.com) or [Gemini Live](https://ai.google.dev/) | Native / Multimodal | [OpenAI Realtime](https://openai.com) or [Gemini Live](https://ai.google.dev/) | Ultra-low latency (<300ms), full-duplex conversations, expressive tone |
| **Offline-First** | **Minimal (CPU/Edge)** | [Moonshine](https://github.com/usefulsensors/moonshine) or Whisper-Base | [Llama-3.2-1B-Instruct](https://huggingface.co/meta-llama/Llama-3.2-1B-Instruct) (Ollama) | [Kokoro-82M](https://github.com/hexgrad/kokoro) or [Piper](https://github.com/rhasspy/piper) | Run on standard CPU (laptops/Pi), fully offline, zero API costs |
| | **Optimal (GPU/Server)** | [Whisper Large V3 Turbo](https://github.com/openai/whisper) via Faster-Whisper | [Qwen-2.5-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-7B-Instruct) or [Llama-3.1-8B](https://huggingface.co/meta-llama/Llama-3.1-8B-Instruct) | [F5-TTS](https://github.com/SWivid/F5-TTS) or [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) | Dedicated local GPU server, zero-shot voice cloning, professional quality |

### Language-Specific Recommendations

Depending on your target audience, select the appropriate regional optimizations:

| Target Language | Focus Area | Recommended STT | Recommended LLM | Recommended TTS | Local (Offline) Alternative |
|-----------------|------------|-----------------|-----------------|-----------------|----------------------------|
| **English-Focused** | High-speed, natural intonation, multiple dialects (US/UK/AU) | [Deepgram Nova-2 (EN)](https://deepgram.com) | [Gemini Flash](https://ai.google.dev/) or [GPT-4o-mini](https://openai.com) | [Cartesia Sonic](https://cartesia.ai) or [ElevenLabs](https://elevenlabs.io) | **STT**: [Distil-Whisper](https://github.com/huggingface/distil-whisper) <br>**TTS**: [Kokoro-82M](https://github.com/hexgrad/kokoro) (US/UK voices) or [StyleTTS 2](https://github.com/yl4579/StyleTTS2) |
| **Japanese-Focused** | Accurate pitch accent, kanji/kana context, culturally natural prosody | [Kotoba-Whisper](https://huggingface.co/kotoba-tech) or Google Cloud STT | [Qwen-2.5-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-7B-Instruct) or [Llama-3-Swallow](https://github.com/tokyotech-llm/swallow) | [VOICEVOX](https://github.com/voicevox/voicevox) (anime/character voices) or ElevenLabs JP | **STT**: [Kotoba-Whisper-Base](https://huggingface.co/kotoba-tech) <br>**TTS**: [VOICEVOX](https://github.com/voicevox/voicevox) or [Tsukasa-Speech](https://huggingface.co/tsukasa-speech) (StyleTTS2 JP) |
| **Multilingual** | Dynamic language switching, accent preservation, cross-lingual voice cloning | [Whisper Large V3](https://github.com/openai/whisper) or [SenseVoice-Small](https://github.com/FunAudioLLM/SenseVoice) | [GPT-4o](https://openai.com) or [Qwen-2.5-72B-Instruct](https://huggingface.co/Qwen/Qwen2.5-72B-Instruct) | [ElevenLabs Multilingual V2](https://elevenlabs.io) or [Fish Audio](https://fish.audio) | **STT**: [SenseVoice](https://github.com/FunAudioLLM/SenseVoice) (extremely fast JP/ZH/EN/KO) <br>**TTS**: [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) or [Coqui XTTS-v2](https://github.com/coqui-ai/TTS) |

---

### Online-First Setup (Cloud APIs)

> Requires active internet connection. Zero local hosting requirements, fastest to deploy, and uses top-tier foundational models.

#### Minimal Setup (Cascaded API Pipeline)
A straightforward HTTP-based pipeline where components are called sequentially.

```bash
pip install deepgram-sdk openai cartesia
```

```python
import os
from deepgram import DeepgramClient, PrerecordedOptions
from openai import OpenAI
from cartesia import Cartesia

# 1. Speech-to-Text (Deepgram Nova-2)
dg_client = DeepgramClient(os.getenv("DEEPGRAM_API_KEY"))
with open("input.wav", "rb") as audio:
    response = dg_client.listen.prerecorded.v("1").transcribe_file(
        {"buffer": audio.read()}, 
        PrerecordedOptions(model="nova-2", smart_format=True)
    )
user_text = response.results.channels[0].alternatives[0].transcript
print(f"User: {user_text}")

# 2. LLM Reasoning (OpenAI GPT-4o-mini)
openai_client = OpenAI()
completion = openai_client.chat.completions.create(
    model="gpt-4o-mini",
    messages=[{"role": "user", "content": user_text}]
)
assistant_text = completion.choices[0].message.content
print(f"Assistant: {assistant_text}")

# 3. Text-to-Speech (Cartesia Sonic-3)
cartesia_client = Cartesia(api_key=os.getenv("CARTESIA_API_KEY"))
output = cartesia_client.tts.sse(
    model_id="sonic-english",
    transcript=assistant_text,
    voice_id="a0e9987c-abaf-4752-9097-f58c7e2261b5", # Sonic Default Male
    output_format={"container": "raw", "encoding": "pcm_f32le", "sample_rate": 44100}
)
# (In production, stream output chunks directly to audio output device)
```

#### Optimal Setup (Real-time Speech-to-Speech Agent)
A persistent, full-duplex WebRTC agent built on the LiveKit framework.

```bash
pip install livekit-agents livekit-plugins-deepgram livekit-plugins-cartesia livekit-plugins-openai
```

```python
from livekit.agents import Agent, AgentSession, AgentServer

class Assistant(Agent):
    def __init__(self):
        super().__init__(instructions="You are a helpful voice assistant.")

server = AgentServer()

@server.rtc_session(agent_name="voice-agent")
async def run_agent(ctx):
    session = AgentSession(
        stt="deepgram/nova-3:multi",
        llm="openai/gpt-4o-mini",
        tts="cartesia/sonic-3:<voice-uuid>",
    )
    await session.start(room=ctx.room, agent=Assistant())
    await session.generate_reply()
```

#### Cost Reference

| Service | STT | TTS |
|---------|-----|-----|
| OpenAI | $0.006/min | $0.015 - $0.030 / 1k chars |
| Deepgram | $0.0043/min | $0.015 / 1k chars (Aura-2) |
| ElevenLabs | — | $0.10/min (or $0.15 - $0.24 / 1k chars) |
| Cartesia | — | $0.05 / 1k chars |

---

### Offline-First Setup (Self-Hosted)

> No internet required after downloading models. Best for data privacy, air-gapped environments, and zero operational API fees.

#### Minimal Setup (CPU & Edge Optimized)
Designed to run efficiently on low-resource machines (laptops, Raspberry Pi, edge devices).

```bash
pip install faster-whisper ollama kokoro-onnx soundfile
```

```python
from faster_whisper import WhisperModel
import ollama
from kokoro_onnx import Kokoro
import soundfile as sf

# 1. Local STT (Faster-Whisper Tiny on CPU)
stt_model = WhisperModel("tiny", device="cpu", compute_type="int8")
segments, _ = stt_model.transcribe("input.wav")
user_text = "".join([seg.text for seg in segments])
print(f"User: {user_text}")

# 2. Local LLM (Ollama Llama 3.2 1B)
response = ollama.chat(
    model="llama3.2:1b",
    messages=[{"role": "user", "content": user_text}]
)
assistant_text = response["message"]["content"]
print(f"Assistant: {assistant_text}")

# 3. Local TTS (Kokoro 82M ONNX - highly optimized for CPU)
# Download model and voices json from: https://github.com/hexgrad/kokoro
kokoro = Kokoro("kokoro-v0_19.onnx", "voices.json")
samples, sample_rate = kokoro.create(
    assistant_text, voice="af_bella", speed=1.0, lang="en-us"
)
sf.write("output.wav", samples, sample_rate)
```

#### Optimal Setup (GPU Server)
Designed for dedicated GPU instances (e.g. RTX 4090, A10G) to provide near-instantaneous response times and expressive, natural voice cloning.

```bash
pip install faster-whisper openai f5-tts
```

```python
from faster_whisper import WhisperModel
from openai import OpenAI
from f5_tts.api import F5TTS

# 1. Local GPU STT (Faster-Whisper Large V3 Turbo)
stt_model = WhisperModel("large-v3-turbo", device="cuda", compute_type="float16")
segments, _ = stt_model.transcribe("input.wav")
user_text = "".join([seg.text for seg in segments])
print(f"User: {user_text}")

# 2. Local GPU LLM (vLLM OpenAI-Compatible Server hosting Qwen 2.5 7B)
openai_client = OpenAI(base_url="http://localhost:8000/v1", api_key="none")
completion = openai_client.chat.completions.create(
    model="qwen-2.5-7b-instruct",
    messages=[{"role": "user", "content": user_text}]
)
assistant_text = completion.choices[0].message.content
print(f"Assistant: {assistant_text}")

# 3. Local Expressive TTS (F5-TTS Zero-Shot Voice Cloning on GPU)
f5tts = F5TTS()
f5tts.generate(
    gen_text=assistant_text,
    ref_audio="reference_voice.wav", # 3-10s voice clone sample
    ref_text="Reference speech transcription",
    file_wave="output.wav"
)
```

#### Model Size vs Quality Reference

| Model | Parameters / Size | Speed | Quality | Ideal Platform |
|-------|-------------------|-------|---------|----------------|
| Whisper `tiny` | 39M | Extremely Fast | Fair | CPU / Edge / Mobiles |
| Whisper `base` | 74M | Fast | Good | CPU / Laptops |
| Whisper `large-v3-turbo` | 809M | Very Fast (on GPU) | Excellent | GPU Server |
| Whisper `large-v3` | 1.55B | Moderate | Best | High-end GPU |
| Piper TTS | ~50M | Extremely Fast | Good | Raspberry Pi / CPU |
| Kokoro TTS | 82M | Very Fast | Excellent | CPU / Edge |
| Coqui XTTS-v2 | 2.3B | Slow | Excellent | Mid-tier GPU |
| F5-TTS | 385M | Fast (on GPU) | State-of-the-Art | GPU (Zero-shot cloning) |

#### Deployment & Inference Serving

| Tool | Purpose | Supported Technologies |
|------|---------|------------------------|
| [Ollama](https://github.com/ollama/ollama) | Easy local LLM deployment (CPU/GPU) | Llama 3.2, Qwen 2.5, Gemma |
| [vLLM](https://github.com/vllm-project/vllm) | High-throughput production LLM serving | Llama, Qwen, Mistral |
| [CTranslate2](https://github.com/OpenNMT/CTranslate2) | Highly optimized fast Whisper inference | Whisper models |
| [ONNX Runtime](https://github.com/microsoft/onnxruntime) | CPU/GPU cross-platform edge execution | Kokoro TTS, Piper, Whispers |
| [TensorRT](https://developer.nvidia.com/tensorrt) | Ultra-low latency NVIDIA GPU inference | Whisper, LLMs |
| [OpenVINO](https://github.com/openvinotoolkit/openvino) | Intel hardware execution optimization | Whispers, LLMs |

---

### Language-Focused Setups

#### English-First Setup

> Optimized for English-only applications. Best quality-to-resource ratio for English speakers.

```bash
pip install faster-whisper piper-tts kokoro-onnx
```

```python
from faster_whisper import WhisperModel
from kokoro_onnx import Kokoro
import soundfile as sf

# STT — English-optimized
stt = WhisperModel("large-v3-turbo", device="cuda", compute_type="float16")
segments, _ = stt.transcribe("audio.mp3", language="en")
text = " ".join([seg.text for seg in segments])

# TTS — English with natural prosody
kokoro = Kokoro("kokoro-v0_19.onnx", "voices.json")
samples, sr = kokoro.create(text, voice="af_bella", speed=1.0, lang="en-us")
sf.write("output.wav", samples, sr)
```

| Component | Recommended | Alternative |
|-----------|-------------|-------------|
| STT | Whisper large-v3-turbo | Parakeet TDT 0.6B |
| TTS | Kokoro 82M | Piper lessac, StyleTTS 2 |
| LLM | Llama 3.2 1B (Ollama) | Qwen 2.5 7B |
| Voice Cloning | Chatterbox, F5-TTS | GPT-SoVITS, XTTS-v2 |

---

#### Japanese-First Setup

> Optimized for Japanese speech recognition and synthesis. Includes Japanese-specific models and character handling.

```bash
pip install faster-whisper open-jtalk pyopenjtalk
```

```python
from faster_whisper import WhisperModel

# STT — Japanese (Whisper supports Japanese natively)
stt = WhisperModel("large-v3", device="cuda", compute_type="float16")
segments, _ = stt.transcribe("audio_ja.mp3", language="ja")
text = " ".join([seg.text for seg in segments])
```

| Component | Recommended | Alternative |
|-----------|-------------|-------------|
| STT | Whisper large-v3 (language="ja") | VoicePeaker |
| TTS | VoicePeaker | Coqui TTS (jvs-vctk) |
| TTS (formant) | Open JTalk | pyopenjtalk |
| LLM | Qwen 2.5 (supports Japanese) | Llama 3.1 (via translation) |
| Voice Cloning | GPT-SoVITS | CosyVoice 2 (50+ langs) |
| Datasets | JVS Corpus (30h, 100 speakers) | Common Voice Japanese |

> **Note:** Whisper's Japanese recognition is strong but benefits from `condition_on_previous_text=False` for long-form Japanese to prevent hallucination loops. For TTS, VoicePeaker provides natural Japanese prosody with native phoneme handling.

---

#### Multilingual Setup

> Supports 50+ languages with automatic language detection. Best for global applications.

```bash
pip install faster-whisper CosyVoice
```

```python
from faster_whisper import WhisperModel

# STT — Auto-detect language, transcribe in detected language
stt = WhisperModel("large-v3", device="cuda", compute_type="float16")
segments, info = stt.transcribe("audio.mp3")  # auto-detect language
print(f"Detected language: {info.language} ({info.language_probability:.2f})")
text = " ".join([seg.text for seg in segments])

# TTS — Multilingual (CosyVoice supports 50+ languages)
# CosyVoice handles code-switching within a single utterance
```

| Component | Languages | Recommended |
|-----------|-----------|-------------|
| STT | 99+ | Whisper large-v3 (auto-detect) |
| STT (fast) | 99+ | Whisper large-v3-turbo |
| TTS | 50+ | CosyVoice 2 (flow matching + LLM) |
| TTS | 100+ | Coqui TTS (XTTS-v2) |
| TTS (edge) | 600+ | OmniVoice |
| Voice Cloning | Multi | CosyVoice 2 (3-10s sample) |
| LLM | Multi | Qwen 2.5 7B (strong multilingual) |

> **Key Difference:** Multilingual setups use models trained on diverse language data. Whisper's `large-v3` has the best multilingual support (99 languages). For TTS, CosyVoice 2 and Coqui XTTS-v2 support voice cloning across languages — clone a voice from English audio, generate Japanese speech.

---

#### Language Support Matrix

| Model | STT Languages | TTS Languages | Voice Cloning |
|-------|---------------|---------------|---------------|
| Whisper large-v3 | 99 | — | — |
| Parakeet TDT | 1 (EN) | — | — |
| Kokoro | — | EN | No |
| Piper | — | Multi (varies by voice) | No |
| CosyVoice 2 | — | 50+ | Yes (cross-lingual) |
| Coqui XTTS-v2 | — | 16+ | Yes (6s reference) |
| VoicePeaker | — | JA | No |
| GPT-SoVITS | — | Multi | Yes (~10s reference) |
| F5-TTS | — | Multi | Yes (~10s reference) |

---

## Use Cases & Applications

Natural speech-to-speech technologies are transforming how we interact with machines and each other. Here is how these building blocks are applied across industries.

### Speech-to-Text Use Cases

| Use Case | Description | Tools |
|----------|-------------|-------|
| **Meeting Transcription** | Multi-speaker meetings with speaker labels | WhisperX, Cohere Transcribe |
| **Customer Service** | Real-time call transcription, intent detection | Deepgram, Google Cloud STT |
| **Medical Documentation** | Automated clinical notes, HIPAA-compliant | Whisper V3, AssemblyAI, Azure Speech |
| **Legal Discovery** | Searchable text from audio evidence, PII redaction | AssemblyAI, Rev AI, Speechmatics |
| **Education** | Automatic captioning, lecture transcription | Whisper V3, Vosk (offline) |
| **Live Captioning** | Low-latency captions for broadcasts | Parakeet TDT, Deepgram |
| **Video Content** | Captions, timestamps, content repurposing | Whisper V3, Gladia Solaria |
| **Market Research** | Extract insights from customer interactions | AssemblyAI, Deepgram |
| **Call Analysis** | Sentiment analysis, key phrase detection | AssemblyAI, WhisperX |
| **Sales Intelligence** | Capture and analyze sales calls | AssemblyAI, WhisperX |

### Text-to-Speech Use Cases

| Use Case | Description | Tools |
|----------|-------------|-------|
| **Accessibility** | Screen readers, visual impairment aids, WCAG compliance | Piper, eSpeak NG, Coqui TTS |
| **Audiobook Narration** | Large-scale audio book production | ElevenLabs, Fish Audio, StyleTTS 2 |
| **Voice Assistants** | AI voice responses for apps | OpenAI TTS, Qwen3-TTS, Chatterbox |
| **Content Localization** | Dubbing video content into multiple languages | ElevenLabs AI Dubbing, Coqui TTS |
| **E-Learning** | Audio lessons, pronunciation training | MeloTTS, Coqui TTS, Azure AI Speech |
| **Video Production** | Voiceovers for YouTube, ads, social content | ElevenLabs, Fish Audio, CosyVoice 2 |
| **Gaming & Storytelling** | Dynamic real-time dialogue | Cartesia Sonic-3, Bark, ChatTTS |
| **News & Articles** | Convert written content to audio | Coqui TTS, OpenAI TTS |
| **GPS Navigation** | Spoken directions and traffic alerts | Piper (offline), eSpeak NG |
| **Customer Support IVR** | Dynamic menus and account details | Deepgram Aura-2, Amazon Polly |

### Combined STT + TTS Patterns

| Pattern | Description | Example Stack |
|---------|-------------|---------------|
| **Voice Agent** | Speech → STT → LLM → TTS → Speech | Whisper → GPT-4 → Cartesia |
| **Real-Time Translation** | Speech → STT → Translate → TTS | Whisper → Translation → Coqui TTS |
| **Meeting Summarizer** | Audio → STT → LLM Summary → TTS | WhisperX → LLM → ElevenLabs |
| **Podcast Search** | Podcast → STT → Text Search → Timestamps | Faster-Whisper → Elasticsearch |
| **Voice Memo Assistant** | Voice → STT → NLP Extraction → Notes | Whisper → NLP Pipeline |

---

## Apps & Products

A collection of frameworks, applications, and commercial services showcasing natural voice AI in action.

### Open-Source Applications

| App | Description | Tech Stack |
|-----|-------------|------------|
| [LiveKit Agents](https://github.com/livekit/agents) | Framework for real-time voice agents | Deepgram, Cartesia, OpenAI |
| [Open WebUI](https://github.com/open-webui/open-webui) | Chat interface with TTS/STT integration | Whisper, Coqui TTS |
| [Faster-Whisper-Transcriber](https://github.com/oliverguhr/faster-whisper-server) | REST API server for Faster-Whisper | Faster-Whisper |
| [GPT-SoVITS WebUI](https://github.com/RVC-Boss/GPT-SoVITS) | Web interface for few-shot voice cloning | GPT-SoVITS |
| [Kokoro WebUI](https://github.com/nazdridoy/kokoro-webui) | Web interface for Kokoro TTS | Kokoro |
| [AllTalk TTS](https://github.com/erew123/alltalk_tts) | TTS extension for text generation web UIs | Coqui TTS, Piper, gTTS |
| [Bark UI](https://github.com/camenduru/bark-ui) | Web interface for Bark | Bark |
| [RVC WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) | Web interface for voice conversion | RVC |
| [WhisperX](https://github.com/m-bain/whisperX) | CLI tool for transcription with diarization | Whisper + pyannote |
| [Pinokio](https://github.com/pinokio-computer/pinokio) | One-click installer for AI apps | Multiple |

### Notable Commercial Products

| Product | Category | Description |
|---------|----------|-------------|
| [ElevenLabs](https://elevenlabs.io/) | Voice Platform | Voice cloning, dubbing, reader app |
| [Descript](https://descript.com) | Audio/Video Editing | Edit audio by editing text, overdub with cloned voice |
| [Otter.ai](https://otter.ai) | Meeting Transcription | Real-time transcription with AI summaries |
| [Fireflies.ai](https://fireflies.ai/) | Meeting Assistant | AI notetaker for meetings |
| [Speechify](https://speechify.com/) | Text-to-Speech Reader | Read articles, PDFs, books aloud |
| [Murf AI](https://murf.ai/) | Voice Generator | Voiceover generation |
| [Sonix](https://sonix.ai/) | Transcription | Automated transcription with translation |
| [Trint](https://trint.com/) | Transcription | AI transcription with collaborative editing |

---

## Tooling & Infrastructure

Low-latency audio streaming requires specialized plumbing. These frameworks and libraries form the backbone of modern audio manipulation and model deployment.

### Speech Frameworks

| Framework | Description | License |
|-----------|-------------|---------|
| [ESPnet](https://github.com/espnet/espnet) | End-to-end speech processing (ASR + TTS + ST) | Apache 2.0 |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | PyTorch speech toolkit | Apache 2.0 |
| [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) | Platform for ASR, TTS, and NLP | Apache 2.0 |
| [Kaldi](https://github.com/kaldi-asr/kaldi) | ASR toolkit (C++) | Apache 2.0 |
| [k2 / Icefall](https://github.com/k2-fsa/icefall) | FSA-based ASR recipes | Apache 2.0 |
| [Fairseq (Meta)](https://github.com/facebookresearch/fairseq) | Sequence modeling including Wav2Vec | MIT |
| [TTS Server / AllTalk](https://github.com/erew123/alltalk_tts) | TTS integration for text generation UIs | AGPL v3 |

### Audio Libraries

| Library | Purpose | License |
|---------|---------|---------|
| [FFmpeg](https://ffmpeg.org/) | Audio/video processing | LGPL/GPL |
| [Librosa](https://github.com/librosa/librosa) | Audio and music analysis | ISC |
| [Torchaudio](https://github.com/pytorch/audio) | PyTorch audio I/O, transforms, models | BSD |
| [SoundFile](https://github.com/bastibe/python-soundfile) | Audio file I/O via libsndfile | BSD |
| [pydub](https://github.com/jiaaro/pydub) | Audio manipulation | MIT |
| [Hugging Face Transformers](https://github.com/huggingface/transformers) | Whisper, Wav2Vec 2.0, SpeechT5 models | Apache 2.0 |

### Python Libraries

| Library | Purpose | License |
|---------|---------|---------|
| [speech_recognition](https://github.com/Uberi/speech_recognition) | Unified STT interface for multiple engines | BSD |
| [gTTS](https://github.com/pndurette/gTTS) | Google Translate TTS API wrapper | MIT |
| [pyttsx3](https://github.com/nateshmbhat/pyttsx3) | Offline TTS (Sapi5, nsss, espeak) | MIT |
| [webrtcvad](https://github.com/wiseman/py-webrtcvad) | Voice activity detection | MIT |
| [noisereduce](https://github.com/timsainb/noisereduce) | Noise reduction | MIT |
| [praat-parselmouth](https://github.com/YannickJadoul/Parselmouth) | Python interface to Praat for phonetics | MIT |

### Deployment & Optimization

| Tool | Description |
|------|-------------|
| [CTranslate2](https://github.com/OpenNMT/CTranslate2) | Fast inference for Transformer models |
| [ONNX Runtime](https://github.com/microsoft/onnxruntime) | Cross-platform ML inference |
| [TensorRT](https://developer.nvidia.com/tensorrt) | NVIDIA GPU inference optimization |
| [OpenVINO](https://github.com/openvinotoolkit/openvino) | Intel hardware optimization |
| [Triton Inference Server](https://github.com/triton-inference-server/server) | NVIDIA cloud inference serving |
| [vLLM](https://github.com/vllm-project/vllm) | High-throughput LLM serving |

---

## Datasets

High-quality data is the lifeblood of natural speech. Here are the primary open datasets for training speech recognition and synthesis models.

### Speech Recognition (STT) Datasets

| Dataset | Hours | Languages | Description |
|---------|-------|-----------|-------------|
| [Common Voice](https://commonvoice.mozilla.org/) | 30,000+ | 100+ | Crowdsourced multilingual corpus, CC0 |
| [LibriLight](https://github.com/facebookresearch/libri-light) | 60,000 | EN | Unlabelled audiobook dataset |
| [MLS](https://www.openslr.org/94) | 50,000 | 8 | Multilingual audiobook corpus |
| [VoxPopuli](https://github.com/facebookresearch/voxpopuli) | 400K unlabelled | 23 | European Parliament recordings |
| [GigaSpeech](https://github.com/SpeechColab/GigaSpeech) | 10,000 | EN | Podcasts, YouTube, audiobooks |
| [LibriSpeech](https://www.openslr.org/12) | 1,000 | EN | Read speech from LibriVox |
| [AISHELL](https://www.openslr.org/33) | 178 | ZH | Mandarin read speech |

### Speech Synthesis (TTS) Datasets

| Dataset | Hours | Speakers | Description |
|---------|-------|----------|-------------|
| [LibriTTS](https://www.openslr.org/60) | 585 | 2,456 | Read speech for TTS, derived from LibriSpeech |
| [VCTK](https://datashare.ed.ac.uk/handle/10283/3443) | 44 | 109 | English speech with diverse accents |
| [Common Voice TTS splits](https://commonvoice.mozilla.org/) | Varies | 100+ | Multilingual crowdsourced TTS data |
| [JVS Corpus](https://sites.google.com/site/shinnosuketakamichi/research-topics/jvs_corpus) | 30 | 100 | Japanese speech corpus |
| [LJSpeech](https://keithito.com/LJ-Speech-Dataset/) | 24 | 1 (female) | Single-speaker English TTS |

---

## Learning Resources

Dive deep into the science behind natural speech processing, with foundational papers, tutorials, and communities.

### Key Papers

| Paper | Year | Contribution |
|-------|------|-------------|
| **Speech Recognition (STT)** | | |
| [Wav2Vec 2.0](https://arxiv.org/abs/2006.11477) | 2020 | Self-supervised speech representation |
| [Whisper](https://arxiv.org/abs/2212.04356) | 2022 | Speech recognition at scale |
| **Speech Synthesis (TTS)** | | |
| [Tacotron 2](https://arxiv.org/abs/1712.05884) | 2017 | TTS via WaveNet conditioning |
| [FastSpeech](https://arxiv.org/abs/1905.09263) | 2019 | Non-autoregressive TTS |
| [FastSpeech 2](https://arxiv.org/abs/2006.04558) | 2020 | End-to-end TTS |
| [VITS](https://arxiv.org/abs/2106.06103) | 2021 | Variational inference + adversarial TTS |
| [Bark](https://github.com/suno-ai/bark) | 2023 | Generative audio transformer |
| [StyleTTS 2](https://arxiv.org/abs/2306.07691) | 2023 | TTS via style diffusion |
| [Tortoise-TTS](https://github.com/neonbjb/tortoise-tts) | 2023 | High-quality TTS with autoregressive + diffusion |
| [OpenVoice](https://arxiv.org/abs/2312.01479) | 2023 | Voice cloning with style control |
| [CosyVoice](https://arxiv.org/abs/2407.05407) | 2024 | Multi-lingual voice generation |
| [F5-TTS](https://arxiv.org/abs/2410.06885) | 2024 | Flow matching for zero-shot TTS |
| **Speech-to-Speech (STS)** | | |
| [Mini-Omni](https://arxiv.org/abs/2409.00666) | 2024 | Low-latency bilingual speech-to-speech |
| [Moshi](https://arxiv.org/abs/2410.00037) | 2024 | Real-time full-duplex spoken dialogue |
| **General** | | |
| [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | 2017 | Transformer architecture |

### Courses & Tutorials

| Resource | Description |
|----------|-------------|
| [CS 224S - Stanford](http://web.stanford.edu/class/cs224s/) | Spoken Language Processing course |
| [Hugging Face Audio Course](https://huggingface.co/learn/audio-course) | Hands-on audio ML course |
| [ESPnet Tutorial](https://github.com/espnet/espnet) | Speech processing recipes |
| [Speech and Language Processing (Jurafsky)](https://web.stanford.edu/~jurafsky/slp3/) | Textbook, 3rd ed. draft |
| [NVIDIA NeMo Tutorials](https://docs.nvidia.com/nemo-framework/user-guide/) | TTS/ASR training pipelines |
| [Librosa Tutorials](https://librosa.org/doc/latest/tutorial.html) | Audio analysis with Python |

### Blogs & Communities

| Resource | Description |
|----------|-------------|
| [Hugging Face Audio Hub](https://huggingface.co/models?pipeline_tag=text-to-speech) | Audio model repository |
| [NVIDIA Developer Blog](https://developer.nvidia.com/blog/) | Speech AI and NeMo updates |
| [r/LocalLLaMA (Reddit)](https://www.reddit.com/r/LocalLLaMA/) | Self-hosted AI including speech models |
| [r/speechrecognition (Reddit)](https://www.reddit.com/r/speechrecognition/) | Speech recognition community |
| [r/TextToSpeech (Reddit)](https://www.reddit.com/r/TextToSpeech/) | TTS community and discussion |
| [The Neural Maze](https://theneuralmaze.substack.com/) | Speech AI newsletter |
| [The Puddle Report](https://thepuddlereport.com/) | Speech technology news |

---

## Conferences & Workshops

| Conference | Focus |
|------------|-------|
| [ICASSP](https://2026.ieeeicassp.org/) | IEEE Acoustics, Speech, and Signal Processing |
| [INTERSPEECH](https://www.interspeech2026.org/) | Speech science and technology |
| [ASRU](https://asruworkshop.org/) | IEEE Automatic Speech Recognition Workshop |
| [SLT](https://slt2026.org/) | IEEE Spoken Language Technology Workshop |
| [WASPAA](https://waspaa.com/) | IEEE Workshop on Applications of Signal Processing to Audio |

---

## Contributing

Contributions to make this resource list even better are highly welcome! Help us catalog the state-of-the-art in natural voice interaction.

### Contribution Guidelines

- Add one link per Pull Request
- Use the format: `[Name](URL) - Description`
- Keep descriptions factual and neutral
- Add table rows following existing format
- Check that the link is not already in the list before submitting
- Verify that the project is active and maintained

---

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
