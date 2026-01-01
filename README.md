# CLI Translator

A command-line interface translator that brings the power of language translation to your terminal, similar to Google Translate but designed for command-line usage.

## Overview

CLI Translator is a terminal-based translation tool that allows you to translate text between different languages directly from your command line. It's designed to be simple, fast, and efficient for developers and users who prefer working in the terminal.

## Features

- **Multi-language Support**: Translate between numerous languages
- **Language Auto-detection**: Automatically detect the source language
- **Interactive Mode**: Translate multiple phrases in a single session
- **Direct Translation**: Quick one-off translations via command-line arguments
- **Text File Translation**: Translate entire text files
- **History**: Keep track of your translation history
- **Configurable**: Customize default languages and preferences

## Requirements

- Python 3.7 or higher
- Internet connection (for accessing translation APIs)
- API key for translation service (instructions below)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/fampyvs/cli-translator.git
cd cli-translator
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Configure your API settings (see Configuration section)

## Configuration

Before using the translator, you need to set up your translation API credentials:

1. Create a configuration file (the application will guide you on first run)
2. Add your API key for the translation service
3. Set your default source and target languages (optional)

### Supported Translation APIs

The application is designed to support multiple translation services:
- Google Cloud Translation API
- Microsoft Azure Translator
- LibreTranslate (free, self-hosted option)
- DeepL API

## Usage

### Basic Translation

Translate a single phrase:
```bash
python translator.py "Hello, world!" --source en --target es
```

### Auto-detect Source Language

Let the tool detect the source language automatically:
```bash
python translator.py "Bonjour le monde" --target en
```

### Interactive Mode

Start an interactive translation session:
```bash
python translator.py --interactive
```

### Translate a File

Translate an entire text file:
```bash
python translator.py --file input.txt --output output.txt --target fr
```

### List Supported Languages

View all available languages:
```bash
python translator.py --list-languages
```

### View Translation History

See your recent translations:
```bash
python translator.py --history
```

## Command-Line Options

```
usage: translator.py [-h] [--source SOURCE] [--target TARGET] 
                     [--interactive] [--file FILE] [--output OUTPUT]
                     [--list-languages] [--history] [--config]
                     [text]

positional arguments:
  text                  Text to translate

optional arguments:
  -h, --help            Show this help message and exit
  --source SOURCE, -s SOURCE
                        Source language code (e.g., 'en', 'es', 'fr')
  --target TARGET, -t TARGET
                        Target language code (e.g., 'en', 'es', 'fr')
  --interactive, -i     Start interactive translation mode
  --file FILE, -f FILE  Translate text from a file
  --output OUTPUT, -o OUTPUT
                        Output file for translation
  --list-languages, -l  List all supported languages
  --history             Show translation history
  --config, -c          Configure translator settings
```

## Project Structure

```
cli-translator/
├── translator.py          # Main application entry point
├── requirements.txt       # Python dependencies
├── README.md             # This file
├── CONCEPT.md            # Design and architecture documentation
└── .gitignore            # Git ignore patterns
```

## Development

This project is designed with clear function stubs and documentation to make it easy to understand and extend. Each function includes:
- Detailed docstrings explaining purpose
- Input parameter descriptions
- Output/return value descriptions
- Expected behavior documentation

See `CONCEPT.md` for architectural details and design decisions.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the MIT License.

## Future Enhancements

- Offline translation support using pre-trained models
- Speech-to-text integration
- Text-to-speech for translations
- Support for translating code comments
- Plugin system for custom translation providers
- Web interface option
- Mobile companion app

## Troubleshooting

### API Connection Issues
- Verify your internet connection
- Check that your API key is valid and has not exceeded quota
- Ensure the API endpoint is accessible from your network

### Installation Issues
- Make sure you have Python 3.7 or higher installed
- Try creating a virtual environment before installing dependencies
- On Windows, you may need to run the terminal as administrator

### Language Not Supported
- Use `--list-languages` to see all available languages
- Some APIs may have limited language support

## Support

For issues, questions, or contributions, please visit the GitHub repository or open an issue.

---

**Note**: This is a learning project designed to help understand CLI development, API integration, and Python programming. The code structure includes comprehensive function stubs with detailed comments to facilitate learning and implementation.
