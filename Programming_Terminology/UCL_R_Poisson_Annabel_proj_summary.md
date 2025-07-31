Purpose - Needed to find statistically significantly replicating TCRs across certain days, as this helps to indicate when the adaptive immune response kicks in.

**Method and results**
- Load in all the data which was (count of that TCR on that day, TCR amino acid sequence, day, patient ID)
- Use Poisson statistics:  ![[Poisson_dist_img.png]] ![[Poisson_formula_img.png]] 
- The mean of the distribution (lambda) is the number of counts on the first day (day 2), and check whether the number of counts on the second day (day 10) is outside of the significance level 10**(-10). This gives a very broad range over x dimension of graph
- If the second day count is outside, the this TCR has significantly replicated
- Run the jobs on a high-powered remote cluster
- Plot a graph of the number of significantly replicating genes at each final day.
- We found that day 10 was this peak. Hence 10 day is the delay until adaptive response kicks in.

**Contributions**
- Taught an undergraduate how to use this R pipeline for her project
- Was a co-author for a paper on this published in the Nature journal

