# Null-Class-Data-Science-Internship-
to Build Your Real-Time Translation App.
# Neural Machine Translation (NMT) System

This project implements a feature-rich Neural Machine Translation (NMT) system using a pre-trained LSTM-based model. The goal is to translate sentences between languages with added functionalities—such as beam search decoding, conditional translations, smart error handling, dual-language conversion, and time-dependent audio translation.

---

## Table of Contents

- [Features](#features)
- [Technical Details](#technical-details)
- [Future Enhancements](#future-enhancements)
- [Author](#author)

---

## Features

1. **Basic Translation**
   - Load a pre-trained LSTM-based NMT model.
   - Translate sentences from one language to another with basic inference.

2. **Beam Search Decoding**
   - Implement beam search decoding to improve the quality of translation outputs.
   - Maintain multiple hypotheses and choose the most probable translation.

3. **Conditional Translation (French to Tamil)**
   - Translate only if the French input word is exactly five letters long.
   - If the word has more than or fewer than five letters, the model will skip translation.

4. **Smart Error Handling & Suggestions**
   - If an incorrect or non-existent word is entered:
     - Throw an error message: “word is not available.”
     - Provide suggestions for a correct word.
   - If the user enters two consecutive wrong words, the error notification displays:
     - A list of all incorrect words entered so far.
     - Suggestions for each incorrect entry.

5. **Dual-Language Translation**
   - Enable simultaneous translation of a single English word into both French and Hindi.
   - Feature activates only for English words that have exactly 10 letters.
   - If the input word does not meet the 10-letter condition, translation is skipped.

6. **Audio-to-Text Translation (English to Hindi)**
   - Listen for English audio input from the user and translate it to Hindi.
   - If the system does not understand the audio, it will prompt the user to repeat the audio.
   - This feature activates only after 6 PM IST.
   - Additionally, it will not translate English words that start with 'M' or 'O'; other words will be translated as normal.

7. **Vowel-Start Translation Blocker**
   - For translating English to Hindi, if an English word starts with a vowel:
     - The system will display an error message: “This word starts with Vowels. Provide some other words.”
   - This feature is designed to work specifically between 9 PM and 10 PM IST.

---

## Technical Details

- **Language:** Python  
- **Libraries/Frameworks:** TensorFlow or PyTorch (for LSTM implementation), NumPy, SpeechRecognition, datetime, Flask (optional for API/web interface)  
- **Model:** Pre-trained LSTM-based NMT model  
- **Decoding Algorithm:** Beam search for improved translation quality  
- **Input/Output Handling:**  
  - Text input via command line or web interface  
  - Audio input processing (for English to Hindi translation) with time-based constraints

---


### Prerequisites

- Python
  
### Future Enhancements
- Graphical User Interface (GUI): Develop a user-friendly GUI for easier interaction.
- Multilingual Extension: Expand the number of supported languages and add additional conditional rules.
- Real-time Feedback: Enhance the error handling module with a more robust suggestion engine using NLP techniques.
- Deployment: Containerize the application with Docker for scalable deployment.

## Author
- Loka Sree Priya Kallam



