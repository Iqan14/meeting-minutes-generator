# Meeting Minutes Generator

An AI-powered tool that transcribes meeting audio and generates structured meeting minutes using both open-source and closed-source models.

## What It Does

- Transcribes audio using both **OpenAI Whisper** (open-source via HuggingFace) and **gpt-4o-mini-transcribe** (closed-source)
- Generates structured meeting minutes using **Llama-3.2-3B-Instruct** with 4-bit quantization
- Outputs summary, discussion points, takeaways, and action items in markdown format

## Tech Stack

- Python, Google Colab
- OpenAI API (gpt-4o-mini-transcribe)
- HuggingFace Transformers (Whisper, Llama-3.2-3B-Instruct)
- BitsAndBytes (4-bit quantization)
- PyTorch

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

1. Audio file is transcribed using both Whisper (open-source) and OpenAI's transcription model
2. Transcriptions are compared side by side
3. Llama-3.2-3B-Instruct with 4-bit quantization generates structured meeting minutes
4. Output includes summary, discussion points, takeaways, and action items

## Note

This project requires a GPU runtime to run the open-source Llama model. Google Colab free tier with T4 GPU works perfectly.