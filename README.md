# Semantic Communication System Using Deep Learning

An end-to-end Semantic Communication framework that shifts the paradigm from traditional bit-level transmission (Shannon's limit) to meaning-preserving image transmission using Deep Joint Source-Channel Coding (JSCC) and Vision-Language Models.

📄 **[Read the Full Thesis / Project Report Here]()**

## 🚀 Project Overview
Traditional digital communication systems (like 64-QAM) suffer from the "cliff effect"—a catastrophic loss of data when channel noise breaches a specific threshold. This project bypasses mathematical pixel-level transmission by utilizing a **Deep JSCC Autoencoder** to map images into a robust continuous latent space. 

By integrating **OpenAI's CLIP** and **VGG-16 Perceptual Loss**, the system ensures that the transmitted signal prioritizes high-fidelity *meaning preservation* over strict pixel accuracy, making it highly robust in low Signal-to-Noise Ratio (SNR) environments designed for upcoming 6G networks.

## 🛠️ Core Technologies & Architecture
* **Deep JSCC:** Convolutional Autoencoder acting as a joint source-channel transceiver.
* **OpenAI CLIP:** Contrastive Language-Image Pretraining utilized for Zero-Shot Semantic Classification.
* **VGG-16:** Feature extraction for human-visual perceptual loss.
* **Optuna:** Bayesian hyperparameter optimization (TPE) for autonomous model sweeping.
* **PyTorch AMP:** Automatic Mixed Precision (FP16) leveraging Tensor Cores to prevent VRAM saturation.

## 📊 Key Results
* **Mitigated the Digital Cliff Effect:** While traditional 64-QAM baselines fail entirely at 5dB SNR, this Deep Semantic framework retains over **65% semantic accuracy** in extremely noisy channels.
* **Hyperparameter Optimization:** Utilized Optuna to execute 15-model sweeps, identifying optimal bandwidth compression ratios (R) and training SNRs to generalize across varying wireless environments.

## 📂 Repository Contents
* `Semantic_Communications_Deep_JSCC.ipynb`: The complete Google Colab notebook containing the PyTorch data pipeline, channel simulation, composite loss functions, and Optuna loop.
* `Semantic_Communication_System_Report.pdf`: The full academic thesis detailing the mathematical formulations, architecture constraints, and detailed graphical analysis.

## ⚙️ How to Run
This project was designed to run in a Google Colab environment equipped with an NVIDIA T4 GPU.
1. Open the `.ipynb` file in Google Colab.
2. Ensure the hardware accelerator is set to GPU (T4).
3. Run the cells sequentially. The script will automatically download the CIFAR-10 dataset, instantiate the models, and begin the Optuna optimization loop.

## 👥 Authors
* Danush Guntupalli
* Nagaraju Marella
* Saba Afreen Khatoon

*Advised by Dr. Rajeev Kumar, Indian Institute of Information Technology, Sri City.*
