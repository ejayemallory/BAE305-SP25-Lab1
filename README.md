# Laboratory Report for Lab 1 of BAE305 Spring 2024
# Lab 1 – Well-Equipped
* By: Carlos Jarro and Anna Conda

# Summary
Lab goal; summary of work performed; summary of outcome
The goal of this lab is to learn ... and ... . We measured ..., ..., using ..., ..., and .... Finally, we created a repository in github to store the lab reports. This report is stored in this repository as a wiki.

# Materials
List materials used in the lab (not the testing equipment, but that used to build the lab project)
4 Resistors, 4 Capacitors

# Assembly Procedures
Provide basic summary of steps performed in lab (**Do not copy and paste from lab assignment.**) The important part here is to provide detail that you had to develop in the lab which will be more important in later labs.
You must include Schematics, Engineering Drawings, and Programming if appropriate in this section.

1. What *YOU* did. How *YOU* did it.
2. We solder the resistors to a solder bread board.
- We set the temperature of the soldering iron to 700 &deg;C.
- We tinned the soldering iron.
- We made contact of the soldering iron, the component to be soldered, and some solder. Below is a picture.

![A test image](https://github.com/cjarro-uky/BAE305-SP24-Lab1/blob/main/20240110_100436.jpg)

Or perhaps a nicer smaller, centered image like this (using html):

<p align="center">
  <img src=https://github.com/cjarro-uky/BAE305-SP24-Lab1/blob/main/20240110_100436.jpg width=50%>
</p>


# Test Equipment
1. Fluke 87 V DMM
2. Oscilloscope Tektronix TS2012
3. Function Generator
4. Power Supply

# Test Procedures
This section deals with the method for obtaining your results. Make sure to be clear and concise such that a student next year can replicate the laboratory. How did you test the system to get your results.
* To measure the equivalent resistance we placed the DMM in terminal X of R1 and terminal X on R3.
* To measure the capacitance of the capacitor we used the DMM in mode X.

If your lab requires code then this sections should be the one that describes the code. Like this:
```c++
void recvWithEndMarker() {
    static byte ndx = 0;
    char endMarker = '\n';
    char rc;
    
    while (mySerial.available() > 0 && newData == false) {
        rc = mySerial.read();

        if (rc != endMarker) {
            receivedChars[ndx] = rc;
            ndx++;
            if (ndx >= numChars) {
                ndx = numChars - 1;
            }
        }
        else {
            receivedChars[ndx] = '\0'; // terminate the string
            ndx = 0;
            newData = true;
        }
    }
}
```
# Test Results
The results obtained for step 1.1 of this lab are shown in the table below.

**Resistor Values Table**
|Expected Value (&Omega;)|Measured Value (&Omega;)|Within Tolerance|
|----------|----------|----------|
|100K|99.89K|Yes|
|21|45|No|
   
2. The results obtained for step 1.2 of this lab are shown in the table below.

**Capacitor Values Table**
|Expected Value (&mu;F)|Measured Value (&mu;F)|Within Tolerance|
|----------|----------|----------|
|1|1.05|Yes|
|0.0002|0.032|No|

3. The code we wrote had several bugs but with some help we made it work. The values displayed for the sensor measurement were XX.XX for a physical distance of XX.XX

# Discussion
Answer every the lab questions in this section. You should do it within a written paragraph like the next one.

We were able to measure all the resistors and found out that only R5's value was not whithin the tolerance as shown in table X

Did you make any design decisions that had an impact on the results? How did they impact the results? What do the results mean?

Think about the lab exercises and make any interesting observation or analysis in this section too. Show that you learned something in this lab.

# Conclusion
Summarize what your aim was, what you did and what were the most important results. If you have any ideas or feedback about the lab you can propose them here (no complaints).

In summary, we measured the resistance using the DMM we found out that most of the resistors fell within the tolerance.
We also used a sensor and an Arduino controller to read a physical value. The error was acceptable/ too large. I think the resistance and capacitance measurements were long and repetitive, a better use of this time would have been t
