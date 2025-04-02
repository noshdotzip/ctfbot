# CTFBot 🤖

A Discord bot designed for CTF enthusiasts and cybersecurity professionals, providing tools for file analysis, EXIF data extraction, and AI-powered assistance.

![Bot Status](https://img.shields.io/badge/status-active-success.svg)
[![License: Apache 2](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://opensource.org/licenses/MIT)
[![Discord](https://img.shields.io/badge/Discord-Join%20Server-7289DA)](https://discord.gg/U9dUVNe6ph)

## 🎯 Features

- **File Analysis**
  - `/strings` - Extract readable strings from files
  - `/floss` - Run FLOSS analysis on files
  - `/filetype` - Analyze file magic bytes for file type identification
  - `/exif` - Extract and display EXIF data from images with GPS mapping

- **AI Integration**
  - `/ask` - Ask questions to various AI models:
    - OlympicCoder 32b
    - DeepSeek R1 Zero 671b
    - DeepSeek V3 685b
    - Gemini 2.5 Pro Experimental

- **Real-time Status**
  - Dynamic guild count
  - User installation tracking
  - Engaging status messages

## 🚀 Getting Started

### Prerequisites

```bash
# System requirements
sudo apt-get update
sudo apt-get install -y exiftool

# Python requirements
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Configuration

Create a `config.json` file:

```json
{
    "discord_token": "your_discord_bot_token",
    "openrouter_api_key": "your_openrouter_api_key",
    "mapbox_token": "your_mapbox_token"
}
```

### Running the Bot

```bash
python main.py
```

## 📚 Commands

### `/strings [file] [limit] [as_file]`
Extract readable strings from uploaded files.
- `file`: File to analyze
- `limit`: Minimum string length (default: 4)
- `as_file`: Return results as file attachment (default: false)

### `/floss [file] [limit] [as_file]`
Run FLOSS (FireEye Labs Obfuscated String Solver) analysis.
- `file`: File to analyze
- `limit`: Result limit (default: 4)
- `as_file`: Return results as file attachment (default: false)

### `/filetype [file]`
Analyze file magic bytes to determine file type.
- `file`: File to analyze

### `/exif [file]`
Extract EXIF metadata from images.
- `file`: Image to analyze
- Displays: Camera info, GPS location, timestamps, and more
- Includes interactive map for GPS coordinates

### `/ask [model] [question]`
Ask questions to AI models.
- `model`: Choose from available AI models
- `question`: Your question or prompt

## 🛠️ Technical Details

### Dependencies

```plaintext
discord.py
openai
Pillow
requests
asyncio
```

### File Structure

## 🔒 Security Features

- Rate limiting on commands
- File size restrictions
- Secure file handling with automatic cleanup
- Permission-based command access

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenRouter](https://openrouter.ai/) for AI model access
- [ExifTool](https://exiftool.org/) for metadata extraction
- [FLOSS](https://github.com/fireeye/flare-floss) for string analysis

## 🔗 Links

- [Discord Server](https://discord.gg/U9dUVNe6ph)
- [Bug Report](https://github.com/yourusername/ctfbot/issues)
- [Feature Request](https://github.com/yourusername/ctfbot/issues)

## 📊 Status

- Bot Status: Online
- Latest Version: 1.0.0
- Python Version: 3.8+