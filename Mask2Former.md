# Mask2Former

Masked attention Mask Transformer (Mask2Former)

## Aims & Contribution

![image](https://github.com/user-attachments/assets/31c4ebb0-828a-4533-8791-316b34f975ce)
Mask2Former is an architecture that can be used in any image segmentation task. 
- Semantic Segmentation   -   [Assigning each pixel of an image to one of multiple classes]
- Instance Segmentation   -  [Segmenting each object instance in an image, and assigning each pixel of an instance to its instance class ID]
- Panoptic Segmentation   -  [Combining Semantic segmentation and Instance segmentation - Assigning each pixel of an image to either a class or an instance ID]

Mask2Former is easier to train and more efficient than other universal image segmentation architectures.

## Architecture
![image](https://github.com/user-attachments/assets/9d55509c-42fc-4e2e-bf76-5b7b652b9558)

Mask2Former consists of a backbone feature extractor, a pixel decoder, and a Transformer decoder.

### backbone 
Extracts image features by encoding the original image into low-resolution feature representations.

### pixel decoder
Upsamples low-resolution features to produce high-resolution pixel-level representations. 

### Transformer decoder
Transformer decoder combines queries and image features through a cross-attention mechanism and decodes these combined features to produce task-specific outputs, such as object classes and masks. 
Mask2Former's Transformer decoder includes a masked attention 

__Masked Attention__
- Extracts localized features using Cross-Attention for each query, but restricts its operation to the predicted mask regions.
- Masked Attention applies cross-attention only on the label mask region, and ensures that the model's attention is concentrated on the most relevant parts of the input.
- Improving both efficiency and accuracy.  

![image](https://github.com/user-attachments/assets/72f835e6-77af-4f25-84af-869eeb86970c)

Attention mask $M_{l-1}(x,y)$ takes 0 if ... otherwise $\infinite$   





