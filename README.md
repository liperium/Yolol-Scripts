# Yolol-Scripts
## These are all scripts made by me. Hope they can be usefull to you commanders out there. 🚀

**I am currently re-structuring the database to make it more user friendly. Sorry if stuff seems out of place.**

✨ : Favorites

---
## Mining ⛏

### - [Material Point Scanner](/MaterialPointScanner.md/) ✨
 
<!--MARKDOWN-AUTO-DOCS:START (CODE:src=./src/MaterialPointScanner.yolol) -->
<!-- The below code snippet is automatically added from ./src/MaterialPointScanner.yolol -->
```yolol
n="\n" z="Ore" x="Crystal" s=1728//1
IF :scan>0 THEN GOTO3 ELSE :chk=0 GOTO2 END
:reset=1 :::::MAT:::="" :chk=1 
IF :scan>0 THEN IF :rslt==0 THEN :chk=1 GOTO4 END ELSE GOTO2 END
:::::MAT:::="" :scan=0 :chk=0 :idx=:rslt
IF:idx-->=0 THEN:::::MAT:::+=:mat-z-x+n+(:vol/s)+n GOTO6 END GOTO2
```
<!--MARKDOWN-AUTO-DOCS:END-->

### - [Mining Laser Pulse](/MiningLaserPulse.md/)
<!-- 
### - []() 
-->

## Movement 🛸

### - [ISAN V2](/src/IsanV2.yolol/) This is a copy paste from official source
### - [Approach Basic](/ApproachBasicBETA.md/)
<!-- 
### - []() 
-->

## Energy ⚡

### - **Generator Efficiency** = [Basic](/src/GeneratorEfficiencyBasic.yolol/) ✨ | [Advanced](/src/GeneratorEfficiencyAdvanced.yolol/)
<!-- 
### - []() 
-->

## Combat 💥

### - [Missile Launcher](/MissileLauncher.md/)
### - [Automatic Gun Firing](/src/AutoGun.yolol/) 
<!-- 
### - []() 
-->

## General 💡

### - [Information Display](/src/InformationDisplay.yolol/)✨
### - [Ship Diagnostic Scanner](/ShipDiagnosticScanner.md/)
<!-- 
### - []() 
-->
---
# If you have any questions Discord 👾 Liperium#7591