# Smart Waste Classifier — Streamlit App

A simple web UI around the CNN trained in `Waste_Classification_CNN_from_Scratch.ipynb`.

## Setup

1. Run the training notebook first (or supply your own model) so that one of these
   files exists in this same folder:
   - `waste_classifier_cnn_scratch.h5` (preferred), or
   - `waste_classifier.tflite`

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the app:
   ```bash
   streamlit run app.py
   ```

4. Open the URL Streamlit prints (usually `http://localhost:8501`).

## Features

- Upload an image or capture one with your webcam
- Shows the predicted waste category with confidence
- Displays a probability breakdown across all classes
- Basic disposal guidance per category (edit `DISPOSAL_TIPS` in `app.py` for your
  local recycling rules)
- Warns when prediction confidence is low, suggesting a retake

## Customizing classes

If you retrained the model on different categories (e.g. a binary
biodegradable/non-biodegradable setup), update `CLASS_NAMES`, `DISPOSAL_TIPS`,
and `CLASS_COLORS` in `app.py` to match.
