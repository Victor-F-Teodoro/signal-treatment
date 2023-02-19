# signal-treatment

This code makes the indentification of the frequencies of a signal composed by sinusoids. Two methods are utilised: the [FTT](https://en.wikipedia.org/wiki/Fast_Fourier_transform) and the [Burg parametric algorithm](https://pyspectrum.readthedocs.io/en/latest/ref_param.html). 

The sinusoid's frequencies change through time, and when the signal's frequencies cross, we can make an analysis, through the level is the intensities, how was the evolution of the two sinusoids during the crossing.

![img_1_gh](https://user-images.githubusercontent.com/117582978/219874445-357fab54-5abf-459a-97f6-a544a488737b.jpeg)

 When the frequencies have a similar value, for example f1 = 400 hz and f2 = 405 hz, the FFT method can't differentiate the frequencies and return a unique value.

![img_2_gh](https://user-images.githubusercontent.com/117582978/219874447-8c682ebf-86b9-43c0-84e3-a18eac067a51.jpeg)

To solve this problem, we implement the Burg parametric algorithm, which utilises autoregression instead of the Fourier Transform. With the right set of parameters, the Burg method can tell the frequencies appart at every instant of time.

![img_3_gh](https://user-images.githubusercontent.com/117582978/219874565-53d987fe-6e95-47c3-a307-eb2123e336e4.jpeg)


The library numpy was utilised for the FFT and the  the burg algorithm was implemented through the [Spectrum](https://pyspectrum.readthedocs.io/en/latest/index.html) module.
