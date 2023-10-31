# MeshAttire
Framework for Reliable Image-Based Virtual Wardrobe Try-On

- **Alignment of Clothing and Model:** The framework commences by aligning the chosen clothing product image (Ip) with the target model's pose and body shape using a two-stage warping process.
- **Two-Stage Warping:** A two-stage structure is adopted for precise warping. The first stage predicts a coarse-level transformation, while the second stage refines it with fine-level corrections.
- **Addressing Occlusion and Pose Variations:** Challenges such as occlusions in the model image and variations in shape or pose are tackled through the two-stage network.
- **Perceptual Geometric Matching Loss:** The system uses a novel perceptual geometric matching loss to ensure the quality of the alignment between the clothing and the model.
- **Conditional Segmentation Mask Prediction:** To accurately segment clothing boundaries, a conditional segmentation mask prediction network is employed.
- **Segmentation-Assisted Texture Translation:** The final step involves transferring the clothing onto the model image while maintaining accurate segmentation, ensuring a realistic virtual try-on experience.

# Usage #
Clone the repo and install requirements through ```pip install -r requirements.txt``` 

# Traning #
#### Coarse-to-Fine Warping module ####
&nbsp;&nbsp;&nbsp;&nbsp; In `config.py` set ```self.datamode='train'``` and ```self.stage='GMM'```
</br> &nbsp;&nbsp;&nbsp;&nbsp; then run ```python train.py```

####  Conditional Segmentation Mask generation module ####
&nbsp;&nbsp;&nbsp;&nbsp; In `config.py` set ```self.datamode='Train'``` and ```self.stage='SEG'```
</br> &nbsp;&nbsp;&nbsp;&nbsp; then run ```python train.py```


####  Segmentation Assisted Texture Translation module ####
&nbsp;&nbsp;&nbsp;&nbsp; In `config.py` set ```self.datamode='Train'``` and ```self.stage='TOM'```
</br> &nbsp;&nbsp;&nbsp;&nbsp; then run ```python train.py```
</br>


