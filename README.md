# Automatic Speech Recognition

## Description

This project aims at developing an end-to-end Automatic Speech Recognition system in Keras (Python)

## Data

The speech data was taken from the [LJ Speech Dataset](https://keithito.com/LJ-Speech-Dataset/), which is a public domain speech dataset by the [LibriVox](https://librivox.org/) project, consisting of 13,100 short audio clips of a single speaker reading passages from 7 non-fiction books.
* A transcription is provided for each clip.
* Clips vary in length from 1 to 10 seconds and have a total length of approximately 24 hours.

## Model

The model is based on a transformer architecture, adapted from the paper [Very Deep Self-Attention Networks for End-to-End Speech Recognition](https://arxiv.org/abs/1904.13377).
This implementation uses the following architecture:
* Number of heads: 2
* Number of Encoder layers: 4
* Number of Decoder layers: 1
* Num classes: 34 (27 alphabets + 7 common symbols)

## Result

A Word Error Ratio (WER) of 46% accuracy was obtained. However, this is expected to decrease with more epochs.

## References

1. [Automatic Speech Recognition with Transformer](https://keras.io/examples/audio/transformer_asr/)
2. [Very Deep Self-Attention Networks for End-to-End Speech Recognition](https://arxiv.org/abs/1904.13377).

