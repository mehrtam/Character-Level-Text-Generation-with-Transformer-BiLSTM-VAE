Character-Level Text Generation using Transformer + BiLSTM + VAE
This project implements a hybrid deep learning model that combines Transformer Self-Attention, Bidirectional LSTM, and a Variational Autoencoder (VAE) for character-level next-character prediction using Wikipedia data. The model is trained on a noisy, augmented version of English Wikipedia text from topics like Artificial Intelligence and Neural Networks.

🧩 Features
Character-level tokenization using Keras Tokenizer

Embedding layer followed by Transformer-style self-attention

BiLSTM for sequential context modeling

Predicts the next character given a short character sequence

Variational Autoencoder (VAE) to extract latent representations of BiLSTM outputs

Latent feature classifier trained on VAE embeddings

Model and tokenizer saving/loading using Google Drive

Real-time character prediction via interactive input loop

🧠 Model Architecture
Embedding Layer

Transformer Self-Attention Block

Bidirectional LSTM

Dense Output Layer (softmax over vocabulary)

(Optional) VAE block for latent regularization and compressed feature representation

Latent Feature Classifier trained on VAE output

📚 Data Source
Text is fetched automatically from Wikipedia using the wikipedia-api Python library.

Topics used:

Artificial Intelligence

Neural Networks

Machine Learning

Text is cleaned (lowercased, non-letter characters removed) and augmented by randomly deleting characters.

🔧 Key Components
Transformer Self-Attention Block: Enables better context modeling by dynamically attending to previous characters

BiLSTM Layer: Captures forward and backward dependencies

VAE: Compresses BiLSTM output into a latent vector using a variational bottleneck

Latent Classifier: Learns to predict the next character directly from VAE-encoded features

🎮 Interactive Features
Type a character sequence and get the predicted next character in real-time

Option to generate multiple characters sequentially

Visual feedback through printed output in a loop

💾 Saving and Loading
The trained model is saved in .keras format

The tokenizer is saved using pickle

Both are stored and retrieved from Google Drive for persistence and reuse

📦 Requirements
Install all required dependencies using:

bash
Copy
Edit
pip install wikipedia-api gensim transformers tensorflow keras numpy matplotlib seaborn
📤 Output Files
bilstm_transformer_model.keras: Saved Keras model

tokenizer.pkl: Saved tokenizer object

Latent features: Extracted using the VAE

Real-time predictions: Printed in terminal or notebook output

👨‍🎓 Author
Developed as part of an advanced NLP and sequence modeling study project at the University of Birmingham.

