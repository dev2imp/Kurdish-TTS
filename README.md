# Kurdish-TTS
In this repository, I will take you through the Tacotron2 model step by step to generate Text-to-Speech (TTS) for Kurdish.

Here’s your GitHub **Markdown-formatted** post:  

```md
# **Step 1: Preparing the Dataset for Kurdish Text-to-Speech (TTS)**  

The most crucial part of training a **Tacotron2 model** is having a properly structured dataset. In this step, we will organize our audio files and create a list file (`list.txt`) that maps each audio file to its corresponding text.  

## **1. Organizing Audio Files**  
Inside your dataset folder, create a directory named **`wavs`**, where all your recorded `.wav` files will be stored. The structure should look like this:  

```
dataset/
│── wavs/
│   ├── 1.wav
│   ├── 2.wav
│   ├── 3.wav
│   ├── ...
│── list.txt
```

All **audio files** must be in **WAV format**, with the following properties:  
- **Sample rate**: 22050 Hz  
- **Channels**: Mono (1 channel)  

To ensure all files meet these requirements, use the following Python code:  

```python
from pydub import AudioSegment

# Convert audio to 22050 Hz, mono channel
destination_path = "wavs/1.wav"  # Example file
audio = AudioSegment.from_file(destination_path)
audio = audio.set_frame_rate(22050)
audio = audio.set_channels(1)
audio.export(destination_path, format="wav")
```

---

## **2. Creating the `list.txt` File**  
The `list.txt` file maps each **audio file** to its corresponding **text transcription**. It must follow this format **without extra spaces**:  

```
wavs/1.wav|silav dinya
wavs/2.wav|ez baş im
wavs/3.wav|navê min ali ye
```

Each line contains:  
- The **relative path** to the `.wav` file  
- A **text transcription**, separated by `|`  

---

This dataset structure is essential for Tacotron2 training. In the next step, we will preprocess this data for the model. 🚀  
```
