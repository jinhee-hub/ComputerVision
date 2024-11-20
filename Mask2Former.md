# Mask2Former

Masked attention Mask Transformer (Mask2Former)

## Aims & Contribution

![image](https://github.com/user-attachments/assets/31c4ebb0-828a-4533-8791-316b34f975ce)
Mask2Former is an architecture that can be used in any image segmentation task. 
- Semantic Segmentation   -   [Assigning each pixel of an image to one of multiple classes]
- Instance Segmentation   -  [Segmenting each object instance in an image, and assigning each pixel of an instance to its instance class ID]
- Panoptic Segmentation   -  [Combining Semantic segmentation and Instance segmentation - Assigning each pixel of an image to either a class or an instance ID]

Mask2Former is easier to train and more efficient than other universal image segmentation architectures.

** Key Components **

Masked Attention - Extracts localized features using Cross-Attention, but restricts its operation to the predicted mask regions

## Architecture
![image](https://github.com/user-attachments/assets/9d55509c-42fc-4e2e-bf76-5b7b652b9558)

Mask2Former consists of a backbone feature extractor, a pixel decoder, and a Transformer decoder.

