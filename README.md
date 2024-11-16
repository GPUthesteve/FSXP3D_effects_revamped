# P3D_LandingLightEffectUpd
A simplest update to your old fx_landing.fx utilizing latest Dynamic Lighting Technology in Prepar3Dv4, V5.
no need to close source since it's "Modifiable", Use in any project is very welcome.


Wait, in P3Dv4, replacing fx_landing.fx is not working, so please rename it to something else, then call this effect in your project as needed.

TL;DR
below are the code for the effect, rendering 8.5deg light beam. If you configure correctly it won't lit your VC up
(fyi, typical landing light beam aren't that wide, less than 15deg. taxi lights are much wider than 30, but less than 60deg.
```

[Library Effect]
Lifetime=5
Version=2.00
Display Name=8.5deg LL
Radius=-1
Priority=0

[Properties]

//begin cosmetics
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
Color Start=255, 255, 215, 255
Color End=255, 255, 215, 0
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

//actual lights
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
X Scale=3000.00, 3000.00 //range in metres
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
Color Start=255, 255, 215, 135
Color End=255, 255, 215, 135
Bounce=0.00
X Scale Goal=0.00
Y Scale Goal=0.00
Z Scale Goal=0.00
Falloff Exponent=2.00
Inner Cone Angle=1.00
Outer Cone Angle=8.00
//eof

```
below is result, TDS 737(NGX Merged)
![image](https://github.com/GPUthesteve/P3D_LandingLightEffectUpd/assets/89721316/3ec13a7b-fb83-4fae-a65a-c9b0c332dd29)

VC
![image](https://github.com/GPUthesteve/P3D_LandingLightEffectUpd/assets/89721316/0c4fe356-4f20-4d40-a76c-cc33590bad89)
Rumors about DL litting entire VC. I think because wrong angle is used to create light. even though P3D treats "VC viewpoint" fuselage as transparent. (I mean, not much ppl are modelling fuse anyways)
