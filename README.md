I tried running a notebook with Latent Diffusion model to understand Ghibli image generation with original and prompt = horse and new prompt Zebra.

Latent Diffusion Models (LDMs), a type of diffusion model optimized for efficiency and high-quality image generation. 

Key steps:
1. Encoding into Latent Space

A high-resolution image is compressed into a lower-dimensional representation using an Autoencoder.

This latent space captures the essential features of the image but in a more compact form.


2. Diffusion Process (Noise Addition & Removal)

Noise is gradually added to the latent representation over multiple steps, destroying details and making it look like pure noise.

A neural network (U-Net with attention layers) learns to reverse this process step-by-step, predicting how to remove noise and reconstruct the original structure.



3. Guidance & Text Conditioning

Text prompts guide the image generation by conditioning the diffusion process using a text encoder (CLIP).



4. Decoding Back to Pixel Space

Once the denoised latent representation is obtained, it is converted back into a high-resolution image using the decoder.


