# Mask2Former

Masked attention Mask Transformer (Mask2Former)

## Aims & Contribution

Mask2Former is an architecture that can be used in any image segmentation task. 
- Semantic Segmentation   -   [Assigning each pixel of an image to one of multiple classes]
- Instance Segmentation   -  [Segmenting each object instance in an image, and assigning each pixel of an instance to its instance class ID]
- Panoptic Segmentation   -  [Combining Semantic segmentation and Instance segmentation - Assigning each pixel of an image to either a class or an instance ID]

Mask2Former is easier to train and more efficient than other universal image segmentation architectures.

## Architecture

** Key Components **

Masked Attention - Extracts localized features using Cross-Attention, but restricts its operation to the predicted mask regions

Mask2Former consists of a backbone feature extractor, a pixel decoder, and a Transformer decoder.
