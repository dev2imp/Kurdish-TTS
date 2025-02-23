# Step 1: Prepare the Dataset for Kurdish TTS  

To train **Tacotron2**, we need a well-structured dataset. This step includes:  
✅ Organizing audio files  
✅ Formatting text transcriptions  

---

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
