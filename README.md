# **Next Word Prediction using LSTM**

Next Word Prediction model using an **LSTM-based neural network** trained on a text corpus. Given a sequence of words, the model predicts the most likely next words.

---

### **1. Data Preparation**
- The **text is read from `novel.txt`** and preprocessed.
- A **tokenizer** assigns each unique word a numeric index.
- **Training sequences** are created: each input `X` contains a sequence of `WORD_LENGTH` words, and the output `Y` is the next word.

### **2. Model Architecture**
The model consists of:
- **Embedding Layer**: Converts word indices into vector representations.
- **Bidirectional LSTM**: Captures contextual information from both directions.
- **Dropout Layers**: Prevents overfitting.
- **Dense Output Layer**: Uses a softmax activation to predict the next word.

### **3. Training**
- The model is trained using **sparse categorical cross-entropy loss** and the **Adam optimizer**.
- **Early stopping** prevents overfitting.
- **Learning rate scheduling** reduces the learning rate if no improvement is detected.

### **4. Prediction**
- The trained model takes a sequence of words and **predicts the most probable next words**.
- A **sampling function** `sample()` selects the top probable words.
- **Recursive generation** allows generating multiple words in sequence.

---

## **Project Files**
- **`novel.txt`**  The training text corpus.
- **`next_word_model.h5`**  The trained LSTM model.
- **`history.p`**  Training history (loss & accuracy).
- **`next_word_prediction.ipynb`**  Code for training the model and next-word predictions.

---

## **Setup & Installation**
1. **Install dependencies:**
   ```bash
   pip install tensorflow numpy matplotlib
   ```

2. **Run:**
   ```bash
   next_word_prediction.ipynb
   ```

---

### **Next Steps**
- Train on **larger datasets** for better accuracy.
- Experiment with **different LSTM depths**.

---
