# Synthetic Data Generation for Enhanced Object Detection of Roadway Assets

## 🚀 Overview
This project explores **Synthetic Data Generation** to improve the object detection of roadway assets using state-of-the-art generative AI models. The aim is to supplement real-world datasets with high-fidelity synthetic images to enhance object detection in autonomous driving and intelligent transportation systems.

## 📌 Key Highlights
- **Addresses Data Scarcity**: Reduces the need for expensive real-world dataset collection and annotation.
- **Improves Model Robustness**: Enhances object detection performance under diverse environmental conditions.
- **Explores Five Generative Models**:
  1. **ResNet-based U-Net Diffusion Model**
  2. **U-Net Diffusion Model**
  3. **Conditional Generative Adversarial Network (Conditional GAN)**
  4. **U-Net Vision Transformer (ViT)**
  5. **Pre-trained Diffusion Model**

## 🏗️ Methodology
### Dataset
- **Size**: 12,000 images (8,000 train, 2,000 validation, 2,000 test)
- **Resolution**: 1280×720
- **Annotations**: COCO-format bounding boxes for roadway assets

### Generative Models
1. **ResNet-based U-Net Diffusion Model**
   - Uses a ResNet-50 encoder within a U-Net architecture for denoising diffusion.
   
2. **U-Net Diffusion Model**
   - Implements diffusion-based image generation using a simplified U-Net design.

3. **Conditional GAN**
   - Employs adversarial training to generate realistic images conditioned on input features.

4. **U-Net Vision Transformer (ViT)**
   - Integrates a ViT module into the U-Net for improved spatial consistency.

5. **Pre-trained Diffusion Model**
   - Fine-tunes a large-scale diffusion model (e.g., Stable Diffusion) for roadway asset synthesis.

## 📊 Experimental Results
| Model | FID ↓ | PSNR ↑ | mAP ↑ | Training Time (hrs) ↓ |
|--------|------|------|------|------|
| No Synthetic Data | - | - | 0.58 | - |
| Traditional Augmentation | - | - | 0.60 | - |
| Conditional GAN | 32.4 | 26.5 | 0.64 | 48 |
| U-Net Diffusion | 28.7 | 27.2 | 0.66 | 72 |
| U-Net ViT | 25.9 | 27.8 | 0.68 | 80 |
| **Pre-trained Diffusion** | **23.5** | **28.4** | **0.69** | **40** |
| **ResNet U-Net Diffusion** | **21.8** | **29.1** | **0.71** | **85** |

- **Best-performing model**: The **Pre-trained Diffusion Model** achieved the highest quality synthetic images and object detection improvement.
- **Conditional GAN** showed moderate improvements, while other diffusion-based approaches required more computational resources for optimal performance.

## 🔬 Observations
- The **Pre-trained Diffusion Model** produced the most realistic images and significantly improved object detection performance.
- **Conditional GANs** provided a good balance between realism and computational efficiency.
- **U-Net Vision Transformers** showed potential but required more extensive training.
- **Training Limitations**: Restricted GPU access limited hyperparameter tuning and long-run training experiments.

## 🚀 How to Run
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/synthetic-data-roadway-detection.git
   ```
2. Run the provided Jupyter notebooks for generating synthetic images and evaluating detection performance.

## 🔜 Future Work
- **Extended Training**: Train models on more powerful GPUs to improve synthetic image fidelity.
- **Multi-Modal Conditioning**: Incorporate additional modalities (e.g., LiDAR, depth maps) to enhance image realism.
- **Domain Adaptation**: Blend synthetic and real datasets to bridge the synthetic-to-real gap.

## 📜 Conclusion
This project demonstrates that synthetic data generation significantly enhances object detection of roadway assets. The **Pre-trained Diffusion Model** emerged as the most effective method, while Conditional GANs provided a viable alternative. Further improvements require larger-scale computing resources and more sophisticated conditioning techniques.

---

Enhancing roadway asset detection through synthetic data generation! 🚦📷
