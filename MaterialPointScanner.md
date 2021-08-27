# Material Point Scanner

Scans constantly until it finds a result (or you release the button).

Shows ore contents in **stacks**.

Reads the ores in the opposite way, so you always have the core material first.

## Usage
### Naming
```
-- Button --
    Name = Scan
    Type = 1
```
```
-- Screen --
    Name = ::::MAT:::
```
```
-- Material Point Scanner --
    Active = Scan
    Index=Idx
    Result=Rslt
    Material=Mat
    Volume=Vol
    Scan=Chk
    Reset=Reset
```

## [Code](src/MaterialPointScanner.yolol/)

```
n="\n" z="Ore" x="Crystal" s=1728//1
IF :scan>0 THEN GOTO3 ELSE :chk=0 GOTO2 END
:reset=1 :::::MAT:::="" :chk=1 
IF :scan>0 THEN IF :rslt==0 THEN :chk=1 GOTO4 END ELSE GOTO2 END
:::::MAT:::="" :scan=0 :chk=0 :idx=:rslt
IF:idx-->=0 THEN:::::MAT:::+=:mat-z-x+n+(:vol/s)+n GOTO6 END GOTO2
```
