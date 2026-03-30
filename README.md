# Harmonic Eigenspace Dataset

Dataset and experiment materials accompanying the paper:

**"Harmonic Eigenspace: A Web-based Application for Navigating and Composing Microtonal Harmony"**

Submitted to the *Journal of New Music Research* (JNMR).

---

## Overview

This repository contains the listening test data, audio stimuli, and experiment code used to evaluate the Harmonic Eigenspace, a four-dimensional psychoacoustic space for locating and navigating tetrad chord types across 12-TET, 31-TET, and 53-TET.

The listening study investigates two questions:

1. Whether listeners' perception of isolated 53-TET chords correlates with the spectral dissonance values predicted by the Eigenspace model.
2. How tolerant listeners are to microtonal chord progressions composed using modal interchange in 53-TET, and how perceptual ratings vary with the tonic chord's proximity to familiar 12-TET qualities.

---

## Participants

- **N = 31** (22 male, 5 female, 2 prefer not to say, 2 non-binary)
- Mean age: 36.0 years (SD = 10.4, range 22–58)
- Mean completion time: 17.7 minutes (SD = 23.1)

---

## Repository Structure

```
.
├── README.md
├── data/                    # Participant response data
│   └── ...                  # CSV/JSON files with anonymized responses
├── audio/                   # Audio stimuli
│   ├── chords/              # 20 isolated 53-TET chords (Part 1)
│   └── progressions/        # 10 chord progressions (Part 2)
└── experiment/              # jsPsych experiment code
    └── ...
```

---

## Experiment Design

### Part 1: Chord Dissonance Ratings

Participants rated **20 isolated 53-TET seventh chords** on a dissonance scale from 1 (very consonant) to 10 (very dissonant). Chords were drawn from six perceptual categories:

| Category        | Description                                      |
|-----------------|--------------------------------------------------|
| Consonant       | Chords near local minima of the Eigenspace       |
| Intermediate    | Chords with moderate Eigenspace dissonance        |
| Neutral         | Chords with neutral intervals (no 12-TET equivalent) |
| Dominant        | Chords resembling dominant-type qualities         |
| Less Consonant  | Chords farther from local minima                  |
| Diminished      | Chords with diminished fifth and high dissonance  |

A consonant reference chord (maj6) and a dissonant reference chord (M+sm7) were presented during calibration to anchor the rating scale.

### Part 2: Chord Progression Ratings

Participants rated **10 chord progressions** composed in 53-TET using the Modal Studio interface. Each progression was rated on four dimensions:

- **Coherence** (1–10)
- **Musicality** (1–10)
- **Dissonance** (1–10)
- **Novelty** (1–10)

Progressions were grouped by tonic chord type: Major (vMvM7), Neutral (NN7), Minor (ˆmˆm7), and Dominant (vMvm7).

### General Protocol

- Stimuli presented in randomized order
- White noise palate cleansers between trials
- Participants required to listen to complete audio before responding
- Preliminary harmonic identification task as screening
- Exit survey for comments and difficulty reports

---

## Audio Stimuli

All audio was synthesized using the Web Audio API with basic waveforms (sine, triangle, sawtooth, square). Chords are rendered at A3 (220 Hz) as the default root. Audio files are provided in WAV format.

---

## Data Format

Response data is anonymized (participant IDs only, no personal identifiers). Each record includes:

- Participant ID
- Trial type (chord / progression)
- Stimulus identifier
- Rating(s) on the relevant scale(s)
- Completion timestamp

---

## Ethics

All participants provided informed consent. The study collected only age, gender, and microtonal experience as demographic variables. No personally identifiable information is included in this dataset.

---

## Web Application

The interactive Harmonic Eigenspace application is available at:

🔗 [https://dazzid.github.io/ANIMA_Harmonic_Eigenspace/](https://dazzid.github.io/ANIMA_Harmonic_Eigenspace/)

---

## License

This dataset is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt the material with appropriate attribution.

---

## Citation

If you use this dataset, please cite the accompanying paper (full reference available upon publication).
