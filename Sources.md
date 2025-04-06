# DIY ECG with AD8232 and Sound Card

**from: https://www.youtube.com/watch?v=sP_-f5nsOEo**

*what you're seeing on the screen is my
actual ECG signal being displayed and
analyzed in real-time using this device
and if you look at it closely you can
see the blue light flashing in
coordination with my heart beating in
this video I'm going to discuss how I
made this device it's based on an ad ad
232 breakout board which amplifies the
electrical signals coming from my heart
it then sends them to the computer
through the microphone jack of my sound
card I'm going to show how I wrote
custom software to analyze the signals
coming in the sound card and do
Reutimann straight heartbeat detection
now before we go into the details of how
this device is made let's talk about
what it is that ECG machines actually
measure when the heart contracts its
chambers and one-way valves help push
blood around the body the top chambers
called atria squeeze to load the
ventricles with blood the ventricles are
much stronger and when they contract
one-way valves between the atria and
ventricles slam shut and the ventricles
squeeze blood throughout the body if you
put your head up to someone's chest and
you hear their heart beating as lub dub
lub dub well you're actually hearing is
those one-way valves slamming shut as
the ventricles contract and relax
different regions of the heart have to
contract in the right sequence for the
heart to function properly this
contraction is controlled by neurons at
a high level the heart is generally
controlled by the brain excitatory and
inhibitory messages travel down nerves
from the brain to the heart but they
don't actually tell the heart when to
beat
individual heart beats are controlled by
little clusters of neurons called
ganglia which live on the heart itself
the SA node in AV node are ganglia which
control the timing and strength of heart
beats in the atria and ventricles these
intrinsic cardiac ganglia have what it
takes to beat the heart on their own
this is why if you remove the heart it
will continue to keep beating for a
while when the brain controls cardiac
output it does so by relaying messages
to the intrinsic cardiac ganglia the
cardiac ganglia then send chemical
signals to cardiomyocytes the muscle
cells in the heart telling them when to
get tracked contraction is achieved to
encar do myocytes
open sodium and calcium channels
allowing positive ions to rush inside
the cells it's this flow of positive
ions into muscle cells that produces the
electrical signal we can measure with an
electrocardiogram the large spike you
see on an ECG is the electrical activity
associated
ventricular depolarization and the
little hump before it is when the atria
depolarize now electrocardiography is
its own branch of medical science but
for the purposes of this video we've
described enough to be able to
understand what it is we're looking at
when we see an ECG signal let's go back
to talking about the adat 2:32 analog
devices announced the ship in 2012 and
it was really convenient because it was
so simple and it's very low-power but
it's a little bit difficult to work with
because it's so small it has 20 pins and
it's only 4 millimeters by 4 millimeters
in the last few years though a lot of
different companies have been making
breakout boards for them and in recent
years these breakout boards have become
extremely inexpensive and easy to obtain
I don't remember exactly where I got
mine but I'm pretty sure it was an ebay
atom like this large quantities of
disposable electrodes are also cheap on
eBay is worth noting that similar
devices can be found on Amazon and more
officially unspread fun although you'll
have to purchase the cable and pads
separately for an additional fee if you
decide to make an ECG machine based on
the adat 232 i recommend getting some
high quality electrodes now mine came
with a little plug here and snap
electrodes and these are really
inexpensive online you can get bags and
bags or these electrodes and let's take
a closer look here focus there we go so
that's what an electrode looks like and
you can pretty easily snap it like that
and it peels and it reveals a goop
now that goop in the center is silver
chloride gel that makes a really good
electrical connection with your body so
if you put this on your body it's going
to get a really high quality signal with
low noise so I recommend definitely get
these don't skimp on the electrodes
because your signal will be a lot
noisier this is the adat 232 breakout
board to get started we need to supply
power at 3.3 volts I prefer using a
linear voltage regulator hooked up to a
9-volt battery
and although this configuration isn't
power efficient it's simple and small
and a good place to start definitely use
a battery instead of a power supply
because it is safer and it's usually
lower noise to
the electrodes could be soldered
directly to the board but I prefer using
the built-in audio jack let's take a
moment to discuss where to place the
electrodes
now electrode placement is actually
pretty important because it affects the
shape of the ECG signal now is a good
time to note that technically this is a
single lead ECG because it only measures
the voltage between two electrodes with
the third electrode being ground
therefore this system is a three
electrode single lead ECG system let's
take a moment to talk about placement
ideal placement looks like this with
electrodes typically labeled ra and la
for right arm and left arm and ll for
left leg although you can put these
electrodes on your arms and legs ideal
position is on your chest forming a
right triangle around your heart
placement in different locations will
change the shape of the ECG signal as
different muscle groups are being
measured there are international
standards which define ECG electrode
color codes but if you're going to get a
cable from this a mysterious vendor on
the Internet you can't always rely that
they're accurate so it's probably
worthwhile to use a continuity meter to
beep out your connections and make sure
you're connecting the right electrodes
to the right part of your body with the
circuit powered up and the electrodes
and the right spot on your body you can
use an oscilloscope to see the ECG
signal coming right off the breakout
board to feed the signal into a computer
using the sound card use a socket or a
creative soldering to connect it to a
stereo cable and then plug the other end
into the microphone jack of your
computer sound card I prefer to short
the left and right channels together
because I can't always be sure if the
computer software is going to average
the left and right channels together or
just raw data from the left channel this
may be all you need to get started
visualizing your ECG with a computer but
in my case I found that my PC sound card
was too sensitive and the output signal
from the breakout board is too large do
you reduce the size of the signal you
could use a resistor divider or a
potentiometer okay I've already put on
two of the three this is a third one
I'll peel off the backing and I'm gonna
put it on my upper chest on the left
side kind of like right there and we
should see the signal start to stabilize
and there's the ECG coming through
this is the device I'll packaged up in a
nice enclosure let's take a closer look
and see what we have on the front
there's a power LED which also doubles
to serve as the output of the ECG signal
we also have a stereo connector here but
it's not to connect to the computer
sound card instead this is what I use to
plug in the ECG chest electrodes - so
these wires go up to my chest on the
back we've got a few things we've got a
barrel connector which can be used to
supply DC power and in this example I'm
just using a 9v battery with a little
barrel jack attached to it so it's
really convenient I'll just plug that in
and when I do the light starts coming on
solid in the front to indicate we have
power I also have an SMA connector where
I output the voltage coming directly off
of the chip so this lets me access the
actual voltage coming off the ECG
amplifier but oftentimes this is too
strong and it can overwhelm the
microphone jack of your sound card so as
a result I added a voltage divider to
bring the signal down to microphone
audio levels and that's what comes out
of this this is a one-eighth inch female
stereo adapter and I can plug in a cable
like this one that goes to the
microphone jack of my computer sound
card and we can analyze the signal that
way let's take a look on the front of
this device and I'll plug in my chest
leads and pretty much right away you'll
be able to see a heartbeat coming
through and again the the solid blue
light and the kits has power but this
device has been modified so that it also
fluctuates the light tend to get the
artbeads so let's take a look inside and
see how it works right now I've got it
hooked up to my chest which is why the
blue light is flashing in coordination
with my heartbeats we can open it up and
you'll see that I have a little more
here than is necessary but it adds a few
features that I might find useful in the
future on the left you can see the adat
232 breakout board and it has its own
little light that beats when my heart
beats on the connector
has the whole job through so I can
easily access it from the front panel
and the only three connections going to
the main board are ground power 3.3
volts in the output signal let's quickly
talk about the power chain it's actually
super basic on the right side of the
board where the barrel connector is
power comes in here and then it runs
into this LD 3 3v linear voltage
regulator to bring it down to 3.3 volts
I added a zero point 1 micro farad
decoupling capacitor on the input and
the output and also a 10 micro farad
capacitor on the input and the output
just for good measure
there's a little power indicator LED and
yeah and that's bringing pretty much all
we need for the power supply now rather
than take the output of this chip
directly and send it right out the SMA
connector I decided to use an
operational amplifier to help buffer the
signal a bit so this is an LM 324 being
powered from the nine volts coming in
here it's not being powered from the 3.3
volts but the output of the signal is
going straight into one of the inputs
and it's configured in inverting unity
unity gain configuration so really it's
just acting as a voltage follower and
it's serving the purpose of a buffer in
this circuit I use a bit of a voltage
divider here to mix the output of that
buffered signal in with the power supply
voltage to supply signal to my LED
that's what lets the LED be always on
sort of glowing gently blue but then to
have large up-and-down fluctuations
based on the heartbeat the output goes
to the SMA connector and then from there
it goes through a voltage divider to go
to the stereo jack let's hook this up to
the oscilloscope so we can see what the
signal looks like I'm going to ground it
to the cage and then probe the output of
the voltage follower buffer here and we
can take a look
I've seen some tutorials and videos out
there demonstrating how to analyze the
ECG from an ad 8230 to using a computer
and a complicated chain of an ADC
running on an Arduino sending serial
values over USB with a USB to serial
adapter and it's kind of complicated and
although it works I think that using the
microphone jack is a really interesting
idea because it's so simple I mean
everybody has one and it requires no
special hardware so I wrote some Windows
software specifically for this project
to make it easy for anyone to visualize
their ECG signal and also to perform
rudimentary heartbeat detection now this
software is really easy to use you just
click it and it runs and it's fully open
source on github so anyone can have a go
at improving it any way they like you
can find it by googling the phrase sound
card ECG all one word or by using the
link in the description one of the
things I wanted to mention is that it's
been a while since I've shared a project
online and that's because I have
undergone some pretty serious medical
treatments recently my last video about
bit banging spi devices with FTDI chips
was supposed to be a two-part video but
shortly after I filmed part one I got
started with chemotherapy and I actually
tried to film part two while undergoing
chemotherapy but I was always too sick
to actually get it done since then I've
done radiation treatment and pretty soon
I'm going to be starting more
chemotherapy and if anyone's interested
in following the progress of my medical
treatments I've set up a special website
where anyone can check out the latest
and there's a link to that in the
description so with that being said it's
a little bit hard to predict when I'm
gonna share my next project but I still
have some pretty good ideas for future
directions I'd like to go with this ECG
circuit you might have noticed that the
output has a connector where I can get
the unattenuated signal directly off the
chip and there's a good reason for that
it's because there are several ways of
this project could go in the future to
extend the functionality of the circuit
so let's run through a few of those one
of my future goals is to use a circuit
to detect heart rate that doesn't
involve computer and in order to design
circuitry to detect heartbeats I found
out really convenient to actually make a
circuit that generates heartbeats rather
than having to
an ECG electrode every time I want to
practice detecting my heartbeats
so I did that here this is a five five
five in the configuration that produces
one square pulse about once a second and
it runs through a combination of
resistors in the series capacitor to
make it look somewhat like a QRS complex
now that's centered around zero volts so
I used Ln through 24 quad op amp to add
a standing DC voltage to that and then
but for the output signal in an
inverting configuration because out of
the five five five it is always high and
then it just dips low very quickly and
it ended up making it appear that the
ECG signal was upside down but anyway
now it's inverted in buffered I have
coming out of this wire a signal that
actually looks an awful lot like an ECG
so I can practice doing event detection
or qrs detection this is the circuit I
came up with to do really rudimentary
QRS detection the output is here in the
core idea is that it turns this ECG
signal so this light indicates the ECG
it's a standing voltage around two volts
and you can see the light fluctuating as
the ECG occurs this circuit detects this
ECG signal and turns it into a square
wave the reason why I want to turn into
square wave is because it's really easy
to measure the period of square waves
using for example a timer on a
microcontroller
I'd much prefer to do that rather than
use an analog to digital converter to do
high-speed measurements to measure the
actual shape of an ECG signal and they
try to do calculations on that if I can
make a little analog circuit that
converts the ECG signal to a square wave
it's much easier to do heart rate
detection and potentially you could even
do it all analog or at least mostly
analog nothing fancy but having this
synthetic circuit to generate an ECG
signal was really convenient in testing
out different signs for this this method
uses a fixed voltage detection so
anytime the voltage goes above the
voltage set by this potentiometer this
light flashes is this capacitor charges
or discharges and then the square wave
is produced but one of the ways this
circuit could be improved is by using
the equivalent
automatic gain control where the voltage
on the potentiometer always lowers until
it starts detecting heartbeats and then
the heart beats kind of keep it going
that way even if the amplitude of
heartbeats change or the amplitude of
the QRS complex changes it can still
automatically adapt to detect heartbeats
and convert them in square pulses so
this is a really rudimentary first step
but indicates a lot of future directions
of this project could go especially for
people who are just getting into
electronics or want to have a practical
application to practice designing analog
circuits when compared to some of the
other ECG circuits have made over the
years working with the ADEA 323 is one
of the easiest ways to get started that
I've experienced so if you're new to the
world of electronics or this is the
first ECG machine you've built
definitely start with this chip and
you'll have a pretty easy experience if
you build something cool let me know
about it I'd love to see what you come
up with my email address is on my
website and if you're interested in this
project and will I see more like it you
can see all of my projects on my website
and that's SW hardened com*
