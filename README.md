# Collaborative Consortium of Foundation Models for Open-World Few-Shot Learning
This paper has been accepted by **AAAI 2024**. We are profoundly grateful for the significant insights provided by [CaFo](https://arxiv.org/pdf/2303.02151.pdf).

## Abstract
Open-World Few-Shot Learning (OFSL) is a crucial research field dedicated to accurately identifying target samples in scenarios where data is limited and labels are unreliable. 
This research holds significant practical implications and is highly relevant to real-world applications. 
Recently, the advancements in foundation models like CLIP and DINO have showcased their robust representation capabilities even in resource-constrained settings with scarce data. 
This realization has brought about a transformative shift in focus, moving away from “building models from scratch” towards “effectively harnessing the potential of foundation models to extract pertinent prior knowledge suitable for OFSL and utilizing it sensibly”. 
Motivated by this perspective, we introduce the **C**ollaborative C**o**nsortium of F**o**undation M**o**dels (**CO3**), which leverages CLIP, DINO, GPT-3, and DALLE to collectively address the OFSL problem. CO3 comprises four key blocks: 
(1) the Label Correction Block (LC-Block) corrects unreliable labels, (2) the Data Augmentation Block (DA-Block) enhances available data, 
(3) the Feature Extraction Block (FE-Block) extracts multi-modal features, and (4) the Text-guided Fusion Adapter (TeFu-Adapter) integrates multiple features while mitigating the impact of noisy labels through semantic constraints. 
Only the adapter’s parameters are adjustable, while the others remain frozen.
Through collaboration among these foundation models, CO3 effectively unlocks their potential and unifies their capabilities to achieve state-of-the-art performance on 11 datasets.

## Get Started
1. Create a conda environment and install dependencies.
2. Download the "cache" folder and place it in the root directory.
3. Download the DINO model and place it in the "dino" directory.   
   e.g., "./dino/dino_resnet50_pretrain.pth".
4. Download the datasets.
5. Modify the **main_path** on line 22 of the [main.py](https://github.com/ZJLAB-AMMI/CO3/blob/main/main.py) to align with the specific dataset you are planning to validate.  
   e.g., change the **main_path** to "./configs/imagenet/config.yaml".
6. Update the **root_path** in the second line of the **config.yaml** file for the dataset you are validating.  
   e.g., in the "./configs/imagenet/config.yaml" file, change the **root_path** to "./DATA/".
