# Ambika Build Checklist

# Note: for these instructions it is assumed the motherboard PCB is oriented
# such that Atmel 644p is at the lower left-hand side and legends for ICs
# are oriented t the top of footprints.

Resistors

# These four are, left to right, flanking the optocoupler with the label OK1
# with that label being right-side up at the upper left, the notch of the IC
# facing "up". 
[ ] R?? 220R
[ ] R?? 10K
[ ] R?? 220R
[ ] R?? 220R

# These seven 470R resistors are for output protection. Solder six of them in
# the pads at the bottom left of J3-J8. The final one is solder just under the
# button left of J2.

[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R

# These two 100K resistors are mounted directly below the 470R below J2.
[ ] R?? 100K
[ ] R?? 100K

# Solder a jumper to the area labeled SW right near the power inlet on the 
# upper-right of the board.
[ ] J?? 0R   # Jumper that is installed in lieu of a power switch.

# Near the rectangular hole for the display, there is a pad for a resistor
# at the top-right. The resistor is not labeled but shows a jumper lead. The
# Ambika instructions say that most displays don't need an external resistor
# for display brightness, but that Optrex displays need a 100R resistor.
# Since I don't know which display this is, I am electing to install a 51R
# resistor to split the difference. If the display is not bright enough then
# I'll remove it and install a jumper. I've opted to use a 10% R that's tan
# in color to draw attention to this change.
[ ] R?? 51R  # Note: this may need to be 0R to get correct display brightness.

# There is a resistor network labeled RN1 a the top-middle of the board. It is
# roughly between J2 and J3. Above that, there is a resistor labeled "4.7K to
# 10K". This sets gain for the mix output. The value of 4.7K or 6.8K is
# suggested if you plan to install all six voice cards. Since I do, I am going
# to go ahead and install a 4K7 resistor and make note of this for later if
# the levels are too low. As above, I will use a tan-colored, 10% resistor
# here to make it a little more obvious that the value is contended in some
# way
[ ] R?? 4K7  # Note: this may need to be 6KR to raise the output levels.

# At the upper-left of the the ATMEGA 644P (IC8) solder a pull-up resistor
[ ] R?? 10K  # RST Pull-up for theATMEGA 644P 

# To the left of the MCU, solder the 20Mhz crystal
[ ] X?? # 20Mhz Crystal for ATMEGA 644P

# Flip the board over, so that the legends are readable in the orientation.
# to the lower left of the rectangular hole for the display, there is an IC
# that may be marked IC10 but is marked IC13 on the Ambika instructions. To
# the left of that, there are locations for 7 470R current-limiting resistors
# for LEDs
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R

# Near the middle of the board (below the hole for the display) is another
# part, labeled IC11 on my PCB but labeled IC14 on the Ambika instructions.
# There are 8 470R current-limiting resistors here for LEDs.
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R
[ ] R?? 470R

# The RN1 10K resistor network has 7 pins and is located between J2 and J3.
[ ] RN1 10K

# The 4K7 trimmer used to set the display contrast. When the board is flipped
# to the side where you can read the legend for this part, it is at the upper
# left hand side of the display cutout, where we previously soldered a 51R
# resistor to set the brightness (but on the reverse side.
[ ] VR? 4K7 

# The 4148 small-signal diode near the optocoupler. It is marked D1 in the
# old official instructions and D3 on the PCB that I bought.
[ ] D? # 4148 small-signal diode used in MIDI

# 1N4001 rectifier diodes that are installed near the power section, right
# near the power connector. They are labeled D2, D3 in the official old
# instruction, but are labeled D1, D2 on my PCB.
[ ] D? # 1N4001 rectifier for power section
[ ] D? # 1N4001 rectifier for power section

# There are three more 1N4001 rectifiers to mount on my PCB they are labeled
# As D4, D6, D8. They are also labeled as such on the old official version
# of the instructions. This can be confusing because immediately to their
# right, you will be mounting 1N5819 diodes. 
[ ] D4 # 1N4001
[ ] D6 # 1N4001
[ ] D8 # 1N4001

# These are the 1N5819 diodes. The locations are labeled as follows on both
# my PCB as well as in the old instructions.
[ ] D5
[ ] D7
[ ] D9


