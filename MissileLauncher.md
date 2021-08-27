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

## [Code](src/MissileLauncher.yolol/)

```
:MissileLock=1 :LauncherLock=1 i=0 :ResetM=0 :MissilesLeft=10
i++ :ShootM=0 IF --:MissilesLeft<1 THEN GOTO5 END 
IF:ResetM THENGOTO1END IF:ShootM THEN:ST=i :LaunchM=1 GOTO2ENDGOTO3

IF:ResetM THENGOTO1END GOTO5
```
