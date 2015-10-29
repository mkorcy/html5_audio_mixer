# tts-mp3-mixer

All songs are hardcoded into HTML via a local path. To make a new track, copy a new HTML div with class="trackclass", 
paste it after the last track, and give the track a unique id. Then, in the script, add another call to makeNewTrack(),
specifying your new track.

Desired functionality almost complete, two primary problems at the moment:

When skipping using the time slider above the tracks, the Overheads track is consistently the only one that
gets off tempo. At first I suspected this was because the file was twice the sampling rate as the others, but I tried
compressing the file using Audacity and the problem has persisted.

The other problem is the difficulty I'm having with cross browser compatibility. I've been following many tutorials
online about making the Web Audio API work in Chrome and Safari, but thus far I can only successfully get it working 
in Firefox.
