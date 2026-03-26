# Edge-AI-Offline-Assistant
A privacy-focused offline AI assistant using a quantized small language model running locally with llama.cpp, enhanced with safety and prompt control layers.


## Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/Aarya695/Edge-AI-Offline-Assistant.git
cd Edge-AI-Offline-Assistant
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Install llama.cpp
```bash
git clone https://github.com/ggerganov/llama.cpp
cd llama.cpp
cmake -B build
cmake --build build --config Release
```

### 4. Download Model
Download GGUF model manually:
https://huggingface.co/

(Example: Qwen 0.5B GGUF)

Place it in:
```
C:\models\
```

### 5. Run llama server
```bash
.\build\bin\Release\llama-server.exe -m C:\models\your_model.gguf
```

### 6. Run backend
```bash
uvicorn backend:app
```
