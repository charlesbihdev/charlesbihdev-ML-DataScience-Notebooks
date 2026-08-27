# Face Recognition System

An end-to-end face-recognition pipeline built on **FaceNet**: MTCNN for face
detection and a VGGFace2-pretrained InceptionResnetV1 for 512-dimensional
embeddings, with SQLite persistence and a FastAPI serving layer.

## Pipeline

| Step | Notebook | What it does |
|------|----------|--------------|
| 1 | `1_train_embeddings.ipynb` | Detects faces in a person's training images, generates embeddings, averages them into one reference embedding, and saves it to a SQLite DB. |
| 2 | `2_test_recognition.ipynb` | Embeds unseen test images and matches them against the stored reference via **cosine similarity**, reporting a match percentage. |
| 3 | `3_fastapi_service.ipynb` | Wraps the logic in a **FastAPI** app, served publicly from Colab through ngrok. |

## Tools
PyTorch · facenet-pytorch (MTCNN + InceptionResnetV1) · NumPy · Pillow ·
SQLite · FastAPI · uvicorn

## Notes
- Designed to run in **Google Colab**, reading images from Google Drive. Adjust
  the `image_folder` / database paths for a local run.
- Set your own ngrok auth token in the FastAPI notebook where marked
  `YOUR_NGROK_AUTH_TOKEN` (no credentials are committed to this repo).
