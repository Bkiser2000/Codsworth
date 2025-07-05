# Codsworth
# Codsworth

**Codsworth** is your personal robotic butler—a Python-powered, extensible chatbot assistant that can answer questions, fetch weather and stock data, summarize news, and more. Designed for flexibility and easy extension, Codsworth is ideal for anyone who wants a smart, scriptable assistant in their terminal.

---

## Features

- **Conversational AI:** Interact with Codsworth using natural language.
- **Stock Market Data:** Get real-time stock prices and predictions.
- **Cryptocurrency Info:** Fetch crypto prices and make predictions.
- **Weather Reports:** Ask for current weather in any city.
- **News Summarization:** Summarize news articles and get sentiment analysis.
- **Extensible:** Easily add new skills and intent handlers.
- **Trainable:** Use your own intents and patterns to customize Codsworth’s responses.
- **CLI Integration:** Launch Codsworth from the terminal with the `codsworth` command.

---

## Installation

You can install Codsworth from source:

```sh
pip install .
```

Or, if published on PyPI:

```sh
pip install codsworth
```

---

## Usage

### **Start the Chatbot**

After installation, activate your virtual environment (if needed) and run:

```sh
codsworth
```

You’ll see a prompt where you can type messages. Type `/quit` to exit.

### **Train the Chatbot**

Before first use, you should train Codsworth (this creates the model file):

```sh
codsworth --train
```

This will parse your intents, prepare data, train the model, and save it to your home directory as `~/.codsworth_model.pth`.

---

## Example Interactions

```
You: What’s the weather in London?
Codsworth: The weather in London is cloudy with a temperature of 18°C

You: Predict AAPL stock price for next week
Codsworth: Predicted price of AAPL on 2024-07-12: $189.23 (range: $180.00 - $195.00)

You: Summarize this news article: [URL]
Codsworth: [Summary and sentiment]
```

---

## Configuration & Customization

- **Intents:** Codsworth uses `intents.json` to define what it can do. You can edit this file to add new patterns and responses.
- **Data Files:** All necessary data files (`intents.json`, `dimensions.json`) are included in the package.
- **Model:** The trained model is saved as `~/.codsworth_model.pth`.

---

## Extending Codsworth

To add new skills:
1. Define a new intent in `intents.json`.
2. Add a corresponding function in the code.
3. Map the intent to your function in the `function_mappings` dictionary.

---

## Development

Clone the repository and install in editable mode:

```sh
git clone https://github.com/Bkiser2000/Codsworth.git
cd Codsworth
pip install -e .
```

### **Project Structure**

```
codsworth/
    __init__.py
    intents.json
    dimensions.json
    cryptodata.csv
    stockdata.csv
setup.cfg
pyproject.toml
README.md
```

---

## Requirements

- Python 3.8+
- See `setup.cfg` for dependencies (e.g., `requests`, `spacy`, `nltk`, `torch`, etc.)

---

## License

MIT License

---

## Author

Brendan Kiser  
[GitHub](https://github.com/Bkiser2000/Codsworth)

---

## Contributing

Pull requests and suggestions are welcome! Please open an issue or submit a PR.

---

## Troubleshooting

- **Model file not found:** Run `codsworth --train` before first use.
- **Missing dependencies:** Ensure all requirements are installed.
- **Data files missing:** Reinstall the package or check your installation.

---

Enjoy your new AI butler!
