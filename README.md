# tts-mp3-mixer

All songs are hardcoded into HTML via a local path. To make a new track, copy a new HTML div with class="trackclass", 
paste it after the last track, and give the track a unique id. Then, in the script, add another call to makeNewTrack(),
specifying your new track.

Desired functionality almost complete, two primary problems at the moment:

(Firefox) When skipping using the time slider above the tracks, the Overheads track is consistently the only one that
gets off tempo. At first I suspected this was because the file was twice the sampling rate as the others, but I tried
compressing the file using Audacity and the problem has persisted.

(Safari) Sound will play, but the quality seems very poor. Additionally, the mute buttons do not work in Safari, which
I find rather confusing since the mute functionality is based entirely around HTML elements and doesn't actually make
use of the Web Audio API. One idea I have is to upload the audio into a buffer firt, rather than grabbing it from an
HTML5 audio element. See here: http://tinyurl.com/npxlgbs
I feel this might address the poor audio playback quality, though I'm not convinced this will help with the muting
problems. 
