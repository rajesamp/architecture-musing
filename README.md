# Rajesh Sampathrajan's architecture-musing

## Jargon buster

* Immutable means unchanging. Usually used in reference to resources like a docker image, once it's uploaded it should stay there and remain available from the same reference but you can revert to it etc. 
* Idempotent means you get the same output everytime you run something. 2+2 is idempotent x+2 isn't. Very often CI/CD pipelines are not designed to be idempotent, they may do some kind of operation that means everytime it runs the output changes. That creates problems in your software release flow.

* Declarative means you have a description of your desired outcome and some kind of controller attempts to achieve that. Imperative means you give a specific instruction. 
For example, I have a thermostat, I declaratively specify that I want the temperature to be 68 degrees. The termostat will run the A/C, turn on the heater, do whatever it needs to try to keep the temperature where I specified.

* Imperative would be if I made a schedule that said "turn on my furnace for 15 minutes at this time". Then the furnace will turn on even if it's way too hot. If the power went out when it was suppose to turn on, it won't turn on after the time I scheduled etc.

* Kubernetes manifests are declarative, you specify how many containers you want running and their policy for starting and health etc.
