
# Caption to Image generation using Semi-Supervised Generative Adversarial Networks



<p align="center">
<img src="https://github.com/sajmaru/GAN/blob/main/Readme%20Images/img%201.png">
</p>

## Usage
1. Please refer to the READMEs in the folder Dataset, Captions, and word2vec_pretrained_model to obtain the necessary data. 
2. Run ```python process_images.py``` to resize and normalize the images and generate numpy arrays or use one provided in Dataset foler
3. Run ```python process_captions.py``` to generate sentence embeddings for the captions or use one provided in Captions folder
5. Import the jupyter notebook ```Text2Image_GAN_MS.ipynb``` in Google Colab and load the data.
6. Run code snippets in Google Colab.

## Results

We trained the GAN model for 500 epochs with the ADAM optimizer [4] for the discriminator and generator with a learning rate of 0.00004 and beta_1=0.5. Most of the synthesized images do depict plausible colors and shapes of birds and there does seem to be a lot of diversity; however, the GAN did have some minor mode collapse problems when generating images based on made up captions as seen below.

<p align="center">

<img src="https://github.com/Yoan-D/exploring-text-to-image-synthesis-with-conditional-GANs/blob/master/readme_images/screenshots.png" width="650">
</p>

<p align="center">

<img src="https://github.com/Yoan-D/exploring-text-to-image-synthesis-with-conditional-GANs/blob/master/readme_images/red_birds.png" width="550">

</p>

<p align="center">

<img src="https://github.com/Yoan-D/exploring-text-to-image-synthesis-with-conditional-GANs/blob/master/readme_images/yellow_birds.png" width="550">

</p>


### References
[1] Meng Wang, Huafeng Li, Fang Li: Generative Adversarial Network based on Resnet for Conditional Image Restoration, 2017. arXiv:1707.04881. <br />
[2] Tingting Qiao, Jing Zhang, Duanqing Xu, and   DachengTao. Mirrorgan: Learning text-to-image generation by redescription, 2019. arXiv:1903.05854. <br />
[3] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. Bert: Pre-training of deep bidirectional transformers for language understanding. arXiv preprint arXiv:1810.04805, 2018. <br />
[4] Han Zhang, Tao Xu, Hongsheng Li, ShaotingZhang, Xiaogang Wang, Xiaolei Huang, and Dimitris Metaxas. Stackgan: Text to photo-realistic image synthesis with stacked generative adversarial networks, 2016. arXiv:1612.03242.
[5] https://machinelearningmastery.com/practical-guide-to-gan-failure-modes/
[6] https://machinelearningmastery.com/how-to-implement-the-frechet-inception-distance-fid-from-scratch/
