# SmartText-Predictor
An LSTM-Based Next Word Prediction System 

# 🧠 What is LSTM?

**Long Short-Term Memory (LSTM)** is a specialized type of Recurrent Neural Network (RNN) designed to learn and retain long-term dependencies in sequential data. Traditional RNNs often struggle to preserve information from earlier parts of a sequence due to the **vanishing gradient problem**. LSTMs overcome this challenge through memory cells and gating mechanisms that selectively store, update, and forget information.

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20251215093010988409/introduction_to_lstms.webp" width="700">
</p>

LSTMs are widely used in **Natural Language Processing (NLP)** applications such as:

* 📝 Text Generation
* 🔮 Next Word Prediction
* 🌍 Machine Translation
* 🎙️ Speech Recognition
* 😊 Sentiment Analysis
* 🤖 Conversational AI

Since language is inherently sequential, LSTMs are highly effective at understanding context and predicting future words based on previously observed text.


# 🚀 Project Overview

**SmartText Predictor** is an AI-powered **Next Word Prediction System** built using **Natural Language Processing (NLP)** and **Long Short-Term Memory (LSTM)** networks.

The objective of this project is to predict the most probable next word based on a sequence of previously entered words. The model is trained on the renowned **Sherlock Holmes Corpus** sourced from **Project Gutenberg**.

During training, the model learns:

* 📖 Language patterns
* 🧩 Sentence structures
* 🔗 Contextual relationships between words
* 📝 Grammar and syntax

Once trained, the system can generate meaningful text continuations similar to predictive typing features found in smartphones, search engines, and virtual assistants.


# ⚙️ How the Project Works

## 📂 1. Data Collection

The project uses the **Sherlock Holmes text corpus** as the training dataset.

### Dataset Features

* 📚 Thousands of sentences
* 📝 Rich English vocabulary
* 🔍 Real-world language patterns
* 📖 Story-based contextual learning


## 🧹 2. Text Preprocessing

The raw text is cleaned and converted into lowercase format to maintain consistency.

### Example

```text
Sherlock Holmes Was Here
```

⬇️

```text
sherlock holmes was here
```

The processed text is then tokenized into individual words.


## 🔢 3. Sequence Generation

The dataset is transformed into input-output training pairs.

### Example

```text
Input : the adventures of sherlock
Target: holmes
```

```text
Input : sherlock holmes was
Target: sitting
```

These sequences serve as the training data for the model.


## 🔤 4. Token Encoding

Each word is assigned a unique numerical index using TensorFlow's Tokenizer.

### Example

```text
sherlock → 15
holmes   → 28
watson   → 43
```

This conversion allows the neural network to process textual data efficiently.


## 📏 5. Padding

Input sequences may vary in length. To ensure consistent input dimensions, padding is applied.

### Example

```text
[0, 0, 0, 15, 28]
```

Padding enables the model to process all sequences uniformly during training.


## 🧩 6. Embedding Layer

The Embedding Layer converts words into dense vector representations.

Instead of treating a word as a simple numerical index:

```text
holmes = 28
```

The model learns a meaningful vector representation:

```text
holmes = [0.24, -0.18, 0.75, ...]
```

This helps capture semantic and contextual relationships between words.


## 🧠 7. LSTM Model Training

The embedded sequences are fed into an LSTM network.

The model learns:

✅ Contextual information

✅ Word relationships

✅ Sentence structures

✅ Long-term dependencies

A Dense Layer with Softmax Activation then predicts the most probable next word.


## 🔮 8. Prediction

After training, users provide a starting phrase.

### Example Input

```text
the adventures of sherlock
```

### Generated Output

```text
the adventures of sherlock holmes sat in the door and ushered in a hearty meal
```

The model predicts words sequentially to generate coherent text continuations.


# 🏗️ Model Architecture

```text
Input Sequence
       │
       ▼
🧩 Embedding Layer
       │
       ▼
🧠 LSTM Layer (150 Units)
       │
       ▼
🎯 Dense Layer (Softmax)
       │
       ▼
🔮 Predicted Next Word
```

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20250528172141936296/architecture_of_lstms.webp" width="700">
</p>

# 📈 Training Configuration

| Parameter           | Value                           |
| ------------------- | ------------------------------- |
| 🧠 Model            | LSTM                            |
| ⚙️ Optimizer        | Adam                            |
| 📉 Loss Function    | Sparse Categorical Crossentropy |
| 🔁 Epochs           | 20                              |
| 📦 Batch Size       | 128                             |
| 📊 Validation Split | 10%                             |


# 💡 Example Prediction

### Input

```text
the adventures of sherlock
```

### Output

```text
the adventures of sherlock holmes sat in the door and ushered in a hearty meal
```


# 🎯 Applications

### 📱 Smart Keyboard Suggestions

Predicts the next word while users type.

### 🔎 Search Engine Autocomplete

Provides intelligent search query suggestions.

### 🤖 Chatbots & Virtual Assistants

Enhances conversational interactions through contextual predictions.

### ✍️ Writing Assistants

Assists users in composing text more efficiently.

### 📚 Language Modeling

Serves as a foundation for advanced NLP and text-generation systems.


# 🛠️ Technologies Used

* 🐍 Python
* 🔢 NumPy
* 🧠 TensorFlow
* ⚡ Keras
* 📝 Natural Language Processing (NLP)
* 🔮 Long Short-Term Memory (LSTM)


# 🎓 Learning Outcomes

This project demonstrates key NLP and Deep Learning concepts, including:

* 📖 Text Preprocessing
* 🔤 Tokenization
* 🔢 Sequence Generation
* 🧩 Word Embeddings
* 🧠 Deep Learning with LSTMs
* 🔄 Recurrent Neural Networks (RNNs)
* 🔮 Next Word Prediction
* 🤖 Language Modeling


# 🚀 Future Enhancements

* 🔄 GRU-Based Language Models
* 🤖 Transformer-Based Architectures
* 🌐 Web Application Deployment
* 💬 Real-Time Text Prediction Interface
* 📈 Training on Larger Datasets
* 🎯 Top-K Next Word Suggestions


# 🏁 Conclusion

This project successfully implements a **Next Word Prediction System** using **Natural Language Processing (NLP)** and **Long Short-Term Memory (LSTM)** networks.

By learning contextual relationships between words from a large text corpus, the model can predict and generate meaningful text sequences. The project demonstrates how Deep Learning techniques can be applied to real-world language modeling tasks and provides a strong foundation for building intelligent writing assistants, predictive text systems, and conversational AI applications.
