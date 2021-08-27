# Ship Diagnostic Scanner

Makes all of the outputs fit on one display.

## Usage

### Naming
```
-- Button --
    Name = Diag
    Type = 1
```
```
-- Diagnostic Scanner --
    Active = Diag
```
**Optional. You can set Diag to 1**
```
-- Button -- 
    Name = Diag
    Type = 1
```

## [Code](src/ShipDiagnostics.yolol/)

```
x="Scanner OFF" w="WarpClass: \n" d="D-Errors: \n" n="\n"
IF:diag THENx=:WarpClass+n y=:DurabilityErrors :Diagnostic=w+x+d+y END
IF:diag==0 THEN:Diagnostic="Scanner OFF" END GOTO2
```