# TTS for Kurdish Language  What you Need to Know

In this Repository I will Give you Important things about Tacotron2 so that you can train your own dataset for Kurdish language. 
Depending on Your Quality of Audios You might have a perfect model that will generate Speech for any given Text. 
lets assume you wrote:"Silav Gelî Hevalan" then you run 
you have audio file that says exactly the same thing what a Kurdish speaker or You would say.
## Need 1: What Do we need ?
  - Python script that will help you convert any media(.mp4,.mp3) to .wav files. 
  - Python script that will convert .wav files to:
      - ✅ Sample rate: 22050 Hz 
      - ✅ Channels: Mono (1 channel)
## How to Prepare my audios:
  -  If you are going to follow the way I am doing you need your audio to be less than 12 seconds.
  -  Clear audios no background voices.
### Folders should look like this:
 dataset/
        ├── wavs/
        │   ├── 1.wav
        │   ├── 2.wav
        │   ├── 3.wav
        └── list.txt

