# Notes

```xml
<config>
  <!-- Ran into this on forums:
  ambientInsideSpeed = 0.2 for slow transition
  ambientInsideThreshold = 0.1  so that it works so that there are fewer transitions back and forth.
  ambientInsideEquatorScale = 0.6 to reduce the difference in lighting
  -->

  <!-- How much light the moon gives off?
    do not know what the setting *is* just setting it to 1 makes indoors darker, mostly
  -->
  <!-- a19,a20,a21 Default: .2 -->
  <!-- NOTE: Used to have this set to 2 in older version of a19 and it worked well -->
  <set xpath="/worldglobal/environment/property[@name='ambientInsideThreshold']/@value">0.1</set>

  <!-- slow transition when going inside -->
  <!-- a19,a20,a21 Default: .3 -->
  <!-- NOTE: Cannot see a difference in vanilla game? tried  0.1 -> 1 -->
  <!-- NOTE: Seting to 0.01 seems to break the effect, no dimming at all-->
  <!-- NOTE: Also Seems to work in reverse, like a light turned on in dark room takes time to light, then off taes time to dim
  also going outside takes time to brighten, in ful daylight-->
  <!-- NOTE: .1 = super slow transition, 2 = super fast.  Having it super fast screws up when you
  cross a boundary, like it goes from "I can see the entire inside of a room, to nope I cannot." -->
  <set xpath="/worldglobal/environment/property[@name='ambientInsideSpeed']/@value">.4</set>

  <!-- when its determined your inside? -->
  <!-- a19,a20,a21 Default: .2 -->
  <!-- NOTE: Cannot see a difference in vanilla game? tried  0.1 -> 1 -->
  <!-- <set xpath="/worldglobal/environment/property[@name='ambientInsideThreshold']/@value">0.1</set> -->

  <!-- WARNING: Setting thse too low (like 0.01) makes it way too dark when its full day outside
   it literally looks wrong, like light cannot throw shadows-->

  <!-- difference in lighting from inside/outside? -->
  <!-- a19 Default: .4 -->
  <!-- a20 Default: .5 -->
  <!-- a21 Default: ".55, 1.5" = day, night -->
  <!-- ran a test and 1 = gets lighter indoors ?-->
  <set xpath="/worldglobal/environment/property[@name='ambientInsideEquatorScale']/@value">0.3,0</set>

  <!-- a19 Default: .3 -->
  <!-- a20 Default: .4 -->
  <!-- a21 Default: ".2, .2" -->
  <set xpath="/worldglobal/environment/property[@name='ambientInsideGroundScale']/@value">0.1,0</set>

  <!-- a19 Default: .6 -->
  <!-- a20 Default: .7 -->
  <!-- a20 Default: .2, .4 -->
  <set xpath="/worldglobal/environment/property[@name='ambientInsideSkyScale']/@value">0.2,0</set>


  <!-- my outdoor edits -->
  <!-- <property name="ambientEquatorScale" value=".7, .45"/> -->
  <set xpath="/worldglobal/environment/property[@name='ambientEquatorScale']/@value">.3, .15</set>
  <!-- <property name="ambientGroundScale" value=".3, .05"/> -->
  <set xpath="/worldglobal/environment/property[@name='ambientGroundScale']/@value">.1, .005</set>
  <!-- <property name="ambientSkyScale" value="1, .7"/> -->
  <set xpath="/worldglobal/environment/property[@name='ambientSkyScale']/@value">.7, .4</set>
  <!-- <property name="ambientSkyDesat" value=".7, .7"/> -->
  <set xpath="/worldglobal/environment/property[@name='ambientSkyDesat']/@value">.45, .3</set>

</config>
```
