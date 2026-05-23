# Image Caption Generator

This project trains a CNN + LSTM image caption generator and serves it with Streamlit.

## Project structure

```text
image_caption_generator/
  Images/
  captions.txt
  image_captioner.ipynb
  app.py
  requirements.txt
  artifacts/
  resource/
```

## Setup

```bash
py -3.12 -m venv .venv
source .venv/Scripts/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m pip install ipykernel
python -m ipykernel install --user --name image-caption-env --display-name "Python (.venv image caption)"
```

## Training

Open `image_captioner.ipynb`, select the `.venv` kernel, and run the notebook from top to bottom.

Training creates these files in `artifacts/`:

```text
caption_model.keras
caption_tokenizer.pkl
caption_config.pkl
mobilenetv2_features.pkl
```

## Running the project

You can use the deployed app here:

https://joannas-imagecaptiongenerator.streamlit.app/#image-caption-generator

To run the app locally after training, use:

```bash
streamlit run app.py
```
