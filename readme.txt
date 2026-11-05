# TEAC: Teaching EEG Assessment Corpus

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23954544.svg)](https://doi.org/10.5281/zenodo.23954544)

## 1. Dataset Overview
The Teaching EEG Assessment Corpus (TEAC) is an educational EEG dataset collected during instructional-video learning. It was designed to support the study of attention-, confusion-, and cognitive-load-related EEG variation in a continuous learning setting, including data-driven cognitive-state discovery.

The current release contains EEG from 17 university students. Each participant completed two video sessions, giving 34 participant-video recording files. The dataset also contains event annotations and repeated self-reported attention and confusion scores. The total retained EEG duration is approximately 3.851 hours.

## 2. Dataset Inventory
- **Participants:** 17 pseudonymized participants (sub01–sub17)
- **Participant-video recordings:** 34
- **EEG files:** 34 FIF files
- **Behavior-score file:** 1 TXT file
- **Data volume:** approx. 206 MB

## 3. EEG acquisition parameters
- **Recording system:** portable 16-channel dry-electrode EEG system
- **Original sampling frequency:** 500 Hz
- **Released sampling frequency:** 250 Hz
- **Recording reference:** earlobe electrode

## 4. File Structure & Download
The raw data files are hosted on Zenodo. You can download the full dataset here:
👉 **[Download from Zenodo (DOI: 10.5281/zenodo.23954544)](https://doi.org/10.5281/zenodo.23954544)**

- `TEAC.zip`: Contains all the raw `.fif` EEG data files.
- `behavior_scores.txt`: Contains the behavioral ratings and scores for each participant.

## 5. How to Load the Data
```python
import mne
# Assuming you have extracted the .fif files from TEAC.zip
raw = mne.io.read_raw_fif("sub01_session1.fif", preload=True)
print(raw.info)