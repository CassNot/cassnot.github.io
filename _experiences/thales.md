---
layout: experience
title: Ingénieure R&D (Stage)
company: Thales DMS France
company_url: https://www.thalesgroup.com/fr
location: Brest, France
start_date: Avril 2022
end_date: Juillet 2022
image: /assets/imgs/eeg.jpeg
order: 4
highlights:
  - "Conception et développement d'une interface cerveau-ordinateur pour valider l'utilisation des potentiels liés aux erreurs (ErrP)"
  - "Pipeline expérimental complet : configuration matérielle, traitement du signal, analyse et rapport écrit"
---

Stage de 4 mois réalisé pendant ma deuxième année d'école d'ingénieurs, sous la co-direction de **Thales DMS France**, d'**IMT Atlantique** et de l'**École Navale**.

**Mission** : Explorer les capacités de contrôle sans les mains par électroencéphalographie (EEG), via la détection de potentiels liés aux erreurs (ErrP).

*Les potentiels d'erreur sont les signatures électrophysiologiques des processus d'erreur dans le cerveau — détectables par EEG. Ils reflètent la capacité humaine à reconnaître et s'adapter à ses erreurs.*

- Rédaction d'une revue de littérature sur les interfaces cerveau-ordinateur (BCI)
- Proposition et rédaction du protocole expérimental
- Implémentation complète de l'expérience et collecte de données avec des participants

## *Speed Images* — Jeu de détection ErrP

Les joueurs voient deux formes toutes les 3 secondes et doivent indiquer si elles sont identiques (**Identique**) ou différentes (**Différent**). Des bugs d'interface aléatoires (mauvais retour visuel) sont introduits pour déclencher des potentiels d'erreur endogènes et exogènes.

![Interface du jeu Match / Clash](/assets/imgs/Match_Clash.png){: style="max-width: 480px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

- A score bar motivates the player; the system displays *"BRAVO"* or *"DOMMAGE"* after each round.
- **Tools**: Python (PyGame, NumPy, PyAudio), OpenBCI Ganglion + sound board for EEG capture

![Game feedback display](/assets/imgs/Squares.png){: style="max-width: 480px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

## Results

We observe a **drop in amplitude on the Fz and Cz electrodes** when the player clicks incorrectly:

![EEG signal — player errors](/assets/imgs/EEG_errors.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

We observe a **large amplitude variation on Fz and Cz** when the interface provides wrong feedback:

![EEG signal — interface feedback errors](/assets/imgs/EEG_feedback.png){: style="max-width: 560px; display: block; margin: 1.5rem auto; border-radius: 8px;"}

[View code on GitHub](https://github.com/CassNot/Stage-EEG-2022)
