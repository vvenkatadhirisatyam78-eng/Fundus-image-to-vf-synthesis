

# Fundus-image-to-vf-synthesis

A multimodal deep learning system designed to synthesize **Visual Field (VF)** data directly from **retinal fundus images** and clinical parameters, bridging the structural–functional gap in glaucoma diagnosis and monitoring.

## Project Objectives
* **Structural-to-Functional Synthesis:** Develop a deep learning pipeline to predict functional Visual Field (VF) data from accessible structural fundus imaging.
* **Multimodal Learning:** Integrate **Fundus Images**, **Visual Field (VF) data**, and **Intraocular Pressure (IOP)** measurements to improve prediction fidelity.
* **Advanced Architecture & Optimization:** Design and benchmark multiple model variations—including **Vision Transformers (ViT)** and **Diffusion Models**—enhanced with **contrastive loss**, **reliability weighting**, and **Particle Swarm Optimization (PSO)**.
* **Clinical Prototyping:** Evaluate performance using metrics such as **Mean Squared Error (MSE)** to build a reliable prototype pipeline for glaucoma progression monitoring.

---

##My Contributions
As the primary developer, I managed the entire GitHub codebase from initial setup to final deployment, handling end-to-end implementation, data engineering, and experimental validation:
• Data Engineering & Multimodal Preprocessing: Cleaned retinal imaging and clinical datasets, implementing automated pipelines to extract structured features from fundus images and align them with VF and IOP records.
• Model Architecture & Training: Built, trained, and iteratively refined Vision Transformer (ViT) and Diffusion Model pipelines tailored for fundus-to-VF synthesis.
• Loss Design & Optimization: Implemented and tested model variations incorporating contrastive loss, reliability weighting, and PSO to enhance synthesis stability and accuracy.
• Evaluation & Error Analysis: Benchmarked model outputs using MSE and visual inspection, diagnosing failure cases and implementing targeted corrections across iterations.
• Repository Management & Documentation: Maintained structured version control, clean commit histories, and comprehensive README documentation on GitHub alongside technical presentations of experimental results and clinical insights.

---

## Acknowledgments
* **Dr Raja Chandru** — *Project Mentor & Domain Advisor*: Provided academic mentorship, conceptual guidance on Vision Transformers and Diffusion Models, and clinical domain expertise in glaucoma pathology.

fundus to vf synthesis project
## Objectives

- Develop a deep learning-based system to synthesize Visual Field (VF) data from fundus images.  
- Bridge the structural–functional gap in glaucoma diagnosis by predicting VF from easily acquired fundus images.  
- Design and evaluate multiple model variations using advanced loss functions and optimization techniques (contrastive loss, reliability weighting, PSO).  
- Leverage multimodal data (Fundus images, Visual Field data, and Intraocular Pressure) to improve prediction accuracy.  
- Analyze and compare model performance using evaluation metrics such as MSE.  
- Build a prototype pipeline that can support future clinical applications for glaucoma monitoring.
---

---

# Dataset

### Retrospective Dataset for Usability Testing
- Grape dataset: 1261 Fundus and VF pairs
  - Includes:
    - (Age ,Sex, CCT, Longitudinal details)
- Available in Reference [11] in PPT

### Prospective Dataset for User-Acceptance Testing
- Real-time hospital paired data (Fundus–VF)
- Stored in this repository:
  1. Fundus Images from Hospital - Prospective Data
  2. VFs (paired to Fundus Images) from Hospital - Prospective Data

---
<img width="940" height="412" alt="image" src="https://github.com/user-attachments/assets/58c237ff-3bf3-4c28-a77a-29884a8a8e34" />

                         A preview of the prospective data collected for User Acceptance testing

                                   

---

##Descriptions

### 1. Base Model for VF Synthesis (`base_model_for_vf_synthesis.ipynb`)
Implements the baseline pipeline for synthesizing Visual Field (VF) data from fundus images using a Vision Transformer (ViT) encoder and Conditional Diffusion Probabilistic Model (CDPM). Uses conventional loss functions to establish a performance benchmark.

---

### 2. Model with Reliability Weights (`model_with_reliability_weights.ipynb`)
Enhances the base model by incorporating reliability-weighted loss. This approach assigns different importance to training samples based on their reliability, improving robustness and handling noisy or uncertain data.

---

### 3. Model with Contrastive Loss (`model_with_contrastive_loss.ipynb`)
Introduces contrastive learning to improve feature representation. The model learns better structural relationships between fundus images and VF outputs, leading to improved generalization and prediction accuracy.

---

### 4. Model with PSO Optimization (`model_with_pso_optimization.ipynb`)
Applies Particle Swarm Optimization (PSO) to automatically tune model hyperparameters such as contrast temperature and loss weights. This results in optimized performance compared to manual tuning.

---

### 5. Model with only Optimized Parameters (`model_with_only_optimized_parameters.ipynb`)
Uses manually tuned optimal parameters (derived from PSO experiments) without running the optimization process again. Serves as a comparison to evaluate the effectiveness of PSO.

---

### 6. Pretrained Model (`pretrained_model.ipynb`)
Loads a pretrained ViT + CDPM model and performs inference on test data. Includes evaluation metrics (MSE, MAE, RMSE, Pearson correlation) and generates synthesized VF outputs for analysis.

---

## Outputs

| Model | Objective | Algorithm |
|-------|----------|-----------|
| Base Model for VF Synthesis | VF synthesis from fundus image | ViT + CDPM with conventional loss |
| Model with Reliability Weights | VF synthesis from fundus image | ViT + CDPM with reliability-weighted loss |
| Model with Contrastive Loss | VF synthesis from fundus image | ViT + CDPM with contrastive loss |
| Model with PSO Optimization | VF synthesis from fundus image | ViT + CDPM with optimized parameters (PSO) |
| Model with only optimized parameters | VF synthesis from fundus image | ViT + CDPM with manually tuned parameters |
| Pretrained Model | VF synthesis from fundus image | ViT + CDPM for inference/testing only |



---

 # sample output
 https://github.com/Rajachandru/Fundus-image-to-vf-synthesis/blob/df9b27f3c771ba43acfdc046629e9773048222e8/sample_output.png

 
