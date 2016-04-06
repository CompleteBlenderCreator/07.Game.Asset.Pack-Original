# SECTION 7 Game Asset Pack

****

Part of the Complete Blender Creator course on Udemy, see [here](https://www.udemy.com/blendertutorial/?couponCode=GitHubDiscount) for a special GitHub offer. The full course is part of [this](https://www.kickstarter.com/projects/bentristem/how-to-create-3d-assets-using-blender-online-cours) Kickstarter campaign which was 1000% funded.

Click [here](https://www.udemy.com/blendertutorial/?couponCode=GitHubDiscount) to find out more about the course, and how we build these assets step-by-step.

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

### Building Blocks & Modular Thinking
* Think about ways of building that make parts reusable and modular… Think Lego.
* Realise this gives you quick iterations, and great prototyping potential from a few parts.
* If you are supplier of assets your level maker is going to love that they can redesign with your assets!

## An Overview of Source Control
* The what and why of Version Control Systems
* Choosing your Version Control System (VCS)
* What files to include / exclude
* Commit = save a local snapshot
* Reset = roll-back to a previous state
* Branch, Push and Large File Support later.

### Popular Version Control Systems
* Git
* Mercurial
* Perforce
* Subversion / TortoiseSVN
* Alienbrain (for art but of order $10,000)
* https://en.wikipedia.org/wiki/Comparison_of_version_control_software

### About SourceTree
* Free software by Atlassian
* Visual front-end for Git or Mercurial
* Mac and PC but Mac version is a little ahead
* Good when learning as easy to visualise.

## File Structure & Naming
* Understand that there is NO one way of setting up your filing system. 
* Have a personal style of filing, if you don’t like mine, use yours.
* Talk with your ‘team’ you will form guidelines from your own needs.

### Some Rigidty
*In a Team environment you will have guidelines or discuss with colleagues.
* Some other software might expect certain things to be stored and named in a certain way.

### Naming
* In a Team / larger project it is critical that you can find assets, materials, textures.
* Naming files well will help you and others.
* There are some naming conventions that we will use in this section.

### In Blender Organisation
* We are going to be making a much more complex scene than any previously made.
* Organise it as you go, not afterwards!
* Use description names, cube, cube.001 etc is not helpful to anyone!

## Level Of Detail (LOD)
* Focus on representations of the right size and shape, but JUST Block work models.
* This allows quick iteration of your models.
* Remember higher detail ofter requires more processing time too!

### LOD Numbers and Letters
* LOD 0 often refers to the highest detail model sometimes called the base model.
* To avoid confusion, we are going to use Letters!
* A represents the lowest polygon model, with B,C,D etc increasing in detail.

### Watch Your Time / LOD
* LOD and time taken at usually directly proportional to one another.
* When fleshing out a scene and prototyping you probably want quiet a few assets. 
* You can test models and your scene quickly.

### LOD vs. Time Taken Example
#### “LOD”
* A - B - C - D
#### Polygons*
* 200 - 2,000 - 20,000 - 200,000
#### Time Taken**
*30mins - 2 hours - 1 day - 1 Week+

*Every polygon counts!*

*Time includes other artwork too*

## Setting Up Our Repo & Committing
* Setup Up Our Repository.
* Register SourceTree.
* Learn how to exclude data from our repository.
* Stage our files.
* Make our first commit.

### How Many Repositories?
* You could use a repo per model that you create, this would give you the best level of control.
* You could track your whole project in a repo.
* It will depend on the complexity of your project and how much control you NEED.

### Excluding Data
* Allow faster commits at a smaller size and keeps the database simple and manageable.
* Avoid storing derived / generated data in the repository.
* Example here: will be our reference material.

### Committing
* You’ll need to save all the documents that constitute that commit first.
* Just like saving your working folder and zipping it up at that moment in time.

## Repetitive Tasks In Blender
* Learn how to manage repetitive tasks.
* Understand good uses for appending an Blend file into your scene.

## Using Our Building Blocks
* Set your commit message before working
* Start building your building.
* Notice a few issues and work out a way around them.

## Introduction To Datablocks
* Learn about Datablocks.
* Understand that knowing about them is about to become much more important.
* We have come into contact with data blocks lots but let now go and explore them directly.

### Datablock’s Characteristics 
* Must have unique names per type. 
* Can link to each other.
* Can link across blend files.
* Unused Datablocks are eventually removed.
* This is Where we have used Fake Users in the past to preserve that particular datablock.

### Sharing Datablocks Example
* The same texture on many materials.
* The same material on many meshes.
* The same particle system and so on.
* We will often share and then make the data block unique.

## Linking To An External Datablock
* Learn more about linking to another blend file.
* Link an object datablock.
* Understand that there is a datablock hierarchy.
* Keep an eye out for when you might loose data.

## Linking Blend Files: Making a Proxy
* Learn more about linking datablocks.
* Understand what is happening when you link.
* Realising when you need to use a Proxy.

### Make Proxy
* Creates a New object, that is a parent of the linked data.
* Allows transformation of an object.
* Can now Scale, Move, Rotate etc.
* Otherwise exactly the same as the linked file.
* The object datablock is linked to original and any dependant datablocks.

## Linking Blend Files: Making Local
* Learn why you want to make a linked datablock local.
* Understand we are starting to sever links by doing this.
* Learn about the various stages of making it local.
* Decide when would be a good time to localise a datablock.

### Advantages And Disadvantages
* Advantage: You will have more local control.
* External files moved, project can stay together.
* Disadvantage: Potentially more work involved.
* Any edits you make on the original affect all linked data blocks but not the ones made local.

### When Do you Localise?
* When the link is not required.
* When you want to make the asset unique in this particular file.
* When you want to make changes irrelevant to other potential projects.

### Make Local: Option 1
* Selected Objects: Clones the object Datablock to the new blend file.
* All other datablocks remain linked to the original file.
* This allows changing of anything in the object datablock.

### Make Local: Option 2
* Selected Objects and Data: Clones the object & data Datablock to the new blend file.
* This allows editing of the mesh data, breaking that link and making it a local file. 
* The materials & other datablocks remain linked to the original object.

### Make Local: Option 3
* Selected Objects, Data and Materials: Clones the object, data and materials Datablock.
* This allows editing of the object data & materials datablocks. 
* Breaks those links, making them local to this file.

### Make Local: Option 4
* All: As it sounds, this is pretty much the same as appending the object into the scene. It is now entirely local with no links to the original file.

## Walking And Flying Around The Model
* See how our scene looks and feels walking around it. Using the Fly / Walk Mode.
* Show you how to see the scene in Unity.
* Understand I am using Unity to keep the iterations quick and simple at this early stage.

###Unity Is Optional
* Anything external to Blender, you can watch to see how it works and is coming across.
* Better understanding of external programs.
* Join in, if you have Unity installed and are interested in learning more about this prototyping method.

## Better Camera Control
* Use a different way of moving the camera.
* See this gives you better control over what the camera is pointing at.
* Combine with fly mode for good control.
* Learn how to track a target.

## What Can You Export?
* Understand what will export
* Realise some elements of your models will not export or will once, or not properly.
* Depends on the target package.

### What Appears on Import
* Mesh data including UV Maps. 
* Armatures and animation data will appear too if supported in the target package.
* Textures may appear or simple the base diffuse colour.

### Reconstruction
* Textures often have to be reapplied.
* Shaders work differently in other packages.
* Materials would have to be remade.
* Particle systems are local to Blender.
* Test

## Re-linking Blend Files
* Make a commit!
* Understand the order you NEED to do things in if you wish to change a linked file or it’s datablocks.
* See what happens if you change a link.

### Moving or Renaming Blend Files
* Make a commit!
* COPY file(s) to new location.
* Rename the COPIED file(s) appropriately.
* Doing it it any other order will break links.
* Any links broken when saving will be lost forever!

### Moving or Renaming Datablocks
* Make a commit!
* COPY file(s)
* Open up Copy and make datablock adjustments.
* Link new file into scene.
* Make links to the new object, replacing the old.
* Delete / Archive Old Blend file.

## Profile Modelling By Extrusion
* Understand what a “profile modelling” is.
* Potentially speed up modelling by mirroring.
* Use a series of methods to produce a profile that we can use in our scene.
* Future: Use the same profile in different ways

### Profile Modelling
* A profile is the outline you get when you view something from a particular angle.
* Imagine slicing through your model.
* Realise we have used them in the past: Lamp Base was produces with curves and the Pin was geometry based.

### Methods Used
* We’re going to bump up our extrude speed
* We’re going to be using the bevel tool for construction and defining sharp edges.
* A subsurface modifier for making the surface.

## Profile Modelling Using Curves
* Create some alternative detail.
* Convert Mesh objects into a Curve objects.
* Use those 2 curves to create geometry, one controlling the profile, the other a path.
* See this is great for more accurate path following.

## Profile Modelling Using Mesh Objects
* Use the Array modifier to repeat a mesh object the length of a curve.
* Deform the array using the same curve data.
* End up with some pretty awesome results!

## Light Portals
* Learn how to use light portals.
* Understand the limitations of their use.
* See that they can dramatically increase quality given a fixed number of samples.
* See they’re especially useful for indoor environments. lit by environmental lighting.

### How Cycles Lighting Works
* Light rays are fired out from the camera until they hit a light source.
* With a Lamp Blender knows where the light source is so ONLY fires rays that will eventually hit the light source.

### Emissive Materials
* With an emissive material Blender doesn’t know where the light source is.
* When the camera fires those rays, some of them will never reach a light source, this introduces more noise.

### Environmental Lighting
* In an Interior with only windows letting light in. The rays bounce around a lot and only a few reach the light source. HDR/Environment lighting.
* This introduces a lot of noise in the final image.

### How Prtals Help
* Portals help by telling Blender where to aim those rays.
* This produces much less noise in the final image.

### Limitations
* Portals are a cycles lighting feature.
* They increase light calculation time, however produce much much less noisy environments.
* Portals only work with Environmental light. Using them otherwise can reduce image quality.
* Have little impact if you put something in the way!

## Using Source Control: Resetting
* Go over how to extract a previous version of your files.
* Become aware that Blender files that are made up of linked files need to be accessed and restored  a different way.

## Introduction To UV Unwrapping
* No longer ask what does UV stand for?!
* Overview the mapping in upcoming lectures
* Understand that we will be creating these maps from scratch, and then using them again to speed up further workflow.
* X,Y and Z are used for the Co-ordinates.
* UV are like the ‘X’ and ‘Y’ co-ordinates of an image.
* UV mapping is the process of projecting a 2D image to a 3D model's surface.

## Smart UV Project
* Understand more about unwrapping.
* Be able to unwrap more complex models
* Realise this is a great starting point for a lot of meshes.
* See it gives a basic unwrap that we can work with.

### Why Unwrap?
* A UV map, is a projection of a 3D mesh to 2D.
* Whilst unwrapping is necessary to project an image
* We can let blender ‘guess’ how to unwrap.
* Unwrapping gives you control over how your model is mapped in 2D space.
* Essential when using assets outside Blender.
* Essential when using textures within Blender.
* Necessary if you want control over how something looks.

## How Is It Coming Together
* Check that things are looking right in your main scene.
* Check externally to Blender that the model is working correctly.

## Adding More Detail
* Do some organisation to our outliner before things get out of hand!
* Get an “LOD_B” Mesh Object Ready to be Linked into our main scene.

## Problem Solving
*  Realise starting again is sometimes the best option.
* See that even well prepared scenes can be broken by subtle changes.
* Get help with problems you may have run into when making your building.

## UV Manipulation
* Realise sometimes Smart UV project is 99% of the way there but something is not quiet right.
* Use UV/Image Editor to change individual parts on your mapping.

## Complex Shapes & UV Mapping
* Have a quick tour around my Church Vault.
* See the challenges that we can have with more complex Models.
* Troubleshoot some common unwrapping issues.
* Work out ways to make an unwrap easier and quicker.

## Introduction To Marking Seams
* Realise that UV unwraps will have seams in them.
* Learn how to mark seams where you want them.
* Understand that this gives us the most control over our models unwrap.

### What Is A Seam?
* It is a “cut” it your model, telling Blender how to unwrap your model.
* It allows you to separate parts of your meshes.
* Texture those parts individually.

### Tips For Marking Seams
* Seams can easily cause distortion and misalignment of textures.
* Seams often occur on hard edges.
* They are made where you are least likely to see them.
* Understand that this gives us the most control over our model.

## Painting In The Image Editor
* Create your own Image using Blender.
* Become more familiar with the image editor.
* Realise Blender’s limitations when it comes to image editing.
* Understand you may have to use external packages for better control.

## The Diffuse Map
* Create a hand painted texture in the UV image editor and apply it to your models! 
* Be creating the diffuse map from scratch
* Explain what the diffuse map does.

### What Is A Diffuse Map?
* Is the most common map, and the one most people think of when someone says “texture”.
* It defines the colour and patterns on a surface.

### Diffuse Maps
* Can be challenging to imagine a surface without light source, or rather with uniform light
* Avoid creating detail that would usually be generated by bumps on the surface.
* We are going to avoid painting shadows too.
* If done, this is called ‘baking’ into the image.

## Using Images For Control
* Learn how to use images to control your materials.
* Understand why these control images are black and white.
* Create a simple stage for our building.

### Why Black and White?
* These Greyscale images define “values” on a per pixel basis.
* Black represents a value of 0 and white a value of 1.
* You map them to your model like you would any other image.

## Illusion of Detail- Using Bump Maps
* Use a texture to control how light interacts with a surface.
* See how to use a texture as a bump map in Blender Render.
* Use Generated textures rather than hand made.

### Bump Maps
* Normal and Height/Displacement maps are both types of bump maps.
* We’re going to use a displacement map.
* They tell a shader HOW to interact with light.
* This gives the illusion of detail on a surface.
* Can increase render speeds vs geometry.

## Using Displacement Maps
* Create real detail using a texture.
* Use a displacement map to alter geometry.
* Understand that you need geometry first to modify.
* Use the displacement influence in Blender Render.
* Then use the displacement modifier in a similar manner.

### An Important Reality
* They are not suited to things like generating a final brick wall. V High Poly count required.
* They're very useful for applying detail e.g. scales on a lizard/fish or dragon.
* Great for generating geometry and then optimising 
* For larger items, like terrain.

## Normal Maps 

* Understand they are a type of bump map.
* Gain a greater understanding of how normals work.
* They contain direction information not height information.
* There are 3 Main Types.

## Baking A Normal Map In Blender
* Create a normal map.
* Understand when to create a normal map.
* Use a process called baking.
* See the baking is the fundamental process for creating other map types too in Blender.
* Understand about cages and why they are used.


## Applying A Normal Map In Blender

## Texture Resolution
* Understand that resolution will control the level of detail at a particular distance.
* Realise when a texture is too large or too small.
* Learn about the power of two (POT) and why and when it is important.

## The Multi-Resolution Modifier
* Learn how to use the multi resolution modifier.
* See it is similar to the subsurf. modifier and great for multiple resolutions of a single model.
* Learn to control how sharp edges.
* Understand that this is best applied to a base mesh that is close to the ‘final’ low-poly version. 

## Baking Using The Multires Modifier 
* Learn how bake detail from the higher multires to a lower one.
* Very similar to before, but this time only one model.

## Copying Mesh Properties

## Optimising A UV Map

——
Videos in this section of the [full Udemy course](https://www.udemy.com/blendertutorial/?couponCode=GitHubDiscount)...

---
