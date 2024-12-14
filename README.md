# FSXP3D_effects_revamped
This project beginned as a revamp to `fx.landing.fx` yet it grows larger by revamping vital aircraft lightings especially nav lights, beacons and strobe



A simplest update to your old `fx.landing.fx` utilizing latest Dynamic Lighting Technology in Prepar3Dv4, V5.
no need to close source since it's "Modifiable", Use in any project is very welcome.

sadly in P3Dv4, replacing `fx.landing.fx` is not working, so please rename it to something else, then call this effect in your project as needed.
also this would not work in p3dv6 (who use it anyways?)

TL;DR
below are the code for the effect, rendering 8.5deg light beam with color temperature of 6000K and 600kcd. (If you configure correctly it won't lit your VC up)
(fyi, typical landing light beam aren't that wide, typically than 15deg vert/horiz. taxi lights on the other hand, are much wider than 30, but less than 60deg.
```
[Library Effect]
Lifetime=5
Version=2.00
Display Name=8.5deg LL 600kcd
Radius=-1
Priority=0

[Properties]

//begin cosmetics, taken from default landing.fx
[Emitter.0]
Lifetime=0.50, 0.50
Delay=0.00, 0.00
Bounce=0.00
No Interpolate=1
Rate=1.00, 1.00
X Emitter Velocity=0.00, 0.00
Y Emitter Velocity=0.00, 0.00
Z Emitter Velocity=0.00, 0.00
Drag=0.00, 0.00
X Particle Velocity=0.00, 0.00
Y Particle Velocity=0.00, 0.00
Z Particle Velocity=0.00, 0.00
X Rotation=0.00, 0.00
Y Rotation=0.00, 0.00
Z Rotation=0.00, 0.00
X Offset=0.00, 0.00
Y Offset=0.00, 0.00
Z Offset=0.00, 0.00
Pitch=0.00, 0.00
Bank=0.00, 0.00
Heading=0.00, 0.00

[Particle.0]
Lifetime=0.00, 0.00
Type=19
X Scale=0.42, 0.42
Y Scale=0.42, 0.42
Z Scale=0.00, 0.00
X Scale Rate=0.00, 0.00
Y Scale Rate=0.00, 0.00
Z Scale Rate=0.00, 0.00
Drag=0.00, 0.00
Color Rate=0.00, 0.00
X Offset=0.00, 0.00
Y Offset=0.00, 0.00
Z Offset=0.00, 0.00
Fade In=0.00, 0.00
Fade Out=0.00, 0.00
Rotation=0.00, 0.00
Static=1
Face=1, 0, 1

[ParticleAttributes.0]
Blend Mode=2
Texture=fx_2.bmp
Bounce=0.00
Color Start=255, 243, 239,128 //day
Color End=255, 243, 239, 128  //night
Jitter Distance=0.00
Jitter Time=0.00
uv1=0.00, 0.00
uv2=0.50, 0.50
X Scale Goal=0.00
Y Scale Goal=0.00
Z Scale Goal=0.00
Extrude Length=0.00
Extrude Pitch Max=0.00
Extrude Heading Max=0.00
//end cosmetics

//begin actual dynamic light
[Emitter.1]
Lifetime=0.50, 0.50
Delay=0.00, 0.00
Bounce=0.00
No Interpolate=1
Rate=1.00, 1.00
X Emitter Velocity=0.00, 0.00
Y Emitter Velocity=0.00, 0.00
Z Emitter Velocity=0.00, 0.00
Drag=0.00, 0.00
X Particle Velocity=0.00, 0.00
Y Particle Velocity=0.00, 0.00
Z Particle Velocity=0.00, 0.00
X Rotation=0.00, 0.00
Y Rotation=0.00, 0.00
Z Rotation=0.00, 0.00
X Offset=0.00, 0.00
Y Offset=0.00, 0.00
Z Offset=0.00, 0.00
Pitch=0.00, 0.00
Bank=0.00, 0.00
Heading=0.00, 0.00

[Particle.1]
Lifetime=0.00, 0.00
Type=28
X Scale=1500.00, 1500.00 //estimated effective range/throw in metres, calculated using "sqrt(rated candela*4)"
Y Scale=0.00, 0.00
Z Scale=0.00, 0.00
X Scale Rate=0.00, 0.00
Y Scale Rate=0.00, 0.00
Z Scale Rate=0.00, 0.00
Drag=0.00, 0.00
Color Rate=0.00, 0.00
X Offset=0.00, 0.00
Y Offset=0.00, 0.00
Z Offset=0.00, 0.00
Fade In=0.00, 0.00
Fade Out=0.00, 0.00
Static=1
Face=0, 0, 0

[ParticleAttributes.1]
//color setted to 6000K temp, aviation white
            //r,g,b,a arrangement. The Intensity value here applies throughout. 128 is equal to an intensity of 1. Lower than 128 is scaled to an intensity of 0. 255 is equal to an intensity of 50.
Color Start=255, 243, 239,128 //day
Color End=255, 243, 239, 128  //night
Bounce=0.00
X Scale Goal=0.00
Y Scale Goal=0.00
Z Scale Goal=0.00
Falloff Exponent=1.8 //too much means light would decay faster in range, vice versa
Inner Cone Angle=1.00 //value must not approach outer angle else unwanted result would happen
Outer Cone Angle=8.5 //vertical and horizontal effective beam angle
//eof

```
below is result, TDS 737(NGX Merged)
![image](https://github.com/GPUthesteve/P3D_LandingLightEffectUpd/assets/89721316/3ec13a7b-fb83-4fae-a65a-c9b0c332dd29)

VC
![image](https://github.com/GPUthesteve/P3D_LandingLightEffectUpd/assets/89721316/0c4fe356-4f20-4d40-a76c-cc33590bad89)
Rumors about DL litting entire VC. I think because wrong angle is used to create light. even though P3D treats "VC viewpoint" fuselage as transparent. (I mean, not much ppl are modelling fuse anyways)
