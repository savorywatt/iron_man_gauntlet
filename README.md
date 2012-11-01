Simple project for a Halloween Costume I did in 2012
Full build details on my website http://savorywatt.com/2012/10/31/build-a-tony-stark-iron-man-gauntlet-in-a-weekend/

Build Time (including Dev time prototyping the electronics)
20 hours
Re-using code ~10 hours

Build Cost - 65$
Consumables - 25$
Electronics - 40$ (if bought new, high estimate).

Required Tools
Soldering Iron
Wire Strippers
Solder
Hot glue gun
Drill and drill bit (matches screws chosen)

Required Electronics
Accelerometer (MMA8452Q breakout board from Sparkfun)
Microprocessor (Arduino / AVR based)
Breadboard
Small perfboard / protoboard
Small Speaker
2 LEDs
2 220 Ohm Resistors

Required Hardware
1 Ethernet Cable
1 2 fore arm length peices of 1/4 inch plastic tubing/pipe.
1 RCA Cable
1 Cable TV cable
1 Antennae Cable (Wi-Fi)
A few more random cables
1 pipe clamp that fits your wrist
1 pipe clamp that fits your forearm
2 pieces of metal strip the length of your fore arm
4 Screws and nuts
A few zip ties
1 roll of electrical tape
1 ping pong ball
1 glove
1 plastic mouth wash bottle
1 can silver spray paint
1 can gold spray paint 1 4' cable organization strip (Got mine at Ikea)

Nice to haves
Heat Gun
Heat Shrink tube
Multimeter
Epoxy Resin
Super Glue


##################################

The basic outline of the program is like this

There are Four states
- Stable/Idle
- Power up
- Power down
- Fireing

During the main loop of the Arduino the program checks which state it is in and responds accordingly.

Stable - LED gentle Pulse
Power Up - LED faster pulse & Play Audio
Power Down - LED faster pulse & Play Audio
Fire - LED fastest pulse & Play Audio

In the code you can change a few things to fit your build better

Change the values from the Accelermoter that trigger a state change

int stableThreshold = 0;
int rampThreshold = 60;
int fireThreshold = 160;

Change how many seconds you want to have to hold your hand cocked back before switching to the fire state

//The amount of time in seconds that you have pass the fire threshold
float fireDelay = 1.0;


####################################

The code currently does not do the power down sound correctly, next improvement.