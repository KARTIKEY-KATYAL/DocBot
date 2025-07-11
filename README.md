# DocBot - AI-Powered Medical Assistant 🩺

DocBot is an intelligent medical assistant that combines computer vision, speech recognition, and natural language processing to provide AI-powered medical consultations. The application can analyze medical images, process voice queries, and respond with synthesized speech, creating an interactive healthcare experience.

## 🌟 Features

- **Voice-to-Text Processing**: Record voice queries and convert them to text using Whisper
- **Medical Image Analysis**: Analyze medical images using advanced vision models
- **AI Medical Consultation**: Get AI-powered medical advice and differential diagnoses
- **Text-to-Speech**: Hear responses in natural-sounding voice using gTTS or ElevenLabs
- **Interactive Web Interface**: User-friendly Gradio-based web application
- **Multi-Platform Support**: Works on Windows, macOS, and Linux

## 🚀 Demo

The application provides a web interface where users can:
1. Upload medical images (skin conditions, X-rays, etc.)
2. Record voice queries about their symptoms
3. Receive AI-powered medical analysis and suggestions
4. Listen to the response via text-to-speech

## 🛠️ Tech Stack

### Core Technologies
- **Python 3.11**: Primary programming language
- **Gradio**: Web interface framework
- **GROQ API**: LLM inference and speech-to-text processing
- **ElevenLabs**: Premium text-to-speech synthesis
- **gTTS**: Google Text-to-Speech (fallback option)

### AI/ML Models
- **Whisper Large V3**: Speech recognition model
- **Llama 4 Scout 17B**: Vision-language model for medical analysis
- **Aria Voice (ElevenLabs)**: Natural voice synthesis

### Audio Processing
- **PyAudio**: Audio input/output
- **SpeechRecognition**: Voice recording and processing
- **Pydub**: Audio file manipulation
- **FFmpeg**: Audio codec support

### Additional Libraries
- **Pillow**: Image processing
- **Requests**: HTTP client
- **NumPy/Pandas**: Data manipulation
- **FastAPI**: Backend API framework

## 📋 Prerequisites

Before setting up DocBot, ensure you have:

1. **Python 3.11** or higher
2. **API Keys**:
   - GROQ API key (for LLM and speech processing)
   - ElevenLabs API key (for premium voice synthesis)
3. **System Dependencies**:
   - FFmpeg (for audio processing)
   - PortAudio (for microphone access)

## 🔧 Installation & Setup

### Step 1: System Dependencies

#### macOS
```bash
# Install Homebrew (if not already installed)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install FFmpeg and PortAudio
brew install ffmpeg portaudio
```

#### Linux (Ubuntu/Debian)
```bash
# Update package list
sudo apt update

# Install FFmpeg and PortAudio
sudo apt install ffmpeg portaudio19-dev
```

#### Windows
1. **Download FFmpeg**:
   - Visit [FFmpeg Downloads](https://ffmpeg.org/download.html)
   - Download the latest static build for Windows

2. **Extract and Set Up FFmpeg**:
   - Extract ZIP file to `C:\ffmpeg`
   - Add `C:\ffmpeg\bin` to system PATH:
     - Search "Environment Variables" in Start menu
     - Edit system environment variables
     - Add path to System PATH variable

3. **Install PortAudio**:
   - Download from [PortAudio Downloads](http://www.portaudio.com/download.html)
   - Follow installation instructions

### Step 2: API Keys Setup

Create a `.env` file in the project root and add your API keys:

```env
GROQ_API_KEY=your_groq_api_key_here
ELEVEN_API_KEY=your_elevenlabs_api_key_here
```

**How to get API keys:**
- **GROQ API**: Sign up at [console.groq.com](https://console.groq.com) and create an API key
- **ElevenLabs API**: Sign up at [elevenlabs.io](https://elevenlabs.io) and get your API key from the profile section

### Step 3: Python Environment Setup

Choose one of the following methods:

#### Option 1: Using Pipenv (Recommended)
```bash
# Install Pipenv
pip install pipenv

# Install dependencies
pipenv install

# Activate virtual environment
pipenv shell
```

#### Option 2: Using pip and venv
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

#### Option 3: Using Conda
```bash
# Create conda environment
conda create --name docbot python=3.11

# Activate environment
conda activate docbot

# Install dependencies
pip install -r requirements.txt
```

## 🚀 Usage

### Quick Start
1. **Clone the repository**:
   ```bash
   git clone https://github.com/KARTIKEY-KATYAL/DocBot.git
   cd DocBot
   ```

2. **Set up environment** (follow installation steps above)

3. **Run the application**:
   ```bash
   python gradio_app.py
   ```

4. **Open your browser** and go to `http://127.0.0.1:7860`

### Application Components

DocBot consists of several modular components that can be run independently:

#### 1. Brain of the Doctor (`brain_of_the_doctor.py`)
- Handles image processing and medical analysis
- Uses vision-language models to analyze medical images
- Provides differential diagnoses and treatment suggestions

```bash
python brain_of_the_doctor.py
```

#### 2. Voice of the Patient (`voice_of_the_patient.py`)
- Records and processes voice input
- Converts speech to text using Whisper
- Handles microphone input and audio processing

```bash
python voice_of_the_patient.py
```

#### 3. Voice of the Doctor (`voice_of_the_doctor.py`)
- Converts AI responses to speech
- Supports both gTTS and ElevenLabs TTS
- Handles audio playback across platforms

```bash
python voice_of_the_doctor.py
```

#### 4. Gradio Web Interface (`gradio_app.py`)
- Complete web-based application
- Integrates all components into a user-friendly interface
- Provides real-time interaction with the AI doctor

```bash
python gradio_app.py
```

## 📖 How It Works

1. **Image Upload**: User uploads a medical image (skin condition, X-ray, etc.)
2. **Voice Query**: User records their symptoms and questions
3. **AI Analysis**: The system processes both inputs using advanced AI models
4. **Medical Response**: AI provides analysis, potential diagnoses, and recommendations
5. **Voice Output**: Response is converted to speech and played back to the user

## 🔒 Disclaimer

⚠️ **Important**: This application is for educational and demonstration purposes only. It should not be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult with qualified healthcare professionals for medical concerns.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Kartikey Katyal**
- GitHub: [@KARTIKEY-KATYAL](https://github.com/KARTIKEY-KATYAL)

## 🐛 Issues

If you encounter any problems or have suggestions, please [open an issue](https://github.com/KARTIKEY-KATYAL/DocBot/issues) on GitHub.

---

*Built with ❤️ by Kartikey Katyal *

