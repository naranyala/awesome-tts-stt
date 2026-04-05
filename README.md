# Awesome Text-to-Speech & Speech-to-Text [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome text-to-speech (TTS), speech-to-text (STT), speech synthesis, recognition, voice cloning, and audio processing resources.

[📊 Benchmarks](#benchmarks--leaderboards) · [💬 TTS](#text-to-speech-tts) · [🎙️ STT](#speech-to-text-stt) · [🔊 Voice Cloning](#voice-cloning--conversion) · [🎧 Speech Enhancement](#speech-enhancement--audio-processing) · [📚 Datasets](#datasets) · [🛠️ Tooling](#tooling--infrastructure) · [🎓 Learning](#learning-resources)

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
| [ElevenLabs](https://elevenlabs.io/) | Industry-leading quality, professional voice cloning (3min), AI dubbing, 70+ languages | $0.10/min | ~200ms |
| [Cartesia Sonic-3](https://cartesia.ai/) | Ultra-low latency streaming, natural laughs/emotes, 40+ languages, 15s cloning | Pay-per-char | 40ms (Turbo) |
| [OpenAI TTS](https://platform.openai.com/docs/guides/text-to-speech) | Steerable output (tone, pacing), 13+ custom voices, GPT-4o mini integration | Pay-per-char | ~300ms |
| [Deepgram Aura-2](https://deepgram.com/) | Sub-200ms TTFB, 40+ English accents, semantic turn detection | $0.03/1k chars | 90ms |
| [Amazon Polly](https://aws.amazon.com/polly/) | Standard/Neural/Generative tiers, colloquial speech, 5M free chars/mo | $4-100/1M chars | ~200ms |
| [Google Cloud TTS](https://cloud.google.com/text-to-speech) | Natural voices, pitch/rate customization, AudioLM neural voices | Pay-per-char | ~200ms |
| [Azure AI Speech](https://azure.microsoft.com/products/ai-services/ai-speech/) | Neural TTS, custom voice creation, personal voice cloning | Pay-per-char | ~250ms |
| [PlayHT](https://play.ht/) | 829 AI voices, 142 languages, instant cloning, multi-platform integrations | $39-99/mo | ~300ms |
| [Resemble AI](https://www.resemble.ai/) | Rapid cloning (10s), enterprise security, custom brand voices | Enterprise | ~200ms |
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

| Project | WER (EN) | Languages | Speed | Parameters | Notes |
|---------|----------|-----------|-------|------------|-------|
| [Cohere Transcribe](https://huggingface.co/CohereLabs/cohere-transcribe-03-2026) | **5.42%** | 14 | 3× throughput | 2B | #1 HF ASR, Apache 2.0, vLLM optimized |
| [Whisper Large V3 (OpenAI)](https://github.com/openai/whisper) | 7.4% | 99+ | ~10× RT | 1.55B | Most popular STT model |
| [Canary Qwen 2.5B (NVIDIA)](https://huggingface.co/nvidia/canary-qwen-2.5b) | **5.63%** | EN | 418× RTF | 2.5B | #1 Open ASR Leaderboard, NeMo toolkit |
| [IBM Granite Speech 3.3](https://huggingface.co/ibm-granite/granite-speech-3.3-8b) | 5.85% | EN, FR, DE, ES | — | 8B | Enterprise accuracy |

#### ⭐ Tier 2: Strong Alternatives

| Project | WER (EN) | Languages | Speed | Parameters | Notes |
|---------|----------|-----------|-------|------------|-------|
| [Whisper Large V3 Turbo](https://github.com/openai/whisper) | 7.75% | 99+ | 216× RTF | 809M | 6× faster, transcription-only |
| [Parakeet TDT 0.6B](https://huggingface.co/nvidia/parakeet-tdt-0.6b-v2) | 6.05% | EN | 3386× RTF | 600M | Auto-punctuation, batch processing |
| [Parakeet TDT 1.1B (NVIDIA)](https://huggingface.co/nvidia/parakeet-tdt-1.1b) | ~8.0% | EN | **>2000× RTF** | 1.1B | Ultra-low-latency streaming |
| [Distil-Whisper](https://github.com/huggingface/distil-whisper) | ~8.4% | EN | 5-6× faster | 756M | Frozen encoder, lightweight |
| [Faster-Whisper](https://github.com/SYSTRAN/faster-whisper) | — | 99+ | 4× faster | — | CTranslate2 optimization |

#### 🔧 Tier 3: Specialized & Niche

| Project | Languages | Speed | Parameters | Notes |
|---------|-----------|-------|------------|-------|
| [WhisperX](https://github.com/m-bain/whisperX) | Multi | — | — | Word-level timestamps + diarization |
| [Wav2Vec 2.0 XLSR (Meta)](https://github.com/facebookresearch/fairseq) | 53+ | — | — | Self-supervised, needs fine-tuning |
| [Vosk](https://github.com/alphacep/vosk-api) | 20+ | Real-time | — | Offline, edge devices |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | Multi | — | — | All-in-one speech toolkit |
| [NeMo (NVIDIA)](https://github.com/NVIDIA/NeMo) | Multi | — | — | End-to-end ASR/TTS platform |
| [SenseVoice](https://github.com/FunAudioLLM/SenseVoice) | Multi | — | — | ASR + LID + SER + AED |
| [Silero Models](https://github.com/snakers4/silero-models) | Multi | — | — | Pretrained STT, VAD, punctuation |
| [Moonshine](https://github.com/usefulsensors/moonshine) | Edge-optimized | Low-latency | **27M** | Smartphones, IoT, embedded |
| [FunASR](https://github.com/modelscope/FunASR) | Multi | — | — | Alibaba's industrial-grade ASR |
| [Microsoft MAI-Transcribe-1](https://microsoft.ai/news/state-of-the-art-speech-recognition-with-mai-transcribe-1/) | Multi | — | — | 2026 SOTA, enterprise-grade |
| [ESPnet](https://github.com/espnet/espnet) | Multi | — | — | End-to-end ASR/TTS/SE toolkit |
| [Kaldi](https://github.com/kaldi-asr/kaldi) | Multi | — | — | Classic ASR toolkit (C++) |
| [Coqui STT](https://github.com/coqui-ai/STT) | Multi | — | — | Built on Mozilla DeepSpeech |

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
| [Gladia Solaria](https://www.gladia.io/) | First truly universal STT model, multilingual, real-time | Pay-per-char |

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

| Tool | Description | Latency | Best For |
|------|-------------|---------|----------|
| [RVC](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) | Retrieval-based voice conversion with GUI, widely used in music/streaming | Real-time | Music, streaming, live conversion |
| [so-vits-svc](https://github.com/svc-develop-team/so-vits-svc) | High-quality singing voice conversion using VITS architecture | Near real-time | Singing voice conversion |
| [WhisperSpeech](https://github.com/WhisperSpeech/WhisperSpeech) | Speech-to-speech translation and conversion pipeline | — | Cross-language voice transfer |
| [MetaVoice STS](https://github.com/metavoiceio/metavoice-src) | Speech-to-speech with tone color preservation | — | Conversational AI |

---

## Speech Enhancement & Audio Processing

### Noise Suppression & Enhancement

| Tool | Description | Type |
|------|-------------|------|
| [DeepFilterNet](https://github.com/Rikorose/DeepFilterNet) | Low-complexity speech enhancement using deep filtering | Open Source |
| [Demucs (Meta)](https://github.com/facebookresearch/demucs) | Music/source separation with high-quality audio extraction | Open Source |
| [Spleeter (Deezer)](https://github.com/deezer/spleeter) | Source separation with pretrained models | Open Source |
| [RNNoise](https://github.com/xiph/rnnoise) | Recurrent neural network for audio noise reduction | Open Source |
| [VoiceFixer](https://github.com/haoheliu/voicefixer) | Restore speech quality under real-world degradation | Open Source |
| [AudioSep](https://github.com/Audio-AGI/AudioSep) | Separate audio with natural language queries | Open Source |

### Voice Activity Detection (VAD)

| Tool | Description |
|------|-------------|
| [Silero VAD](https://github.com/snakers4/silero-vad) | Pretrained enterprise-grade VAD, fast and accurate |
| [WebRTC VAD](https://github.com/wiseman/py-webrtcvad) | Lightweight VAD for real-time audio processing |
| [PyAnnote VAD](https://github.com/pyannote/pyannote-audio) | Neural VAD as part of the pyannote ecosystem |

### Speaker Diarization

| Tool | DER | Description |
|------|-----|-------------|
| [pyannote.audio](https://github.com/pyannote/pyannote-audio) | ~10% | De facto standard for speaker diarization, v3.1 with pretrained models |
| [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) | ~10% | MSDD (Multi-scale Diarization Decoder), GPU-accelerated |
| [SpeechBrain](https://github.com/speechbrain/speechbrain) | ~12% | Built-in diarization as part of speech processing toolkit |
| [WhisperX](https://github.com/m-bain/whisperX) | — | Adds diarization on top of Whisper transcriptions |

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

### Evaluation & Benchmarking

| Tool | Description |
|------|-------------|
| [Open ASR Leaderboard (HF)](https://huggingface.co/spaces/hf-audio/open_asr_leaderboard) | Community ASR leaderboard with WER benchmarks |
| [Superb Benchmark](https://superbbenchmark.org/) | Speech Universal Performance Benchmark |
| [TTS Evaluation](https://github.com/keonlee94/tts-evaluation) | MOS, MCD, F0 metrics for TTS quality |
| [LibriSpeech test sets](https://www.openslr.org/12) | Standard clean/other ASR evaluation splits |

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

### Blogs & Communities

| Resource | Description |
|----------|-------------|
| [r/speechrecognition (Reddit)](https://www.reddit.com/r/speechrecognition/) | Speech recognition community |
| [r/TextToSpeech (Reddit)](https://www.reddit.com/r/TextToSpeech/) | TTS community and discussion |
| [r/LocalLLaMA (Reddit)](https://www.reddit.com/r/LocalLLaMA/) | Self-hosted AI including speech models |
| [Hugging Face Audio Hub](https://huggingface.co/models?pipeline_tag=text-to-speech) | Audio model repository |
| [NVIDIA Developer Blog](https://developer.nvidia.com/blog/) | Speech AI and NeMo updates |
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

## Benchmarks & Leaderboards

### STT/ASR Benchmarks

| Benchmark | Metric | Description |
|-----------|--------|-------------|
| **Hugging Face Open ASR** | WER (lower is better) | Community leaderboard, #1: Cohere Transcribe (5.42%) |
| **LibriSpeech test-clean** | WER | Standard academic benchmark, SOTA < 2% |
| **Common Voice test** | WER | Crowdsourced multilingual evaluation |

### TTS Benchmarks

| Metric | Description |
|--------|-------------|
| **MOS (Mean Opinion Score)** | Human-rated audio quality (1-5), human speech ~4.5 |
| **CMOS (Comparative MOS)** | Relative quality comparison between systems |
| **MCD (Mel-Cepstral Distortion)** | Objective spectral distance (lower is better) |
| **WER (TTS output)** | ASR evaluated on generated speech |
| **RTF (Real-Time Factor)** | Inference speed (< 1 = real-time) |

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