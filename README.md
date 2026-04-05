# Awesome Text-to-Speech & Speech-to-Text [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome text-to-speech (TTS), speech-to-text (STT), speech synthesis, recognition, voice cloning, and audio processing resources.

[💬 TTS](#text-to-speech-tts) · [🎙️ STT](#speech-to-text-stt) · [🔊 Voice Cloning](#voice-cloning--conversion) · [🎧 Speech Enhancement](#speech-enhancement--audio-processing) · [🚀 Quick Start](#quick-start-guides) · [💡 Use Cases](#use-cases--applications) · [💻 Hardware](#hardware--requirements) · [📦 Apps & Products](#apps--products) · [🛠️ Tooling](#tooling--infrastructure) · [📚 Datasets](#datasets) · [🎓 Learning](#learning-resources)

---

## Text-to-Speech (TTS)

### Open-Source Models & Libraries

#### 🏆 Tier 1: Most Impactful & Innovative

| Project | Description | Languages |
|---------|-------------|-----------|
| [🐸 Coqui TTS](https://github.com/coqui-ai/TTS) | Deep learning toolkit with pretrained models, voice cloning, custom training | 1100+ |
| [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) | Powerful few-shot voice cloning, massive community adoption | Multi |
| [Bark (Suno)](https://github.com/suno-ai/bark) | Transformer-based TTS, generative audio with emotions, music, multilingual | Multi |
| [Qwen3-TTS](https://github.com/QwenLM/Qwen3-TTS) | Alibaba's SOTA streaming TTS: 97ms latency, 3s voice cloning, text-based voice design | 10 |
| [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) | Multi-lingual large voice model: zero-shot, cross-lingual, instruction-following | 50+ |

#### ⭐ Tier 2: Strong Alternatives

| Project | Description | Languages |
|---------|-------------|-----------|
| [OpenVoice](https://github.com/myshell-ai/OpenVoice) | Instant voice cloning with fine-grained style control | Multi |
| [Fish Speech](https://github.com/fishaudio/fish-speech) | SOTA open-source TTS with rapid voice cloning from 10-30s samples | Multi |
| [F5-TTS](https://github.com/SWivid/F5-TTS) | Flow-matching TTS with strong zero-shot voice cloning | Multi |
| [ChatTTS](https://github.com/2noise/ChatTTS) | TTS optimized for conversational scenarios with natural prosody | EN, ZH |
| [MeloTTS](https://github.com/myshell-ai/MeloTTS) | High-quality multi-language, multi-speaker TTS library | EN, ES, FR, ZH, JP, KR |
| [Kokoro](https://github.com/hexgrad/kokoro) | Lightweight 82M-parameter TTS with high-quality output | EN |
| [Piper](https://github.com/rhasspy/piper) | Fast, fully local neural TTS for on-device/offline Raspberry Pi | Multi |
| [VITS](https://github.com/jaywalnut310/vits) | Conditional VAE with adversarial learning for end-to-end TTS | Multi |
| [ESPnet-TTS](https://github.com/espnet/espnet) | End-to-end speech toolkit: Tacotron2, FastSpeech, VITS | Multi |
| [StyleTTS 2](https://github.com/yl4579/StyleTTS2) | Human-level TTS with style diffusion modeling | EN |

#### 🔧 Tier 3: Specialized & Niche

| Project | Description | Languages |
|---------|-------------|-----------|
| [Parler-TTS](https://github.com/huggingface/parler-tts) | Hugging Face's lightweight TTS with controllable voice | EN |
| [VoxCPM](https://github.com/OpenBMB/VoxCPM) | Tokenizer-free TTS with context-aware speech generation | Multi |
| [OmniVoice](https://github.com/k2-fsa/OmniVoice) | High-quality voice cloning TTS for 600+ languages | 600+ |
| [Chatterbox (Resemble AI)](https://github.com/resemble-ai/chatterbox) | MIT-licensed real-time TTS with emotion control, sub-200ms | 23+ |
| [IndexTTS 2](https://github.com/index-tts/index-tts) | High-quality TTS with zero-shot voice cloning and emotional control | EN, ZH |
| [Sesame CSM](https://github.com/SesameAILabs/csm) | Conversational speech generation with human-like prosody | EN |
| [Mistral Voxtral TTS](https://huggingface.co/mistralai/Voxtral-4B-TTS-2603) | Mistral's 4B open-weight streaming TTS, low-latency multilingual | Multi |
| [MOSS-TTS](https://github.com/OpenMOSS/MOSS-TTS) | High-fidelity speech/sound generation, multi-speaker dialogue | Multi |
| [MetaVoice-1B](https://github.com/metavoiceio/metavoice-src) | 1.2B parameter foundation TTS, fine-tunable | EN |
| [Hume TADA](https://github.com/HumeAI/tada) | LLM-based TTS with zero hallucinations, 0.09 RTF | Multi |
| [KaniTTS2](https://github.com/rhasspy/kani) | 400M parameter TTS running on 3GB VRAM with voice cloning | EN |
| [Ming-omni-tts](https://github.com/inclusionAI/Ming-omni-tts) | Unified generation of speech, music, and sound | Multi |
| [Mozilla TTS](https://github.com/mozilla/TTS) | Community-driven TTS framework, predecessor to Coqui | Multi |
| [eSpeak NG](https://github.com/espeak-ng/espeak-ng) | Compact TTS engine for embedded systems | 100+ |
| [MaryTTS](https://github.com/marytts/marytts) | Java-based multilingual TTS with extensive customization | Multi |
| [Silma TTS](https://github.com/SILMA-AI/silma-tts) | Lightweight open bilingual TTS | EN, ES |

#### API Wrappers

| Project | Description |
|---------|-------------|
| [xTTS](https://github.com/daswer123/xtts-api-server) | API server for Coqui XTTS with streaming support |

### Cloud & Commercial APIs

| Service | Key Features | Pricing | Latency |
|---------|-------------|---------|---------|
| [ElevenLabs](https://elevenlabs.io/) | Industry-leading quality, voice cloning (3min), AI dubbing, 70+ languages | $0.10/min | ~200ms |
| [Cartesia Sonic-3](https://cartesia.ai/) | Ultra-low latency streaming, natural laughs/emotes, 40+ languages | Pay-per-char | 40ms (Turbo) |
| [OpenAI TTS](https://platform.openai.com/docs/guides/text-to-speech) | Steerable output (tone, pacing), 13+ custom voices | Pay-per-char | ~300ms |
| [Deepgram Aura-2](https://deepgram.com/) | Sub-200ms TTFB, 40+ English accents, semantic turn detection | $0.03/1k chars | 90ms |
| [Amazon Polly](https://aws.amazon.com/polly/) | Standard/Neural/Generative tiers, colloquial speech, 5M free chars/mo | $4-100/1M chars | ~200ms |
| [Google Cloud TTS](https://cloud.google.com/text-to-speech) | Natural voices, pitch/rate customization | Pay-per-char | ~200ms |
| [Azure AI Speech](https://azure.microsoft.com/products/ai-services/ai-speech/) | Neural TTS, custom voice creation | Pay-per-char | ~250ms |
| [PlayHT](https://play.ht/) | 829 AI voices, 142 languages, instant cloning | $39-99/mo | ~300ms |
| [Resemble AI](https://www.resemble.ai/) | Rapid cloning (10s), enterprise security | Enterprise | ~200ms |
| [Fish Audio](https://fish.audio/) | Rapid voice cloning, multilingual TTS API | Freemium | ~250ms |

### TTS Architecture Reference

| Category | Models / Approaches |
|----------|-------------------|
| **Autoregressive** | Tacotron, Tacotron2, VITS, Bark, WaveNet |
| **Non-Autoregressive** | FastSpeech, FastSpeech 2, ParaNet, FastPitch, Aligner TTS |
| **Flow-based** | Glow-TTS, Flowtron, F5-TTS (flow matching) |
| **GAN-based** | HiFi-GAN, MelGAN, BigVGAN, UnivNet |
| **Diffusion** | StyleTTS 2 (style diffusion), OmniVoice, CosyVoice 2 |
| **Vocoders** | WaveNet, WaveRNN, HiFi-GAN, MelGAN, Parallel WaveGAN, LPCNet, BigVGAN |

---

## Speech-to-Text (STT)

### Open-Source Models & Libraries

#### 🏆 Tier 1: Most Impactful & Innovative

| Project | Description | Languages |
|---------|-------------|-----------|
| [Cohere Transcribe](https://huggingface.co/CohereLabs/cohere-transcribe-03-2026) | #1 HF ASR leaderboard, Apache 2.0, vLLM optimized | 14 |
| [Whisper Large V3 (OpenAI)](https://github.com/openai/whisper) | Most popular STT model, robust multilingual | 99+ |
| [Canary Qwen 2.5B (NVIDIA)](https://huggingface.co/nvidia/canary-qwen-2.5b) | Top-tier accuracy, NeMo toolkit | EN |
| [IBM Granite Speech 3.3](https://huggingface.co/ibm-granite/granite-speech-3.3-8b) | Enterprise accuracy, translation support | EN, FR, DE, ES + JP/ZH |

#### ⭐ Tier 2: Strong Alternatives

| Project | Description | Languages |
|---------|-------------|-----------|
| [Whisper Large V3 Turbo](https://github.com/openai/whisper) | 6× faster, transcription-only | 99+ |
| [Parakeet TDT 0.6B (NVIDIA)](https://huggingface.co/nvidia/parakeet-tdt-0.6b-v2) | Extreme speed, auto-punctuation, batch processing | EN |
| [Parakeet TDT 1.1B (NVIDIA)](https://huggingface.co/nvidia/parakeet-tdt-1.1b) | Ultra-low-latency streaming, RNN-T | EN |
| [Distil-Whisper](https://github.com/huggingface/distil-whisper) | Frozen encoder, lightweight, long-form optimized | EN |
| [Faster-Whisper](https://github.com/SYSTRAN/faster-whisper) | CTranslate2 optimization of Whisper, 4× faster | 99+ |

#### 🔧 Tier 3: Specialized & Niche

| Project | Description | Languages |
|---------|-------------|-----------|
| [WhisperX](https://github.com/m-bain/whisperX) | Word-level timestamps + speaker diarization | Multi |
| [Wav2Vec 2.0 XLSR (Meta)](https://github.com/facebookresearch/fairseq) | Self-supervised, needs fine-tuning | 53+ |
| [Vosk](https://github.com/alphacep/vosk-api) | Offline, runs on edge devices | 20+ |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | All-in-one speech toolkit | Multi |
| [NeMo (NVIDIA)](https://github.com/NVIDIA/NeMo) | End-to-end ASR/TTS platform | Multi |
| [SenseVoice](https://github.com/FunAudioLLM/SenseVoice) | ASR + LID + SER + AED understanding | Multi |
| [Silero Models](https://github.com/snakers4/silero-models) | Pretrained STT, VAD, punctuation | Multi |
| [Moonshine](https://github.com/usefulsensors/moonshine) | 27M params, smartphones, IoT, embedded | Edge |
| [FunASR](https://github.com/modelscope/FunASR) | Alibaba's industrial-grade ASR toolkit | Multi |
| [Microsoft MAI-Transcribe-1](https://microsoft.ai/news/state-of-the-art-speech-recognition-with-mai-transcribe-1/) | 2026 SOTA, enterprise-grade | Multi |
| [ESPnet](https://github.com/espnet/espnet) | End-to-end ASR/TTS/SE toolkit | Multi |
| [Kaldi](https://github.com/kaldi-asr/kaldi) | Classic ASR toolkit (C++) | Multi |
| [Coqui STT](https://github.com/coqui-ai/STT) | Built on Mozilla DeepSpeech | Multi |
| [k2 / Icefall](https://github.com/k2-fsa/icefall) | Next-gen ASR with FSA-based recipes | Multi |

### Cloud & Commercial APIs

| Service | Key Features | Pricing |
|---------|-------------|---------|
| [OpenAI Whisper API](https://platform.openai.com/docs/guides/speech-to-text) | Whisper-powered transcription & translation | $0.006/min |
| [Deepgram](https://deepgram.com/) | Fastest STT, custom models, summarization, PII redaction | $0.0043/min |
| [Google Cloud Speech-to-Text](https://cloud.google.com/speech-to-text) | Real-time/batch, 125+ languages, custom models | $0.006/15s |
| [Azure Speech Service](https://azure.microsoft.com/products/ai-services/ai-speech/) | Real-time transcription, custom models, speaker ID | $1/hr |
| [AssemblyAI](https://www.assemblyai.com/) | Transcription + summarization, PII redaction, LLM integration | $0.00025/sec |
| [Speechmatics](https://www.speechmatics.com/) | Multilingual, diarization, real-time streaming | Custom |
| [Rev AI](https://www.rev.ai/) | Human-level accuracy, AI + human transcription | $0.005/sec |
| [Amazon Transcribe](https://aws.amazon.com/transcribe/) | Automatic recognition, PII redaction, custom vocab | $0.024/min |
| [Gladia Solaria](https://www.gladia.io/) | Universal STT model, multilingual, real-time | Pay-per-char |

### STT Architecture Reference

| Category | Models / Approaches |
|----------|-------------------|
| **CTC-based** | DeepSpeech, Jasper, QuartzNet, Conformer-CTC, Wav2Vec 2.0 |
| **RNN-T** | Transducer-based end-to-end, Emformer-RNNT, Parakeet TDT |
| **Encoder-Decoder** | Listen Attend Spell, Whisper, Canary, Transformer-ASR |
| **Hybrid** | HMM-DNN, Wav2Vec + CTC, HuBERT |
| **Streaming** | Emformer-RNNT, ContextNet, Chunk-based Conformer |

---

## Voice Cloning & Conversion

### Voice Cloning (TTS)

| Tool | Clone From | Languages | Best For |
|------|-----------|-----------|----------|
| [ElevenLabs](https://elevenlabs.io/) | 3 minutes | 70+ | Professional quality (closed source) |
| [Qwen3-TTS](https://github.com/QwenLM/Qwen3-TTS) | 3 seconds | 10 | Fastest open-source, text-based voice design |
| [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) | ~10 seconds | Multi | Few-shot cloning, massive community adoption |
| [Fish Speech V1.5](https://github.com/fishaudio/fish-speech) | 10-30 seconds | Multi | SOTA timbre capture, production-ready |
| [XTTS-v2 (Coqui)](https://github.com/coqui-ai/TTS) | 6 seconds | 16+ | Multilingual cloning, established ecosystem |
| [IndexTTS 2](https://github.com/index-tts/index-tts) | ~10 seconds | EN, ZH | Zero-shot cloning quality, emotional control |
| [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) | 3-10 seconds | 50+ | Cross-lingual cloning, instruction-following |
| [F5-TTS](https://github.com/SWivid/F5-TTS) | ~10 seconds | Multi | Zero-shot flow matching, research-friendly |
| [Chatterbox](https://github.com/resemble-ai/chatterbox) | 5 seconds | 23+ | Real-time inference, emotion control |
| [OpenVoice V2](https://github.com/myshell-ai/OpenVoice) | ~5 seconds | Multi | Speed, lightweight deployment |

### Voice Conversion (STS)

| Tool | Description | Best For |
|------|-------------|----------|
| [RVC](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) | Retrieval-based voice conversion with GUI, widely used in music/streaming | Music, streaming, live conversion |
| [so-vits-svc](https://github.com/svc-develop-team/so-vits-svc) | High-quality singing voice conversion using VITS architecture | Singing voice conversion |
| [WhisperSpeech](https://github.com/WhisperSpeech/WhisperSpeech) | Speech-to-speech translation and conversion pipeline | Cross-language voice transfer |
| [MetaVoice STS](https://github.com/metavoiceio/metavoice-src) | Speech-to-speech with tone color preservation | Conversational AI |

---

## Speech Enhancement & Audio Processing

### Noise Suppression & Enhancement

| Tool | Description |
|------|-------------|
| [DeepFilterNet](https://github.com/Rikorose/DeepFilterNet) | Low-complexity speech enhancement using deep filtering |
| [Demucs (Meta)](https://github.com/facebookresearch/demucs) | Music/source separation with high-quality audio extraction |
| [Spleeter (Deezer)](https://github.com/deezer/spleeter) | Source separation with pretrained models |
| [RNNoise](https://github.com/xiph/rnnoise) | Recurrent neural network for audio noise reduction |
| [VoiceFixer](https://github.com/haoheliu/voicefixer) | Restore speech quality under real-world degradation |
| [AudioSep](https://github.com/Audio-AGI/AudioSep) | Separate audio with natural language queries |

### Voice Activity Detection (VAD)

| Tool | Description |
|------|-------------|
| [Silero VAD](https://github.com/snakers4/silero-vad) | Pretrained enterprise-grade VAD, fast and accurate |
| [WebRTC VAD](https://github.com/wiseman/py-webrtcvad) | Lightweight VAD for real-time audio processing |
| [PyAnnote VAD](https://github.com/pyannote/pyannote-audio) | Neural VAD as part of the pyannote ecosystem |

### Speaker Diarization

| Tool | Description |
|------|-------------|
| [pyannote.audio](https://github.com/pyannote/pyannote-audio) | De facto standard for speaker diarization, v3.1 with pretrained models |
| [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) | MSDD (Multi-scale Diarization Decoder), GPU-accelerated |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | Built-in diarization as part of speech processing toolkit |
| [WhisperX](https://github.com/m-bain/whisperX) | Adds diarization on top of Whisper transcriptions |

---

## Quick Start Guides

### "I Want To..." Cheat Sheet

| Goal | Recommended Tool | Why |
|------|-----------------|-----|
| Transcribe a podcast/audio file | **Whisper V3** or **Faster-Whisper** | Best balance of accuracy and multilingual support |
| Clone a voice from a short sample | **Qwen3-TTS** (3s) or **GPT-SoVITS** (10s) | Fastest cloning with high quality |
| Generate expressive/creative speech | **Bark (Suno)** | Emotions, laughter, music, highly expressive |
| Run TTS on a Raspberry Pi / edge device | **Piper** or **Moonshine** (STT) | Lightweight, fully local, low resource |
| Build a real-time voice agent | **LiveKit Agents** + Deepgram + Cartesia | End-to-end framework with sub-200ms latency |
| Convert singing voice | **RVC** | Real-time, massive community, GUI ecosystem |
| Transcribe meetings with speaker labels | **WhisperX** or **AssemblyAI** | Word-level timestamps + diarization |
| Clean up noisy audio recordings | **DeepFilterNet** or **VoiceFixer** | Deep learning-based enhancement |
| Transcribe in 50+ languages | **Whisper V3** or **Coqui TTS** | Broadest language coverage |
| Self-host TTS with zero per-minute cost | **Qwen3-TTS** or **Coqui TTS** | Apache 2.0 / open license, self-hostable |
| Generate voiceovers for videos | **ElevenLabs** or **Fish Audio** | Professional quality, rapid generation |
| Real-time transcription with extreme speed | **Parakeet TDT 0.6B** | >3000× real-time factor |

### Quick Start: Self-Hosted TTS

```bash
# Option 1: Coqui TTS (most versatile)
pip install TTS
tts --model_name tts_models/en/ljspeech/tacotron2-DDC \
    --text "Hello world" --out_path output.wav

# Option 2: Piper (lightweight, local)
pip install piper-tts
echo "Hello world" | piper --model en_US-lessac-medium --output_file output.wav

# Option 3: Bark (expressive, creative)
pip install git+https://github.com/suno-ai/bark.git
python -c "from bark import generate_audio; generate_audio('Hello world')"
```

### Quick Start: Self-Hosted STT

```bash
# Option 1: Whisper (most popular)
pip install openai-whisper
whisper audio.mp3 --model large --language en

# Option 2: Faster-Whisper (4× speedup)
pip install faster-whisper
python -c "
from faster_whisper import WhisperModel
model = WhisperModel('large-v3', device='cuda')
segments, info = model.transcribe('audio.mp3')
for seg in segments: print(f'[{seg.start:.1f}s - {seg.end:.1f}s] {seg.text}')
"

# Option 3: Vosk (offline, edge devices)
pip install vosk
python -c "
from vosk import Model, KaldiRecognizer
import wave
wf = wave.open('audio.wav', 'rb')
model = Model('vosk-model-small-en-us-0.15')
rec = KaldiRecognizer(model, wf.getframerate())
"
```

### Quick Start: Voice Agent (STT → LLM → TTS)

```python
# Using LiveKit Agents framework
# pip install livekit-agents livekit-plugins-deepgram livekit-plugins-cartesia
from livekit.agents import Agent, AgentSession, AgentServer

class Assistant(Agent):
    def __init__(self):
        super().__init__(instructions="You are a helpful voice assistant.")

server = AgentServer()

@server.rtc_session(agent_name="voice-agent")
async def run_agent(ctx):
    session = AgentSession(
        stt="deepgram/nova-3:multi",
        llm="openai/gpt-4.1-mini",
        tts="cartesia/sonic-3:<voice-uuid>",
    )
    await session.start(room=ctx.room, agent=Assistant())
    await session.generate_reply()
```

---

## Use Cases & Applications

### Text-to-Speech Use Cases

| Use Case | Description | Recommended Tools |
|----------|-------------|-------------------|
| **Accessibility** | Screen readers, visual impairment aids, WCAG compliance | Piper, eSpeak NG, Coqui TTS |
| **Audiobook Narration** | Large-scale audio book production with consistent voice quality | ElevenLabs, Fish Audio, StyleTTS 2 |
| **E-Learning** | Audio lessons, pronunciation training, multilingual education | MeloTTS, Coqui TTS, Azure AI Speech |
| **Gaming & Storytelling** | Dynamic real-time dialogue adapting to player choices | Cartesia Sonic-3, Bark, ChatTTS |
| **Voice Assistants** | Natural AI voice responses for banking, retail, service apps | OpenAI TTS, Qwen3-TTS, Chatterbox |
| **Customer Support IVR** | Dynamic menus and account details in call centers | Deepgram Aura-2, Amazon Polly |
| **Video Production** | Rapid voiceovers for YouTube, ads, social content | ElevenLabs, Fish Audio, CosyVoice 2 |
| **GPS Navigation** | Spoken directions and traffic alerts for automotive | Piper (offline), eSpeak NG |
| **Content Localization** | Dubbing video content into multiple languages | ElevenLabs AI Dubbing, Coqui TTS |
| **News & Articles** | Convert written content to audio for multitasking | Coqui TTS, OpenAI TTS |

### Speech-to-Text Use Cases

| Use Case | Description | Recommended Tools |
|----------|-------------|-------------------|
| **Medical Documentation** | Automate clinical notes, HIPAA-compliant transcription | Whisper V3, AssemblyAI, Azure Speech |
| **Customer Service** | Real-time call transcription, intent detection, routing | Deepgram, Google Cloud STT |
| **Call Analysis** | Sentiment analysis, key phrase detection, business insights | AssemblyAI, WhisperX |
| **Video Content** | Generate captions, timestamps, repurpose content into clips | Whisper V3, Gladia Solaria |
| **Legal Discovery** | Searchable text from audio evidence, PII redaction | AssemblyAI, Rev AI, Speechmatics |
| **Education** | Automatic captioning, lecture transcription, summaries | Whisper V3, Vosk (offline) |
| **Market Research** | Extract insights from customer interactions | AssemblyAI, Deepgram |
| **Live Captioning** | Low-latency captions for broadcasts and events | Parakeet TDT, Deepgram |
| **Sales Intelligence** | Capture and analyze sales calls for coaching | AssemblyAI, WhisperX |
| **Meeting Transcription** | Multi-speaker meetings with speaker labels | WhisperX, Cohere Transcribe |

### Combined STT + TTS Patterns

| Pattern | Description | Example Stack |
|---------|-------------|---------------|
| **Voice Agent** | Speech → STT → LLM → TTS → Speech | Whisper → GPT-4 → Cartesia |
| **Real-Time Translation** | Speech in Language A → STT → Translate → TTS in Language B | Whisper → Translation → Coqui TTS |
| **Meeting Summarizer** | Meeting audio → STT → LLM Summary → TTS Audio Summary | WhisperX → LLM → ElevenLabs |
| **Podcast Search** | Podcast → STT → Text Search → Return Timestamps | Faster-Whisper → Elasticsearch |
| **Voice Memo Assistant** | Voice memo → STT → NLP extraction → Structured notes | Whisper → NLP Pipeline |

---

## Hardware & Requirements

### TTS Hardware Requirements

| Model | VRAM (GB) | GPU Required | Notes |
|-------|-----------|--------------|-------|
| **KaniTTS2** | 3 | Any | Lowest requirement, consumer GPU |
| **Piper** | 1-2 | Integrated | CPU inference possible, no GPU |
| **Kokoro** | 2-4 | Modern GPU | 82M parameters, lightweight |
| **MeloTTS** | 4-6 | Mid-range GPU | Multi-language support |
| **GPT-SoVITS** | 6-8 | NVIDIA recommended | Requires fine-tuning |
| **Qwen3-TTS** | 6-8 | Modern GPU | Streaming, fast inference |
| **Bark** | 8-10 | High-end GPU | Large transformer model |
| **Coqui TTS (XTTS)** | 8-12 | High-end GPU | Multi-lingual, voice cloning |
| **CosyVoice 2** | 10-16 | High-end GPU | Large language model |

### STT Hardware Requirements

| Model | VRAM (GB) | Speed | Notes |
|-------|-----------|-------|-------|
| **Moonshine** | 0.5 | Low | Edge devices, smartphones |
| **Vosk** | 1-2 | Real-time | CPU inference, no GPU |
| **Distil-Whisper** | 2-4 | Fast | Lightweight, long-form |
| **Whisper V3 Turbo** | 4-6 | Fast | 6× faster than base |
| **Parakeet TDT 0.6B** | 4-6 | **Extreme** | >3000× real-time |
| **Whisper V3 Base** | 6-8 | Medium | Good balance |
| **Faster-Whisper** | 6-8 | Fast | 4× faster, CTranslate2 |
| **Whisper V3 Large** | 10-14 | Medium | Highest accuracy |
| **Cohere Transcribe** | 8-12 | Fast | vLLM optimized |
| **IBM Granite 8B** | 16-24 | Medium | Enterprise, high VRAM |

### Minimum Hardware for Common Tasks

| Task | Minimum Setup | Recommended |
|------|--------------|-------------|
| **Offline TTS (Piper)** | Intel i5, 4GB RAM | Raspberry Pi 4 |
| **Whisper Transcription** | 6GB VRAM GPU | RTX 3060 / 8GB |
| **Real-Time Voice Agent** | 8GB VRAM GPU | RTX 4070 / 12GB |
| **Voice Cloning (GPT-SoVITS)** | 12GB VRAM GPU | RTX 3090 / 24GB |
| **Production STT Server** | 16GB VRAM GPU | A100 40GB |

---

## Apps & Products

### Open-Source Applications

| App | Description | Tech Stack |
|-----|-------------|------------|
| [Open WebUI](https://github.com/open-webui/open-webui) | ChatGPT-like UI with TTS/STT integration | Whisper, Coqui TTS |
| [AllTalk TTS](https://github.com/erew123/alltalk_tts) | TTS extension for text generation web UIs | Coqui TTS, Piper, GTTS |
| [Pinokio](https://github.com/pinokio-computer/pinokio) | One-click installer for AI apps including TTS/STT | Multiple |
| [RVC WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) | Web interface for real-time voice conversion | RVC |
| [GPT-SoVITS WebUI](https://github.com/RVC-Boss/GPT-SoVITS) | Web interface for few-shot voice cloning | GPT-SoVITS |
| [WhisperX](https://github.com/m-bain/whisperX) | CLI tool for transcription with diarization | Whisper + pyannote |
| [LiveKit Agents](https://github.com/livekit/agents) | Framework for building real-time voice agents | Deepgram, Cartesia, OpenAI |
| [Bark UI](https://github.com/camenduru/bark-ui) | Web UI for Bark text-to-speech | Bark |
| [Kokoro WebUI](https://github.com/nazdridoy/kokoro-webui) | Simple web interface for Kokoro TTS | Kokoro |
| [Faster-Whisper-Transcriber](https://github.com/oliverguhr/faster-whisper-server) | REST API server for Faster-Whisper | Faster-Whisper |

### Notable Commercial Products

| Product | Category | Description |
|---------|----------|-------------|
| [Otter.ai](https://otter.ai) | Meeting Transcription | Real-time transcription with AI summaries |
| [Descript](https://descript.com) | Audio/Video Editing | Edit audio by editing text, overdub with cloned voice |
| [ElevenLabs](https://elevenlabs.io/) | Voice Platform | Voice cloning, dubbing, reader app |
| [Murf AI](https://murf.ai/) | Voice Generator | Studio-quality voiceover generation |
| [Speechify](https://speechify.com/) | Text-to-Speech Reader | Read articles, PDFs, books aloud |
| [Sonix](https://sonix.ai/) | Transcription | Automated transcription with translation |
| [Trint](https://trint.com/) | Transcription | AI transcription with collaborative editing |
| [Fireflies.ai](https://fireflies.ai/) | Meeting Assistant | AI notetaker for meetings |

### AI Voice Agent Platforms

| Platform | Description |
|----------|-------------|
| [Vapi](https://vapi.ai/) | Inbound/outbound voice agents for customer support |
| [Bland AI](https://www.bland.ai/) | Real-time AI phone calls with custom personalities |
| [Retell AI](https://www.retellai.com/) | Build human-like conversational AI voice agents |
| [Play AI](https://play.ai/) | Conversational AI voice agents with low latency |
| [Synthflow AI](https://synthflow.ai/) | No-code voice agent builder |
| [LiveKit](https://livekit.io/) | Open-source WebRTC infrastructure for voice AI |

---

## Tooling & Infrastructure

### Frameworks & SDKs

| Tool | Description |
|------|-------------|
| [Hugging Face Transformers](https://github.com/huggingface/transformers) | Whisper, Wav2Vec 2.0, SpeechT5, and more |
| [Torchaudio](https://github.com/pytorch/audio) | PyTorch audio I/O, transforms, and models |
| [Librosa](https://github.com/librosa/librosa) | Python audio and music analysis library |
| [SoundFile](https://github.com/bastibe/python-soundfile) | Audio file I/O via libsndfile |
| [pydub](https://github.com/jiaaro/pydub) | Simple audio manipulation for Python |
| [FFmpeg](https://ffmpeg.org/) | Universal audio/video processing |

### ASR/TTS Frameworks

| Framework | Description |
|-----------|-------------|
| [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) | End-to-end platform for ASR, TTS, and NLP |
| [ESPnet](https://github.com/espnet/espnet) | End-to-end speech processing (ASR + TTS + ST) |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | All-in-one PyTorch speech toolkit |
| [Kaldi](https://github.com/kaldi-asr/kaldi) | Classic ASR toolkit (C++), widely used in research |
| [k2 / Icefall](https://github.com/k2-fsa/icefall) | Next-gen ASR with FSA-based recipes |
| [Fairseq (Meta)](https://github.com/facebookresearch/fairseq) | Sequence modeling including Wav2Vec |
| [TTS Server / AllTalk](https://github.com/erew123/alltalk_tts) | TTS integration for text generation UIs |

### Deployment & Optimization

| Tool | Description |
|------|-------------|
| [CTranslate2](https://github.com/OpenNMT/CTranslate2) | Fast inference for Transformer models (Faster-Whisper) |
| [vLLM](https://github.com/vllm-project/vllm) | High-throughput LLM serving (Cohere Transcribe) |
| [TensorRT](https://developer.nvidia.com/tensorrt) | NVIDIA GPU inference optimization |
| [ONNX Runtime](https://github.com/microsoft/onnxruntime) | Cross-platform ML inference |
| [OpenVINO](https://github.com/openvinotoolkit/openvino) | Intel hardware optimization |
| [Triton Inference Server](https://github.com/triton-inference-server/server) | NVIDIA cloud inference serving |

### Python Libraries

| Library | Purpose |
|---------|---------|
| [gTTS](https://github.com/pndurette/gTTS) | Google Translate TTS API wrapper |
| [pyttsx3](https://github.com/nateshmbhat/pyttsx3) | Offline TTS for Python (Sapi5, nsss, espeak) |
| [speech_recognition](https://github.com/Uberi/speech_recognition) | Unified STT interface supporting multiple engines |
| [webrtcvad](https://github.com/wiseman/py-webrtcvad) | Voice activity detection |
| [noisereduce](https://github.com/timsainb/noisereduce) | Noise reduction in Python |
| [praat-parselmouth](https://github.com/YannickJadoul/Parselmouth) | Python interface to Praat for phonetics |

---

## Datasets

### Speech Recognition (STT) Datasets

| Dataset | Hours | Languages | Description |
|---------|-------|-----------|-------------|
| [Common Voice (Mozilla)](https://commonvoice.mozilla.org/) | 30,000+ | 100+ | Crowdsourced multilingual corpus, CC0 |
| [LibriSpeech](https://www.openslr.org/12) | 1,000 | EN | Read speech from LibriVox, standard ASR benchmark |
| [MLS (Multilingual LibriSpeech)](https://www.openslr.org/94) | 50,000 | 8 | Multilingual audiobook corpus |
| [GigaSpeech](https://github.com/SpeechColab/GigaSpeech) | 10,000 | EN | Podcasts, YouTube, audiobooks |
| [VoxPopuli](https://github.com/facebookresearch/voxpopuli) | 400K unlabelled | 23 | European Parliament recordings |
| [LibriLight](https://github.com/facebookresearch/libri-light) | 60,000 | EN | Unlabelled audiobook dataset |
| [GigaST](https://huggingface.co/datasets) | 400,000 | Multi | Largest multilingual STT dataset |
| [AISHELL](https://www.openslr.org/33) | 178 | ZH | Mandarin read speech |

### Speech Synthesis (TTS) Datasets

| Dataset | Hours | Speakers | Description |
|---------|-------|----------|-------------|
| [LibriTTS](https://www.openslr.org/60) | 585 | 2,456 | Read speech for TTS, derived from LibriSpeech |
| [VCTK](https://datashare.ed.ac.uk/handle/10283/3443) | 44 | 109 | English speech with diverse accents |
| [LJSpeech](https://keithito.com/LJ-Speech-Dataset/) | 24 | 1 (female) | Standard single-speaker TTS benchmark |
| [JVS Corpus](https://sites.google.com/site/shinnosuketakamichi/research-topics/jvs_corpus) | 30 | 100 | Japanese speech corpus |
| [Common Voice TTS splits](https://commonvoice.mozilla.org/) | Varies | 100+ | Multilingual crowdsourced TTS data |

---

## Learning Resources

### Key Papers

| Paper | Year | Contribution |
|-------|------|-------------|
| [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | 2017 | Transformer architecture foundation |
| [Tacotron 2](https://arxiv.org/abs/1712.05884) | 2017 | Natural TTS synthesis via WaveNet conditioning |
| [FastSpeech](https://arxiv.org/abs/1905.09263) | 2019 | Fast, robust non-autoregressive TTS |
| [FastSpeech 2](https://arxiv.org/abs/2006.04558) | 2020 | Fast and high-quality end-to-end TTS |
| [VITS](https://arxiv.org/abs/2106.06103) | 2021 | Variational inference + adversarial TTS |
| [Whisper](https://arxiv.org/abs/2212.04356) | 2022 | Robust speech recognition at scale |
| [Wav2Vec 2.0](https://arxiv.org/abs/2006.11477) | 2020 | Self-supervised speech representation |
| [StyleTTS 2](https://arxiv.org/abs/2306.07691) | 2023 | Human-level TTS via style diffusion |
| [Bark](https://github.com/suno-ai/bark) | 2023 | Generative audio transformer with GPT-style tokens |
| [OpenVoice](https://arxiv.org/abs/2312.01479) | 2023 | Instant voice cloning with style control |
| [CosyVoice](https://arxiv.org/abs/2407.05407) | 2024 | Multi-lingual large voice generation |
| [F5-TTS](https://arxiv.org/abs/2410.06885) | 2024 | Flow matching for zero-shot TTS |

### Courses & Tutorials

| Resource | Description |
|----------|-------------|
| [CS 224S - Stanford](http://web.stanford.edu/class/cs224s/) | Spoken Language Processing course |
| [Hugging Face Audio Course](https://huggingface.co/learn/audio-course) | Free hands-on audio ML course |
| [Speech and Language Processing (Jurafsky)](https://web.stanford.edu/~jurafsky/slp3/) | Definitive textbook, 3rd ed. draft |
| [ESPnet Tutorial](https://github.com/espnet/espnet) | Hands-on speech processing recipes |
| [Librosa Tutorials](https://librosa.org/doc/latest/tutorial.html) | Audio analysis with Python |
| [NVIDIA NeMo Tutorials](https://docs.nvidia.com/nemo-framework/user-guide/) | TTS/ASR training pipelines |

### Blogs & Communities

| Resource | Description |
|----------|-------------|
| [r/speechrecognition (Reddit)](https://www.reddit.com/r/speechrecognition/) | Speech recognition community |
| [r/TextToSpeech (Reddit)](https://www.reddit.com/r/TextToSpeech/) | TTS community and discussion |
| [r/LocalLLaMA (Reddit)](https://www.reddit.com/r/LocalLLaMA/) | Self-hosted AI including speech models |
| [Hugging Face Audio Hub](https://huggingface.co/models?pipeline_tag=text-to-speech) | Audio model repository |
| [NVIDIA Developer Blog](https://developer.nvidia.com/blog/) | Speech AI and NeMo updates |
| [The Neural Maze](https://theneuralmaze.substack.com/) | Speech AI newsletter |
| [The Puddle Report](https://thepuddlereport.com/) | Speech technology news |

---

## Conferences & Workshops

| Conference | Focus |
|------------|-------|
| [INTERSPEECH](https://www.interspeech2026.org/) | Largest speech science & technology conference |
| [ICASSP](https://2026.ieeeicassp.org/) | IEEE Acoustics, Speech, and Signal Processing |
| [ASRU](https://asruworkshop.org/) | IEEE Automatic Speech Recognition Workshop |
| [SLT](https://slt2026.org/) | IEEE Spoken Language Technology Workshop |
| [WASPAA](https://waspaa.com/) | IEEE Workshop on Applications of Signal Processing to Audio |

---

## Contributing

Contributions are welcome! Please read the guidelines below.

### Contribution Guidelines

- Add one link per Pull Request
- Use the format: `[Name](URL) - Description`
- Place new entries in the appropriate tier based on impact and innovation
- Keep descriptions concise, informative, and neutral
- Add table rows following existing format
- Check that the link is not already in the list before submitting
- Verify that the project is active and maintained

---

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.