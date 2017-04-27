# Project 1
## Vacuum-cleaning World

### Specifications

A vacuum-cleaning robot moves around a 3x3 grid

It either moves one step forward or turns right 90°

Find a deterministic, memoryless strategy for the robot in which

* its next action only depends on its current square and orientation (north, south, west, east)

* all squares are visited infinitely often

We ignore actions of vacuuming and only focus on actions of movement

Rules given by Wooldridge

* if IN(0,0) and FACING(north) then DO(forward)
* if IN(0,1) and FACING(north) then DO(forward)
* if IN(0,2) and FACING(north) then DO(turn)
* if IN(0,2) and FACING(east) then DO(forward)

According to Wooldridge similar rules can easily be generated that will get the agent to (2,2) and once at (2,2) back to (0,0)

### Task

Model above scenario and determine using Uppaal whether Wooldridge's claim is true. If so, find other rules.

Then verify using Uppaal if there is a (shorter) strategy meeting Wooldridge criteria that follows above given rules for (0,0) and (0,1). If so, find the other rules.

Next use Uppaal to find if there is a (shorter) strategy meeting Wooldridge's criteria that follows previous rules for position (0,0). If so, find the other rules.

Finally, assume that the robot is very fast at turning but slow moving. Turning 90° takes 1 unit of time while moving forward takes 5 units of time. Can you find the *fastest* strategy for the robot that follows the above-given rule for position (0,0) and visits each square? Is there a fastest or shortest strategy that assumes no preset rule?

### Deliverables

ZIP file containing

* PDF report describing the model of the vacuum-cleaning scenario in Uppaal, the queries used to determine the answers to the above-stated questions and the results of the verifications. Make sure that you include clear pictures describing visually the strategies you found using Uppaal

* The files for your Uppaal models and queries