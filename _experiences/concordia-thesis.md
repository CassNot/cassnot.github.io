---
layout: experience
title: Etudiante assistante de recherche M.Sc. (Thèse)
company: Université Concordia — Atlas Analytics Lab
company_url: https://atlasanalyticslab.ai
location: Montréal, QC
start_date: Mai 2023
end_date: Août 2024
image: /assets/imgs/colon.png
order: 2
highlights:
  - "Proposition d'une nouvelle méthode auto-supervisée pour le dépistage des polypes colorectaux — thèse validée avec la mention <strong>«outstanding»</strong>"
  - "Jeu de données de 1 037 images entières de lames (WSI) du Kingston General Hospital, partiellement annotées par un pathologiste"
  - "Financement du <em>Fonds de Recherche du Québec en Nature &amp; Technologies</em>"
---

Recherche menée à l'[Atlas Analytics Lab](https://atlasanalyticslab.ai) sous la direction du [Dr Mahdi S. Hosseini](https://scholar.google.com/citations?user=SO-FFrgAAAAJ), dans le cadre de ma maîtrise M.Sc. en informatique à l'Université Concordia.

> 🚀 Thèse intitulée *«Enhanced Colorectal Polyps Screening with Optimized Barlow Twins»* — validée le 24 juillet 2024 avec la mention **«outstanding»** du jury.

> 🚀 Financée par le **Fonds de Recherche du Québec en Nature & Technologies**.

## Les données

Les images pathologiques sont des images gigapixel (jusqu'à 100 000 × 50 000 px) de lames de tissu. J'ai travaillé avec un jeu de données de **1 037 images entières de lames (WSI)** de polypes colorectaux (4 sous-types) et de côlon normal, partiellement annotées par un pathologiste.

![Aperçu des images entières de lames](/assets/imgs/WSIs.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

## Enjeux

- Le cancer colorectal est la 2e cause de mortalité par cancer chez les femmes, la 4e chez les hommes — pourtant **100 % évitable** si détecté tôt.
- Les jeux de données pathologiques sont massifs (>1 To) et coûteux à annoter.
- La pénurie croissante de pathologistes crée des goulots d'étranglement et des retards de prise en charge.

> Il est donc crucial de développer des algorithmes efficaces, libres d'annotation, capables d'assister les pathologistes.

## Méthode proposée

- Pipeline efficace et léger pour la préparation des données (extraction de patches, suppression du fond et des artefacts).
- Optimisation de [Barlow Twins](https://arxiv.org/abs/2103.03230), une méthode d'apprentissage auto-supervisé initialement conçue pour des images naturelles :
  - Adaptation de la stratégie d'augmentation aux données pathologiques.
  - Étude d'ablation des hyperparamètres clés.
- Précision de classification **>89 %** avec AUC **>0,99** — résultats cliniquement significatifs.

## Visualisations

À l'aide de [CLAM](https://github.com/mahmoodlab/CLAM), les régions à haute valeur diagnostique (en rouge) sont mises en évidence — en accord avec les annotations du pathologiste :

![Visualisation CLAM des régions à haute valeur diagnostique](/assets/imgs/CLAM_WSIs.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

Using [GradCAM](https://github.com/jacobgil/pytorch-grad-cam), per-patch attention maps confirm the model focuses on biologically relevant areas, validated by the pathologists:

![GradCAM visualization on patches](/assets/imgs/GradCAM_patches.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

## Publication

Ongoing submission to *Medical Image Analysis*:

![Medical Image Analysis paper preview](/assets/imgs/MEDIA_paper.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

[View code on GitHub](https://github.com/AtlasAnalyticsLab/PathBT)
