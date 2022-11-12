Title: Developing an Alexa that doesn't suck
Date: 2022-11-11 21:00
Category: Chatbots
Tags: NLP, TTS, STT, GPT-3

## The problem

Amazon is aggressively promoting its Smart Home devices, and some people are apparently buying them. I kind of understand why. Don't get me wrong, I still think that they are useless, a security threat and probably collecting all your data, but still: There is something fun about having all sorts of gadgets that promise a future where every problem will be resolved by an artificial intelligence or a robot.

I asked myself: Can we do an open source Alexa that one can talk to?: [So I wired together Python libraries until I got something roughly fitting.](https://github.com/Vuizur/gpt3-chatbot)

1. Speech recognition can be done with this [speech recognition Python library](https://github.com/Uberi/speech_recognition). It offers several backends and has a pretty good API, I can only recommend.
2. The digital assistant part can be done (like soon everything else) by the great GPT-3 API of OpenAI. One simply needs to tell GPT-3 that they are a digital assistent and engineer a small dialogue, and GPT-3 is happy to fulfill this role.
3. The output part can be done by any Text-to-Speech engine. My favourite is the [Edge-TTS](https://github.com/rany2/edge-tts) library based on the reverse engineered API that is used by the Edge browser.

## Does it work?

Well... Kind of. You can talk with it, and it gives reasonable answers. You can also set the character of the bot. If you set your bot to be a rude Alexa, be prepared to get helpful responses such as:

Q: _Alexa, what time is it?_
A: **It is time for you to die.**

But overall, talking to it is quite painful. Unless you are blind, it makes no sense to use this instead of a [proper chatbot](https://github.com/Vuizur/react-gpt3-chatbot). There are two problems that this program (and likely also Alexa) still have:

1. Speech recognition still sucks. Evolution optimized our ears for millions of years to understand language, and for algorithms it is still to hard. Ok, my microphone is not the best and I used the free Google Speech API, but even paid state-of-the-art solutions still have a high word error rate. [Speech recognition has not yet been solved](https://awni.github.io/speech-recognition/). I have not tried one of the commercial state of the art APIs yet though, because they also would not solve the second problem:
2. The latency is still too high. The main culprit is that the speech recognition waits for you to stop talking, which already adds a significant amount of time. Then the stuff needs to be sent to GPT-3, and their super huge model also takes a while to respond, and then the answer needs to be sent to Microsoft for speech synthesis. Which is then saved to disk and played by pyaudio. You see, a lot happens, and it adds up, and you get bored waiting for the answer, which is probably only a short sentence. A push-to-talk mechanism might help reduce the first type of latency, but everything else will still be too slow.

Positive: GPT-3 is decent and the Microsoft speech synthesis is also good, but this still does not make the product worth using.

## Overall takeaway

Digital assistants still need better technology to become usable conversationalists. Maybe it is better for humanity, we will have to endure talking to other people - and not robots - for a while longer.