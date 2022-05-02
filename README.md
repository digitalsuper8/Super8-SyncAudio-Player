# Super8-SyncAudio-Player
Super8 SyncAudio Player is a C++ application running on the Raspberry Pi.
Its purpose is to play audio files to projected Super 8 films in a way that the audio is synchronized to the film frame-by-frame.
To that end the SyncAudio player loads an audio file that contains the soundtrack of the film that is projected. The super 8 projector must be able to deliver a trigger
signal to the raspberry pi and the SyncAudio player code monitors a dedicated raspberry pi I/O input for that trigger signal. Alternative a trigger signal can be used from any other external trigger-generator (oscillator, crystal sync trigger generator etc), to trigger both the SyncAudio player running on the pi as well as to trigger the super8 projector (in case that has an input for trigger signals, e.g. Elmo GS-1200).

The player plays 1 frame of audio when a trigger is sensed on the input port. The trigger signal should be 0 volts (Low) in default and rise to ~3.3 Volts (High) when
the projector displays the next frame of film. 
The SyncAudio Player is therefore edge-triggered by low-to-high input triggers coming in from the Super 8 film projector or another trigger source.

SyncAudio Player runs on Raspberry Pi 2, 3 and 4 but 4 is recommended from performance perspective.
