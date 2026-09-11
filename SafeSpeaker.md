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


alexa-board interface: SAI peripheral, DMA, 4-byte word, shenanigans


mic-board interface: I2S peripheral

## Firmware and Configurations

## Tools
oscilloscope, cubeMX, cubeIDE, logic analyzer, microscope, minicom, python, 

ping-pong buffer

LOOK THROUGH PHOTOS ON PHONE


I worked on SafeSpeaker, where I interfaced a microcontroller to the audio bus of an Amazon Echo. I used a logic analyzer to record the Alexa's I2C commands, which told me how the Alexa's ADCs were configured. I configured a microcontroller to transmit audio data in the same manner, and connected the microcontroller to the Alexa. Additionally, I connected the microcontroller to a I2S MEMS microphone, and streamed the audio from the microphone to the Alexa. I also configured the microcontroller to change its audio-processing mode based an external button, as well as playback it's processed audio to a set of headphones. I also had to tweak the audio-processing program loaded onto the microcontroller such that it mitigates digital filter overflow/wrap-around issues and requires a smaller amount of memory. I also helped design and build a 3D-printed enclosure for SafeSpeaker.
