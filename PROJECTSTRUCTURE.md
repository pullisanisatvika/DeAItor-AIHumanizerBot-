DeAItor-AIHumanizerBot/
├── loop_controller.py         # Controls the retry process
├── humanizeai.py              # Automates HumanizeAI.pro input/output
├── zerogpt_checker.py         # Extracts and parses ZeroGPT detection score
├── quillbot_checker.py        # (Planned) Validates via QuillBot UI or unofficial API
├── utils/
│   ├── browser_setup.py       # Common Playwright setup and helpers
│   └── logger.py              # Logging outputs, timestamps, retry tracking
├── outputs/
│   ├── final_output.txt       # Human-passed final version
│   └── logs.json              # Score history, retries, metadata
├── inputs/
│   └── sample_ai_input.txt    # Your raw AI-generated text
├── README.md
├── requirements.txt
└── .gitignore
