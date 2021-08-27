# Missile Launcher

Shoots missiles one by one.

Reset button lets you refill the launcher.

Has a screen so you can see how many missiles are remaining.

## Usage
### Preparation

Make sure your missiles are built correcly and that they are locked from the fuel tank.

### Naming
```
-- Button --
    Name = ShootM
    Type = 1
```
```
-- Button --
    Name = ResetM
    Type = 1
```
```
-- Progress Bar 12x24 --
    Name = MissilesLeft
    MinValue=0
    MaxValue=9
```
```
-- Missile Launcher --
    Selected Tube = ST
    LaunchMissile = LaunchM
```

## [Code](src/MissileLauncher.yolol/)
<!--MARKDOWN-AUTO-DOCS:START (CODE:src=./src/MissileLauncher.yolol) -->
<!-- The below code snippet is automatically added from ./src/MissileLauncher.yolol -->
```yolol
:LauncherLock=0 x=10 :MissilesLeft=0
:MissileLock=1 :LauncherLock=1 :ResetM=0 f=0 :ChipWait=6 i=1
IF ++f<x THEN IF :ML=="Locked" THEN:MissilesLeft++ ENDGOTO3 END GOTO5
i++ :ShootM=0 IF --:MissilesLeft<1 THEN GOTO6 END
IF :ResetM THENGOTO1END IF:ShootM THEN:ST=i :LaunchM=1 GOTO4ENDGOTO5
IF :ResetM THENGOTO1END GOTO6
```
<!--MARKDOWN-AUTO-DOCS:END-->