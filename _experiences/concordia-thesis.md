---
layout: experience
title: M.Sc. Thesis Researcher
company: Concordia University — Atlas Analytics Lab
company_url: https://atlasanalyticslab.ai
location: Montréal, QC
start_date: May 2023
end_date: August 2024
image: /assets/imgs/colon.png
order: 2
highlights:
  - "Proposed a new self-supervised method for colorectal polyp screening — thesis validated with <strong>outstanding</strong> mention"
  - "Dataset of 1,037 Whole Slide Images from Kingston General Hospital, partially annotated by a pathologist"
  - "Funded by the <em>Fonds de Recherche du Québec en Nature &amp; Technologies</em>"
---

Research conducted at the [Atlas Analytics Lab](https://atlasanalyticslab.ai) under the supervision of [Dr. Mahdi S. Hosseini](https://scholar.google.com/citations?user=SO-FFrgAAAAJ), as part of my M.Sc. in Computer Science at Concordia University.

> 🚀 Thesis entitled *"Enhanced Colorectal Polyps Screening with Optimized Barlow Twins"* — validated on July 24th, 2024 with **outstanding** mention from the thesis committee.

> 🚀 Funded by the **Fonds de Recherche du Québec en Nature & Technologies**.

## The Data

Pathological images are gigapixel images (up to 100,000 × 50,000 px) of tissue slides. I worked with a dataset of **1,037 Whole Slide Images (WSIs)** of colorectal polyps (4 subtypes) and normal colon, partially annotated by a pathologist.

![Whole Slide Images overview](/assets/imgs/WSIs.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

## Why It Matters

- Colorectal cancer is the 2nd leading cause of cancer death among women, 4th among men — yet **100% preventable** if detected early.
- Pathological datasets are massive (>1 TB) and expensive to annotate.
- A growing shortage of pathologists creates bottlenecks and delays in care.

> It is therefore crucial to develop efficient, annotation-free algorithms that can assist pathologists.

## Proposed Method

- Efficient and lightweight pipeline for dataset preparation (patch extraction, background and artefact removal).
- Optimization of [Barlow Twins](https://arxiv.org/abs/2103.03230), a self-supervised learning method originally designed for natural images:
  - Adaptation of the augmentation strategy to pathological data.
  - Ablation study of key hyperparameters.
- Classification accuracy **>89%** with AUC **>0.99** — clinically meaningful results.

## Visualizations

Using [CLAM](https://github.com/mahmoodlab/CLAM), high-value diagnostic regions (in red) are highlighted — aligned with the pathologist's annotations:

![CLAM visualization of high diagnosis-value regions](/assets/imgs/CLAM_WSIs.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

Using [GradCAM](https://github.com/jacobgil/pytorch-grad-cam), per-patch attention maps confirm the model focuses on biologically relevant areas, validated by the pathologists:

![GradCAM visualization on patches](/assets/imgs/GradCAM_patches.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

## Publication

Ongoing submission to *Medical Image Analysis*:

![Medical Image Analysis paper preview](/assets/imgs/MEDIA_paper.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

[View code on GitHub](https://github.com/AtlasAnalyticsLab/PathBT)
