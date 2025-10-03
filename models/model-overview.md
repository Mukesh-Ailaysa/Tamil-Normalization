# Model Overview: Tamil-Normalization

## Purpose
This document describes the models used in the Tamil-Normalization project to convert vernacular Tamil into standard Tamil.

---

## Model Architecture
- **Base Model**: LLaMA (or other LLM)
- **Fine-tuning**: The model is fine-tuned on manually sourced and synthetically generated vernacular → standard Tamil sentence pairs.
- **Embedding & Tokenization**: Uses UTF-8 Tamil tokenization for accurate handling of characters, diacritics, and punctuation.

---

## Training Details
- **Data Source**:
  - Manually curated vernacular sentences from social media, forums, spoken transcripts.
  - Synthetic variations generated using text augmentation techniques.
- **Preprocessing**:
  - Normalization of fonts (Latha/Avvaiyar/Noto Tamil).
  - Removing duplicate entries and correcting typos.
- **Hyperparameters**:
  - Learning rate: 2e-5 (example)
  - Batch size: 16–32
  - Epochs: 3–5 (depending on dataset size)
- **Evaluation Metrics**:
  - BLEU, ROUGE for text similarity.
  - Human validation for correctness of normalization.

---

## Usage
- **Input**: Vernacular Tamil sentence.  
- **Output**: Standardized Tamil sentence.  
- **Example**:
Here is the data presented in a clean, Markdown-formatted table, as requested.

## Tamil Normalization Sentence Pairs

| S. No. | Vernacular Tamil (பேச்சுத் தமிழ்) | Standard Tamil (செந்தமிழ்/எழுத்துத் தமிழ்) |
| :---: | :--- | :--- |
| **1** | என்ன பண்றீங்க? | என்ன செய்கிறீர்கள்? |
| **2** | அங்க போறேன். | அங்கே போகிறேன். |
| **3** | சாப்டுட்டேன். | சாப்பிட்டுவிட்டேன். |
| **4** | வரேனுங்க. | வருகிறேன். |
| **5** | ஒங்களுக்குத் தெரியுமா? | உங்களுக்குத் தெரியுமா? |
| **6** | நேத்து சினிமா பாத்தேன். | நேற்று திரைப்படம் பார்த்தேன். |
| **7** | அது நல்லாருக்கு. | அது நன்றாக இருக்கிறது. |
| **8** | எங்க வீட்ல இல்ல. | எங்கள் வீட்டில் இல்லை. |
| **9** | இன்னைக்கு வர மாட்டான். | இன்று வர மாட்டான். |
| **10** | அவள எங்க கண்ட? | அவளை எங்கே கண்டாய்? |
| **11** | நாளைக்கு வருவாளா? | நாளைக்கு வருவாளா? |
| **12** | எத்தன மணிக்கு? | எத்தனை மணிக்கு? |
| **13** | படிச்சியா? | படித்தாயா? |
| **14** | அதுக்கப்புறம் என்னாச்சு? | அதற்கப்புறம் என்ன ஆனது? |
| **15** | பணம் வேணுமா? | பணம் வேண்டுமா? |
---

---

## Future Work
- Explore **multilingual models** for code-mixed Tamil-English normalization.
- Improve **domain-specific datasets** (social media, legal, medical texts).
- Integrate with **TTS/STT pipelines** for end-to-end voice-based normalization.

---

## References
- LLaMA: [https://github.com/facebookresearch/llama](https://github.com/facebookresearch/llama)  
- BLEU Metric: Papineni et al., 2002.  
- ROUGE Metric: Lin, 2004.
