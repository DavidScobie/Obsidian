https://www.youtube.com/watch?v=FJucFIKlW2I
[[resonance_circuit]] - You have an [[inductor]] (+90 deg phase) and a [[capacitor]] (-90 deg phase) 

Series circuit resonance website (with diagrams and examples) - https://www.electronics-tutorials.ws/accircuits/series-resonance.html

**AC Resistance and Impedance** https://www.electronics-tutorials.ws/accircuits/ac-resistance.html
For a resistor, the voltage is in-phase with the current

**AC Inductance and inductive reactance**
An inductor is a coil of wire. 
Therefore a DC current flow would induce an emf in the other direction to the applied voltage. This would slow the current with a slight delay. 
An AC current flow would also induce a delayed backward emf, which restricts the current. The voltage leads the current. The bigger the AC frequency, the greater the reactance.  Therefore inductive reactance: ![[inductive_reactance_eqn.png]]
![[Pasted image 20250721152338.png]]

**AC capacitance and capacitive reactance**
A capacitor is essentially 2 plates with a space between.
With a DC supply, the charge builds up on 1 plate, resists more charge build up, and eventually restricts current flow completely.
With an AC supply, the charge builds on 1 plate (as the emf is +ve), then the charge is pushed over the plate (as the emf is -ve). Therefore a current flows.
The current flows more easily if the AC frequency is increased. Therefore ![[cap_reac_eqn_img.png]]
Here the current leads the voltage:
![[cap_phase_img.png]]

Summarised in this table: 
![[imp_reac_table.png]]

If we now consider an RLC series circuit:
As the capacitor impedance has a negative phase, and the inductor impedance has a positive phase, the 3 impedances can combined:
![[RLC_impedance_eqn.png]]
If we factor out the j, and have the condition that XL = XC, then resonance occurs
![[resonance_RLC_eqn_2.png]]
We can fine tune R, L and C to **choose the frequency of resonance**
If we choose this to be the same resonant frequency as the [[piezoelecrtic_material]] then the material will resonate, and this can be used to [[clock_a_digital_circuit]].