# BREATHE
an adaptive live performance audio enhancer (max for live device)

[BREATHE Max for live plugin.pdf](https://github.com/Skinnygiraffe1235/BREATHE/files/14469657/BREATHE.Max.for.live.plugin.pdf)

[BREATHE.zip](https://github.com/Skinnygiraffe1235/BREATHE/files/14469658/BREATHE.zip)


ONE-STOP AUDIO ENHANCER (AUTO-MASTER)

INTRODUCTION

This is a brief report about a Max patch I made to ease and speed up the process of mastering, especially for poorly live recorded audios.
Cleaning, balancing and enhancing an audio file, can be a frustrating and boring task, especially when your audio file is recorded in a noisy and untreated environment. Whether it's a speech or a song played at a bar, we need to take several steps in order to make our recordings "Presentable". 
The idea behind the creation of this plugin is to provide a simple chain of effects that can help us enhance our recorded file by tweaking a few simple variables.
As a rule of thumb, there are basically three steps in mastering: Equalizing, compression and saturating, which are provided in this patch, (Although, there's no definite rule and every engineer has their own approach.) plus an automatic multi-band noise gate with 1024 band that helps enhance your audio.
As you probably already know, Max is a visual programming language for music and multimedia that has provided a platform for students like me to bring our ideas to life.

LITRETURE OVERVIEW

There are several plugins that provide the features I've mentioned, more or less, but there are some exclusive features that I'm going to mention later on.
First and foremost, as I mentioned in the topic, it's a one-stop, All-in-one patch that makes you needless of using any other plugin.
Secondly, it gives you just enough control to achieve the best sound quality, not so much that it confuses you and not so little that you feel tied up, which also is rare in the world of plugins. (For example, "Soundgoodizer" doesn't give you enough control and "Ozone" is kind of overwhelming, although in new ozone 11 they have fixed that.)
Lastly, the main purpose of this plugin is not mastering, but enhancing and balancing a poorly recorded audio file, as well as helping your audio to sound acceptable in different sound systems. (Which is the main purpose of mastering.)

FEATURES AND FUNCTIONALITY

The main users of this plugin are going to live performers, whether in street or bar or an untreated room to help them enhance their recordings.
There are four main parts to this patch with a dedicated dry/wet knob to prevent killing the original vibe and ambience of the recording.

1. Multi-band Noise gate
By using the fast Fourier transform, I divided the frequency spectrum to 1024 bands which provides the user with a pretty accurate noise gating. The band below the given threshold will be eliminated. You can control the threshold and adjust it to taste.

2. Pink noise normalizer
As you probably know, pink noise caries the same amount of energy per octave, therefore, it sounds less hissy in comparison to white noise which has a flat frequency spectrum.
I've split the incoming audio into eight octaves and calculated the amount energy that each band carries. So, by definition, if you play a pink noise through this energy calculator, it will show the same amount for every band. (Because It's divided into eight octaves.) 
Another part of the patch calculates the average power in the mentioned bands. The patch assigns the average power to each band, by reducing or increasing the RMS value, and as a result, making a balanced EQ curve.
By this fair distribution of energy among different octaves, your audio would be more vivid to the human ear.

3. Four-band compressor
Unlike other features of this patch, there's nothing special about the compressor. It's just a simple four-band compressor with common variables. Making a couple of pre-sets, and making it somehow unique, is one of the things I wish to Improve the future. For now, it's just a simple multi-band compressor, but it's a necessary tool for mastering and enhancing audio.

4. Four-band overdrive and stereo enhancer
By summing the eight bands, (that I split in the pink noise normalizer section) two by two, we got ourselves four bands that we can apply overdrive to taste, but there's another feature that makes this patch unique. 
By tweaking the "wideness" parameter, you can activate a new patch that randomly changes the overdrive amount in right channel. The higher the amounts of wideness cause bigger intervals between overdrive amounts of left and right channels. as you already probably know, wideness and stereo imaging occurs when there are differences in right and left channels of the audio. So, by increasing the gaps, we're basically altering the right channel to be more and more different in comparison to the left channel and as a result, the stereo image will be improved.

USER INTERFACE AND EXPERIENCE

For now, It's a simple, user-friendly and easy-to-use max for live plugin, and hopefully in the future, with the help of experts, it will be upgraded to a top-notch plugin for all DAWs.

TESTING, VALIDATION AND RESULT

In the process of designing the patch, I tested it with different samples, but as I mentioned, it's specially designed for a live performance. So, I found an untreated room and set up a condenser microphone. I recorded vocals and guitar and the result was pretty good. 
This process shed light on the weaknesses of my project and helped me to list the features that need to be improved for the future, which we will discuss further on.

FUTURE WORKS AND IMPROVEMENTS

Overall, the patch works fine and It's presentable but there are some parts that needs to be improved.
First and foremost, the compression section. Although It's perfectly fine, there's nothing unique about it and it sounds so "digital". What I would really like to do is replace this compressor with an analogue model compressor, preferably a smooth-sounding, glue type compressor, with a load of presets.
I'd really like to consult a mathematician to optimize the math, especially behind the FFT parts. I think there are more efficient ways to do the math, (with the help of other programs like Python) which will lead to better sound quality , and less CPU usage.
Lastly, I would like to replace the overdrive with saturation with soft clipping. The harmonics will be more helpful with the purpose of the patch.

CONCLUSION

Overall, it's a nice, easy-to-use plugin that saves you a lot of time, and also gives you a nice control to enhance, de-noise and master your live performance and make it presentable.
