# MoneyPrinterTurbo README

## Introduction

MoneyPrinterTurbo is your ultimate AI-powered video creation tool. Simply provide a topic or keyword, and it will automatically generate a high-definition video, complete with script, materials, subtitles, and background music.

## Features

- **AI-Generated Content**: Automatically creates video scripts, subtitles, and background music.
- **Multiple Video Formats**: Supports both 9:16 (portrait) and 16:9 (landscape) high-definition formats.
- **Customization Options**: Choose from various voices, adjust subtitle styles, and set your preferred background music volume.
- **Batch Processing**: Generate multiple videos at once and select the best one.
- **Cross-Platform Support**: Compatible with OpenAI, Azure, and many other AI providers.

## Quick Start

### Try Instantly with Google Colab

Want to try MoneyPrinterTurbo without setting up a local environment? Run it directly in Google Colab!

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/harry0703/MoneyPrinterTurbo/blob/main/docs/MoneyPrinterTurbo.ipynb)

### Download for Windows

[Download the latest version for Windows](https://drive.google.com/file/d/1HsbzfT7XunkrCrHw5ncUjFX8XX4zAuUh/view?usp=sharing)  
*(Double-click `start.bat` to launch!)*

## Installation & Deployment

### System Requirements

- 4+ CPU cores recommended
- 4GB+ RAM
- Windows 10+, MacOS 11+, or Linux

### Docker Deployment

1. **Clone the Project**:
   ```shell
   git clone https://github.com/harry0703/MoneyPrinterTurbo.git
   cd MoneyPrinterTurbo
   ```

2. **Launch the Docker Container**:
   - Install Docker first if you haven't: [Docker Installation](https://www.docker.com/products/docker-desktop/)
   - For Windows, ensure WSL is set up: [Windows WSL Guide](https://learn.microsoft.com/en-us/windows/wsl/install)
   - Run the following command:
     ```shell
     docker-compose up
     ```

3. **Access the Web Interface**:
   Open your browser and visit [http://localhost:8501](http://localhost:8501)

4. **Access the API Documentation**:
   Open your browser and visit [http://localhost:8080/docs](http://localhost:8080/docs)

### Manual Deployment

1. **Clone the Project**:
   ```shell
   git clone https://github.com/harry0703/MoneyPrinterTurbo.git
   cd MoneyPrinterTurbo
   ```

2. **Set Up a Python Environment**:
   ```shell
   conda create -n MoneyPrinterTurbo python=3.11
   conda activate MoneyPrinterTurbo
   pip install -r requirements.txt
   ```

3. **Install ImageMagick**:
   - **Windows**: Download and install [ImageMagick](https://imagemagick.org/script/download.php). Do not install in a path with Chinese characters.
   - **MacOS**: `brew install imagemagick`
   - **Ubuntu**: `sudo apt-get install imagemagick`
   - **CentOS**: `sudo yum install ImageMagick`

4. **Launch the Web Interface**:
   - **Windows**: Run `webui.bat`
   - **MacOS/Linux**: Run `sh webui.sh`

5. **Launch the API Service**:
   ```shell
   python main.py
   ```

## Common Issues & Solutions

### FFmpeg Not Found
If you encounter a "No ffmpeg exe could be found" error:
1. Download FFmpeg from [here](https://www.gyan.dev/ffmpeg/builds/).
2. Set the `ffmpeg_path` in `config.toml` to your FFmpeg installation path.

### ImageMagick Installation Issues
- Ensure you install the **static library** version of ImageMagick.
- Avoid installation paths with spaces or special characters.

### Whisper Model Download Issues
If you cannot download the Whisper model:
1. Use the provided Baidu Netdisk or Quark Netdisk links to download the model.
2. Place the extracted model directory in `./MoneyPrinterTurbo/models/`.

## License

This project is licensed under the terms of the [MIT License](LICENSE).