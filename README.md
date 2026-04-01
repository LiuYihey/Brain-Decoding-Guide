<div align="center">

<img src="Title image.png" width="100%">

# 🧠 Brain-Decoding-Guide

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

</div>

> 📚 This repo aims to guide researchers who are new to the **Brain Decoding** field to quickly learn about its techniques, datasets, and applications.

---

## 📖 Table of Contents

- [Introduction](#-introduction)
- [Brain Signal Modalities](#-brain-signal-modalities)
- [Datasets](#-datasets)
- [Key Surveys](#-key-surveys)
- [Foundational Works](#-foundational-works-pre-2023)
- [Recent Advances & Core Algorithms](#-recent-advances--core-algorithms)
  - [Visual Reconstruction](#-visual-reconstruction)
  - [Speech & Language Decoding](#-speech--language-decoding)
  - [Motor & Intention Decoding](#-motor--intention-decoding)
- [Metrics & Tools](#-metrics--tools)
- [Clinical Application Cases](#-clinical-application-cases)
- [Learning Resources](#-learning-resources)
- [Contributing](#-contributing)

---

## 📌 Introduction

**Brain decoding** (also referred to as neural decoding) is a computational and neuroscientific technique that extracts meaningful, interpretable information about an individual's **subjective mental states**, **perceptual experiences**, **cognitive processes**, or **behavioral intentions** directly from recorded brain activity (e.g., **fMRI, EEG, MEG, or invasive neural recordings**). It relies on machine learning algorithms, statistical modeling, and neuroscientific insights to map patterns of neural activity to specific mental content, with applications in neuroscience research, brain-computer interfaces (BCIs), and clinical neuroscience.

---

## 🧬 Brain Signal Modalities

| Modality | Full Name | Spatial Res. | Temporal Res. | Invasiveness | Common Use Cases |
|----------|-----------|--------------|---------------|--------------|------------------|
| **fMRI** | Functional Magnetic Resonance Imaging | ~1-3 mm | ~1-2 s | Non-invasive | Visual/Semantic decoding |
| **EEG** | Electroencephalography | ~10 mm | ~1 ms | Non-invasive | Motor imagery, emotion, sleep |
| **MEG** | Magnetoencephalography | ~5 mm | ~1 ms | Non-invasive | Language, auditory processing |
| **ECoG** | Electrocorticography | ~1 cm | ~1 ms | Invasive | Speech BCI, epilepsy |
| **sEEG** | Stereoelectroencephalography | ~5 mm | ~1 ms | Invasive | Deep brain structures |
| **NIRS** | Near-Infrared Spectroscopy | ~10 mm | ~100 ms | Non-invasive | Portable BCI, infants |

> 💡 **Tip**: fMRI excels at *where* (spatial), while EEG/MEG excel at *when* (temporal). Invasive methods (ECoG, sEEG) offer the best of both but require surgery.

---

## 📊 Datasets

## Brain Decoding Dataset Collection

---

### fMRI Datasets

| Modality | Dataset | Description | Links |
|----------|---------|-------------|-------|
| Clinical | **ABIDE-I** | 1035 subjects (~111.8 hours) fMRI for autism detection and gender classification | [website](https://fcon_1000.projects.nitrc.org/indi/abide/) |
|          | **ADHD200** | 973 subjects (~129.5 hours) fMRI for ADHD diagnosis | [website](https://fcon_1000.projects.nitrc.org/indi/adhd200/) |
| Image | **NSD (2021)** | 7 subjects viewing ~70,000 natural images (~1.5–2TB, application required) | [website](https://registry.opendata.aws/nsd/) |
|       | **BOLD5000 (2021)** | 4 subjects viewing ~5,000 COCO/ImageNet images (~150–200GB) | [website](https://bold5000-dataset.github.io/website/download.html) |
|       | **GOD (2019)** | 5 subjects viewing object categories (~5–10GB) | [website](https://github.com/KamitaniLab/GenericObjectDecoding) |
|       | **THINGS fMRI1** | 3 subjects, 8,640 object images event-related fMRI dataset | [website](https://things-initiative.org/) |
|       | **vim-1 (2011)** | 1–2 subjects viewing thousands of natural images (~10GB, application required) | [website](https://crcns.org/data-sets/vc/vim-1/about-vim-1) |
| Video | **Algonauts (2021/2023)** | 10–30 subjects watching short natural videos (~50–150GB) | [website](https://algonautsproject.com/index.html) |
|       | **Human Connectome Project** | 1200 subjects multi-task and resting-state fMRI (~80–100TB) | [website](https://hub.datalad.org/hcp-openaccess/hcp1200-functional-connectivity) |
|       | **CC2017 (2017)** | 3 subjects watching ~3 hours of videos (~30–40GB) | [website](https://purr.purdue.edu/publications/2809/1) |
|       | **BOLD Moments Dataset** | 10 subjects watching 1,102 short videos (~88GB) | [website](https://github.com/blahner/BOLDMomentsDataset) |
|       | **vim-2 (2014)** | 3 subjects watching natural videos (~50–100GB, application required) | [website](https://crcns.org/data-sets/vc/vim-2/about-vim-2) |
|       | **NFED (2024)** | 5 subjects watching ~1320 facial expression videos (~176GB) | [website](https://openneuro.org/datasets/ds005047) |
|   3D  | **fMRI-Shape** | 14 subjects viewing 1600+ 3D objects | [website](https://huggingface.co/datasets/Fudan-fMRI/fMRI-Shape) |
|   3D  | **fMRI-Objaverse** | 5 subjects viewing 3,142 3D objects across 117 categories | [website](https://huggingface.co/datasets/Fudan-fMRI/fMRI-Objaverse) |
| Audio | **Narratives (2011–2018)** | 345 subjects listening to 28 spoken stories (~132GB) | [website](https://openneuro.org/datasets/ds002345) |
|       | **Nature Story Listening (2016)** | 11 subjects listening to long-form stories | [website](https://gin.g-node.org/gallantlab/story_listening) |
| Audio/Language | **MOUS-fMRI** | 200+ subjects reading or listening to sentences (well-formed vs scrambled) | [website](https://data.ru.nl/collections/di/dccn/DSC_3011020.09_236) |
| Language | **Semantic Listening vs Reading Dataset** | fMRI during reading and listening to natural stories | [website](https://gin.g-node.org/denizenslab/narratives_reading_listening_fmri) |


### EEG Datasets

| Modality | Dataset | Description | Links |
|----------|---------|-------------|-------|
| General | **RawEEGData** | 10 subjects with multiple sessions, 64-channel raw EEG recordings | [website](https://dataverse.tdl.org/dataset.xhtml?persistentId=doi:10.18738/T8/SS2NHB) |
| Clinical (AD) | **OpenNeuro AD/FTD Dataset** | 36 AD + 23 FTD patients (~14.9 hours EEG) | [website](https://github.com/OpenNeuroDatasets/ds004504) |
| Clinical (MDD) | **Mumtaz2016** | 35 subjects (~20.3 hours EEG) for depression detection | [website](https://figshare.com/articles/dataset/EEG_Data_New/4244171/2) |
| Clinical (MDD) | **MODMA** | Multimodal mental disorder dataset with EEG (128+3 channels) and speech | [website](https://modma.lzu.edu.cn/) |
| Epilepsy | **SienaScalpEEGDatabase** | Clinical scalp EEG dataset with seizure annotations | [website](https://physionet.org/content/siena-scalp-eeg/1.0.0/) |
|          | **CHB-MIT** | 20 pediatric subjects with epilepsy EEG (~40GB) | [website](https://physionet.org/content/chbmit/1.0.0/) |
| Clinical (PD) | **PD31** | 31 subjects (~2.5 hours EEG) for Parkinson’s detection | [website](https://openneuro.org/datasets/ds002778/versions/1.0.5) |
| Clinical | **TUAB** | 2000+ subjects, 1000+ hours EEG (application required) | [website](https://isip.piconepress.com/projects/nedc/html/tuh_eeg/) |
| Image | **THINGS-EEG1 (2022)** | 50 subjects viewing object images (~40GB) | [website](https://things-initiative.org/) |
|       | **THINGS-EEG2 (2025)** | 10 subjects viewing 16,740 images | [website](https://osf.io/user/6jt4f) |
|       | **Kaneshiro2015** | 10 subjects EEG responses to image stimuli | [website](https://purl.stanford.edu/bq914sc3730) |
|       | **Grootswagers2019** | 16 subjects viewing 200 images | [website](https://osf.io/a7knv/overview) |
|       | **ImageNet-EEG** | 16 subjects with 87,850 EEG-image pairs (~18GB) | [website](https://github.com/Promise-Z5Q2SQ/EEG-ImageNet-Dataset) |
| Video | **MAHNOB-HCI** | 30 subjects watching emotional videos (partially unavailable) | [website](https://mahnob-db.eu) |
|       | **SEED-DV** | 15 subjects watching emotional videos with EEG recordings | [website](https://bcmi.sjtu.edu.cn/home/seed/index.html) |
| Text | **ZuCo (2018)** | 12 subjects reading text with EEG + eye-tracking (~5–10GB) | [website](https://osf.io/q3zws) |
| Speech/Text | **Inner Speech Dataset** | 10 subjects (~9 hours EEG) for imagined speech decoding | [website](https://github.com/N-Nieto/Inner_Speech_Dataset) |
| Language | **ChineseEEG-2** | 12 subjects performing Chinese reading tasks (~100GB) | [website](https://github.com/ncclab-sustech/ChineseEEG-2) |
|          | **Broderick2018** | 19 subjects listening to natural speech | [website](https://datadryad.org/dataset/doi:10.5061/dryad.070jc) |
|          | **Chisco** | >20k high-density EEG samples for imagined speech | [website](https://github.com/zhangzihan-is-good/Chisco) |
|          | **Brennan-Hale2019** | 33 subjects listening to English speech | [website](https://deepblue.lib.umich.edu/data/concern/data_sets/bn999738r) |
| Imagined Speech | **BCIC2020-3** | 15 subjects, 64-channel EEG, 5-class imagined speech | [website](https://www.kaggle.com/datasets/abdulkareembageri/imagined-speech-eeg-signal-bci2020) |
| Speech | **KARA ONE** | 12 subjects imagined speech dataset (~24GB) | [website](https://www.cs.toronto.edu/~complingweb/data/karaOne/karaOne.html) |
| Event | **TUEV** | ~150 hours EEG with event annotations | [website](https://isip.piconepress.com/projects/nedc/html/tuh_eeg/) |
| Motor Imagery | **WBCIC_SHU** | 51 subjects (~34 hours) motor imagery EEG | [website](https://figshare.com/articles/dataset/Brain_Computer_Interface_Motor_Imagery-EEG_Dataset/22671172) |
|               | **PhysioNet-MI** | 109 subjects (~10.9 hours) motor imagery EEG | [website](https://physionet.org/content/eegmmidb/) |
|               | **BCIC-IV-2a** | 9 subjects, 22-channel EEG, 4-class motor imagery | [website](https://www.bbci.de/competition/iv/#datasets) |
| Mental Load | **MentalArithmetic** | 36 subjects performing arithmetic tasks for stress classification | [website](https://physionet.org/content/eegmat/1.0.0/) |
| Emotion | **SEED (2013)** | 15 subjects emotion EEG (application required) | [website](https://bcmi.sjtu.edu.cn/home/seed/index.html) |
| Sleep | **Sleep-EDF (2013)** | 22 subjects overnight sleep EEG (~8.1GB) | [website](https://physionet.org/content/sleep-edfx/1.0.0/) |
|       | **ISRUC** | 100 subjects sleep EEG with 5-stage classification | [website](https://sleeptight.isr.uc.pt/) |
| Multi-task | **MOABB** | Benchmark platform integrating 30+ pipelines and 36+ EEG datasets | [website](https://moabb.neurotechx.com/) |


### MEG Datasets

| Modality | Dataset | Description | Links |
|----------|---------|-------------|-------|
| Multi-task | **Cam-CAN MEG** | Lifespan dataset with hundreds of subjects (application required) | [website](https://camcan-archive.mrc-cbu.cam.ac.uk) |
| Image | **THINGS MEG1** | 4 subjects, 22,248 image trials MEG dataset | [website](https://things-initiative.org/) |
| Language | **MOUS-MEG** | 200+ subjects reading or listening to sentences | [website](https://data.ru.nl/collections/di/dccn/DSC_3011020.09_236) |
| Language | **MEG-MASC** | 27 subjects listening to speech stimuli | [website](https://osf.io/ag3kj/overview) |
| Clinical | **OMEGA** | 444 controls + 200 patients (>150 hours MEG) | [website](https://www.mcgill.ca/bic/neuroinformatics/omega) |
| Multi-task | **HCP-MEG** | MEG subset of HCP with multiple tasks | [website](https://neuroimage.usc.edu/brainstorm/Tutorials/HCP-MEG) |


### ECoG Datasets

| Modality | Dataset | Description | Links |
|----------|---------|-------------|-------|
| Multi-task | **CRCNS ECoG** | 21 epilepsy patients performing audiovisual tasks (~8GB) | [website](https://deepblue.lib.umich.edu/data/concern/data_sets/4f16c309z) |
| Audio | **Metzger2023** | Single-subject speech-related ECoG dataset | [website](https://zenodo.org/records/8200782) |


### SEEG Datasets
| Language | **Verwoert2022** | 54–127 epilepsy patients performing reading tasks | [website](https://osf.io/nrgx6/overview) |


### MEA Datasets
| Audio | **Willett2023** | Neural recordings for speech prosthesis with 12,100 spoken sentences | [website](https://datadryad.org/dataset/doi:10.5061/dryad.x69p8czpq) |


### Multimodal Datasets

| Signal | Modality | Dataset | Description | Links |
|--------|----------|---------|-------------|-------|
| EEG + MEG | Motor | **SomatoMotor** | 5 subjects (~0.7 hours) EEG+MEG motor task dataset | [website](https://openneuro.org/datasets/ds006035/versions/1.0.0) |
| EEG + fMRI | Video + Audio + Text | **CineBrain** | 6 subjects (~6 hours) multimodal dataset with video stimuli and brain recordings | [website](https://huggingface.co/datasets/Fudan-fMRI/CineBrain) |
|            | Resting-state | **LEMON** | 220 subjects (~39.6 hours) resting-state EEG+fMRI dataset | [website](https://fcon_1000.projects.nitrc.org/indi/retro/MPI_LEMON.html) |
|            | Video | **Nat-View** | 22 subjects (~42.8 hours) natural viewing EEG+fMRI dataset | [website](https://openneuro.org/datasets/ds003688) |
| MEG + fMRI | Language | **SMN4Lang** | 12 subjects (~70.4 hours) multimodal language dataset | [website](https://openneuro.org/datasets/ds004078/versions/1.2.1) |
| EEG + fNIRS + PPG | Speech + Vision + Motor | **L-mind** | 12 subjects multimodal dataset with 23,928 instruction-based samples | [website](https://huggingface.co/datasets/Lance1573/L-Mind) |
| EEG + EOG + EMG | Sleep | **CAP** | Sleep dataset with CAP annotations including normal and pathological recordings | [website](https://physionet.org/content/capslpdb/1.0.0/) |
|                 | Sleep | **MASS** | Large-scale multimodal sleep dataset with 200+ subjects | [website](http://ceams-carsm.ca/mass/) |


---

## 📑 Key Surveys

| Year | Title | Venue | Highlights |
|------|-------|-------|------------|
| 2025 | [A Survey on fMRI-based Brain Decoding for Reconstructing Multimodal Stimuli](https://arxiv.org/abs/2503.15978) | TPAMI | Dataset/ROI summaries, model taxonomy (end-to-end, pre-trained, LLM-centric) |
| 2025 | [Deep Neural Networks and Brain Alignment: Brain Encoding and Decoding](https://openreview.net/forum?id=YxKJihRcby) | TMLR | Encoding + decoding, DL-brain alignment [[Code]](https://github.com/subbareddy248/Awesome-Brain-Encoding--Decoding) |
| 2025 | [Transformer-based EEG Decoding: A Survey](https://arxiv.org/abs/2507.02320) | ArXiv | 200+ papers on Transformer for EEG (2019-2024) |
| 2025 | [Brain Foundation Models: A Survey](https://arxiv.org/abs/2503.00580) | ArXiv | Foundation models for neural signals, pre-training paradigms |
| 2024 | [Deep Representation Learning for EEG-based BCIs: A Review](https://arxiv.org/abs/2405.19345) | ArXiv | Autoencoders, SSL, foundation models for EEG |
| 2022 | [fMRI Brain Decoding and Its Applications in BCI: A Survey](https://pubmed.ncbi.nlm.nih.gov/35203991/) | Brain | Classic ML to deep learning evolution |

---

## 📜 Foundational Works (Pre-2023)

> Milestone papers that established the field.

| Year | Title | Task | Feature | Links |
|------|-------|------|---------|-------|
| 2016 | [Natural Speech Reveals the Semantic Maps that Tile Human Cerebral Cortex](https://www.nature.com/articles/nature17637) | Semantic | Cortical semantic atlas | |
| 2017 | [Deep Learning with Convolutional Neural Networks for EEG Decoding and Visualization](https://onlinelibrary.wiley.com/doi/10.1002/hbm.23730) | Motor | Interpretable filters | [[Code]](https://github.com/braindecode/braindecode) |
| 2018 | [EEGNet: A Compact Convolutional Neural Network for EEG-based BCIs](https://iopscience.iop.org/article/10.1088/1741-2552/aace8c) | Motor | BCI baseline | [[Code]](https://github.com/vlawhern/arl-eegmodels) |
| 2019 | [Deep Image Reconstruction from Human Brain Activity](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006633) | Visual | Feature optimization | |

---

## ⚙️ Recent Advances & Core Algorithms

> High-impact papers from 2023-2025.

### 🖼️ Visual Reconstruction

#### fMRI → Image

| Year | Title | Arch | Feature | Links |
|------|-------|------|---------|-------|
| 2023 | [High-Resolution Image Reconstruction with Latent Diffusion Models from Human Brain Activity](https://openaccess.thecvf.com/content/CVPR2023/html/Takagi_High-Resolution_Image_Reconstruction_With_Latent_Diffusion_Models_From_Human_Brain_CVPR_2023_paper.html) | `Diffusion` | Direct fMRI-to-LDM mapping without fine-tuning | [[Code]](https://github.com/yu-takagi/StableDiffusionReconstruction) |
| 2023 | [Seeing Beyond the Brain: MinD-Vis](https://arxiv.org/abs/2211.06956) | `Diffusion` | Large-scale resting-state fMRI pre-training + sparse coding | [[Code]](https://github.com/zjc062/mind-vis) |
| 2023 | [Reconstructing the Mind's Eye: MindEye](https://arxiv.org/abs/2305.18274) | `Diffusion` | Dual-path: contrastive retrieval + diffusion prior | [[Code]](https://github.com/MedARC-AI/fmri-reconstruction-nsd) |
| 2024 | [MindEye2: Shared-Subject Models Enable fMRI-to-Image with 1 Hour of Data](https://arxiv.org/abs/2403.11207) | `Diffusion` | Cross-subject transfer via functional alignment; only 1hr data needed | [[Code]](https://github.com/MedARC-AI/MindEyeV2) [[Website]](https://medarc-ai.github.io/mindeye2/) |
| 2024 | [MindBridge: A Cross-Subject Brain Decoding Framework](https://arxiv.org/abs/2404.07850) | `Diffusion` | Single model for multi-subject; bio-inspired aggregation | [[Code]](https://github.com/littlepure2333/MindBridge) |

#### EEG → Image

| Year | Title | Arch | Feature | Links |
|------|-------|------|---------|-------|
| 2024 | [DreamDiffusion: Generating High-Quality Images from Brain EEG Signals](https://arxiv.org/abs/2306.16934) | `Diffusion` | Temporal masking pre-train + CLIP alignment; first EEG-to-image | [[Code]](https://github.com/bbaaii/DreamDiffusion) |

#### fMRI → Video

| Year | Title | Arch | Feature | Links |
|------|-------|------|---------|-------|
| 2023 | [Cinematic Mindscapes: High-Quality Video Reconstruction from Brain Activity](https://arxiv.org/abs/2305.11675) | `Diffusion` | Spatiotemporal attention + contrastive learning; arbitrary frame-rate | [[Code]](https://github.com/jqin4749/MindVideo) [[Website]](https://www.mind-video.com) |
| 2025 | [Animate Your Thoughts: Reconstruction of Dynamic Natural Vision from Human Brain Activity](https://openreview.net/forum?id=BpfsxFqhGa) | `Diffusion` | 将 fMRI 信号解耦为语义、结构和运动三种独立特征，解码驱动T2I模型重建每帧合成gif | [[Code]](https://github.com/ReedOnePeck/MindAnimator) |

---

### 🗣️ Speech & Language Decoding

#### Invasive Speech (ECoG/Intracortical)

| Year | Title | Arch | Feature | Links |
|------|-------|------|---------|-------|
| 2023 | [A High-Performance Speech Neuroprosthesis](https://www.nature.com/articles/s41586-023-06377-x) | `RNN` | 62 wpm; first large-vocab decoding (125k words) | [[Code]](https://github.com/fwillett/speechBCI) |
| 2023 | [A High-Performance Neuroprosthesis for Speech Decoding and Avatar Control](https://www.nature.com/articles/s41586-023-06443-4) | `RNN` | Real-time avatar control with facial expression + speech | |
| 2025 | [A Streaming Brain-to-Voice Neuroprosthesis](https://www.nature.com/articles/s41593-025-01905-6) | `RNN-Transducer` | 80ms streaming decoding; real-time speech synthesis | [[Code]](https://github.com/cheoljun95/streaming.braindecoder) |

#### Non-invasive Semantic (fMRI/EEG)

| Year | Title | Arch | Feature | Links |
|------|-------|------|---------|-------|
| 2023 | [Semantic Reconstruction of Continuous Language from Non-invasive Brain Recordings](https://www.nature.com/articles/s41593-023-01304-9) | `Transformer` | GPT autoregressive decoding + beam search; multi-cortex support | |
| 2024 | [DeWave: Discrete EEG Waves Encoding for Brain Dynamics to Text Translation](https://arxiv.org/abs/2309.14030) | `Transformer` | Discrete codebook alignment to LLM; no word-level gaze annotation | |

---

### 🎯 Motor & Intention Decoding

| Year | Title | Arch | Feature | Links |
|------|-------|------|---------|-------|
| 2024 | [CTNet: A Convolutional Transformer Network for EEG-based Motor Imagery Classification](https://www.nature.com/articles/s41598-024-71118-7) | `CNN-Transformer` | CNN local features + Transformer global dependencies | |
| 2023 | [EEG Conformer: Convolutional Transformer for EEG Decoding and Visualization](https://ieeexplore.ieee.org/document/9991178) | `Conformer` | Conv + self-attention; CAM-based topographic visualization | [[Code]](https://github.com/eeyhsong/EEG-Conformer) |
| 2022 | [ATCNet: Attention Temporal Convolutional Network for EEG-based Motor Imagery Classification](https://ieeexplore.ieee.org/document/9852687) | `TCN` | Sliding window + multi-head attention + TCN residual | [[Code]](https://github.com/Altaheri/EEG-ATCNet) |

---

## 📏 Metrics & Tools

### Evaluation Metrics

| Category | Metric | Description |
|----------|--------|-------------|
| **Encoding** | Pearson r, R² | Correlation between predicted and actual brain activity |
| **Low-level Reconstruction** | PixCorr, SSIM, PSNR | Pixel-level similarity |
| **High-level Reconstruction** | CLIP Score, Inception Score | Semantic/perceptual similarity |
| **Classification** | Accuracy, F1, AUC | Standard classification metrics |
| **Retrieval** | Top-k Accuracy, MRR | Retrieval-based evaluation |

### Software & Libraries

| Tool | Description | Link |
|------|-------------|------|
| **MNE-Python** | MEG, EEG, sEEG, ECoG, NIRS analysis | [[Website]](https://mne.tools/) [[GitHub]](https://github.com/mne-tools/mne-python) |
| **Nilearn** | Statistical learning on fMRI data | [[Website]](https://nilearn.github.io/) [[GitHub]](https://github.com/nilearn/nilearn) |
| **Braindecode** | Deep learning for EEG/ECoG/MEG decoding; EEGNet, ShallowNet, etc. | [[Website]](https://braindecode.org/) [[GitHub]](https://github.com/braindecode/braindecode) |
| **TorchEEG** | PyTorch library for EEG processing & models | [[GitHub]](https://github.com/torcheeg/torcheeg) |
| **Net2Brain** | Compare DNN activations with brain activity (RSA, encoding) | [[GitHub]](https://github.com/cvai-roig-lab/Net2Brain) |
| **Neural_Decoding** | Classic + DL decoders (Kalman, Wiener, LSTM, etc.) | [[GitHub]](https://github.com/KordingLab/Neural_Decoding) |
| **PyCortex** | fMRI visualization on cortical surface | [[GitHub]](https://github.com/gallantlab/pycortex) |
| **RSA Toolbox** | Representational Similarity Analysis | [[GitHub]](https://github.com/rsagroup/rsatoolbox) |

### Benchmark Platforms

| Platform | Description | Link |
|----------|-------------|------|
| **Algonauts Project** | Annual challenge for predicting brain responses to visual stimuli | [[Website]](http://algonauts.csail.mit.edu/) |
| **Brain-Score** | Benchmark for comparing DNNs with primate visual cortex | [[Website]](https://www.brain-score.org/) [[GitHub]](https://github.com/brain-score/brain-score) |
| **MOABB** | Mother of All BCI Benchmarks; 36 EEG datasets, 30 pipelines | [[Website]](https://moabb.neurotechx.com/) [[GitHub]](https://github.com/NeuroTechX/moabb) |

---

## 🏥 Clinical Application Cases

> Recent breakthroughs demonstrating real-world clinical impact.

| Case | Year | Description | Links |
|------|------|-------------|-------|
| **Synchron & Apple: Thought-Controlled iPad** | 2025 | ALS patient controlled iPad via Stentrode implant + Apple BCI HID protocol—navigating apps, composing texts using only thoughts | [[News]](https://www.businesswire.com/news/home/20250804537175/en/Synchron-Debuts-First-Thought-Controlled-iPad-Experience-Using-Apples-New-BCI-Human-Interface-Device-Protocol) [[Video]](https://www.youtube.com/watch?v=YK8r5vdpozA) |
| **Neuralink Telepathy** | 2024 | First Neuralink human implant; quadriplegic patient played chess & Civilization VI via cursor control using thoughts alone | [[News]](https://neuralink.com/blog/) [[Video]](https://www.youtube.com/watch?v=2rXrGH52aoM) |
| **UC Davis ALS Speech BCI** | 2024 | Restored speech for ALS patient with >97% accuracy; preserved voice identity using high-density ECoG | [[Press]](https://health.ucdavis.edu/news/headlines/new-brain-computer-interface-allows-man-with-als-to-speak-again/2024/08) [[Paper]](https://www.nejm.org/doi/full/10.1056/NEJMoa2314132) |

---

## 📚 Learning Resources

### 📺 Video Tutorials & Courses

| Resource | Description | Link |
|----------|-------------|------|
| **Neuromatch Academy** | World-class open course on computational neuroscience; encoding/decoding basics | [[Website]](https://neuromatch.io/) [[YouTube]](https://www.youtube.com/@neuaboratory) [[Bilibili]](https://search.bilibili.com/all?keyword=Neuromatch) |
| **INCF: Deep Learning in Neuroscience** | Beginner-level DL for neuroscience applications | [[Website]](https://training.incf.org/lesson/fundamentals-deep-learning-neuroscience) |

### 📖 Textbooks & Reading

| Resource | Description | Link |
|----------|-------------|------|
| **Deep Learning (Goodfellow et al.)** | Deep learning bible; free online | [[Website]](https://www.deeplearningbook.org/) |
| **Awesome-Brain-Encoding-Decoding** | Curated paper list | [[GitHub]](https://github.com/subbareddy248/Awesome-Brain-Encoding--Decoding) |

### 🌐 Communities

| Community | Description | Link |
|-----------|-------------|------|
| **NeuroAI WeChat Group** | Chinese community for brain + AI research | Contact via WeChat number `MobiusAI` |
| **BCI Society** | International BCI research community | [[Website]](https://bcisociety.org/) |
| **OHBM** | Organization for Human Brain Mapping | [[Website]](https://www.humanbrainmapping.org/) |

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

<div align="center">

**If you find this guide helpful, please consider giving it a ⭐!**

</div>
