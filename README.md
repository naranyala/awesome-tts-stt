# Awesome Text-to-Speech & Speech-to-Text [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of text-to-speech (TTS), speech-to-text (STT), speech synthesis, recognition, voice cloning, and audio processing resources.

[💬 TTS](#text-to-speech-tts) · [🎙️ STT](#speech-to-text-stt) · [🔊 Voice Cloning](#voice-cloning--conversion) · [🎧 Speech Enhancement](#speech-enhancement--audio-processing) · [🚀 Quick Start](#quick-start-guides) · [💡 Use Cases](#use-cases--applications) · [📦 Apps & Products](#apps--products) · [🛠️ Tooling](#tooling--infrastructure) · [📚 Datasets](#datasets) · [🎓 Learning](#learning-resources)

---

## Text-to-Speech (TTS)

### Open-Source Models & Libraries

| Project | Architecture | Parameters | Languages | License |
|---------|-------------|------------|-----------|---------|
| [Bark (Suno)](https://github.com/suno-ai/bark) | Transformer | — | Multi | MIT |
| [ChatTTS](https://github.com/2noise/ChatTTS) | Autoregressive | — | EN, ZH | CC BY-NC 4.0 |
| [Chatterbox (Resemble AI)](https://github.com/resemble-ai/chatterbox) | — | — | 23+ | MIT |
| [Coqui TTS](https://github.com/coqui-ai/TTS) | Multi (Tacotron2, VITS, etc.) | — | 1100+ | MPL 2.0 |
| [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) | Flow matching + LLM | — | 50+ | Apache 2.0 |
| [ESPnet-TTS](https://github.com/espnet/espnet) | Multi (FastSpeech, VITS, etc.) | — | Multi | Apache 2.0 |
| [eSpeak NG](https://github.com/espeak-ng/espeak-ng) | Formant synthesis | — | 100+ | GPL v3 |
| [F5-TTS](https://github.com/SWivid/F5-TTS) | Flow matching | — | Multi | MIT |
| [Fish Speech](https://github.com/fishaudio/fish-speech) | — | — | Multi | CC BY-NC-SA 4.0 |
| [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) | GPT + VITS | — | Multi | MIT |
| [Hume TADA](https://github.com/HumeAI/tada) | LLM-based | — | Multi | — |
| [IndexTTS 2](https://github.com/index-tts/index-tts) | — | — | EN, ZH | Apache 2.0 |
| [KaniTTS2](https://github.com/rhasspy/kani) | — | 400M | EN | — |
| [Kokoro](https://github.com/hexgrad/kokoro) | — | 82M | EN | Apache 2.0 |
| [MaryTTS](https://github.com/marytts/marytts) | HMM/Unit selection | — | Multi | LGPL |
| [MeloTTS](https://github.com/myshell-ai/MeloTTS) | — | — | EN, ES, FR, ZH, JP, KR | MIT |
| [MetaVoice-1B](https://github.com/metavoiceio/metavoice-src) | Transformer | 1.2B | EN | Apache 2.0 |
| [Ming-omni-tts](https://github.com/inclusionAI/Ming-omni-tts) | — | — | Multi | — |
| [Mistral Voxtral TTS](https://huggingface.co/mistralai/Voxtral-4B-TTS-2603) | — | 4B | Multi | Apache 2.0 |
| [MOSS-TTS](https://github.com/OpenMOSS/MOSS-TTS) | — | — | Multi | — |
| [Mozilla TTS](https://github.com/mozilla/TTS) | Tacotron2, Glow-TTS | — | Multi | MPL 2.0 |
| [OmniVoice](https://github.com/k2-fsa/OmniVoice) | Diffusion language model | — | 600+ | Apache 2.0 |
| [OpenVoice](https://github.com/myshell-ai/OpenVoice) | — | — | Multi | MIT |
| [Parler-TTS](https://github.com/huggingface/parler-tts) | — | — | EN | Apache 2.0 |
| [Piper](https://github.com/rhasspy/piper) | VITS-based | — | Multi | MIT |
| [Qwen3-TTS](https://github.com/QwenLM/Qwen3-TTS) | — | 0.6B, 1.7B | 10 | Apache 2.0 |
| [Sesame CSM](https://github.com/SesameAILabs/csm) | — | — | EN | — |
| [Silma TTS](https://github.com/SILMA-AI/silma-tts) | — | — | EN, ES | Apache 2.0 |
| [StyleTTS 2](https://github.com/yl4579/StyleTTS2) | Style diffusion + GAN | — | EN | MIT |
| [VITS](https://github.com/jaywalnut310/vits) | VAE + GAN | — | Multi | MIT |
| [VoxCPM](https://github.com/OpenBMB/VoxCPM) | — | — | Multi | MIT |

#### API Wrappers

| Project | Description |
|---------|-------------|
| [xTTS](https://github.com/daswer123/xtts-api-server) | REST API server for Coqui XTTS with streaming support |

### Cloud & Commercial APIs

| Service | Languages | Voice Cloning | Streaming | Pricing |
|---------|-----------|--------------|-----------|---------|
| [Amazon Polly](https://aws.amazon.com/polly/) | 50+ | Yes (Neural) | Yes | $4-100/1M chars |
| [Azure AI Speech](https://azure.microsoft.com/products/ai-services/ai-speech/) | 100+ | Yes (Personal Voice) | Yes | Pay-per-char |
| [Cartesia Sonic-3](https://cartesia.ai/) | 40+ | Yes (15s sample) | Yes (40ms) | Pay-per-char |
| [Deepgram Aura-2](https://deepgram.com/) | 7 + 40 English accents | No | Yes (90ms) | $0.03/1k chars |
| [ElevenLabs](https://elevenlabs.io/) | 70+ | Yes (3min sample) | Yes (~200ms) | $0.10/min |
| [Fish Audio](https://fish.audio/) | Multi | Yes (10-30s) | Yes (~250ms) | Freemium |
| [Google Cloud TTS](https://cloud.google.com/text-to-speech) | 220+ | No | Yes (~200ms) | Pay-per-char |
| [OpenAI TTS](https://platform.openai.com/docs/guides/text-to-speech) | Multi | No | Yes (~300ms) | Pay-per-char |
| [PlayHT](https://play.ht/) | 142 | Yes (instant) | Yes (~300ms) | $39-99/mo |
| [Resemble AI](https://www.resemble.ai/) | Multi | Yes (10s sample) | Yes (~200ms) | Enterprise |

### TTS Architecture Reference

| Category | Models / Approaches |
|----------|-------------------|
| **Autoregressive** | Tacotron, Tacotron2, VITS, Bark, WaveNet |
| **Non-Autoregressive** | FastSpeech, FastSpeech 2, ParaNet, FastPitch, Aligner TTS |
| **Flow-based** | Glow-TTS, Flowtron, F5-TTS (flow matching) |
| **GAN-based** | HiFi-GAN, MelGAN, BigVGAN, UnivNet |
| **Diffusion** | StyleTTS 2 (style diffusion), OmniVoice, CosyVoice 2 |
| **Vocoders** | WaveNet, WaveRNN, HiFi-GAN, MelGAN, Parallel WaveGAN, LPCNet, BigVGAN |
| **Formant Synthesis** | eSpeak NG, Festival |

---

## Speech-to-Text (STT)

### Open-Source Models & Libraries

| Project | Architecture | Parameters | Languages | License |
|---------|-------------|------------|-----------|---------|
| [Canary Qwen 2.5B (NVIDIA)](https://huggingface.co/nvidia/canary-qwen-2.5b) | SALM (Speech-Augmented Language Model) | 2.5B | EN | — |
| [Cohere Transcribe](https://huggingface.co/CohereLabs/cohere-transcribe-03-2026) | Fast-Conformer + X-attention | 2B | 14 | Apache 2.0 |
| [Coqui STT](https://github.com/coqui-ai/STT) | DeepSpeech (CTC) | — | Multi | MPL 2.0 |
| [Distil-Whisper](https://github.com/huggingface/distil-whisper) | Distilled Whisper encoder-decoder | 756M | EN | MIT |
| [ESPnet](https://github.com/espnet/espnet) | Multi (Conformer, Transformer) | — | Multi | Apache 2.0 |
| [Faster-Whisper](https://github.com/SYSTRAN/faster-whisper) | CTranslate2-optimized Whisper | — | 99+ | MIT |
| [FunASR](https://github.com/modelscope/FunASR) | Paraformer, Conformer | — | Multi | MIT |
| [IBM Granite Speech 3.3](https://huggingface.co/ibm-granite/granite-speech-3.3-8b) | — | 8B | EN, FR, DE, ES + JP/ZH translation | — |
| [Kaldi](https://github.com/kaldi-asr/kaldi) | HMM-DNN (C++) | — | Multi | Apache 2.0 |
| [k2 / Icefall](https://github.com/k2-fsa/icefall) | FSA-based recipes | — | Multi | Apache 2.0 |
| [Microsoft MAI-Transcribe-1](https://microsoft.ai/news/state-of-the-art-speech-recognition-with-mai-transcribe-1/) | — | — | Multi | — |
| [Moonshine](https://github.com/usefulsensors/moonshine) | — | 27M | Edge-optimized | Apache 2.0 |
| [NeMo (NVIDIA)](https://github.com/NVIDIA/NeMo) | Multi (Conformer-CTC, RNN-T) | — | Multi | Apache 2.0 |
| [Parakeet TDT 0.6B](https://huggingface.co/nvidia/parakeet-tdt-0.6b-v2) | RNN Transducer | 600M | EN | — |
| [Parakeet TDT 1.1B (NVIDIA)](https://huggingface.co/nvidia/parakeet-tdt-1.1b) | RNN Transducer | 1.1B | EN | — |
| [SenseVoice](https://github.com/FunAudioLLM/SenseVoice) | — | — | Multi | MIT |
| [Silero Models](https://github.com/snakers4/silero-models) | — | — | Multi | — |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | Multi (Conformer, ECAPA) | — | Multi | Apache 2.0 |
| [Vosk](https://github.com/alphacep/vosk-api) | Kaldi-based | — | 20+ | Apache 2.0 |
| [Wav2Vec 2.0 XLSR (Meta)](https://github.com/facebookresearch/fairseq) | Self-supervised CNN-Transformer | — | 53+ | MIT |
| [Whisper Large V3 (OpenAI)](https://github.com/openai/whisper) | Encoder-decoder Transformer | 1.55B | 99+ | MIT |
| [Whisper Large V3 Turbo](https://github.com/openai/whisper) | Reduced decoder layers | 809M | 99+ | MIT |
| [WhisperX](https://github.com/m-bain/whisperX) | Whisper + wav2vec2 alignment | — | Multi | BSD 2-Clause |

### Cloud & Commercial APIs

| Service | Languages | Features | Pricing |
|---------|-----------|----------|---------|
| [Amazon Transcribe](https://aws.amazon.com/transcribe/) | 100+ | PII redaction, custom vocab | $0.024/min |
| [AssemblyAI](https://www.assemblyai.com/) | 18+ | Summarization, PII redaction, LLM integration | $0.00025/sec |
| [Azure Speech Service](https://azure.microsoft.com/products/ai-services/ai-speech/) | 100+ | Custom models, speaker ID | $1/hr |
| [Deepgram](https://deepgram.com/) | 30+ | Custom models, summarization, PII redaction | $0.0043/min |
| [Gladia Solaria](https://www.gladia.io/) | Multi | Universal model, real-time | Pay-per-char |
| [Google Cloud Speech-to-Text](https://cloud.google.com/speech-to-text) | 125+ | Custom models, real-time/batch | $0.006/15s |
| [OpenAI Whisper API](https://platform.openai.com/docs/guides/speech-to-text) | 99+ | Transcription, translation | $0.006/min |
| [Rev AI](https://www.rev.ai/) | 30+ | AI + human transcription | $0.005/sec |
| [Speechmatics](https://www.speechmatics.com/) | 30+ | Diarization, real-time streaming | Custom |

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

| Tool | Clone From | Languages | License | Architecture |
|------|-----------|-----------|---------|-------------|
| [Chatterbox](https://github.com/resemble-ai/chatterbox) | 5 seconds | 23+ | MIT | — |
| [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) | 3-10 seconds | 50+ | Apache 2.0 | Flow matching |
| [ElevenLabs](https://elevenlabs.io/) | 3 minutes | 70+ | Proprietary | — |
| [F5-TTS](https://github.com/SWivid/F5-TTS) | ~10 seconds | Multi | MIT | Flow matching |
| [Fish Speech V1.5](https://github.com/fishaudio/fish-speech) | 10-30 seconds | Multi | CC BY-NC-SA 4.0 | — |
| [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) | ~10 seconds | Multi | MIT | GPT + VITS |
| [IndexTTS 2](https://github.com/index-tts/index-tts) | ~10 seconds | EN, ZH | Apache 2.0 | — |
| [OpenVoice V2](https://github.com/myshell-ai/OpenVoice) | ~5 seconds | Multi | MIT | — |
| [Qwen3-TTS](https://github.com/QwenLM/Qwen3-TTS) | 3 seconds | 10 | Apache 2.0 | — |
| [XTTS-v2 (Coqui)](https://github.com/coqui-ai/TTS) | 6 seconds | 16+ | MPL 2.0 | — |

### Voice Conversion (STS)

| Tool | Description | License |
|------|-------------|---------|
| [MetaVoice STS](https://github.com/metavoiceio/metavoice-src) | Speech-to-speech with tone color preservation | Apache 2.0 |
| [RVC](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) | Retrieval-based voice conversion with GUI | MIT |
| [so-vits-svc](https://github.com/svc-develop-team/so-vits-svc) | Singing voice conversion using VITS | MIT |
| [WhisperSpeech](https://github.com/WhisperSpeech/WhisperSpeech) | Speech-to-speech translation and conversion | — |

---

## Speech Enhancement & Audio Processing

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
| [PyAnnote VAD](https://github.com/pyannote/pyannote-audio) | Neural VAD as part of pyannote ecosystem | MIT |
| [Silero VAD](https://github.com/snakers4/silero-vad) | Pretrained VAD model | MIT |
| [WebRTC VAD](https://github.com/wiseman/py-webrtcvad) | VAD from WebRTC project | BSD |

### Speaker Diarization

| Tool | Description | License |
|------|-------------|---------|
| [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) | MSDD (Multi-scale Diarization Decoder) | Apache 2.0 |
| [pyannote.audio](https://github.com/pyannote/pyannote-audio) | Speaker diarization toolkit (v3.1) | MIT |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | Built-in diarization module | Apache 2.0 |
| [WhisperX](https://github.com/m-bain/whisperX) | Diarization via wav2vec2 alignment | BSD 2-Clause |

---

## Quick Start Guides

### Self-Hosted TTS

```bash
# Coqui TTS
pip install TTS
tts --model_name tts_models/en/ljspeech/tacotron2-DDC \
    --text "Hello world" --out_path output.wav

# Piper
pip install piper-tts
echo "Hello world" | piper --model en_US-lessac-medium --output_file output.wav

# Bark
pip install git+https://github.com/suno-ai/bark.git
python -c "from bark import generate_audio; generate_audio('Hello world')"
```

### Self-Hosted STT

```bash
# Whisper
pip install openai-whisper
whisper audio.mp3 --model large --language en

# Faster-Whisper
pip install faster-whisper
python -c "
from faster_whisper import WhisperModel
model = WhisperModel('large-v3', device='cuda')
segments, info = model.transcribe('audio.mp3')
for seg in segments: print(f'[{seg.start:.1f}s - {seg.end:.1f}s] {seg.text}')
"

# Vosk
pip install vosk
python -c "
from vosk import Model, KaldiRecognizer
import wave
wf = wave.open('audio.wav', 'rb')
model = Model('vosk-model-small-en-us-0.15')
rec = KaldiRecognizer(model, wf.getframerate())
"
```

### Voice Agent (STT → LLM → TTS)

```python
# LiveKit Agents framework
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

| Use Case | Description | Tools Used |
|----------|-------------|------------|
| **Accessibility** | Screen readers, visual impairment aids, WCAG compliance | Piper, eSpeak NG, Coqui TTS |
| **Audiobook Narration** | Large-scale audio book production | ElevenLabs, Fish Audio, StyleTTS 2 |
| **Content Localization** | Dubbing video content into multiple languages | ElevenLabs AI Dubbing, Coqui TTS |
| **Customer Support IVR** | Dynamic menus and account details in call centers | Deepgram Aura-2, Amazon Polly |
| **E-Learning** | Audio lessons, pronunciation training, multilingual education | MeloTTS, Coqui TTS, Azure AI Speech |
| **Gaming & Storytelling** | Dynamic real-time dialogue | Cartesia Sonic-3, Bark, ChatTTS |
| **GPS Navigation** | Spoken directions and traffic alerts | Piper (offline), eSpeak NG |
| **News & Articles** | Convert written content to audio | Coqui TTS, OpenAI TTS |
| **Video Production** | Voiceovers for YouTube, ads, social content | ElevenLabs, Fish Audio, CosyVoice 2 |
| **Voice Assistants** | AI voice responses for apps | OpenAI TTS, Qwen3-TTS, Chatterbox |

### Speech-to-Text Use Cases

| Use Case | Description | Tools Used |
|----------|-------------|------------|
| **Call Analysis** | Sentiment analysis, key phrase detection | AssemblyAI, WhisperX |
| **Customer Service** | Real-time call transcription, intent detection | Deepgram, Google Cloud STT |
| **Education** | Automatic captioning, lecture transcription | Whisper V3, Vosk (offline) |
| **Legal Discovery** | Searchable text from audio evidence, PII redaction | AssemblyAI, Rev AI, Speechmatics |
| **Live Captioning** | Low-latency captions for broadcasts | Parakeet TDT, Deepgram |
| **Market Research** | Extract insights from customer interactions | AssemblyAI, Deepgram |
| **Medical Documentation** | Automated clinical notes, HIPAA-compliant transcription | Whisper V3, AssemblyAI, Azure Speech |
| **Meeting Transcription** | Multi-speaker meetings with speaker labels | WhisperX, Cohere Transcribe |
| **Sales Intelligence** | Capture and analyze sales calls | AssemblyAI, WhisperX |
| **Video Content** | Captions, timestamps, content repurposing | Whisper V3, Gladia Solaria |

### Combined STT + TTS Patterns

| Pattern | Description | Example Stack |
|---------|-------------|---------------|
| **Meeting Summarizer** | Meeting audio → STT → LLM Summary → TTS Audio Summary | WhisperX → LLM → ElevenLabs |
| **Podcast Search** | Podcast → STT → Text Search → Return Timestamps | Faster-Whisper → Elasticsearch |
| **Real-Time Translation** | Speech in Language A → STT → Translate → TTS in Language B | Whisper → Translation → Coqui TTS |
| **Voice Agent** | Speech → STT → LLM → TTS → Speech | Whisper → GPT-4 → Cartesia |
| **Voice Memo Assistant** | Voice memo → STT → NLP extraction → Structured notes | Whisper → NLP Pipeline |

---

## Apps & Products

### Open-Source Applications

| App | Description | Tech Stack |
|-----|-------------|------------|
| [AllTalk TTS](https://github.com/erew123/alltalk_tts) | TTS extension for text generation web UIs | Coqui TTS, Piper, gTTS |
| [Bark UI](https://github.com/camenduru/bark-ui) | Web interface for Bark | Bark |
| [Faster-Whisper-Transcriber](https://github.com/oliverguhr/faster-whisper-server) | REST API server for Faster-Whisper | Faster-Whisper |
| [GPT-SoVITS WebUI](https://github.com/RVC-Boss/GPT-SoVITS) | Web interface for few-shot voice cloning | GPT-SoVITS |
| [Kokoro WebUI](https://github.com/nazdridoy/kokoro-webui) | Web interface for Kokoro TTS | Kokoro |
| [LiveKit Agents](https://github.com/livekit/agents) | Framework for real-time voice agents | Deepgram, Cartesia, OpenAI |
| [Open WebUI](https://github.com/open-webui/open-webui) | Chat interface with TTS/STT integration | Whisper, Coqui TTS |
| [Pinokio](https://github.com/pinokio-computer/pinokio) | One-click installer for AI apps | Multiple |
| [RVC WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) | Web interface for voice conversion | RVC |
| [WhisperX](https://github.com/m-bain/whisperX) | CLI tool for transcription with diarization | Whisper + pyannote |

### Notable Commercial Products

| Product | Category | Description |
|---------|----------|-------------|
| [Descript](https://descript.com) | Audio/Video Editing | Edit audio by editing text, overdub with cloned voice |
| [ElevenLabs](https://elevenlabs.io/) | Voice Platform | Voice cloning, dubbing, reader app |
| [Fireflies.ai](https://fireflies.ai/) | Meeting Assistant | AI notetaker for meetings |
| [Murf AI](https://murf.ai/) | Voice Generator | Voiceover generation |
| [Otter.ai](https://otter.ai) | Meeting Transcription | Real-time transcription with AI summaries |
| [Sonix](https://sonix.ai/) | Transcription | Automated transcription with translation |
| [Speechify](https://speechify.com/) | Text-to-Speech Reader | Read articles, PDFs, books aloud |
| [Trint](https://trint.com/) | Transcription | AI transcription with collaborative editing |

### AI Voice Agent Platforms

| Platform | Description |
|----------|-------------|
| [Bland AI](https://www.bland.ai/) | Real-time AI phone calls |
| [LiveKit](https://livekit.io/) | Open-source WebRTC infrastructure for voice AI |
| [Play AI](https://play.ai/) | Conversational AI voice agents |
| [Retell AI](https://www.retellai.com/) | Build conversational AI voice agents |
| [Synthflow AI](https://synthflow.ai/) | No-code voice agent builder |
| [Vapi](https://vapi.ai/) | Inbound/outbound voice agents |

---

## Tooling & Infrastructure

### Frameworks & SDKs

| Tool | Description | License |
|------|-------------|---------|
| [FFmpeg](https://ffmpeg.org/) | Audio/video processing | LGPL/GPL |
| [Hugging Face Transformers](https://github.com/huggingface/transformers) | Whisper, Wav2Vec 2.0, SpeechT5 models | Apache 2.0 |
| [Librosa](https://github.com/librosa/librosa) | Audio and music analysis | ISC |
| [pydub](https://github.com/jiaaro/pydub) | Audio manipulation | MIT |
| [SoundFile](https://github.com/bastibe/python-soundfile) | Audio file I/O via libsndfile | BSD |
| [Torchaudio](https://github.com/pytorch/audio) | PyTorch audio I/O, transforms, models | BSD |

### ASR/TTS Frameworks

| Framework | Description | License |
|-----------|-------------|---------|
| [ESPnet](https://github.com/espnet/espnet) | End-to-end speech processing (ASR + TTS + ST) | Apache 2.0 |
| [Fairseq (Meta)](https://github.com/facebookresearch/fairseq) | Sequence modeling including Wav2Vec | MIT |
| [k2 / Icefall](https://github.com/k2-fsa/icefall) | FSA-based ASR recipes | Apache 2.0 |
| [Kaldi](https://github.com/kaldi-asr/kaldi) | ASR toolkit (C++) | Apache 2.0 |
| [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) | Platform for ASR, TTS, and NLP | Apache 2.0 |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | PyTorch speech toolkit | Apache 2.0 |
| [TTS Server / AllTalk](https://github.com/erew123/alltalk_tts) | TTS integration for text generation UIs | AGPL v3 |

### Deployment & Optimization

| Tool | Description |
|------|-------------|
| [CTranslate2](https://github.com/OpenNMT/CTranslate2) | Fast inference for Transformer models |
| [ONNX Runtime](https://github.com/microsoft/onnxruntime) | Cross-platform ML inference |
| [OpenVINO](https://github.com/openvinotoolkit/openvino) | Intel hardware optimization |
| [TensorRT](https://developer.nvidia.com/tensorrt) | NVIDIA GPU inference optimization |
| [Triton Inference Server](https://github.com/triton-inference-server/server) | NVIDIA cloud inference serving |
| [vLLM](https://github.com/vllm-project/vllm) | High-throughput LLM serving |

### Python Libraries

| Library | Purpose | License |
|---------|---------|---------|
| [gTTS](https://github.com/pndurette/gTTS) | Google Translate TTS API wrapper | MIT |
| [noisereduce](https://github.com/timsainb/noisereduce) | Noise reduction | MIT |
| [praat-parselmouth](https://github.com/YannickJadoul/Parselmouth) | Python interface to Praat for phonetics | MIT |
| [pyttsx3](https://github.com/nateshmbhat/pyttsx3) | Offline TTS (Sapi5, nsss, espeak) | MIT |
| [speech_recognition](https://github.com/Uberi/speech_recognition) | Unified STT interface for multiple engines | BSD |
| [webrtcvad](https://github.com/wiseman/py-webrtcvad) | Voice activity detection | MIT |

---

## Datasets

### Speech Recognition (STT) Datasets

| Dataset | Hours | Languages | Description |
|---------|-------|-----------|-------------|
| [AISHELL](https://www.openslr.org/33) | 178 | ZH | Mandarin read speech |
| [Common Voice (Mozilla)](https://commonvoice.mozilla.org/) | 30,000+ | 100+ | Crowdsourced multilingual corpus, CC0 |
| [GigaSpeech](https://github.com/SpeechColab/GigaSpeech) | 10,000 | EN | Podcasts, YouTube, audiobooks |
| [LibriLight](https://github.com/facebookresearch/libri-light) | 60,000 | EN | Unlabelled audiobook dataset |
| [LibriSpeech](https://www.openslr.org/12) | 1,000 | EN | Read speech from LibriVox |
| [MLS (Multilingual LibriSpeech)](https://www.openslr.org/94) | 50,000 | 8 | Multilingual audiobook corpus |
| [VoxPopuli](https://github.com/facebookresearch/voxpopuli) | 400K unlabelled | 23 | European Parliament recordings |

### Speech Synthesis (TTS) Datasets

| Dataset | Hours | Speakers | Description |
|---------|-------|----------|-------------|
| [Common Voice TTS splits](https://commonvoice.mozilla.org/) | Varies | 100+ | Multilingual crowdsourced TTS data |
| [JVS Corpus](https://sites.google.com/site/shinnosuketakamichi/research-topics/jvs_corpus) | 30 | 100 | Japanese speech corpus |
| [LibriTTS](https://www.openslr.org/60) | 585 | 2,456 | Read speech for TTS, derived from LibriSpeech |
| [LJSpeech](https://keithito.com/LJ-Speech-Dataset/) | 24 | 1 (female) | Single-speaker English TTS |
| [VCTK](https://datashare.ed.ac.uk/handle/10283/3443) | 44 | 109 | English speech with diverse accents |

---

## Learning Resources

### Key Papers

| Paper | Year | Contribution |
|-------|------|-------------|
| [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | 2017 | Transformer architecture |
| [Bark](https://github.com/suno-ai/bark) | 2023 | Generative audio transformer |
| [CosyVoice](https://arxiv.org/abs/2407.05407) | 2024 | Multi-lingual voice generation |
| [F5-TTS](https://arxiv.org/abs/2410.06885) | 2024 | Flow matching for zero-shot TTS |
| [FastSpeech](https://arxiv.org/abs/1905.09263) | 2019 | Non-autoregressive TTS |
| [FastSpeech 2](https://arxiv.org/abs/2006.04558) | 2020 | End-to-end TTS |
| [OpenVoice](https://arxiv.org/abs/2312.01479) | 2023 | Voice cloning with style control |
| [StyleTTS 2](https://arxiv.org/abs/2306.07691) | 2023 | TTS via style diffusion |
| [Tacotron 2](https://arxiv.org/abs/1712.05884) | 2017 | TTS via WaveNet conditioning |
| [VITS](https://arxiv.org/abs/2106.06103) | 2021 | Variational inference + adversarial TTS |
| [Wav2Vec 2.0](https://arxiv.org/abs/2006.11477) | 2020 | Self-supervised speech representation |
| [Whisper](https://arxiv.org/abs/2212.04356) | 2022 | Speech recognition at scale |

### Courses & Tutorials

| Resource | Description |
|----------|-------------|
| [CS 224S - Stanford](http://web.stanford.edu/class/cs224s/) | Spoken Language Processing course |
| [ESPnet Tutorial](https://github.com/espnet/espnet) | Speech processing recipes |
| [Hugging Face Audio Course](https://huggingface.co/learn/audio-course) | Hands-on audio ML course |
| [Librosa Tutorials](https://librosa.org/doc/latest/tutorial.html) | Audio analysis with Python |
| [NVIDIA NeMo Tutorials](https://docs.nvidia.com/nemo-framework/user-guide/) | TTS/ASR training pipelines |
| [Speech and Language Processing (Jurafsky)](https://web.stanford.edu/~jurafsky/slp3/) | Textbook, 3rd ed. draft |

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
| [ASRU](https://asruworkshop.org/) | IEEE Automatic Speech Recognition Workshop |
| [ICASSP](https://2026.ieeeicassp.org/) | IEEE Acoustics, Speech, and Signal Processing |
| [INTERSPEECH](https://www.interspeech2026.org/) | Speech science and technology |
| [SLT](https://slt2026.org/) | IEEE Spoken Language Technology Workshop |
| [WASPAA](https://waspaa.com/) | IEEE Workshop on Applications of Signal Processing to Audio |

---

## Contributing

Contributions are welcome.

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
