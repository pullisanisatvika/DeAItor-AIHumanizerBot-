# DeAItor – AIHumanizerBot: Full Installation & Folder Guide

Welcome to **DeAItor**, the automated AI humanization loop tool. This guide walks you through setting up the entire project on your local machine—including installing dependencies, understanding folder contents, and running your first AI-to-human text transformation.

---

## Prerequisites

Before continuing, make sure you have:
- ✅ Python **3.8+**
- ✅ Git installed
- ✅ Stable internet
- ✅ Google Chrome (or Chromium-compatible browser)
- ✅ pip (Python package installer)

---

## Step-by-Step Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/DeAItor-AIHumanizerBot.git
cd DeAItor-AIHumanizerBot

### 2. (Optional) Create a Virtual Environment
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows

### 3. Install Python Dependencies
pip install -r requirements.txt
playwright install

---

## Configuration – config.json
Edit this file to customize how the automation behaves.
{
  "zerogpt_threshold": 0,
  "quillbot_threshold": 100,
  "max_attempts": 5,
  "delay_seconds": 6,
  "headless": true
}

### Key	Description
1. zerogpt_threshold:	AI detection must drop below this to stop
2. quillbot_threshold:	QuillBot must report this % or more human-likeness
3. max_attempts:	Maximum retries before giving up
4. delay_seconds:	Wait time between automation steps (in seconds)
5. headless:	If true, browser runs in background without showing window

----
## Input File – inputs/sample_ai_input.txt
This is where you place your AI-generated text. You can also create custom input files inside the inputs/ folder.
----
## Running the Tool(bash)
To process a file and get a humanized version:
python loop_controller.py --input inputs/sample_ai_input.txt
You can also use your own file like:
python loop_controller.py --input inputs/my_draft.txt

###Output Files
1. File :outputs/final_output.txt
Purpose: Final text after successful rewrite loop
2. File :outputs/logs.json
Purpose: Log of all attempts, scores, and intermediate text

----

## Test Your Setup
After running the script, you should:
See a Playwright browser open and interact with HumanizeAI.pro
View logging output in the terminal (e.g., AI score: 0%)
Find your final result in outputs/final_output.txt

-----

## Troubleshooting
| Problem                     | Solution                                           |
| --------------------------- | -------------------------------------------------- |
| `playwright not found`      | Run `pip install playwright && playwright install` |
| Browser window doesn’t open | Set `"headless": false` in `config.json`           |
| Output files not created    | Check if `outputs/` exists and is writable         |
| Script exits early          | Increase `max_attempts` in `config.json`           |
| `ModuleNotFoundError`       | Run `pip install -r requirements.txt`              |

----

## Custom Test Case
Create a new input file:
  nano inputs/test_article.txt
Paste in your AI-generated draft, save, and run:
  python loop_controller.py --input inputs/test_article.txt

---

## What’s Next?
Now that you’re set up:
Try adjusting the thresholds for stricter/faster rewriting
Add new inputs and test various text styles
Watch the logs.json file grow with analysis for each rewrite
Stay tuned for QuillBot and GPTZero integration modules

-----
💬 Need Help?

Open an issue on the GitHub repo
Contact the maintainer if you have feature suggestions or want to contribute
🎉 You’re ready to use DeAItor! Transform any AI text into human-passing content in under 2 minutes.
