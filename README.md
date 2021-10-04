# Automatic Speech Recognition

## Description

This project aims at developing an end-to-end Automatic Speech Recognition system in Keras (Python)

## Data

The speech data was taken from the [LJ Speech Dataset](https://keithito.com/LJ-Speech-Dataset/), which is a public domain speech dataset by the [LibriVox](https://librivox.org/) project, consisting of 13,100 short audio clips of a single speaker reading passages from 7 non-fiction books.
* A transcription is provided for each clip.
* Clips vary in length from 1 to 10 seconds and have a total length of approximately 24 hours.

```
Total train samples:  12969
Total test samples:  131
Shape of each speech feature sample: (2754, 129)


5 train samples
----------------------------------------------------------------------------------------------------
{'audio': './datasets/LJSpeech-1.1/wavs/LJ012-0134.wav', 'text': 'Presently the proper person arrived from the consignees, but found the gold-dust gone.'}
{'audio': './datasets/LJSpeech-1.1/wavs/LJ024-0103.wav', 'text': 'Oh! I was for an amendment all right, but this amendment you proposed is not the kind of amendment that I was thinking about.'}
{'audio': './datasets/LJSpeech-1.1/wavs/LJ015-0180.wav', 'text': 'was densely crowded, and many curious eyes were turned upon the somewhat remarkable man who occupied the dock.'}
{'audio': './datasets/LJSpeech-1.1/wavs/LJ024-0131.wav', 'text': 'The workers were not fooled by that propaganda then. The people of America will not be fooled by such propaganda now.'}
{'audio': './datasets/LJSpeech-1.1/wavs/LJ016-0059.wav', 'text': 'Here he came upon a woman on the leads hanging out clothes to dry.'}


5 test samples
----------------------------------------------------------------------------------------------------
{'audio': './datasets/LJSpeech-1.1/wavs/LJ048-0221.wav', 'text': 'In the early morning hours on November twenty-two, nineteen sixty-three,'}
{'audio': './datasets/LJSpeech-1.1/wavs/LJ041-0056.wav', 'text': 'in his intense desire to join the Marines and get away from his surroundings and his mother.'}
{'audio': './datasets/LJSpeech-1.1/wavs/LJ033-0076.wav', 'text': 'On the morning of November twenty-two, nineteen sixty-three,'}
{'audio': './datasets/LJSpeech-1.1/wavs/LJ017-0069.wav', 'text': 'Originally a doctor in practice at Rugeley, in Staffordshire, he had gradually withdrawn from medicine, and devoted himself to the turf;'}
{'audio': './datasets/LJSpeech-1.1/wavs/LJ031-0074.wav', 'text': 'quote, could have easily been hidden in the blood and hair, end quote,'}
```

## Model

The model is based on a transformer architecture, adapted from the paper [Very Deep Self-Attention Networks for End-to-End Speech Recognition](https://arxiv.org/abs/1904.13377).
This implementation uses the following architecture:
* Number of heads: 2
* Number of Encoder layers: 4
* Number of Decoder layers: 1
* Num classes: 34 (27 alphabets + 7 common symbols)

## Result

A Word Error Ratio (WER) of 46% was obtained. However, a much lower rate can be expected with increase in epochs.

## References

1. [Automatic Speech Recognition with Transformer](https://keras.io/examples/audio/transformer_asr/)
2. [Very Deep Self-Attention Networks for End-to-End Speech Recognition](https://arxiv.org/abs/1904.13377).

