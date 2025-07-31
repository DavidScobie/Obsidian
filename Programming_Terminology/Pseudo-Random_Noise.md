2 different PRN codes have no correlation
Therefore users distinguish different GPS signals from different satellites
The minimum pulse of PRN code is called a chip.

There are 2 types of PRN code:
- [[Coarse_Acquisition]] code.
- [[Precision_code]].

![[Pasted image 20250720115821.png]]
- [[Coarse_Acquisition]] can be easily decoded using [[Xingxin_Gaos_method]]. As it repeats 50 times in 50ms, hence we can use its correlation characteristics to decode the sequence.
- However we cannot decode [[Precision_code]] as its period is 1 week. Hence we need 50 weeks (1 year) of data, which is a huge storage amount.
