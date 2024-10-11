# awg-rfsoc-trigger
Same as the awg-rfsoc package with an additional control signal.
The AWG has a memory of $2^{20}$ points. 
The memory can be loaded with 2 different waveforms, where the first $2^{19}$ points form one waveform and the second $2^{19}$ points form the second wavefom.
The 1-bit control signal can be used to switch between the two waveforms. The AWG outputs the first waveform when the control signal is low and outputs the second waveform when the control signal is high.

Note in usage:
The AWG needs to be loaded with $2^{20}$ points (with $2^{19}$ points on each of the two waveforms), but the user can choose to output the full $2^{19}$ or lesser for each of the waveforms. Due to the way the DAC operates, the number of points has to be a multiple of 16. The relation between the input pin MAX_POINTS and the number of samples to output N is given as <br>
$N = 16*$ MAX_POINTS, <br>
implying MAX_POINTS can have any value between 1 and $2^{15}$

