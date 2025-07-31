https://www.electronics-tutorials.ws/filter/filter_3.html
The signal generator creates the initial signal (uniform amplitude over big frequency range)
The signal is modified electronically via modulation before it is broadcast.

- All the different satellite information is sent to earth over a range of frequencies. 
- The atmosphere attenuates the different frequencies by different amounts. 
- We use the mathematical models on python and MATLAB to find how much each frequency of the signal is attenuated.
- We then use a cascade of [[low_pass_filter]] and [[high_pass_filter]]s to attenuate the frequencies according to our [[atmospheric_model]].

[[capacitive_reactance]]
[[RF_attenuators]]
[[RF_amplifiers]]
[[RF_antennas]]


