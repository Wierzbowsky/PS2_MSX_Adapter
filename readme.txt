PS/S Keyboard Adapter for MSX2 Computers
----------------------------------------

Designed by Kamil Karimov (k2k@list.ru)
Homepage: http://caro.su/

This reposity contains Gerber files as well as firmware and schematics for the PS/2 keyboard adapter for
MSX2 computers. Four different computer type are supported: Sony F500, F700, F900; Daewoo 400 and 400S;
Yamaha YIS-805 and Sakhr AX-500. All these computers have external keyboards that may be lost of damaged
beyond repaid. The PS/2 keyboard adapter is the cheapest and the most reasonable replacement for those
damaged or lost keyboards.

Mr. Karimov gave his permission to put his files into the repository. However it's not allowed to use any
of the files in this repository for commercial purposes without the permission from the author. Making a
small batch of boards, using some of the boards for personal projects and selling the remaining boards is
permitted.

The project can use either Attiny 2313 or 4313 chip. See the partslist.txt file for the information on
the necessary components. The design of the circuit board is the same for 4 variants of this adapter,
only the firmware differs.

The board needs to be programmed after assembling. We recommend to use an USBASP or clone programmer and
the special 2x3 pin adapter for programming the board. Please observe the polarity when connecting the
USBASP programmer. The AVRDUDE software that is included into the repository is configured to use the
generic USBASP programmer. If you use a different programmer, you may need to adjust the batch files
accordingly. The programmer must be connected to the X1 connector.

The FUSES.txt file contains information on how to set correct fuses for 2313 or 4313 chip. Normally,
the AVRDUDE software takes care of this itself, but in case your programmer needs to set fuses itself,
please see the file for reference.

The DIN-13 connector that is used to connect the PS/2 adapter to an MSX2 computer has different pinouts
for different computers. Please see the connection diagram for each computer in the Schematics folder.
As most of the currently sold DIN-13 connectors are machined and not suitable for soldering, it's
recommended to use female-to-female jumber wires to connect the 14-pin header to the DIN connector. For
that, the plastic cover should be removed from one side of the wire and a shrinktube of matching size
should be put onto the terminal. Then the terminal's end should be slightly widened to fit onto the
machined end of the DIN-13 connector. That's the only reasonable way to wire up the connector. There's
an alternative - to buy the already wired connector and cut its cable in half.

DIN-13:
Din Plug 13 Pin Male Inline Audio Adapter Connector
https://de.aliexpress.com/item/1005006533940348.html

Jumper wires:
10/40PIN Cable Dupont Female to Female Jumper Wire
https://de.aliexpress.com/item/1005004647016228.html

DIN-13 cable (option):
1M/3M 13 Pin to 13 Pin DIN CD Changer to Head Unit Extension Cable for Kenwood Tuner
https://de.aliexpress.com/item/1005004895215380.html

For the Yamaha YIS-805 MSX2 computer there exist 2 different firmwares - kbd2yis805_SU.hex where a user
needs to press the Shift key to type numbers and the kbd2yis805_RU.hex where numbers are typed without
the Shift key.

The Gerber files for the board with LEDs is not provided as this is an optional part. But there's a
scematics in the Schematics folder that shows how LEDs should be connected to the board (X4 connector).

PS/2 keyboard layout for Yamaha YIS-805 and Sakhr AX-500:

; SELECT   - F11
; STOP     - F12
; CLS/HOME - Home
; INS      - Ins
; DEL      - Del
; GRAPH    - Alt left or right
; PYC      - Scroll Lock

PS/2 keyboard layout for Sakhr AX-500:

; SELECT   - F11
; STOP     - F12
; CLS/HOME - Home
; INS      - Ins
; DEL      - Del
; GRAPH    - Alt left or right
; CODE     - Scroll Lock

PS/2 keyboard layout for Sony F500, F700 and F900 series:

; SELECT   - F11
; STOP     - F12
; CLS/HOME - Home
; INS      - Ins
; DEL      - Del
; GRAPH    -  Alt left or right
; CODE     -  FlyWin left or right
; DEAD     -  Scroll Lock

PS/2 keyboard keys for Daewoo 400 or 400s:

; SELECT   - F11
; STOP     - F12
; CLS/HOME - Home
; INS      - Ins
; DEL      - Del
; GRAPH    - Alt left or right
; CODE     - Scroll Lock

Please note that Korean, Japanese or Arabic character maps may be inaccurate because there was no way to
verify the input without knowing any of those languages. The main purpose of this adapter is to provide
basic keyboard functionality (Latin characters, numbers and special symbols with Graph). Anomalies and
bugs should be reported to RBSC (info@rbsc.su).

The video that shows how the keyboard adapter works could be found here:
https://www.youtube.com/watch?v=sjwlw_10PEQ

IMPORTANT!
The commercial usage of this project is not allowed without the permission of the author! There's no
guarantee of any kind for the provided material and the author must not be held responsible for any
possible use or misuse of the adapter as well as for any possible damages.
