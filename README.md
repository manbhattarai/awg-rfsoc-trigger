# awg-rfsoc-trigger
Same as the awg-rfsoc package with an additional control signal.
The AWG has a memory of $2^{20}$ points. 
The memory can be loaded with 2 different waveforms, where the first $2^19$ points form one waveform and the second $2^{19}$ points form the second wavefom.
The 1-bit control signal can be used to switch between the two waveforms. The AWG outputs the first waveform when the control signal is low and outputs second waveform when the control signal is high.

Note in usage:
The value of MAX_POINTS should be chosen to correspond to 2^19 points. This makes the value to be $2^{19}/2^4 = 2^{15}$.
