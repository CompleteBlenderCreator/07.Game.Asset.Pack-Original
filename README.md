# Gothic.Church.Game.Assets

# SECTION 7 Gothic Church
****

Part of the Complete Blender Creator course on Udemy, see [here](https://www.udemy.com/blendertutorial/?couponCode=GitHubSpecial) for a special GitHub offer. The full course is part of [this](https://www.kickstarter.com/projects/bentristem/how-to-create-3d-assets-using-blender-online-cours) Kickstarter campaign which was 1000% funded.

Click [here](https://www.udemy.com/blendertutorial/?couponCode=GitHubSpecial) to find out more about the course, and how we build these assets step-by-step.

These are just the files from the course, not the actual tutorial videos. At the time of writing this course has several hours of high-quality videos.

You're welcome to download, fork or do whatever else legal with all the files!

Enjoy yourselves.

Ben Tristem & Michael Bridges

*Below is a rough projection of the topics in this section and is a copy from previous Gothic Church Section*
*This will change as this section is fleshed out*

## Section Introduction

* You are going to make several models. 
* We’ll be making both high poly and low poly versions of out assets.
* We will emphasise how critical naming is when working with a larger project like this.
* You will be able to create your own mapping, with these we can make the illusion of detail.
* We’ll be constantly checking our model externally
* This will be focused mainly on an interior environment.

## Section Specification

* Create assets to be exported straight into an external program, like a game engine.
* Creating our own textures, and other maps from high detail models and apply them to a low poly version.
* Only modelling the interior of the Gothic Church.

* You can use this technique within Blender itself too for optimisation. 
* I am going to be testing my model externally as I go. I will use Unity to do this.

* I will be keeping my scene simple, primarily for teaching purposes! 
* I encourage you to add more detail, experiment and have fun. Wouldn’t the scene look much more interesting with a chess set in it.

## Planning Your Project
* Plan your project, define it’s scope and your goals- important to prevent scope slip!
* Gather your reference material, if possible explore real world locations to get a feeling. Scour the web for images for you references too.

## Walking And Flying Around The Model
* See how our scene looks and feels walking around it. Using the Fly / Walk Mode.
* Show you how to see the scene in Unity.
* Understand I am using Unity to keep the iterations quick and simple at this early stage.

* Anything external to Blender, you can watch to see how it works and is coming across.
* Better understanding of external programs.
* Join in, if you have Unity installed and are interested in learning more about this prototyping method.

## Light Portals
* Learn how to use light portals.
* Understand the limitations of their use.
* See that they dramatically increase quality and are especially useful for indoor environments.
* They aren’t used externally to Blender. 

## UV Mapping In Blender

* No long ask what does UV stand for?!
* Overview the mapping in upcoming lectures
* Understand that we will be creating these maps from scratch, and then using them again to speed up further workflow.
* X,Y and Z are used for the Co-ordinates.
* UV are like the ‘X’ and ‘Y’ co-ordinates of an image.
* UV mapping is the process of projecting a 2D image to a 3D model's surface.
* They create the illusion of surface detail by mapping part of an image to the geometry on our model. 
* They can be applied automatically, great for basic models. Generating a UV map gives best results.
* Diffuse Map: The base colour of the geometry.
* Bump Maps: Tell the shader how to react with light.

## The Multi-Resolution Modifier
* Learn how to use the multi resolution modifier.
* See it is great for multiple resolutions of a model.
* Learn to control how sharp edges.
* Understand that this is best apply to a base mesh that is the final low-poly version. 

## Solving Issues With Subdivision
* See a potential issue you may encounter when you use any form of subsurface division.
* Finish off the solution to the previous challenge.

## Copying Mesh Properties
* Learn how to copy attributes of a mesh object.
* See this is great when you have lots of components, for e.g. need the same material.
* Understand it’s a destructive operation e.g. copying materials will overwrite a meshes current materials.

## UV Unwrapping
* Understand what unwrapping is.
* Learn about seems.
* See the different default unwrapping options.
* Remember a UV map, is a projection of a 3D mesh to a 2D image.
* Unwrapping give us control over any maps we want to place on our model.
* This is because it maps the mesh co-ordinates to the image.
* Essential when using assets outside Blender
* Unwrapping isn’t necessary to apply maps to a mesh in Blender 
* We can let blender ‘guess’ how to apply a map.
* However if you want control over how something looks it is essential.

## Texture Resolution
* Understand that resolution will control the level of detail at a particular distance.
* Realise when a texture is too large or too small.
* Learn about the power of two (POT) and why and when it is important.
* Computers work with 1s and 0s, or Binary.
* A lot of external programs like POT textures.
* They aren’t necessary but are a good standard to adhere too, especially when working with external programs.
* Don’t have to be ‘square’, providing side length is a POT.
* Mathematically they’ll be 2 to the power of n or 2^n. eg. 2^5 = 32
* If you have been around computers for a while you’ll recognise this sequence: 2, 4, 8, 16, 32, 64, 128, 256, 512,1024, 2048, etc.

## Optimising A UV Map
* Be using Blender Render.
* Making your UV map more uniform, minimising distortion and optimising image use.
* Understand the use of margins
* Learn more about seams and their placement.

## The Diffuse Map
* Paint onto your model!
* Be creating the diffuse map from scratch
* Defuse map is for the colour changes in a model, not necessarily surface detail.

## UV Problems And Solutions
* Learn what pinning is.
* See how to reset a UV map if things go wrong.
* Experience sticky selection mode.
* Keeping UV Editor and 3D Editor in Sync.
* Look at the other types of unwrapping.

## Layering Textures
* Learn how to layer textures using Blender Render.
* Understand this is a great way of checking out an effect quickly and simply
* Have a glimpse at what other maps can do!

## Working With Cycles & Blender Render
* Understand that Blender Render (BR) and Cycles are fundamentally different.
* See how to work with only one material.
* Realise you might have to create separate BR and Cycles materials.

## Using A Bump Map In Cycles
* See how to use B&W image as a bump map.
* Normal and height maps are both bump maps.
* See the again illusion of surface detail!

##Creating Tiling Textures

* Understanding what a tiling texture is.
* We’ll be aiming for a basic texture
* Create a tiled texture for the walls of our Church.
* Understand getting it looking right will take time.

## Mesh Re-Topology 
* Use existing mesh data to create new mesh data.
* Understand remaking meshes can take a lot of time, but is often part of the workflow especially with organic models.
* Fix your model, If you have the same problem as me.

## Retopology Continued
* See the solution to the last video
* There is multiple repetition, so only the highlights are shown.

## The Knife Tool
* Use and understand how the knife tool works.
* Create uneven geometry by chopping up our existing mesh.

## Polygon Count
* See multiple ways to cut down the polygon count in your scene.
* Understand that the speed of your computer will dictate how complex a scene can be before it starts to become unmanageable.

## Displacement & Height Maps
* See that these are used to change the underlaying geometry.
* Understand that they are grey scale images, If you used a colour image it will just use the average of RGB- converting it to greyscale.
* They aren’t not suited to things like generating a final brick wall. V High Poly count needed for resolution match. 
* They're very useful for applying detail e.g. scales on a lizard/fish or dragon.
Great for generating geometry and then optimising or for larger items, like terrain.

## The Displacement Modifier
* Use your displacement map to alter geometry.
* Realise that you need geometry to modify.
* Use the displacement in Blender Render.
* Then use the Displacement Modifier in the same manner.

## Normal Maps
* Understand they are a type of bump map.
* Gain a greater understanding of how normals work.
* They contain direction information not height information.

### Normal Maps
* Contain direction information not height information.
* The RGB colour channels define the direction of a normal.
* XYZ components are defined with Red, Green, Blue.

### Normal Maps Appearance
* When creating normal maps they are affected by whether or not the mesh object * has smooth shading turned on.
* Normal direction is very important otherwise the map will be useless.


——
Videos in this section of the [full Udemy course](https://www.udemy.com/blendertutorial/?couponCode=GitHubSpecial)...

---
