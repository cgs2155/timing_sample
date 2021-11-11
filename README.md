# timing_sample

This is sample code for the DESRES internship
Unfortunately there is very little code I am allowed to
release at a time so I wanted to provide a sample of what I usually do

What happens is:

I download an event file containing data of photon arrival times
from a particular binary system, in this case a white
dwarf binary. That will allow me to produce a graph called
a light curve which shows how many photons arrvied at a particular time.
That data is then fourier-transformed to produce power spectrums which
gives the phase of the arriving photons. Frequencies where the most
photons are in phase are peaks and typically model physical phenomena
like orbital or spin periods. Then I run a variety of statistical tests
in different energy bands (e.g. only looking at photons a .2 - 3 keV).
The most useful is the Z^2 Test which can be found under the heading Z^2 
Test in the timing file. This assigns z-scores to significant frequencies
and if they're above the 5-sigma line, they are accepted as physical phenomena
and not background noise.

The code I would like to highlight is the Lomb-Scargle bootstrap. This is section
provides the error of my frequency approximation. Essentially, the peak is a guess of
what the spin period of a white dwarf may be, but the bootstrap, a Monte-Carlo methods, 
tells me that it can be any frequency in a certain range around it.
