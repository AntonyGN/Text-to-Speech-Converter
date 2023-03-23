# Text-to-Speech Converter
This is a Python script that uses the Google Text-to-Speech (gTTS) API to convert text to speech and save it as an MP3 file. The script can be run in a Jupyter Notebook or any other Python environment.

## Dependencies
The script requires the following Python packages:

- ```gtts```: a Python library for the Google Text-to-Speech API
- ```playsound```: a Python library for playing audio files

You can install these packages using ```pip```:

```
pip install gtts playsound
```

## Usage
To use the script in a Jupyter Notebook, follow these steps:

 1. Open a new Jupyter Notebook and create a new code cell.
 2. Copy and paste the script into the cell.
 3. Run the cell to load the necessary packages and define the ```text_to_speech``` function.
 4. Call the ```text_to_speech``` function with the text you want to convert as the argument.
 
 Here's an example:
 
 ```bash
from gtts import gTTS
from playsound import playsound

def text_to_speech(text, language='en'):
    audio_file = 'output.mp3'
    tts = gTTS(text=text, lang=language, slow=False)
    tts.save(audio_file)
    playsound(audio_file)

# Prompt the user for input
text = input("Enter the text you want to convert to speech: ")

# Call the text_to_speech function with user input
text_to_speech(text)
```
The script will prompt the user to enter the text they want to convert to speech. Once the user enters the text and presses "Enter", the script will convert the text to speech using the Google Text-to-Speech API and save it as an MP3 file named "output.mp3" in the same directory as the script. The audio file will then be played using the playsound library.

## License
This project is licensed under the [MIT License](https://opensource.org/license/mit/).

## Acknowledgments
This project was inspired by the gTTS library and the playsound library. Special thanks to the developers of these libraries for their contributions to the open source community.


 
