# Guitar_Chord_Classifier
A machine learning model that classifies what guitar chord is being played and the quality of it: i.e if it's ringy, clear, or muted.

**Data not included**

### Versions:
- Built in [python3](https://www.python.org/downloads/).

### Libraries Required:
- [NumPy](http://www.numpy.org/)
- [PyDub](https://github.com/jiaaro/pydub)
- [FFmpeg](https://github.com/jiaaro/pydub#getting-ffmpeg-set-up) (PyDub Dependency)

### Usage:
- Clone this repository. `git clone https://github.com/McCrearyD/Guitar_Chord_Classifier`
- To ONLY process raw audio into spectrograms for training, run `python3 -u convert_data.py` inside the main directory.
- More instructions will follow as more features come out! Currently under development!

### Adding Custom Data:
- Record your chord and note whether it's clear, ringy, or muted AND what exact chord you're playing.
    - For example, [G, ringy]
- Create a file in the root directory and name it `raw_data` if there isn't already one.
- Inside the `raw_data` directory, create a new directory for the chord name (again, if there isn't already one).
- Inside `raw_data/${chord_name}`, create yet another directory for the "quality" of the strum, in this case "ringy".
- You should have a directory set up similar to: `raw_data/G/ringy` in this example case.
- INSIDE the `ringy` sub-directory, append all files that are "ringy Gs".
- Repeat this process for any chords, qualities, etc. you wish to train on.

#### *Note:* All audio file types are accepted for raw data, as they will be converted into spectrogram images. Also all multi-channel audio files will be converted to 1.

***FILE SIZES MUST BE A MINIMUM OF 2 SECONDS. ALL INPUT DATA WILL BE TRUNCATED FROM THE BEGINNING TO 2 SECONDS***
