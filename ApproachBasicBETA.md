# Approach Basic

Makes your ship go to a certain distance from an object, using a rangefinder. 

Note - (This is the basic version, it has constants in it. You need to fine tune them. **DO NOT PRESS GAS WHEN IN RANGE**)


## Usage
### Naming

RangeFinder name="ra", distance="rfd"

Button name="Approach", type=1

### Constants

Speed modifier - **sm**  ( lower is safer and test for every ship)

Target Distance - **dt**

Activation Distance - **p**

## Code

```
sm = 0.07 dt = 30 p=-90 :ra=:approach GOTO 1+:approach
t=:rfd IF:approach>0 AND :rfd<200 THENGOTO3ENDGOTO1 s=(t-dt)*sm IFs>50
THENs=50 ENDIFs>0 THEN:FCUForward=s ELSE:FCUBackward=s*p ENDGOTO2
```
[Source](src/ApproachBasicBETA.yolol/)