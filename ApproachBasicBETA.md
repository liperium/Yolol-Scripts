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

## [Code](src/ApproachBasicBETA.yolol/)
<!--MARKDOWN-AUTO-DOCS:START (CODE:src=./src/ApproachBasicBETA.yolol) -->
<!-- The below code snippet is automatically added from ./src/ApproachBasicBETA.yolol -->
```yolol
l=0 :approach=0 :FCUForward=0 :FCUBackward=0
sm=0.05 dt=15 p=150 ms=12 IF:approach THEN:range=1 GOTO3ENDGOTO2
IF:rfd<(dt+0.5) AND:rfd>(dt-0.5) THENl++ ELSEl=0 END IFl>8THENGOTO1END
t=:rfd x=(t-dt)*sm IFx<ms AND x>0 THEN:FCUForward=(t-dt)*sm GOTO2END 
IF x>0 THEN :FCUForward=ms ELSE:FCUBackward=-x*p END GOTO2
```
<!--MARKDOWN-AUTO-DOCS:END-->