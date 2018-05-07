---
layout: page
title: Summary report
permalink: /summary-report/
date: 2018-05-06
authors:
    - aleks
    - greta
    - julia
    - lorinc
---

The final concept
=================
**TODO greta**

Elements of the product
====================

Mechanical components
---------------------

### Frame
**TODO julia**

### Moving component
**TODO julia**

Electronic components
---------------------
During the project we designed and produced 4 different circuit board components. 3 of them were built for testing purposes, and the last one was built for the final product.  By the end of it, we developed a quick and straightforward workflow to make these boards. The workflow can be summarized by the following steps:

1. Idea and functional requirements towards the board. This usually involved a number of the group members.
2. Schematic design using the software *Autodesk EAGLE*. Done by Lőrinc.
3. Board layout design with *EAGLE*. Done by Lőrinc, discussed with Aleks to decide if it's possible to hand-solder.
4. Exporting the image files (using *GIMP*) and mill them in FabLab. Cleaning the board.
5. Soldering the components on the board. Performed by Aleks, following an image displaying the solder instructions made by Lőrinc.

### Bill of Materials
The following table lists the exact number of electronic components used in the product:

{:.table}
| idx | part name                    | qty. | supplier | catalog no.           | in list? |
|-----|------------------------------|------|----------|-----------------------|----------|
| 1   | Arduino Uno                  | 1    | DigiKey  | 1050-1024-ND          | yes      |
| 2   | Resistor 100 Ohm             | 8    | DigiKey  | 311-100FRCT-ND        | yes      |
| 3   | Orange LED                   | 10   |          |                       | no       |
| 4   | Blue LED                     | 10   |          |                       | no       |
| 5   | Micro servo motor            | 1    | Jameco   | 2214601               | yes      |
| 6   | 2.54 header pins             | 12   |          |                       | no       |
| 7   | Phototransistor              | 1    | DigiKey  | 1080-1380-1-ND        | yes      |

### Ambient light intensity sensor
The light intensity sensor serves as a general on/off switch for the product electronics. Thus it does not have to provide precise measurements. This is achieved by a common emitter phototransistor circuit. The design of this circuit was performed in 3 steps: [two standalone boards](/example-board/) were created for testing purposes, and the final circuit is placed on the main board of the end product.

![Phototransistor circuit](/static/img/example-board/schematic.gif)

### LED Charlieplexing
We lit the LEDs on the circuit board with the charlieplexing method. This is similar to multiplexing as it also aims for driving a number of LEDs using a small number of microcontroller pins. The following differences can be stated:

Advantages of charlieplexing:
- No need for additional ICs, such as FETs or shift register
- The number of LEDs driven is `O(n^2)` of the used microcontroller GPIO pins. The exact number is `n*(n-1)`

Disadvantages of charlieplexing:
- At a given moment, only one of the LEDs is turned on which leads to lower perceived intensity when switching between a number of LEDs
- The current flowing through the LEDs is limited by the microcontroller technology. In the case of the Arduino, it is `10 mA`

An additional problem raised with the layout designs: the charlieplexing method requires a lot of traces connecting the pins and the LEDs. It was difficult to arrange them on a single sided PCB. The automatic wiring algorithm of *EAGLE* was to good use. At first we planned to place 20 diodes on the board, but it didn't seem to be feasible, so the number has been decreased to 16.

![Charlieplexing circuit](/static/img/charlieplexing/charlieplexing_circuit_4pin.jpg)

Software
--------

### Jekyll documentation site
**TODO greta**

### Lighting pattern simulation
**TODO aleks**

### Arduino code
**TODO lorinc**

Sources
=======

**TODO lorinc** list and name all repositories and the presentation file

Personal reflection
===================

- aleks: **TODO aleks**
- greta: **TODO greta**
- julia: **TODO julia**
- lorinc: **TODO lorinc**
