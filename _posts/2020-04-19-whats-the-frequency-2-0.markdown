---
layout: post
title:  "What's the Frequency 2.0"
date:   2020-04-19 20:56:45 +0000
---

On the 21st February 2014, I released the first version of **What’s the Frequency?** on the iOS App Store.

This was quite an exciting time for me—it was the first app I’d ever developed entirely on my own. I’d had lots of experience designing and managing hardware and software products, delivered by teams of incredibly talented engineers, but this was the first time I’d actually written an app like this myself, from scratch.

## Version 1.0

**What’s the Frequency?** 1.0 was a very simple app in both concept and execution.

The concept is that the app plays a short tone or burst of filtered pink noise and you are challenged to identify the frequency of the tone, or the centre frequency of the filtered noise.

You never lost at the game. You had unlimited attempts to guess the correct frequency but every incorrect attempt resulted in lower accuracy for that game. You could keep going forever, but as soon as you made one incorrect guess, your accuracy would permanently drop below 100% and there would be little motivation to continue with that game. I hated seeing my accuracy drop below 100% so I would start a new game each time I guessed incorrectly. This experience felt broken.

In execution, the app was entirely based on stock iOS views. The main menu was a UITableView that presented the various game options. Tapping one of these would present another UITableView containing a list of all the possible frequencies. You could tap on rows until you got the correct frequency, at which point a modal view would appear, telling you how well your were doing so far. Dismissing this would start the next round and play the next frequency to guess.

It was functional, but rather uninspiring.

<div class="post-image"><img src="/assets/images/writing/whats-the-frequency-2-0/v1.jpg"></div>

The main motivation for creating this app, and the most interesting part to me at the time, was to see if I could write the generators and filters myself. I wanted to understand how to write to iOS audio buffers directly. The audio generation and processing code was relatively simple, but trying to find up to date documentation and references for Audio Units was difficult. It also involved a mix of Objective-C and C++ code which was another interesting challenge. It all worked fine and I certainly learned a lot, but I was never completely happy with the sound of the filters, or the experience of trying to work with those frameworks.

I had lots of ideas for how the app could be improved and where it could go, but given the combination of kids, other projects, and work commitments, I never gave it priority.

If your’e interested, the code for version 1.0 is available in a public GitHub repo [https://github.com/henrybourne/WhatsTheFrequency](https://github.com/henrybourne/WhatsTheFrequency).

## Version 2.0

Sometime in 2018, I became motivated by a few different goals:

- I was inspired by delightful animations I’d seen in some apps and wanted to learn how to make my own custom animations in an iOS app
- I wanted to improve the overall game experience, and make have more of a purpose
- I wanted to learn how to use Auto Layout, and properly support different device sizes
- I wanted to explore an audio engine I’d come across—AudioKit
- I wanted more experience writing Swift

So, I started work on version **What’s the Frequency?** 2.0.

## Cleaner and More Customised UI

Rather than rely completely on stock iOS UI components, I wanted to create a more purpose-built interface for the main game view. So gone is the standard UITableView—replaced by a grid of buttons that allow all possible frequencies to be visible on screen at once. I think it’s a nicer presentation, and one that gives the app much more of its own character.

It also features support for light and dark modes, following the system state of your device.

<div class="post-image"><img src="/assets/images/writing/whats-the-frequency-2-0/v2.jpg"></div>

As part of the custom UI, I wanted to include some animations to represent tones and noise. I decided to show a wave along the bottom of the game view that animates as the audio plays. This can also offer some visual hinting to help identify frequencies which can be useful as you’re starting out.

When you win or lose a round, there are animated waves in the background of the dialogs. These move quickly in the ‘win’ view, and slowly in the ‘lose’ view which help to give the app a little more emotion.

I’m sure these animations could be optimised, which will be one of the next updates. To help with this I might make the code open source and ask for contributions from my more experienced developer friends.

<div class="post-image"><img src="/assets/images/writing/whats-the-frequency-2-0/v2-wavy-lines.jpg"></div>

## Game Experience

Version 2.0 changes the game to give it a clearer purpose. There are three difficulty modes—Practice, Normal, and Difficult.

In Normal difficulty, you have three chances to guess each frequency. If you guess incorrectly three times you lose the round and the game ends. The goal is to identify as many frequencies as possible.

In Difficult difficulty, you only have a single chance to identify each frequency, meaning you have to be much more skilled to play a long game.

In Practice mode, you have unlimited guesses allowing you spend time honing your identification skills.

When the game ends you see a clear summary of your game, giving you a clear goal for you to try to beat next time.

Version 2.0 also adds the ability to disable certain frequencies, removing them from the game. This can be useful if you’re using a device which is limited in low frequency reproduction, or if you’re struggling to identify very high frequencies.

I think these changes create a much better structure and improve the overall experience.

## Audio Engine

AudioKit powers all generation and processing. It’s a fantastic framework that’s incredibly easy to use. For the pure tones, I create an oscillator, send it through an envelope filter to handle fading in and out, then connect it to the output. That’s it. It’s only one extra step for the noise, which uses a white or pink noise generator, a bandpass filter, then the envelope filter. There was a bit more to it than that, particularly around dealing with the audio lifecycle and changing between sounds without clicks or noticeable glides, but overall it was a really simple and great experience. Congratulations to the AudioKit team for creating such a great tool and allowing me to spend more time concentrating on the custom UI and animations.

## Support for all Device Sizes

Version 2.0 properly supports all current Apple device and layout sizes. Using Auto Layout for the views made this very simple, and also enabled iPad support. So whether you’re running the app on an iPhone SE, an iPhone 11 Pro Max, or an iPad in fullscreen, split view, or in popover, the app will look great and work well.

## In Future

There are lots of tweaks and improvements I’d like to make in future. Hopefully I’ll get round to them in less time than it took to release version 2.0…

Thanks to Apple’s Mac Catalyst project, I was able to get the app running on a Mac in a few minutes. It was literally a case of checking a box that says ‘Mac’. Fantastic work to the team at Apple for making it so easy.

Unfortunately I don’t think AudioKit’s support for XCFramework is ready for production yet, so I can’t yet create a single app with Mac Catalyst support. I can create separate build that works on a Mac, but I’m not sure if I can submit this as a separate app… I’m not sure in the submission process. If you know more about this and know how I can get a Mac Catalyst app on the store now, please let me know.

<div class="post-image"><img src="/assets/images/writing/whats-the-frequency-2-0/v2-catalyst.jpg"></div>
