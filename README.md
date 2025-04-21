Deep Learning Assignment – Sequence Modeling & Generation

Name: Udvik Konduru  
Roll No: 160122737186

Question 1: Seq2Seq Character-Level Transliteration

Objective:  
Develop a character-level sequence-to-sequence model to transliterate Hindi words written in Latin script into Devanagari script using an RNN-based encoder-decoder architecture.

Dataset:  
- Source: Dakshina Dataset (Google Research)  
- Format: TSV files – hi.translit.sampled.train.tsv, hi.translit.sampled.dev.tsv, hi.translit.sampled.test.tsv

Model Architecture:  
- Input embedding layer for character-level tokenization  
- Encoder: Configurable RNN (supports LSTM, GRU, SimpleRNN)  
- Decoder: RNN using encoder final state as initial state  
- Output layer: Dense softmax over Devanagari character set

Customizable Parameters:  
- Embedding dimension  
- Hidden state size  
- Number of layers  
- RNN cell type

Evaluation:  
- Greedy decoding for inference  
- Accuracy and loss tracked across training epochs  
- Model demonstrates correct transliteration on test samples

Question 2: GPT-2 Fine-Tuning for English Song Lyrics Generation

Objective:  
Fine-tune the GPT-2 language model on a dataset of English song lyrics to enable the generation of coherent and stylistic lyric lines.

Dataset:  
- Source: Kaggle Dataset by Paul Timothy Mooney  
- Format: Multiple .txt files per artist (e.g., eminem.txt, adele.txt)  
- Preprocessing: Merged all files into a single training file named poems.txt

Model Details:  
- Base Model: GPT-2 (via Hugging Face Transformers)  
- Tokenizer: GPT-2 tokenizer (with EOS token used as pad token)  
- Training Objective: Causal language modeling (no masked language model)

Training Configuration:  
- Epochs: 3  
- Batch size: 2  
- Block size: 64  
- Optimizer and scheduler managed by Hugging Face Trainer

Output:  
The model generates creative and stylistically appropriate lyrical lines from input prompts such as:  
- “Love is a...”  
- “She walked away...”  
- “Dreams fade into...”

File Structure:  
- question1_seq2seq_transliteration.ipynb – Seq2Seq training and evaluation  
- question2_gpt2_lyrics_generation.ipynb – GPT-2 fine-tuning and generation  
- poems.txt – Preprocessed input for GPT-2  
- README.txt – Assignment description and usage

Instructions:  
For Question 1:  
- Upload Dakshina dataset files to Colab  
- Run the notebook to train and evaluate the Seq2Seq transliteration model  

For Question 2:  
- Use KaggleHub or direct upload to access the poetry dataset  
- Merge all artist files into poems.txt  
- Fine-tune GPT-2 using the training notebook and generate lyrics based on sample prompts  

Acknowledgments:  
- Dakshina Dataset by Google Research  
- Poetry Dataset by Paul Timothy Mooney (Kaggle)  
- Hugging Face Transformers Library  
