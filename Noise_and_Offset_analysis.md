# Noise and Offset of folded cascode amplifier

## Noise of folded cascode

The only difference with respect to the telescopic comes from the new devices M9 and M10. These contribute some extra noise. All the other devices contribute the same.

This is the noise contribution of M9 and M10:

![image](https://user-images.githubusercontent.com/95447782/175026926-29ddf8f5-652d-4d77-b6fc-96c16d72d448.png)


This is the overall noise contributions:

![image](https://user-images.githubusercontent.com/95447782/175026940-5b431fcb-1d9d-445b-bfd9-4c7d04a9baef.png)


And this is a comparison of noise between the 5T, the telescopic and the folded cascode.

![image](https://user-images.githubusercontent.com/95447782/175026962-dee01618-41e9-4222-8a4d-ce8609069d4f.png)


## Offset of folded cascode

Like the noise, it’s the same as the telescopic except it has some extra mismatch contribution from the new devices M9 and M10.

![image](https://user-images.githubusercontent.com/95447782/175027005-b2b0ead3-0254-48a8-b0ed-b00dc897fdb0.png)


This is a comparison of offset between the 5T, telescopic and folded cascode op amps:

![image](https://user-images.githubusercontent.com/95447782/175027024-1bc20d2b-37d0-4774-8a39-a9e02b312596.png)


Note, a brief recap so far shows us that the folded cascode, with respect to the telescopic, has so far only got slightly worse results than the telescopic:
* the extra devices M9 and M10 reduce DC gain because they add extra conductance in parallel so higher Gout or lower Rout so lower DC gain
* the extra devices M9 and M10 add some extra noise
* and some extra offset


Next is Slew Rate.


## Slew Rate

Next:

* [Slew Rate](/Slew_Rate_analysis.md)
