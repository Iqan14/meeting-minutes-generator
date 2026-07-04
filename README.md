# Meeting Minutes Generator

An AI-powered tool that transcribes meeting audio and generates structured meeting minutes using both open-source and closed-source models, with a clean Gradio UI.

## What It Does

- Transcribes audio using both **OpenAI Whisper** (open-source via HuggingFace) and **gpt-4o-mini-transcribe** (closed-source)
- Generates structured meeting minutes using **Llama-3.2-3B-Instruct** with 4-bit quantization
- Outputs summary, discussion points, takeaways, and action items in markdown format
- Clean Gradio UI for uploading audio and viewing generated minutes in real time

## Tech Stack

- Python, Google Colab
- OpenAI API (gpt-4o-mini-transcribe, gpt-4.1-mini)
- HuggingFace Transformers (Whisper, Llama-3.2-3B-Instruct)
- BitsAndBytes (4-bit quantization)
- PyTorch
- Gradio

## Setup

1. Clone the repository:
```
git clone https://github.com/Iqan14/meeting-minutes-generator
cd meeting-minutes-generator
```

2. Open `meeting_minutes.ipynb` in Google Colab

3. Set up your secrets in Colab:
   - Add `OPENAI_API_KEY` in Colab secrets
   - Add `HF_TOKEN` in Colab secrets

4. Set runtime to **T4 GPU**:
   - Runtime → Change runtime type → T4 GPU

5. Run all cells from top to bottom

## How It Works

1. Upload a meeting audio file through the Gradio UI
2. Audio is transcribed using OpenAI's transcription model
3. Llama-3.2-3B-Instruct with 4-bit quantization generates structured meeting minutes
4. Output streams in real time including summary, discussion points, takeaways, and action items

## Note

This project requires a GPU runtime to run the open-source Llama model. Google Colab free tier with T4 GPU works perfectly.