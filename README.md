# The Flip Flop 2.0

CEEM guitar audio sequencer and stutter effect for Windows x64 VST3 hosts.

Insert it directly on a guitar/audio track, select your audio input and enable monitoring. Each of the 16 steps can be Off (mute), Play (live guitar), or Stutter (repeat a slice of recent input). Step rate offers quarter, eighth, sixteenth, or thirty-second notes. Stutter repeats the captured slice 2, 3, 4, or 8 times during a step.

Live clock runs from the Tempo knob even while REAPER is stopped. Host clock follows REAPER's tempo and playback position, and passes the guitar through while transport is stopped. Gate adjusts how much of each step or repeat is audible. Mix blends the sequenced and original guitar. Level adjusts output volume.

The stutter captures input immediately before a Stutter step starts. Play a little guitar before a stutter step to fill its capture buffer. Step and loop edges have short fades.

Version 2 replaces the earlier MIDI sequencer with this audio effect. Old MIDI patterns load with rests converted to Off and note steps converted to Play. Save new patterns with the updated plugin.

Extract the complete The Flip Flop.vst3 bundle to your VST3 folder, replacing the earlier bundle, and rescan in REAPER.

Build using Visual Studio C++ tools and CMake.

    cmake -S . -B build -A x64
    cmake --build build --config Release --target FlipFlop_VST3
