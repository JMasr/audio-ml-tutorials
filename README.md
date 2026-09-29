# AI tutorials

Runnable notebooks on AI by [José Manuel Ramírez Sánchez](https://jmramirez.engineer).

Every notebook runs on a laptop CPU in minutes, uses only public or synthetic audio (no personal or clinical data), and is written so the same mechanism can be reused on a real project by swapping only the data-loading section.

| Notebook | What it teaches | English | Español |
|---|---|---|---|
| MFCC and PLP from scratch | The classic acoustic features rebuilt in NumPy (MFCC, PLP, RASTA-PLP), checked against librosa and spafe, a small noise experiment, and the bridge to Whisper's log-Mel input | [en](en/mfcc-plp-from-scratch.ipynb) · [Colab](https://colab.research.google.com/github/JMasr/ai-tutorials/blob/main/en/mfcc-plp-from-scratch.ipynb) | [es](es/mfcc-plp-from-scratch.ipynb) · [Colab](https://colab.research.google.com/github/JMasr/ai-tutorials/blob/main/es/mfcc-plp-from-scratch.ipynb) |
| Fine-tuning Whisper with Optuna, cross-validation and MLflow | Fine-tuning on real speech (LibriSpeech subset): chapter-grouped CV, Optuna pruning, nested MLflow runs, a locked test set and a zero-shot baseline | [en](en/whisper-optuna-mlflow.ipynb) · [Colab](https://colab.research.google.com/github/JMasr/ai-tutorials/blob/main/en/whisper-optuna-mlflow.ipynb) | [es](es/whisper-optuna-mlflow.ipynb) · [Colab](https://colab.research.google.com/github/JMasr/ai-tutorials/blob/main/es/whisper-optuna-mlflow.ipynb) |
| PEFT and LoRA on Whisper | Where to place LoRA adapters for a downstream classifier vs. an embedding extractor; adapter checkpoints (synthetic audio) | [en](en/whisper-peft-lora.ipynb) · [Colab](https://colab.research.google.com/github/JMasr/ai-tutorials/blob/main/en/whisper-peft-lora.ipynb) | [es](es/whisper-peft-lora.ipynb) · [Colab](https://colab.research.google.com/github/JMasr/ai-tutorials/blob/main/es/whisper-peft-lora.ipynb) |

Written walkthroughs: https://jmramirez.engineer/tutorials/

## Run locally

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

On Colab, open a notebook with the badge above; the first cell lists the `%pip install` line it needs.

## Data

The MFCC/PLP and Optuna notebooks download `hf-internal-testing/librispeech_asr_dummy`, a 73-utterance subset of LibriSpeech (Panayotov et al., 2015, CC BY 4.0). The PEFT notebook generates synthetic tones in memory.

## License

Code in these notebooks is released under the MIT License. Text is © José Manuel Ramírez Sánchez, CC BY 4.0 (see `LICENSE` and `LICENSE-TEXT.md`).
