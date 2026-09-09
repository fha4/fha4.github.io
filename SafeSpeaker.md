# SafeSpeaker Project

I worked on SafeSpeaker in collaboration with [Cameron Haire](https://github.com/CallMeRon7) and [Shreyas Narayanan](https://github.com/ShreyasNarayanan06). My work involved the hardware demonstration for SafeSpeaker.



I was responsible for ...

I contributed by ..
- Using a logic analyzer to read I2C commands being sent on the Amazon Echo Dot's I2C bus. These revealed the way in which the Echo Dot communicated its audio data.
- 


# Photos




# Technical Breakdown

## High-Level Overview

An Amazon Echo Dot (aka Alexa) communicates it's audio data (roughly) as follows: First, it records audio using onboard analog microphones. Onboard ADCs convert this to a digital signal, and send that data over an audio bus to it's main processor. The main processor sends this data to Amazon's servers, where the audio is processed (and stored). The Alexa then receives audio from the servers, which the Alexa plays for the user to hear.

SafeSpeaker injects digital audio data on to the audio bus, which the main processor reads as legitimate data from the Alexa's ADCs. By injecting obfuscated audio from a seperate microphone, in conjuction with disabling the Alexa's own microphones, the user's privacy may be protected, while the functionality of the device is maintained.

## Alexa Hardware


## External Hardware
To interface with the Alexa and obfuscate audio, SafeSpeaker uses an [STM32G431KB MCU](https://www.st.com/en/evaluation-tools/nucleo-g431kb). To record audio, SafeSpeaker uses a [SPH0645LM4H-B I2S Microphone on a breakout-board from Adafruit](https://cdn-shop.adafruit.com/product-files/3421/i2S+Datasheet.PDF).


## Firmware and Configurations

## Tools
oscilloscope, cubeMX, cubeIDE, logic analyzer, microscope, minicom, python, 
