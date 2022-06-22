# Frequency response of single stage Folded Cascode amplifier

## A brief recap

We did the Telescopic amplifier by adding an NMOS common gate amplifier (NMOS cascodes) on top of the NMOS differential pair.

But we could have used a PMOS common gate amplifier, getting another topology: the **Folded Cascode amplifier**.

![image](https://user-images.githubusercontent.com/95447782/175026233-fcf7100b-761b-407d-8cd5-e97f7d036fdf.png)


## Transconductance Gm:
It turns out it’s the same as the telescopic and the 5T. Gm=gm1.

![image](https://user-images.githubusercontent.com/95447782/175026276-b50c3189-0134-47f6-bf77-91e55bf84279.png)


## Output conductance Gout:

Gout is a bit larger in the folded cascode than in the telescopic (Rout a bit lower). This is due to the extra devices M9 and M10 on top, which appear in parallel with the input pair devices M1 and M2 in small signal, hence reducing their rds.

Overall, Rout being a bit lower than the telescopic will mean the DC gain of the folded cascode will also be a bit lower than the telescopic.

![image](https://user-images.githubusercontent.com/95447782/175026312-880f16f9-5594-4be9-8eef-9fbda7eb1233.png)


![image](https://user-images.githubusercontent.com/95447782/175026341-9d936083-1197-47cd-a8b7-dc12753f8d62.png)

## DC gain = Gm·Rout

Summary of Gm, Rout and DC gain of folded cascode versus telescopic and 5T:

![image](https://user-images.githubusercontent.com/95447782/175026437-dd180afb-382d-41f2-8bdb-2c2c2368c40d.png)


## Frequency response of the folded cascode:

First of all, the folded cascode, in the absence of parastics, is also just a transconductor which, when driving into a capacitor, is equivalent to a single pole system.

![image](https://user-images.githubusercontent.com/95447782/175026529-d7597696-51f5-4b90-9360-23ab1194331c.png)


**In the single-pole view, neglecting parasitics**, just transconductor driving into a cap, we see that **the three amplifiers (5T, telescopic and folded cascode) have the same unity gain bandwidth**, the difference is in the DC gain and the dominant pole p1, but the unity gain bandwidth, which comes from the product of the DC gain times the dominant pole p1, is the same.

Now, let’s look at the **frequency response including parasitics**.

First of all, if we compare the nodes between the telescopic and the folded cascode, we see there are exactly the same nodes, these are qualitatively the same, the only difference is in the extra transistors M9 and M10 that appear in the folded cascode, which add some extra contribution to Cd1 and Cd2 parasitic caps. The rest of the caps are exactly the same, even their values will be the same (if device sizes were the same).

![image](https://user-images.githubusercontent.com/95447782/175026589-3f5d8400-2e70-474f-810f-d5c24df7b5aa.png)


The poles and zeroes that appear follow the same logic as in the telescopic and 5T op amps.
* The dominant pole is given by the load cap C and the overall Rout.
* Cd5 creates a pole p2 at -gm3/Cd5, due to the “imperfect current mirroring at high frequencies effect” we saw before. Also, since this cap Cd5 only acts on half of the signal current (just the half corresponding to the left input branch) it will also create a zero at twice the frequency of the pole. We saw this in the telescopic and also in the 5T op amp.
* Cd1 and Cd2 create a parasitic pole at -gm5/Cd1. Cd1 acts on the half of the current that corresponds to M1, while Cd2 acts on the other half, the one of M2, hence there is only one pole at -gm5/Cd1, and no corresponding zero here.
* Cd3 and Cd4, like in the telescopic, create parasitic poles at -gm7/Cd3 and they act on the same half of the current, the one from M1, just like Cd5, so they also create pole-zero doublets.

![image](https://user-images.githubusercontent.com/95447782/175026617-aaa46006-2d74-422a-9b5a-6570c39d666e.png)


So, **overall the frequency response of the folded cascode is almost the same as the telescopic**. The main difference between the folded cascode and the telescopic comes from the fact that **the folded cascode has some extra parasitic capacitance due to M9 and M10** and that pushes the corresponding parasitic poles to lower frequency, so **you have to reduce the unity gain frequency** to keep phase margin, so **the folded cascode is usually slower than the telescopic equivalent**.

The following is a summary of the frequency response of the folded cascode op amp. It’s pretty much the same as the previous figure.

![image](https://user-images.githubusercontent.com/95447782/175026670-b0129804-5291-4d07-a3c7-5db8204b4303.png)


Next, Noise and Offset of the folded cascode opamp.

## Noise and Offset of the folded cascode opamp.

Next:

* [Noise and Offset](Noise_and_Offset_analysis.md)


