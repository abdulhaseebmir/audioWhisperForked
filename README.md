# audioWhisper
Listen to any audio stream on your machine and print out the transcribed or translated audio. 

## Setup

[**you need to turn on stereo mix settings on windows first before running the script**](https://www.howtogeek.com/howto/39532/how-to-enable-stereo-mix-in-windows-7-to-record-audio/)

1. choose envs of your choices.
2. clone this repo into your local storage.
3. run ```pip install -r requirements.txt```
4. run ```python audioWhisper.py --devices true``` to get `device_index` and `channel`
5. run ```python audioWhisper.py ```. Make sure to choose stereo mix output device.

<img src="https://raw.githubusercontent.com/Awexander/audioWhisper/main/screenshots/--deviceslist.png">

## Command-line flags
|      --flags          |  Default Value  |      Description                                                                                       |
|:---------------------:|:---------------:|:------------------------------------------------------------------------------------------------------:|
|`--device`             | false           | To print all available devices                                                                         |
|`--model`              | small           | Select model list. refer [here](https://github.com/openai/whisper#available-models-and-languages)      |
|`--task`               | transcribe      | Choose between transcribe the audio or to translate the audio to English                               |
|`--device_index`       | 2               | Choose the output device to listen to and transcribe the audio from this device                        |
|`--channel`            | 2               | Number of channels of the output device                                                                |
|`--rate`               | 44100           | Sampling rate of the output device                                                                     |
|`--audioseconds`       | 5               | Length of audio files to record                                                                        |
|`--audiocounts`        | 5               | Number of audio files to save into path                                                                |
|`--output_dir`         | "audio"         | Output directory to save audio files recorded by audioWhisper.py                                       |

## Disclaimer
The performance of the transcribing and translating the audio are depending on your machine's performance. 

## Performance Test on Intel i5-8265U without CUDA
On default settings, using `small` model and transcribing `5 seconds audio files took 1 minute(s) 30 second(s)` to complete.

**Task Manager**
<img src="https://raw.githubusercontent.com/Awexander/audioWhisper/main/screenshots/taskmanager%20(i5-8265u%20without%20cuda).png">

**Terminal**
<img src="https://raw.githubusercontent.com/Awexander/audioWhisper/main/screenshots/running%20time%20(i5-8265u%20without%20cuda).png">

## License
The code and the model weights of Whisper are released under the MIT License. See their [repo](https://github.com/openai/whisper#license) for more information.
The code of this repo is under MIT License. See [LICENSE](LICENSE) for further details.


