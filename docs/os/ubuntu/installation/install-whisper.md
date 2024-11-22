# Install OpenAI Whisper

## Installation Steps

* Open Terminal
* Update APT  
  `sudo apt update`
* Install FFMPEG  
  `sudo apt install ffmpeg`
* Install Python 3  
  `sudo apt install python3`
* Install PIP  
  `sudo apt install python3-pip`
* Install Open AI Whisper  
  `pip install git+https://github.com/openai/whisper.git`

## Configuration

* Open Terminal
* Whitelist port 10300  
  `ufw allow 10300/tcp`
* Add `whisper` to PATH  
  `export PATH=$PATH:/home/<USER>/.local/bin`
