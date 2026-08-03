# 🎬 YouTube Video Summarizer

An automated command-line utility that extracts transcripts from YouTube videos and leverages the Google Gemini AI framework to generate concise summaries and key takeaways.

## 🚀 Features

* **Instant Transcript Extraction**: Downloads text subtitles automatically without playing the video file.
* **Regular Expression URL Parsing**: Seamlessly extracts 11-character video IDs from standard, shortened, or mobile YouTube links.
* **Next-Gen Gemini Integration**: Utilizes the modern `google-genai` SDK and the efficient `gemini-2.5-flash` model.
* **Robust Error Handling**: Gracefully intercepts private videos, missing subtitles, and formatting anomalies.

## 🛠️ Tech Stack

* **Language**: Python 3.10+
* **AI Engine**: Google Gemini API (`gemini-2.5-flash`)
* **Libraries**: `google-genai`, `youtube-transcript-api`

## 📦 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd youtube-video-summarizer
   ```

2. **Install the required dependencies:**
   ```bash
   pip install youtube-transcript-api google-genai
   ```

3. **Configure your API Key:**
   Get an API key from Google AI Studio and expose it to your environment variables:
   * **Linux/macOS:**
     ```bash
     export GEMINI_API_KEY="your_api_key_here"
     ```
   * **Windows (Command Prompt):**
     ```cmd
     set GEMINI_API_KEY=your_api_key_here
     ```
   * **Windows (PowerShell):**
     ```powershell
     $env:GEMINI_API_KEY="your_api_key_here"
     ```

## 💻 Usage

1. Open the script and modify the target `youtube_url` variable inside the `__main__` block:
   ```python
   youtube_url = "https://youtube.com"
   ```
2. Execute the program:
   ```bash
   python summarizer.py
   ```

## ⚠️ Limitations
* Cannot process videos that have auto-generated captions disabled or completely turned off by the creator.
* Cannot process private or age-restricted videos.
