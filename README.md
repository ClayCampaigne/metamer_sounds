# metamer_sounds
To use:
click the binder link below, wait for the binder site to launch, then open the "metamer_sounds.ipynb" notebook (not sure why I can't get a link directly to the notebook working).

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ClayCampaigne/metamer_sounds/HEAD)

Click the "kernel" menu, and select "restart and run all". Then you can adjust the wavelength and amplitude sliders in the widget at the bottom.
To re-initialize the widget to the starting state, you can click the code cell above the widget display, and type command (or control) enter.

This is a hobby project motivated by my dream of "auralizing," or "hearing," the difference between metamers. 
(I've always found the dimensionality and structure of perception to be interesting.)
Metamers are distinct EM (light) spectral power distributions with the same perceived color.
Color space is 3-dimensional, but tone is essentially infinite-dimensional, due to the respective structures of the sensory organs.
That means that there are, like, infinitely times more tones than colors. 
There is pure, monochromatic yellow of wavelength approximately 590 nm, and there is yellow created by mixing green and red light. 
These look identical, at least holding ambient light and surrounding stimuli constant. 
But if you map the respective spectral distributions to tones, the metamers would sound different. 
(The yellow part of the EM spectrum is exceptionally narrow though, as far as I can tell.)

Another notable difference between color and tone space is that there is not really a question of "perfect color" perception, as there is with perfect pitch, except perhaps in philosophy. 
People can be incapable of learning the mapping between a sound signal at 440 Hz and the concept "middle A," but they can easily learn (and never forget) the mapping between a wavelength of 700nM and the concept "red."

In any case a widget is provided with sliders that independently control the wavelength and amplitude of three pure sinusoidal signals.
Light wavelengths are in nM, and sound is in...1000-Herz, for the moment.
The sum(s) of these signals are mapped simultaneously to a visual (color) representation and an aural (tone) representation. 
For the colors, we also show the components and the pairwise sums. 
Colors (components and sums) are computed using `python-colormath` and displayed in a Venn diagram plotted with `matplotlib-venn`. 


The nature of interaction is quite janky, but c'est la vie. 
Every slider event makes a static matplotlib-venn plot, and also freshly creates an autoplaying IPython Display Audio widget.
BQPlot would be preferable, but that gets complicated, and in particular one would need to re-implement the matplotlib-venn packge that I rely on for the plots.
Making the sound stuff properly interactive seems at least as complicated.

