# P3D_LandingLightEffectUpd
A simplest update to your old fx_landing.fx utilizing latest Dynamic Lighting Technology in Prepar3Dv4, V5.
no need to close source since it's "Modifiable", Use in any project is very welcome.


Wait, in P3Dv4, replacing fx_landing.fx is not working, so please rename it to something else, then call this effect in your project as needed.

TL;DR
below are the code for the effect, rendering 12.5deg light beam. If you configure correctly it won't lit your VC up
(fyi, typical landing light beam aren't that wide, less than 15deg. taxi lights are much wider than 30, but less than 60deg.
```

[Library Effect]
Lifetime=5
Version=2.00
Display Name=12.5deg LL
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
X Scale=0.75, 0.75
Y Scale=0.75, 0.75
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
Color Start=55, 52, 50, 100
Color End=55, 52, 50, 0
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
Type=19
X Scale=0.70, 0.70
Y Scale=0.70, 0.70
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

[ParticleAttributes.1]
Blend Mode=2
Texture=fx_2.bmp
Bounce=0.00
Color Start=55, 52, 50, 255
Color End=55, 52, 50, 0
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

[Emitter.2]
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

[Particle.2]
Lifetime=0.00, 0.00
Type=19
X Scale=0.50, 0.50
Y Scale=0.50, 0.50
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

[ParticleAttributes.2]
Blend Mode=2
Texture=fx_2.bmp
Bounce=0.00
Color Start=55, 52, 50, 255
Color End=55, 52, 50, 0
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
//Cosmetics end

//begin actual beam
[Emitter.3] //calling things part 1
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

[Particle.3] //calling things part 2
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

[ParticleAttributes.3]//the beam itself
Color Start=255, 255, 210, 155
Color End=255, 255, 210, 155
Bounce=0.00
X Scale Goal=0.00
Y Scale Goal=0.00
Z Scale Goal=0.00
Falloff Exponent=3.00
Inner Cone Angle=2.00
Outer Cone Angle=12.5
//end of file
```
below is result, TDS 737(NGX Merged)
https://media.discordapp.net/attachments/859458839426236454/1205049839331844116/2024-2-6_15-31-10-682.png?ex=65d6f51e&is=65c4801e&hm=4e71f547a0fb87caa03ddc143ee89d2d760833c57a8e13b00e3af155a21969f5&=&format=webp&quality=lossless&width=1276&height=671
VC
https://cdn.discordapp.com/attachments/859458839426236454/1205049840116039690/2024-2-6_15-15-3-325.png?ex=65d6f51e&is=65c4801e&hm=3d063ebcf4c1e8050b4dcc42e287c0ab5237eaf1cce7f18082174ac8aad4da3a&
