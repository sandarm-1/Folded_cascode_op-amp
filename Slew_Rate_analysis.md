# Slew Rate of folded cascode amplifier

## Slew Rate

Slew rate is **the maximum rate of change that you can get on the output**.

If you apply **a large enough voltage STEP at the input, large enough that it saturates the diff pair, i.e. all the current goes to one branch while the other is dry**, then the current Io will flow to the output, charging the output cap C up at a constant current, so **the voltage will rise with a slope of that current divided by C**.

That´s the Slew Rate.

To analyze the slew rate in the folded cascode we have to notice that the maximum output current will depend on whether I2 is large or small with respect to Io, i.e. whether the limiting factor is I2 or Io.

In the case where I2 > Io/2:

![image](https://user-images.githubusercontent.com/95447782/175027244-b5b65d74-1889-4bde-8958-9f2873f834da.png)


And in the case where I2<Io/2:

![image](https://user-images.githubusercontent.com/95447782/175027267-0f3401f9-7fe6-4223-96f4-3f0606adc404.png)


**We usually choose I2 to be exactly Io/2** so that I2 will be as small as possible without limiting the slew rate.

But in that case, **the power dissipation (quiescent current) of the folded cascode will be 2 x Io, so twice as much as the 5T and the Telescopic.**

Overall, the slew rate of the folded cascode op amp will be the same as the 5T and the Telescopic, but with extra power dissipation. Here is the comparison:

![image](https://user-images.githubusercontent.com/95447782/175027291-b4a45c88-d0ba-4eb4-91da-01f0d402977e.png)


Next is swing limits (large signal swing).




## Swing limits

Next:

* [Swing limits](Swing_analysis.md)



