# Super8-SyncFrame-Player
Super8 SyncFrame Player is a C++ application running on the Raspberry Pi.
Its purpose is to play audio files to projected Super 8 films in a way that the audio is synchronized to the film frame-by-frame.
To that end the SyncFrame player loads an audio file that contains the soundtrack of the film that is projected. The super 8 projector must be able to deliver a trigger
signal to the raspberry pi and the SyncFrame player code monitor a dedicated raspberry pi I/O input for that trigger signal.
The player plays 1 frame of audio when a trigger is sensed on the input port. The trigger signal should be 0 volts (Low) in default and rise to 3.3 Volts (High) when
the projector displays the next frame of film. 
The SyncFrame Player is therefore edge-triggered by low-to-high input triggers coming in from the Super 8 film projector.

Connecting your super 8 projector.
Whatever means you use to generate a 0V to 3.3V edge trigger, the SyncFrame player set up should be that the raspberry pi that runs the player also
is powering the trigger generating circuit that is used and fitted with the projector. So the GND and 5V pins of the raspberry pi should be connected to 
the triggering circuit and the triggering circuit output (0V to 3.3V triggers) should be connected to the designated input port on the Raspberry Pi.

SyncFrame Player runs on Raspberry Pi 2, 3 and 4 but 4 is recommended from performance perspective.
