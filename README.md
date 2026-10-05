# Watson
## Project summary
### A privacy first local AI assistant with voice interactions, screen awareness, and third party integrations (Google Calendar, Windows, browser) that runs entirely on your machine.
### Additional information
Watson is a desktop AI assistant designed for people who prioritize privacy and data security. Unlike cloud based alternatives, Watson processes all conversations locally using Ollama and open-source language models. The assistant currently features real time streaming responses, text to speech output, conversation memory with context management, and a chat interface inspired by Claude and ChatGPT.
## Demo Video
https://youtu.be/JlHLWexAW-M
## Installation
## Requirements

- Windows 10 or 11
- Dedicated Gpu or a device with unified memory such as new macbooks
- [Git](https://git-scm.com/downloads)
- [Python 3.10+](https://www.python.org/downloads/)
- [Visual Studio 2022](https://visualstudio.microsoft.com/) with the **.NET desktop development** workload
- [Ollama](https://ollama.com/download)

---

## Setup
Risk it by using the WatsonSetup.exe which is not guarenteed to work.
### 1. Clone the repo

```
git clone https://github.com/WSU-CPTS322-SP26/Watson.git
cd Watson
```

### 2. Check which model your computer can run

Go to **[canirun.ai](https://canirun.ai)**, enter the model name, and it will tell you if your hardware can handle it.

Recommended starting points:
- `qwen2.5:3b` — good for most machines (needs ~3 GB RAM)
- `gemma3:4b` — slightly larger, good quality (needs ~4 GB RAM)
- `qwen2.5:7b` — best quality, needs 8 GB+ RAM

### 3. Install Ollama and pull your model

Download and install Ollama from [ollama.com/download](https://ollama.com/download), then open a terminal and run:

```
ollama pull qwen2.5:3b
```

Replace `qwen2.5:3b` with whichever model you chose in step 2.

### 4. Set up the Python backend

Open a terminal in the repo folder and run:

```
cd Repo\WatsonV1\Backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

The `pip install` step will take a few minutes — it downloads Whisper and its dependencies.

### 5. Run the app

Open `Repo\WatsonV1.slnx` in Visual Studio and press **F5** (or the green play button).

The app will start the Python backend automatically and open the chat window.

---

## Usage

- Type a message and press **Enter** to send (Shift + Enter adds a new line)
- Click the microphone button to use voice input — speak, and your words will appear in the input box then send automatically
- Click the settings gear to change the AI model, TTS voice, or microphone
- Past conversations are saved in the sidebar on the left

---

## Known Issues

- Some issues with the detection of user microphones and the Mic test feature
- Response speed depends heavily on your hardware; a dedicated GPU helps significantly
- First launch after setup may be slow while models load
- The WatsonSetup.exe is not currently always working and takes a very long time to load as ollama is quite slow to download and the UI for the installer is a litte small and was not fixed in time for sprint 3
- 3rd party connectors are currently not supported as originally planned
## Additional Documentation
TODO: Provide links to additional documentation that may exist in the repo, e.g.,
* Sprint report 2: [https://emailwsu-my.sharepoint.com/:w:/g/personal/faisal_kherwish_wsu_edu/IQC8SV0fXU6SQrYz8wWBbVf7Acc0T-9O86popif1zs4-sEM?e=iGfrrc](https://emailwsu-my.sharepoint.com/:w:/r/personal/faisal_kherwish_wsu_edu/Documents/SprintReport2.docx?d=w0b21a1f1beec4ef69088db9912eb3e5c&csf=1&web=1&e=W8hEBs)
* Demonstration: [https://www.youtube.com/watch?v=-I9cj47Ug2o](https://youtu.be/p0cxyIK-e4Q)
## License
MIT License

