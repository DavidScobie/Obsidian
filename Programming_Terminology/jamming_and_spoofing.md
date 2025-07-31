https://www.youtube.com/watch?v=sAjWJbZOq6I&t=626s - GPS Jamming & Spoofing video

**Jamming** (less sophisticated)
- You are trying to hear your friend over the road. But a car drives past and blares music really loud. The GPS is now blocked and you are lost.
- Planes can be jammed accidentally. If they tune their navigation radio to a harmonic of the GPS signal they are acquiring, then this will look for audio instead of demodulating for the positional data
- A Russian jammer was located in Kaliningrad as all planes transmit ADSB (signal of GPS location over time). Many planes ADSB went wrong in the same place
- GPS NOTAM's tell pilots to ignore GPS signals in certain regions
- A jamming signal can be made with low power (a few watts)
- If a system has been running for a while it can lock onto the real GPS, but if it is just starting up, it has nothing to lock onto so it is vulnerable to jamming
- Can avoid jamming with a directional antenna

**Spoofing** (more sophisticated)
- A false GPS signal is transmitted which tricks the receiver into thinking it is a different position to where it really is.
- GPS sensors tend to lock onto the largest signal inbound

**How to spoof**
- Send out a signal identical to a satellite, with more power, but with different ephemeris data
- Transmit the same signals as what they hear from their satellites to cancel them out. Then transmit the false signal and gradually evolve the position away from where they think

**How to avoid spoofing**
- Put barriers under the antenna to block out ground signals (only let space ones through). Works fine unless spoof comes from space.
- If spoofing signal is stationary from the ground, the position data wont change, hence it can be identified as different from satellites
- Smarter antenna (cross validation) - Make multiple antenna that combine signals with different phases, which gives the signals directionality. You can find where the signals should come from, and block signals from other places. Or once you locate a spoofed signal, make a hole in your antenna to remove that
- Robust GPS - Detect imposter satellites. E.g. if a signal is too powerful to be from a satellite too far away, ignore it