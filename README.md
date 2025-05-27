# Traveler Co-Pilot

An AI-powered Telegram bot for seamless language and image translation, enabling travelers to communicate and navigate confidently.

![image](https://github.com/user-attachments/assets/0a17f9fd-90da-4469-86cf-ab3bcfacdbee)

---

## 🌍 Use Case Overview

**Rabi**, a frequent traveler seeking authentic cultural experiences abroad. Language barriers make it difficult to:

* Engage in meaningful conversations with locals
* Read restaurant menus or road signs
* Navigate public transport or ask for directions

With **Traveler Co-Pilot**, Rabi can simply send audio or images via Telegram and receive:

* **Real-time speech-to-speech translation** between any of 55 languages
* **Visual translation** by capturing text in images and translating it instantly

This empowers travelers to explore independently and interact with confidence.

---

## 🛠️ Technology Stack

* **Telegram Bot API** – Chat interface for users
* **n8n.io** – No-code workflow orchestration
* **OpenAI Whisper** – Speech-to-text transcription
* **OpenAI GPT-4o Mini** – Language translation and text-to-speech
* **Anisotropic CLIP / Cloud OCR** – Image-to-text extraction
* **LangChain Agent** – Conditional routing and process orchestration
* **Memory Node** – Context preservation (optional)

---

## 🚀 Workflow Overview

1. **Telegram Trigger**: Listens for incoming messages (audio, images, text)
2. **Language Settings**: Specify source and target languages via a Settings node
3. **Switch Node**: Routes messages to the appropriate path (audio vs. image)

### 🔊 Audio Path

* **Whisper**: Transcribes speech to text
* **GPT-4o Mini**: Translates text and converts it back to speech
* **Telegram Reply**: Sends translated audio file and text back to the user

### 📷 Image Path

* **OCR Node**: Extracts text from the image
* **GPT-4o Mini**: Translates the extracted text into the target language
* **Telegram Reply**: Sends translated text back to the user

---

## 💡 Usage Examples

**Translate Speech**:

```bash
# Send an audio message via Telegram:
User: "Where is the bus stop?" (audio)
# Bot responds with translated audio and text
```

**Visual Translation**:

```bash
# Send an image via Telegram:
User: [Photo of a Hindi text]
# Bot responds:
Bot: "We can say that artificial intelligence, with its computers and machines, makes our work easier."
```
