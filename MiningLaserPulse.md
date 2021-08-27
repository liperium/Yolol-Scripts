# Mining Laser Pulsing

Pulses two laser groups for energy reduction.

Turns on collector when pressing the button. **( "//" before ":collect=1" to remove this feature | line 3)**

## Usage

### Naming
```
-- Button --
    Name = Laser
    Type = 1
```
```
-- Mining Lasers --
 - Group 1 -
    Name = LaserG1

 - Group 2 -
    Name = LaserG1
```

## [Code](src/MiningLaserPulse.yolol/)

```
:laserG1=0 :laserG2=0 //collect=0
dist=18 IF :ra==1 AND :rfd<dist THEN:laser=1 :ra=0 :rfd=100 END
if :laser == 0 THEN GOTO2 end :collect=1
:laserG1=0 :laserG2=1 IF :laser==0 THEN GOTO1 END
:laserG1=1 :laserG2=0 IF :laser==0 THEN GOTO1 END GOTO4
```