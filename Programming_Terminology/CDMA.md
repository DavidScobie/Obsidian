Code-Division Multiple Access

Each satellite is assigned a [[Pseudo-Random_Noise]] (PRN) code.
![[PRN_diagram.png]]
Notice how in the 3rd wave, the sign of the 2nd wave is flipped according to the 1st wave.

**Demodulation**
All the users share the same frequency band. Therefore the PRN functions as a key to match the receiver with the transmitter.
- Different satellites have different keys (PRN codes).
- One door (data modulated for one satellite) can be only opened by one key.
- Inserting the key into the door is done by correlation.
The recipient generates a PRN code locally, and correlates it with the signal. If they match then the recipient obtains a denoised signal. 