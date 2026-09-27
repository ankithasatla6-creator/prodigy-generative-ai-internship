# Prodigy Task 4 – Image-to-Image Translation using cGAN (Pix2Pix)

## Objective

Implement an image-to-image translation model using a Conditional Generative Adversarial Network (cGAN) based on the Pix2Pix architecture.

## Dataset

The Facades paired image dataset was used for training.

- Training images: 400
- Image size: 256 × 256
- Input: Building photograph
- Target: Corresponding architectural label/segmentation image

## Method

The Pix2Pix model consists of two neural networks:

### Generator – U-Net

The Generator follows a U-Net encoder-decoder architecture.

It learns to transform the input building image into the corresponding target representation.

Skip connections are used to preserve important spatial information from the input.

### Discriminator – PatchGAN

The Discriminator uses the PatchGAN architecture.

It receives the input image together with either the real target or generated target and learns to distinguish between real and generated image pairs.

## Preprocessing

The paired images were:

1. Split into input and target images.
2. Resized to 256 × 256 pixels.
3. Normalized to the range [-1, 1].

## Loss Functions

The Generator was trained using:

- Adversarial loss
- L1 reconstruction loss

The total Generator loss was:

`Generator Loss = GAN Loss + 100 × L1 Loss`

The L1 component helps the generated image remain close to the target structure.

## Training

- Framework: TensorFlow
- Optimizer: Adam
- Learning rate: 0.0002
- Batch size: 1
- Training epochs: 10+

Checkpoints were saved during training for model recovery.

## Results

The trained model was used to generate an output from the input image.

The result is presented as:

**Input → Generated → Target**

The model learned the basic image-to-image mapping, although some visual artifacts remain due to the limited training duration.

## Saved Models

The trained Generator and Discriminator models were saved in Google Drive along with the training checkpoints.

## References

- GeeksforGeeks – Conditional Generative Adversarial Network
- CGAN – Conditional Generative Adversarial Network
- TensorFlow – Pix2Pix: Image-to-Image Translation
