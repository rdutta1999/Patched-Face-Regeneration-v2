# Patched-Face-Regeneration-v2

## Introduction
This is an updated version of my previous [Patched Face Regeneration model](https://github.com/rdutta1999/Patched-Face-Regeneration-GAN).
Instead of using a Denoising Autoencoder as the Generator and a Deep Convolutional Network as the Discriminator, I used a U-net to generate images and passed the output through a pre-trained VGG16 to calculate the style and content losses, based on Justin Johnson et al's [Perceptual Losses for Real-Time Style Transfer and Super-Resolution](https://arxiv.org/abs/1603.08155).
The idea was inspired by Jeremy Howard's [fastai](https://arxiv.org/abs/1603.08155) course.

Dataset: [Celeb-A](https://www.kaggle.com/jessicali9530/celeba-dataset)

Training Time: ~10.5 hours on a RTX 2060 Super.

The final model can be found [here](https://drive.google.com/drive/folders/1aTHugE11jdmwwKQQWI-nVFuJLYl4-2Mt?usp=sharing).

## Setting Up
1) Create a new Python/Anaconda environment (optional but recommended). You might use the `environment.yml` file for this purpose (Skip Step-2 in that case).

2) Install the necessary packages. Refer to the packages mentioned in `environment.yml`.

3) Download the final model from [here](https://drive.google.com/drive/folders/1aTHugE11jdmwwKQQWI-nVFuJLYl4-2Mt?usp=sharing).

4) Download the [Celeb-A](https://www.kaggle.com/jessicali9530/celeba-dataset) dataset, and place it in the directory in the following manner:-
<pre>
├─── Patched-Face-Regeneration-v2
     ├─── final_model     
     ├─── feat_comp-96x96.png
     ├─── feat_comp-128x128.png
     ├─── feat_comp-160x160.png
     ├─── generator-96x96.png
     ├─── generator-128x128.png
     ├─── generator-160x160.png
     ├─── environment.yml
     ├─── Training.ipynb    
     └─── images 
           └─── img_align_celeba
               ├─── 000001.jpg
               ├─── 000002.jpg
               ├─── 000003.jpg
               ├─── 000004.jpg
               ├─── 000005.jpg
               ├─── ..
               ├─── ..
               ├─── 202597.jpg
               ├─── 202598.jpg
               └─── 202599.jpg
</pre>

## References
- https://course.fast.ai/
- https://arxiv.org/abs/1603.08155
- https://github.com/qubvel/segmentation_models
