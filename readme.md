

# **Caption to Image generation Deep Residual Generative Adversarial Networks [DR-GAN] 🧙🏻‍♂️**



<p align="center">
<img src="https://github.com/sajmaru/GAN/blob/main/Readme%20Images/img%201.png">
</p>

The proposed GAN model is built by conditioning the generated images on a text description instead of on a class label. We implemented a Deep Residual GAN network to create fine pictures from very latent noise. The coarse images are aligned to attributes and are embedded as the generator inputs and classifier labels. A straight route, similar to the Resnet, is covered in a generative network to directly transport coarse pictures to higher layers. In addition, adversarial training is used in a cyclic fashion to prevent picture degradation. Experimental results of applying the Deep Residual GAN model to datasets BIRD CUB-200 and FLICKR 8K show its higher accuracy to the state-of-art GANs.

## Usage 🧾
1. Please refer to the READMEs in the folder Dataset, Captions, and word2vec_pretrained_model to obtain the necessary data. 
2. Images pickle file can be found in Dataset folder that was created using  ```process_images.ipynb``` to resize and normalize the images and generate numpy arrays 
3. Captions pickle file can be found in Captions folder that was created using  ```process_captions.ipynb``` to generate sentence embeddings for the captions or use one provided in Captions folder
4. Trained model weights files can be found in the weights folder 
5. Import the jupyter notebook ```CSE_676_Text2Image_final.ipynb``` in Google Colab and load the data.
6. Run code snippets in Google Colab.

## Results  🚀
Below are some outputs of the DR-GAN model when the input text was given as “a yellow bird with black tail” & “a green  bird with black head”.

<p align="center">
<img src="https://github.com/sajmaru/GAN/blob/main/Readme%20Images/Bird_Results.png">
</p>

Other results can be seen below

<center>

| Epochs   |      Bird Generated Images      |  Flickr8K  Generated Images      | 
|----------|:-------------:|:-------------:|
| 0 - 200   |  [Click here to view](https://drive.google.com/file/d/1RL1MZ3zh9F5cXIuMz10XXLo9yb5rYaE4/view) | [Click here to view](https://drive.google.com/file/d/1vlcwZLVXeqUB-hhrxXpG5oRm_zXEkQ6k/view) | 
| 201 - 400 | [Click here to view](https://drive.google.com/file/d/18zZVyLVabvo2aFLhdc-DZ8Z9_luU_tHl/view) | [Click here to view](https://drive.google.com/file/d/1vlcwZLVXeqUB-hhrxXpG5oRm_zXEkQ6k/view) | 
| 401 - 600 | [Click here to view](https://drive.google.com/file/d/1sfCiQB5mYQM3wuKvVxRPPGL7OdIoJEeI/view) | [Click here to view](https://drive.google.com/file/d/1A2dpbW9pFnXPVQXQ-fG4CkWYbww2mmmI/view) | 
| 601 - 800 | [Click here to view](https://drive.google.com/file/d/1mevryadjLth2BL7R9jNx9hSrJxELgTPu/view) | [Click here to view](https://drive.google.com/file/d/1sZ5igfRxn_91bubRu8Exl6AyDu68GNlO/view) | 
| 801 - 1000 | [Click here to view](https://drive.google.com/file/d/15acAVcG8tYf6qVRpWYbPopuc5NHTDnfT/view) | [Click here to view](https://drive.google.com/file/d/1dV8-0f4Uj3UcX66wxLnmot3xRXoubcho/view) | 

</center>


## References 📚
[1] Meng Wang, Huafeng Li, Fang Li: Generative Adversarial Network based on Resnet for Conditional Image Restoration, 2017. arXiv:1707.04881. <br />
[2] Tingting Qiao, Jing Zhang, Duanqing Xu, and   DachengTao. Mirrorgan: Learning text-to-image generation by redescription, 2019. arXiv:1903.05854. <br />
[3] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. Bert: Pre-training of deep bidirectional transformers for language understanding. arXiv preprint arXiv:1810.04805, 2018. <br />
[4] Han Zhang, Tao Xu, Hongsheng Li, ShaotingZhang, Xiaogang Wang, Xiaolei Huang, and Dimitris Metaxas. Stackgan: Text to photo-realistic image synthesis with stacked generative adversarial networks, 2016. arXiv:1612.03242.
