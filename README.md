# 📢 Government Complaint Audio Dataset (Hindi & English)

This dataset contains **bilingual audio recordings** of government-related customer complaints in **Hindi and English**, generated using Text-to-Speech (TTS). It is designed to help in research and development of **speech recognition**, **intent classification**, **sentiment analysis**, and **multilingual voice-based chatbots** for public service platforms.

---

## 📂 Dataset Structure

GCD-Government_Complaints_Dataset/
├── english/
│ ├── audio/ # English audio files categorized by complaint type
│ └── scripts/ # English text scripts for each complaint type
├── hindi/
│ ├── audio/ # Hindi audio files categorized by complaint type
│ └── scripts/ # Hindi text scripts for each complaint type
├── metadata.csv # File mapping audio to transcript, category, and language

---

## 🧾 metadata.csv Columns

| Column      | Description                                                 |
|-------------|-------------------------------------------------------------|
| filename    | Relative path to the audio file                             |
| category    | Type of complaint (e.g., `water_supply`, `electricity`)     |
| language    | `english` or `hindi`                                        |
| transcript  | The actual spoken content (text) of the complaint           |

---

## 📊 Sample Categories (Customizable)

Some of the complaint categories include:
- Water Supply
- Electricity
- Roads and Infrastructure
- Sanitation and Waste
- Public Transport
- Internet/Connectivity
- Healthcare Services
- Government Schemes
- Education Services
- Police & Security

---

## 🚀 Use Cases

- Training **speech-to-intent models** in Hindi and English
- Building **smart voice-based complaint redressal systems**
- Fine-tuning **ASR (Automatic Speech Recognition)** systems
- Practicing **NLP preprocessing** and **audio feature extraction**
- Multilingual **TTS/ASR/Intent classification** tasks

---

## 🛠 Example Usage (Python)

```python
import pandas as pd

# Load dataset metadata
df = pd.read_csv("metadata.csv")
print(df.head())

# Visualize complaint categories
import matplotlib.pyplot as plt
df['category'].value_counts().plot(kind='bar', color='orange')
plt.title("Complaint Category Distribution")
plt.ylabel("Number of Samples")
plt.xticks(rotation=45)
plt.show()

