# Arabic LLM Authorship Classifier 🇪🇬✍️🤖

Advanced ANN for classifying Arabic text as human-written or machine-generated using LLMs like AraBERTv2, XLM-RoBERTa, AraElectra.

## 🔧 Architecture:
- Pretrained LLMs from Hugging Face
- BiLSTM Layer for sequential context
- Custom Retention + Attention layers
- Classification head for binary output

## 📊 Features:
- EDA with KDE, boxplots, t-tests
- Arabic preprocessing (diacritic/emoji removal, normalization)
- Supports: `bert-base-arabic`, `xlm-roberta-base`, `araelectra`, etc.

## 🧪 Usage:
```bash
python src/train.py --model_name="xlm-roberta-base"
