🧠 Human vs Machine: Arabic Text Classification Using ANN

This repository presents a sophisticated Artificial Neural Network (ANN) architecture tailored for Arabic text classification, specifically to distinguish between human-written and machine-generated content.
📌 Overview

The model architecture combines pre-trained transformer models with advanced recurrent and attention-based layers. Leveraging Hugging Face's Transformers library, the system integrates multiple Arabic language models to create a robust classification pipeline capable of understanding the complex linguistic patterns of Arabic.
🔍 1. Exploratory Data Analysis (EDA)

Before model training, a comprehensive EDA is conducted to better understand the dataset:

    a) Statistical Descriptions: Basic metrics (mean, median, max, min) computed for features like article length.

    b) Visualizations: Histograms, KDE plots, and boxplots show distribution patterns and class-based differences.

    c) Inferential Statistics: A two-sample t-test checks for significant differences in article lengths between real and generated text.

    d) Correlation Analysis: A heatmap reveals inter-feature relationships, aiding ANN input design.

🧠 2. ANN Model Architecture

The architecture is composed of several layers, each enhancing text understanding and classification:
🏗️ Architecture Flow

    Input Layer: Raw Arabic text is tokenized.

    Backbone Transformer Model: Converts tokens into contextual embeddings.

    BiLSTM Layer: Captures sequential dependencies bidirectionally.

    Retention Layer: Enhances and refines the LSTM outputs.

    Attention Mechanism: Focuses on key parts of the sequence.

    Classification Head: Produces logits for binary classification (Human vs Machine).

🔬 Main Components
🔹 Pre-trained Transformers (Backbone)

Five transformer models serve as the foundation:

    bert-base-arabic

    FacebookAI/xlm-roberta-base

    aubmindlab/araelectra-base-discriminator

    aubmindlab/bert-base-arabertv02

    aubmindlab/bert-large-arabertv2

These models generate contextual embeddings for Arabic text. Initially, their parameters may be frozen to prevent overfitting, with fine-tuning applied later.
🔹 Bidirectional LSTM (BiLSTM)

    Processes the sequence both forward and backward.

    Captures complex syntactic dependencies and morphology unique to Arabic.

    Concatenated hidden states retain both past and future context.

🔹 Custom Retention Layer

    Consists of linear layers, activations, and dropout.

    Designed to retain important long-term dependencies in lengthy or complex sentences.

    Helps mitigate overfitting while preserving rich semantic information.

🔹 Attention Mechanism

    Computes attention weights to emphasize semantically important tokens.

    Enhances interpretability and performance.

    Critical for Arabic, which depends heavily on contextual nuance.

🔹 Classification Head

    Multi-layer perceptron with dropout.

    Outputs binary class logits: Human or Machine.

    Generalizes well across diverse writing styles.

🚀 Applications

This architecture is highly adaptable and can be used in:

    Detecting AI-generated content

    Plagiarism detection

    Arabic text authenticity verification

    Educational content filtering
