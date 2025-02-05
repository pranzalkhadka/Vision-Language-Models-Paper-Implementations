# Contrastive Language Image Pre-training

Collection of Research Paper implementation of various Vision Language models.

Overview

    CLIP: A foundational model developed by OpenAI for connecting images and text trained on large amount of image-text pairs. It can recognize various objects based on natural language prompts.

    CLIPSeg: An adaptation of CLIP for segmentation tasks enabling pixel level segmentation based on text prompts.

Approach

    CLIP: 
        Pre-trained ResNet18 as Image Encoder and DistilBert as Text Encoder

        Trained on CIFAR-10 dataset for zero shot classification task

    CLIPSeg: 
        Custom Decoder on top of pre-trained CLIP

        Trained on Refcoco dataset for Referring Image segmentation task



## Results

### CLIP: Image-Text Matching

| Sample Image            | Descriptions                                                                                                   | Best Match                    |
|-------------------------|---------------------------------------------------------------------------------------------------------------|-------------------------------|
| ![image](Images/CLIP/1.png) | "A photo of an airplane", "A photo of an automobile", "A photo of a bird", "A photo of a cat", <br> "A photo of a deer", "A photo of a dog", "A photo of a frog", "A photo of a horse", "A photo of a ship", "A photo of a truck" | "A photo of a automobile" |
| ![image](Images/CLIP/2.png) | "A photo of an airplane", "A photo of an automobile", "A photo of a bird", "A photo of a cat", <br> "A photo of a deer", "A photo of a dog", "A photo of a frog", "A photo of a horse", "A photo of a ship", "A photo of a truck" |"A photo of a frog"         |


### CLIPSeg: Image Segmentation

| Referring Text         | Sample Image            | Predicted Mask          | Ground Truth Mask      |
|------------------------|-------------------------|-------------------------|------------------------|
| "left player" | ![image](Images/CLIPSeg/Img1.png) | ![mask](Images/CLIPSeg/Pred1.png) | ![mask](Images/CLIPSeg/True1.png) |
| "Bottom case"     | ![image](Images/CLIPSeg/Img2.png) | ![mask](Images/CLIPSeg/Pred2.png) | ![mask](Images/CLIPSeg/True2.png) |


## References

- **CLIP**: [Radford et al., 2021](https://arxiv.org/pdf/2103.00020) - *Learning Transferable Visual Models From Natural Language Supervision*
- **CLIPSeg**: [Lüddecke et al., 2021](https://arxiv.org/pdf/2112.10003) - *Image Segmentation Using Text and Image Prompts*

