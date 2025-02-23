# Step 1: Prepare the Dataset for Kurdish TTS  

To train **Tacotron2**, we need a well-structured dataset. This step includes:  
✅ Organizing audio files  
✅ Formatting text transcriptions  

---

# Step 1: Handling Audio Files  

Before preparing the dataset, we first need to **handle audio files** properly.  

### 🔹 What You Should Have by Now:  
✅ A Python script to **convert MP4, MP3, or any format to WAV**  
✅ A script to **convert WAV files to the correct format** for Tacotron2  

---

## 1️⃣ Convert Any Audio to WAV  
Use this Python script to convert files like **MP4, MP3, etc., to WAV**:  

```python
from pydub import AudioSegment

def convert_to_wav(input_path, output_path):
    audio = AudioSegment.from_file(input_path)
    audio.export(output_path, format="wav")

# Example usage:
convert_to_wav("input.mp3", "output.wav")
2️⃣ Convert WAV Files to the Required Format
Tacotron2 requires:

Sample rate: 22050 Hz
Channels: Mono
Use this script to ensure your .wav files meet these requirements:

python
Copy
Edit
def process_wav(file_path):
    audio = AudioSegment.from_file(file_path)
    audio = audio.set_frame_rate(22050).set_channels(1)
    audio.export(file_path, format="wav")

# Example usage:
process_wav("output.wav")
✅ Now You’re Ready to Organize Your Dataset!
In the next step, we will structure the dataset and create the list.txt file. 🚀

markdown
Copy
Edit

This version:  
✔ **Starts with your main idea** (handling audio first)  
✔ **Includes useful Python scripts**  
✔ **Looks clean and easy to follow**  

## 1️⃣ Organizing Audio Files  
Create a folder named **`wavs/`** to store your recordings:  

dataset/ │── wavs/ │ ├── 1.wav │ ├── 2.wav │ ├── 3.wav │── list.txt

css
Copy
Edit

🔹 **Audio format requirements:**  
- `.wav` files  
- **Sample rate:** 22050 Hz  
- **Channels:** Mono  

Convert files using Python:  

```python
from pydub import AudioSegment

audio = AudioSegment.from_file("wavs/1.wav")
audio = audio.set_frame_rate(22050).set_channels(1)
audio.export("wavs/1.wav", format="wav")
2️⃣ Creating list.txt
This file links audio paths with text transcriptions:

arduino
Copy
Edit
wavs/1.wav|silav dinya
wavs/2.wav|ez baş im
wavs/3.wav|navê min ali ye
📌 Important: No extra spaces. Just wavs/file.wav|text

Now the dataset is ready! ✅ Next, we’ll preprocess the data for Tacotron2. 🚀

markdown
Copy
Edit

This version:  
✔ **Keeps it simple**  
✔ **Looks cleaner** with checkmarks and numbers  
✔ **Maintains all necessary details**  

Let me know if this works better! 😊
