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

<!--MARKDOWN-AUTO-DOCS:END-->