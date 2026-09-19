# CIVIC-EYE-AI
AI-powered community issue reporting platform
# 🌍 CIVIC-EYE AI

### See a Problem. Report a Solution.

CIVIC-EYE AI is an AI-powered civic issue reporting platform. Users upload an image of a community problem, and Google Gemini analyzes it to generate a structured report with the issue category, priority, observation, and recommended action.

## ✨ Features

- AI-powered image analysis
- Civic issue category detection
- Priority classification: Low, Medium, High, Critical
- Automatic report generation
- CSV report saving
- Dashboard with filtering and search
- Downloadable reports
- Gradio web interface
- Secure API-key loading through environment variables or Colab Secrets

## 🧰 Technologies

- Python
- Google Gemini API
- Google Gen AI SDK
- Gradio
- Pandas
- Pillow
- CSV storage
- Google Colab

## 📁 Project Structure

```text
CIVIC-EYE-AI/
├── app.py
├── README.md
├── requirements.txt
└── civic_reports.csv
```

The CSV file is created automatically when the application runs.

## ⚙️ Installation

```bash
pip install gradio pandas google-genai Pillow
```

Or use:

```bash
pip install -r requirements.txt
```

## 🔑 API Key Setup

The application reads the key from `GEMINI_API_KEY`.

Never place your real API key directly in the code or upload it to GitHub.

### Google Colab

Install dependencies:

```python
!pip install -q gradio pandas google-genai Pillow
```

Upload `app.py`:

```python
from google.colab import files
uploaded = files.upload()
```

Load the key from Colab Secrets. If the secret is named `GEMINI_API_KEY`:

```python
import os
from google.colab import userdata

os.environ["GEMINI_API_KEY"] = userdata.get("GEMINI_API_KEY")
```

If the existing secret is named `Civic_API_Key`:

```python
import os
from google.colab import userdata

os.environ["GEMINI_API_KEY"] = userdata.get("Civic_API_Key")
```

Run the app:

```python
!python app.py
```

### Local Computer

Set the environment variable before running:

**Windows PowerShell**
```powershell
$env:GEMINI_API_KEY="YOUR_API_KEY"
python app.py
```

**Linux/macOS**
```bash
export GEMINI_API_KEY="YOUR_API_KEY"
python app.py
```

## 🖥️ How to Use

1. Open the **AI Analysis** tab.
2. Upload a civic issue image.
3. Click **Analyze & Save Report**.
4. Review the AI-generated result.
5. Open the **Dashboard** to filter or search reports.
6. Use the **Download** tab to download the CSV file.

## 🗃️ Report Fields

| Field | Description |
|---|---|
| Date | Date and time of report creation |
| Category | Type of civic issue |
| Issue | Short issue title |
| Priority | Low, Medium, High, or Critical |
| Observation | Description of visible details |
| Action | Recommended response |
| Report | Combined report summary |

## 🎯 Use Cases

- Road damage and pothole reporting
- Garbage accumulation reporting
- Water leakage identification
- Drainage issue documentation
- Broken streetlight reporting
- Community infrastructure monitoring
- Educational and hackathon demonstrations

## 🔮 Future Improvements

- GPS location capture
- Interactive issue map
- User authentication
- Department-wise assignment
- Cloud database integration
- Email or SMS notifications
- Admin review and status tracking
- Multi-language support
- Analytics and charts

## ⚠️ Limitations

AI-generated results may be inaccurate and should be verified by a responsible person. The current version uses local CSV storage, and API availability depends on the Gemini configuration.

## 🔐 Security

- Do not upload API keys or passwords to GitHub.
- Use Colab Secrets or environment variables.
- Avoid uploading private or sensitive images.
- Add private data files to `.gitignore` when appropriate.

## 📜 License

This project is intended for educational, demonstration, and hackathon purposes. Add an open-source license if you plan to distribute it publicly.
