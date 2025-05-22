# Text-Conditioned Image Synthesis with Latent Diffusion Models (LDM)

This project demonstrates how to train a **text-conditioned Latent Diffusion Model (LDM)** on the [CelebA-Dialog](https://github.com/ziqihuangg/CelebA-Dialog) dataset. It uses pretrained encoders and a custom diffusion model to generate face images conditioned on natural language descriptions.

For a detailed explanation of the methodology, training setup, and results, check out the full report:  
📄 [Read the Report (PDF)](LDM_final.pdf)

---

## Results

### Latents and Reconstructions

<table>
  <tr>
    <td align="center"><b>Latent Representation</b></td>
    <td align="center"><b>Reconstructed Image</b></td>
  </tr>
  <tr>
    <td><img src="./Latent.png" width="500"/></td>
    <td><img src="./Reconstruction.png" width="500"/></td>
  </tr>
</table>

---

### Text-Conditioned Generation

The model generates images by denoising in the latent space based on a text prompt and decoding through a pretrained VAE.

<p align="center">
  <img src="./example.png" width="800"/>
</p>

---

## Model Components

- **Latent Encoder (VAE):** Pretrained `CompVis/stable-diffusion-v1-4`
- **Text Encoder:** Pretrained CLIP (`openai/clip-vit-large-patch14`)
- **Diffusion Model:** Trained from scratch on CelebA-Dialog latents and captions

---

## 📦 Preprocessed Data

To speed up training and evaluation, you can use our preprocessed datasets:

- Aligned and captioned images from CelebA-Dialog  
  👉 [Kaggle Dataset](https://huggingface.co/datasets/Om2005Prakash/CelebA_Dialogue_Precomputed/tree/main)

- Precomputed latents and tokenized captions  
  👉 [Hugging Face Dataset](https://huggingface.co/datasets/Om2005Prakash/CelebA_Dialogue_Precomputed/tree/main)