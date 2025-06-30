# Seeing with Consensus: Explainability in Vision Transformers through Hybrid Visualization Techniques

This repository presents modular and extensible methods for visualizing and evaluating explainability techniques in Vision Transformers (ViTs). We explore how combining multiple attribution techniques—such as Layer-wise Relevance Propagation (LRP), Class Activation Mapping (CAM), Saliency Maps, and Attention Rollout—can lead to more robust and informative explanations.

We propose and test two fusion strategies (geometric mean and multiplication) across three diverse datasets: **PH2** (medical imaging), **PascalVOC**, and a subset of **ImageNet**. Our experiments demonstrate that hybrid methods often outperform individual techniques, enhancing the clarity, stability, and reliability of the model's visual explanations.

## Examples

Heatmaps on PH2 dataset
<p align="center">
  <img width="400" height="400" src="https://github.com/anacopo/ViT-XAI/blob/main/images/medical_heatmaps.jpg">
</p>

Segmentation masks on some random PascalVOC images
<p align="center">
  <img width="400" height="400" src="https://github.com/anacopo/ViT-XAI/blob/main/images/main_figure.png">
</p>

## Usage Instructions

This repository contains separate notebooks for each dataset: **PH2**, **PascalVOC**, and an **ImageNet subset**.

- The **PH2** and **PascalVOC** datasets can be downloaded directly using examples provided within their respective notebooks.
- The **ImageNet subset** used in our experiments is *not publicly available* in this repository. If you wish to access it, please contact us directly.

Each notebook is structured into **three sections**, covering:
- **1-way explainability** (single method)
- **2-way combinations**
- **3-way combinations**

### Individual Attribution Methods

To generate simple attribution maps, use:
- `generate_LRP`
- `generate_saliency`
- `generate_rollout`
- `generate_CAM`

To **overlay the attribution map** on the input image, use:
- `combine_and_visualize_attributions_1way`

To **run all 1-way examples**, use:
- `visualize_methods_1way`

### Combined Attribution Methods

To compute and visualize a 2-way or 3-way combination:
- Use `combine_and_visualize_attributions_2way` or `combine_and_visualize_attributions_3way` to get the combined attribution map and the visual overlay for 2/3 specified individual methods.

To generate all combinations using both fusion strategies:
- Use `visualize_all_combinations_2way` `visualize_all_combinations_3way` for an automated walkthrough.
