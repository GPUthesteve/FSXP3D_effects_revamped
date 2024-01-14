# P3D_LandingLightEffectUpd
A simplest update to your old fx_landing.fx utilizing latest Dynamic Lighting Technology in Prepar3Dv4, V5.
no need to close source since it's "Modifiable", Use in any project is very welcome.


Wait, in P3Dv4, replacing fx_landing.fx is not working, so please rename it to something else, then call this effect in your project as needed.

TL;DR
below are the code for the beam section, 12.5deg beam
(fyi, typical landing light beam aren't that wide, less than 15deg. taxi lights are much wider than 30, but less than 60deg.
```
[Emitter.3]
Lifetime=0.5, 0.5
Delay=0.00, 0.00
Bounce=0.00
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

[Particle.3]
Lifetime=0.00, 0.00
Type=28 //DL tag
X Scale=1000.00, 1000.00 //defines range in metres
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

[ParticleAttributes.3]
Color Start=255, 255, 210, 155
Color End=255, 255, 210, 155
Bounce=0.00
X Scale Goal=0.00
Y Scale Goal=0.00
Z Scale Goal=0.00
Falloff Exponent=3.00
Inner Cone Angle=2.00
Outer Cone Angle=12.5

```
