# Swing limits of Folded Cascode amplifier

## Swing limits of the Folded Cascode op amp

So far, we have seen that **the folded cascode ONLY HAS DISADVANTAGES**. It’s worse than the Telescopic at everything we have seen so far (DC gain, although it has better DC gain than the 5T), noise, offset, slew rate is the same but it has higher power dissipation (twice as much), also in terms of frequency response, it has more parasitic poles so it will need to be configured with a lower unity gain frequency and thus it will be slower.

So **here comes the advantage of the folded cascode: the swing limits.**

![image](https://user-images.githubusercontent.com/95447782/175027517-c1b2a548-83c2-41d1-b56a-8b982399da43.png)


This is the comparison of swing limits:

![image](https://user-images.githubusercontent.com/95447782/175027530-773ed4e0-6f0e-4d65-a4f3-2dc927287783.png)


So, clearly in terms of swing limits the folded cascode is the best.

Since the tendency these days is for supply voltages to reduce, that’s why in many applications Telescopic op amps are just not an option, and the folded cascode gets used more commonly.

## Final summary, comparison between 5T, Telescopic and Folded cascode

A quick final summary comparison between 5T, Telescopic and Folded cascode:

* They all have the same transconductance Gm=gm1
* **Telescopic and Folded cascode have higher Rout** than the basic 5T, **hence higher DC gain.** Telescopic having the largest DC gain of the three options.
* **Noise and offset is the same in the 5T and the Telescopic. In the folded cascode case, it’s mostly the same, slightly worse due to the extra devices M9 and M10.** The only difference is in the extra transistors M9 and M10 which contribute some extra noise and offset in the folded cascode.
* **Slew rate is the same in all of them** (assuming the folded cascode is biased with I2=Io/2 which is the common choice). **But in this case, the folded cascode has 2x the power dissipation** with respect to the other two topologies.
* 5T and Telescopic power dissipation (quiescent current) is Io, whereas the folded cascode consumes 2*Io.
* **The folded cascode advantage is in the swing limits**, both input common mode range and output swing. On the input side, the input common mode can go all the way up to supply and even a bit above supply which is good, and in the downwards direction it’s the same as the other two. On the output side, both its upper and lower limits are the best of the three topologies, as the output can swing up to 2 Vdsats below supply and down to 2 Vdsats above ground.
* **In terms of frequency response and overall speed, the Telescopic and the Folded cascode** have more nodes than the basic 5T, and hence they **have more parasitic poles,** and therefore **to keep them stable you will probably have to reduce unity gain frequency** in them, **so the Telescopic and Folded cascode are usually slower** than the basic 5T, differential pair based amplifier.


This is the end of the analysis of the three single stage op amp topologies. Now, in general **single stage op amps are not very useful since they can only drive purely capacitive loads but not resistive loads**, since a resistive load at their output will appear in parallel with their intrinsic Rout, dropping the overall Rout and killing DC gain. **That’s what motivates the use of the 2 stage op amps such as the 2-stage Miller compensated op amp.**




