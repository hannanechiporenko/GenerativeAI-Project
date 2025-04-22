
NanoTransformer: Autoregressives Sprachmodell in PyTorch

Dieses Projekt implementiert ein eigenes, auf Transformer basierendes Sprachmodell, das anhand eines kurzen englischen Textes trainiert wurde. Die Ergebnisse der Textgenerierung werden auch mit dem vortrainierten GPT-2-Modell mit Hugging Face verglichen.

Skript 1.Tokenisiert Text mit „AutoTokenizer“ von Hugging Face.
2. Trainiert sein Transformer-Modell basierend auf NanoTransformer.
3. Visualisiert die Gewichte der Aufmerksamkeit (Selbstaufmerksamkeit).
4. Generiert Text basierend auf der ursprünglichen Eingabe:
- Ihr Modell (NanoTransformer)
- Vortrainiertes Modell „distilgpt2“
5. Protokolliert den Trainingsprozess in Weights & Biases (wandb).

`PyTorch` - Erstellen und Trainieren eines Modells
`torch.nn` – Transformer-Architektur
`AutoTokenizer` - Text-Tokenisierung
`wandb` - Verlustprotokollierung
`matplotlib + seaborn` – Visualisierung der Selbstaufmerksamkeit
`transformers.pipeline` – Schnelle Generierung mit vortrainiertem Modell

   Login Englischer Text `text = "Die Zukunft der KI..."`
Verarbeitung | Tokenisierung → Einbettung + Positionskodierung → Transformatorblöcke
Ausgabe des generierten Textes (2 Optionen):
1. NanoTransformer (Ihr Modell)
2. GPT-2 (`distilgpt2`) über `pipeline()`

Ausgabe an Terminal

----- Unsere Model (NanoTransformer) -----
The future of AI is learning the way the...

----- Pre trenert (GPT-2) -----
In the future, AI will become more powerful and...

----- Hugging Face Pipeline (GPT-2) -----
In the future, AI will be able to perform complex tasks...
```

So starten Sie

```bash
pip install torch transformers wandb matplotlib seaborn
```

```bash
python proekt1_final.py
```
[wandb.ai](https://wandb.ai) — посмотри графики `train_loss` и `val_loss`.
