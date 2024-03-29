# m3pi-Line-Following
This repository contains the code for a line following program implemented onto a Pololu m3pi Robot (note: mbed.zip is to be expanded).

The program uses analog sensors which detects light reflection and converts that to workable, digital data. The two different feedback controllers I experimented with for this project are:
1. Bang-Bang
2. Proportional Integral Derivative (PID)

After much experimenting, I decided using PID was better for this project. This is because PID tends to have a much smoother movement compared to Bang-Bang.

In PID, when the m3pi robot turns, it turns at a speed proportional to margin distance of error. If there is an external force or environment acting on the m3pi robot, the program measures the integral error and acts accordingly. Similarly, if there is an alignment or directional error, the program calculates the rate of change of the error (derivative) and acts accordingly in order to go back into place. Thus, when travelling down a narrow pathway, it is much more efficient than the Bang-Bang movement.
