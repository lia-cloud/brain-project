# Brain Project: Decoding Left vs Right Hand from EEG

A beginner project that teaches a computer to read human brain activity.
It uses real EEG recordings of a volunteer imagining moving their left
or right hand, and a machine learning model that guesses which hand it was.

## What it does

1. Downloads a free public EEG dataset (PhysioNet EEG Motor Movement/Imagery)
2. Filters the signal to the brain rhythms linked to movement (8-30 Hz)
3. Cuts the recording into short left/right pieces
4. Uses CSP (Common Spatial Patterns) to find the best mix of sensors
5. Trains a Logistic Regression model and tests it with cross-validation

## Results

| Method | Accuracy |
|---|---|
| Log-variance features | 0.62 |
| CSP + Logistic Regression | 0.71 |

Random guessing would give 0.50.

## How to run

1. Open the notebook in Google Colab
2. In the first cell, run: `!pip install mne`
3. Run the second cell with the main code
4. Choose "No" if MNE asks to save a default data path

Tools: Python, MNE, scikit-learn.

## Next steps

- Add more volunteers for more training data
- Try other models
- Plot the brain signals with matplotlib
