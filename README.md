<!--
Version: 1.0

**Change Log**

-->

Status Effects 
-------------------------------------
[Asset Store Link](http://u3d.as/2LKM)  
© 2022 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->
* [Status Effects](#status-effects)
	* [Table of Contents](#table-of-contents)
	* [Contact](#contact)
	* [Description Features](#description-features)
	* [Terms of Use](#terms-of-use)
	* [Overview/Setup](#overview/setup)
	* [Scripts](#scripts)
		* [Status_Effect_Manager.cs](#status_effect_manager.cs)
		* [Other Scripts](#other-scripts)
	* [Shaders](#shaders)
		* [CharacterGlow.shadergraph and ZomBunny_Eyes.shadergraphs](#characterglow.shadergraph-and-zombunny_eyes.shadergraphs)
		* [RimGlow](#rimglow)

<!--TOC-->


## Contact  

Questions, suggestions, help needed?  
[https://github.com/jgarza9788](https://github.com/jgarza9788)


## Description Features

Displays a Status Effect using a shader and VFX particles.
* 5 different statuses
* Particles + Shader
* Easily Customize
* Easily Add new statuses
* Fully Commented C# code 

## Terms of Use

Required:  
please follow [Unity's EULA](https://unity3d.com/legal/as_terms) 

Suggestion/Optional:  
please put my name in the credits, or in the special thanks section. :)  

## Overview/Setup 

Status_Effect_Manager.cs manages the statuses of the character and updates the color and sends events to the VFX (for particles).

![image](https://imgur.com/jJyUWf0.gif)
[Link to Video](https://imgur.com/FJtTy86)



## Scripts 

### Status_Effect_Manager.cs
Description:  
This Script will trigger the status of the character(s)

![Imgur](https://imgur.com/orVF2lF.png)

Effect Values:  
This is a list of all the different effects.

* Status:  
the name of the effect, this will be sent to tge VFX object to trigger the correct particles for the status
* Anim:  
the current play value of the animation (0.0 -- 1.0)
* Speed:  
the speed at which the animation plays
* Color:  
the color used for the effect
* Curve:  
the Curve for the animation 

Materials:  
This is a list of the materials with shaders that need to be updated.  
> the shaders must have 2 properties (GlowAnim (float), and GlowColor (a Color))
> Please see the CharacterGlow.shadergraph as an example.
 
VisualEffect_prefab:  
this is a prefab that will be created on Awake.  
and it will spawn the particles when the event is triggered.

Status:  
This is the effect that will be played.


### Other Scripts
The Other scripts are basically just used for the Demos.

AlwaysFace.cs:  
Turns the gameObject to face the Target.  

Rotate.cs:  
Used to rotate the camera.


## Shaders 

### CharacterGlow.shadergraph and ZomBunny_Eyes.shadergraphs
these are the main shaders for rendering the ZomBunny.  
both of these are updated by the Status_Effect_Manager.cs script,
and both use the RimGlow subshader.

### RimGlow
this takes in the GlowAnim, GlowColor, and the Normal Vector (world space).  




