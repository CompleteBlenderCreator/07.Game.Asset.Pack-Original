### 1 Section 7 Introduction

+ You are going to make several models.
+ We’ll be making both high poly and low poly versions of these assets.
+ We will emphasise how critical naming is when working with a larger project like this.
+ You will be able to create your own mapping, with these we can make the illusion of detail.
+ We’ll be constantly checking our model externally
+ This will be focused mainly on an interior environment.

### 4 Section Specification

+ Create assets to be exported straight into an external program, like a game engine.
+ Creating our own textures, and other maps from high detail models and apply them to a low poly version.
+ Focused on modelling the interior of the Gothic Church.
+ You can use this technique within Blender itself too for optimisation.
+ I am going to be testing my model externally as I go so you can appreciate the impact externally.
+ We’ll be looking at Level Of Detail, in detail.
+ I will be keeping my scene simple, primarily for teaching purposes!
+ I encourage you to add more detail, experiment and have fun. Wouldn’t the scene look much more interesting with a chess set in it…

### 5 Planning Your Project



### 6 Version Control 2

**An Overview of Source Control**

+ The what and why of Version Control Systems
+ Choosing your Version Control System (VCS)
+ What files to include / exclude
+ Commit = save a local snapshot
+ Reset = roll-back to a previous state
+ Branch, Push and Large File Support later.

A Look At Git Kracken

(New Video 11/2/2018)

### 7 File Structure & Naming

+ Understand that there is NO one way of setting up your filing system.
+ Have a personal style of filing, if you don’t like mine, use yours.
+ Talk with your ‘team’ you will form guidelines from your own needs.

**Some Rigidity**

+ In a Team environment you will have guidelines or discuss with colleagues.
+ Some other software might expect certain things to be stored and named in a certain way.

**Naming**

+ In a Team / larger project it is critical that you can find assets, materials, textures.
+ Naming files well will help you and others.
+ There are some naming conventions that we will use in this section.

**In Blender Organisation.**  

+ We are going to be making a much more complex scene than any previously made.
+ Organise it as you go, not afterwards!
+ Use description names, cube, cube.001 etc is not helpful to anyone!

### 8 Level Of Detail (LOD)

+ Focus on representations of the right size and shape, but JUST Block work models.
+ This allows quick iteration of your models.
+ Remember higher detail often requires more processing time too!

**LOD Numbers and Letters**

+ LOD 0 often refers to the highest detail model sometimes called the base model.
+ To avoid confusion, we are going to use Letters!
+ A represents the lowest polygon model, with B,C,D etc increasing in detail.

**Watch Your Time / LOD**

+ LOD and time taken at usually directly proportional to one another.
+ When fleshing out a scene and prototyping you probably want quiet a few assets.
+ You can test models and your scene quickly.

**LOD vs. Time Taken Example**

**“LOD”**

A - B - C - D

**Polygons**\*

200 - 2,000 - 20,000 - 200,000

**Time Taken**

30mins - 2 hours - 1 day - 1 Week+

\*Every polygon counts!

Time includes other artwork too

### 9 Building Blocks

**Simple Shapes**  

+ RH Triangle whose sides are 1,1,sqrt(2).
+ Square 1x1 and other Integer Rectangles.
+ Isosceles whose base is 1 and sides are 2.
+ Equilateral Triangles of side length 1.
+ These will all fit together well and consistently

**Disadvantages?**

+ NONE… at this stage.
+ Later it can feel restrictive.
+ That is where you want to be customising and adding detail, not in the early stages

**Formulae In The Fields**

+ You can type formulae into Blender’s fields.
+ We can use this to solve otherwise complicated measurements.

### 10 Setting Up Our Repo & Committing

+ Setup Up Our Repository.
+ Register SourceTree.
+ Learn how to exclude data from our repository.
+ Stage our files.
+ Make our first commit.

**How Many Repositories?**

+ You could use a repo per model that you create, this would give you the best level of control.
+ You could track your whole project in a repo.
+ It will depend on the complexity of your project and how much control you NEED.

**Excluding Data**

+ Allow faster commits at a smaller size and keeps the database simple and manageable.
+ Avoid storing derived / generated data in the repository.
+ Example here: will be our reference material.

**Committing**  

+ You’ll need to save all the documents that constitute that commit first.
+ Just like saving your working folder and zipping it up at that moment in time.

### 11 Repetitive Tasks In Blender

+ Learn how to manage repetitive tasks.
+ Understand good uses for appending an Blend file into your scene.

### 12 Using Our Building Blocks

+ Set your commit message before working
+ Start building your building.
+ Notice a few issues and work out a way around them.

### 13 Introduction To Datablocks

+ Learn about Datablocks.
+ Understand that knowing about them is about to become much more important.
+ We have come into contact with data blocks lots but let now go and explore them directly.

**Datablock’s Characteristics**

+ Must have unique names per type.
+ Can link to each other.
+ Can link across blend files.
+ Unused Datablocks are eventually removed.
+ This is Where we have used Fake Users in the past to preserve that particular datablock.

**Sharing Datablocks Example**

+ The same texture on many materials.
+ The same material on many meshes.
+ The same particle system and so on.
+ We will often share and then make the data block unique.

### 14 Linking To An External Datablock

+ Learn more about linking to another blend file.
+ Link an object datablock.
+ Understand that there is a datablock hierarchy.
+ Keep an eye out for when you might loose data.

### 15 Linking Blend Files- Making a Proxy

+ Learn more about linking datablocks.
+ Understand what is happening when you link.
+ Realising when you need to use a Proxy

**Make Proxy**  

+ Creates a New object, that is a parent of the linked data.
+ Allows transformation of an object.
+ Can now Scale, Move, Rotate etc.
+ Otherwise exactly the same as the linked file.
+ The object datablock is linked to original and any dependant datablocks.

### 16 Linking Blend Files: Making Local

+ Learn why you want to make a linked datablock local.
+ Understand we are starting to sever links by doing this.
+ Learn about the various stages of making it local.
+ Decide when would be a good time to localise a datablock.

**Advantages And Disadvantages**

+ Advantage: You will have more local control.
+ External files moved, project can stay together.
+ Disadvantage: Potentially more work involved.
+ Any edits you make on the original affect all linked data blocks but not the ones made local.

**When Do you Localise?**

+ When the link is not required.
+ When you want to make the asset unique in this particular file.
+ When you want to make changes irrelevant to other potential projects.

**Make Local: Option 1**

+ Selected Objects: Clones the object Datablock to the new blend file.
+ All other datablocks remain linked to the original file.
+ This allows changing of anything in the object datablock.

**Make Local: Option 2**

+ Selected Objects and Data: Clones the object & data Datablock to the new blend file.
+ This allows editing of the mesh data, breaking that link and making it a local file.
+ The materials & other datablocks remain linked to the original object.

**Make Local: Option 3**

+ Selected Objects, Data and Materials: Clones the object, data and materials Datablock.
+ This allows editing of the object data & materials datablocks.
+ Breaks those links, making them local to this file.

**Make Local: Option 4**

+ All: As it sounds, this is pretty much the same as appending the object into the scene. It is now entirely local with no links to the original file.

### 17 Walking And Flying Around The Model

+ See how our scene looks and feels walking around it. Using the Fly / Walk Mode.
+ Show you how to see the scene in Unity.
+ Understand I am using Unity to keep the iterations quick and simple at this early stage.

**Unity Is Optional**

+ Anything external to Blender, you can watch to see how it works and is coming across.
+ Better understanding of external programs.
+ Join in, if you have Unity installed and are interested in learning more about this prototyping method.

### 18 Better Camera Control

+ Use a different way of moving the camera.
+ See this gives you better control over what the camera is pointing at.
+ Combine with fly mode for good control.
+ Learn how to track a target.

### 19 What Can You Export?

+ Understand what will export
+ Realise some elements of your models will not export or will once, or not properly.
+ Depends on the target package.

**What Appears on Import**

+ Mesh data including UV Maps.
+ Armatures and animation data will appear too if supported in the target package.
+ Textures may appear or simple the base diffuse colour.

**Reconstruction**

+ Textures often have to be reapplied.
+ Shaders work differently in other packages.
+ Materials would have to be remade.
+ Particle systems are local to Blender.
+ Test

### 20 Re-linking Blend Files

**Re-linking Blend Files**

+ Make a commit!
+ Understand the order you NEED to do things in if you wish to change a linked file or it’s datablocks.
+ See what happens if you change a link.

**Moving or Renaming Blend Files**

+ Make a commit!
+ COPY file(s) to new location.
+ Rename the COPIED file(s) appropriately.
+ Doing it it any other order will break links.
+ Any links broken when saving will be lost forever!

**Moving or Renaming Datablocks**

+ Make a commit!
+ COPY file(s)
+ Open up Copy and make datablock adjustments.
+ Link new file into scene.
+ Make links to the new object, replacing the old.
+ Delete / Archive Old Blend file.

### 21 Profile Modelling By Extrusion

+ Understand what a “profile modelling” is.
+ Potentially speed up modelling by mirroring.
+ Use a series of methods to produce a profile that we can use in our scene.
+ Future: Use the same profile in different ways

**Profile Modelling**

+ A profile is the outline you get when you view something from a particular angle.
+ Imagine slicing through your model.
+ Realise we have used them in the past: Lamp Base was produces with curves and the Pin was geometry based.

**Methods Used**

+ We’re going to bump up our extrude speed
+ We’re going to be using the bevel tool for construction and defining sharp edges.
+ A subsurface modifier for making the surface.

### 22 Profile Modelling Using Curves

+ Create some alternative detail.
+ Convert Mesh objects into a Curve objects.
+ Use those 2 curves to create geometry, one controlling the profile, the other a path.
+ See this is great for more accurate path following.

### 23 Profile Modelling Using Mesh Objects

+ Use the Array modifier to repeat a mesh object the length of a curve.
+ Deform the array using the same curve data.
+ End up with some pretty awesome results!

### 24 Light Portals

+ Learn how to use light portals.
+ Understand the limitations of their use.
+ See that they can dramatically increase quality given a fixed number of samples.
+ See they’re especially useful for indoor environments, lit by environmental lighting.

**How Cycles Lighting Works**

+ Light rays are fired out from the camera until they hit a light source.
+ With a Lamp Blender knows where the light source is so ONLY fires rays that will eventually hit the light source.

**Emissive Materials**

+ With an emissive material Blender doesn’t know where the light source is.
+ When the camera fires those rays, some of them will never reach a light source, this introduces more noise.

**Environmental Lighting**

+ In an Interior with only windows letting light in. The rays bounce around a lot and only a few reach the light source. HDR/Environment lighting.
+ This introduces a lot of noise in the final image.

**How Portals Help**

+ Portals help by telling Blender where to aim those rays.
+ This produces much less noise in the final image.

**Limitations**

+ Portals are a cycles lighting feature.
+ They increase light calculation time, however produce much much less noisy environments.
+ Portals only work with Environmental light. Using them otherwise can reduce image quality.
+ Have little impact if you put something in the way!

### 25 Using Source Control- Resetting

+ Go over how to extract a previous version of your files.
+ Become aware that Blender files that are made up of linked files need to be accessed and restored a different way.

### 26 Introduction To UV Unwrapping

+ No longer ask what does UV stand for?!
+ Overview the mapping in upcoming lectures
+ Understand that we will be creating these maps from scratch, and then using them again to speed up further workflow.
+ X,Y and Z are used for the Co-ordinates.
+ UV are like the ‘X’ and ‘Y’ co-ordinates of an image.
+ UV mapping is the process of projecting a 2D image to a 3D model's surface.

### 27 Smart UV Project

+ Understand more about unwrapping.
+ Be able to unwrap more complex models
+ Realise this is a great starting point for a lot of meshes.
+ See it gives a basic unwrap that we can work with.

**Why Unwrap?**

+ A UV map, is a projection of a 3D mesh to 2D.
+ Whilst unwrapping is necessary to project an image
+ We can let blender ‘guess’ how to unwrap.
+ Unwrapping gives you control over how your model is mapped in 2D space.
+ Essential when using assets outside Blender.
+ Essential when using textures within Blender.
+ Necessary if you want control over how something looks.

### 28 How Is It Coming Together?



### 29 Adding More Detail

+ Do some organisation to our outliner before things get out of hand!
+ Get an “LOD_B” Mesh Object Ready to be Linked into our main scene.

### 30 Problem Solving

+ Realise starting again is sometimes the best option.
+ See that even well prepared scenes can be broken by subtle changes.
+ Get help with problems you may have run into when making your building.

### 31 UV Manipulation

+ Realise sometimes Smart UV project is 99% of the way there but something is not quiet right.
+ Use UV/Image Editor to change individual parts on your mapping.
+ (Updated 18/09/2017)

### 32 Complex Shapes & UV Mapping

+ Have a quick tour around my Church Vault.
+ See the challenges that we can have with more complex Models.
+ Troubleshoot some common unwrapping issues.
+ Work out ways to make an unwrap easier and quicker.

### 33 Introduction To Marking Seams

+ Realise that UV unwraps will have seams in them.
+ Learn how to mark seams where you want them.
+ Understand that this gives us the most control over our models unwrap.

**What Is A Seam?**

+ It is a “cut” it your model, telling Blender how to unwrap your model.
+ It allows you to separate parts of your meshes.
+ Texture those parts individually.

**Tips For Marking Seams**

+ Seams can easily cause distortion and misalignment of textures.
+ Seams often occur on hard edges.
+ They are made where you are least likely to see them.
+ Understand that this gives us the most control over our model.

### 34 Painting In The Image Editor

+ Create your own Image using Blender.
+ Become more familiar with the image editor.
+ Realise Blender’s limitations when it comes to image editing.
+ Understand you may have to use external packages for better control.

### 35 Diffuse Maps

**The Diffuse Map**

+ Create a hand painted texture in the UV image editor and apply it to your models!
+ Be creating the diffuse map from scratch
+ Explain what the diffuse map does.

**What Is A Diffuse Map?**

+ Is the most common map, and the one most people think of when someone says “texture”.
+ It defines the colour and patterns on a surface.

**Diffuse Maps**

+ Can be challenging to imagine a surface without light source, or rather with uniform light
+ Avoid creating detail that would usually be generated by bumps on the surface.
+ We are going to avoid painting shadows too.
+ If done, this is called ‘baking’ into the image.

### 36 Using Images For Control

+ Learn how to use images to control your materials.
+ Understand why these control images are black and white.
+ Create a simple stage for our building.

**Why Black and White?**

+ These Greyscale images define “values” on a per pixel basis.
+ Black represents a value of 0 and white a value of 1.
+ You map them to your model like you would any other image.

### 37 Illusion of Detail- Using Bump Maps

+ Use a texture to control how light interacts with a surface.
+ See how to use a texture as a bump map in Blender Render.
+ Use Generated textures rather than hand made.

**Bump Maps**

+ Normal and Height/Displacement maps are both types of bump maps.
+ We’re going to use a displacement map.
+ They tell a shader HOW to interact with light.
+ This gives the illusion of detail on a surface.
+ Can increase render speeds vs geometry.

### 38 Using Displacement Maps

+ Create real detail using a texture.
+ Use a displacement map to alter geometry.
+ Understand that you need geometry first to modify.
+ Use the displacement influence in Blender Render.
+ Then use the displacement modifier in a similar manner.

**An Important Reality**

+ They are not suited to things like generating a final brick wall. V High Poly count required.
+ They're very useful for applying detail e.g. scales on a lizard/fish or dragon.
+ Great for generating geometry and then optimising
+ For larger items, like terrain.

### 39 Normal Maps

+ Understand they are a type of bump map.
+ Gain a greater understanding of how normals work.
+ They contain direction information _not_ height information.
+ There are 4 Main Types

### 40 Baking A Normal Map In Blender

+ Create a normal map.
+ Understand when to create a normal map.
+ Use a process called baking.
+ See the baking is the fundamental process for creating other map types too in Blender.
+ Understand about cages and why they are used.
+ (Updated 15/09/2017)

### 41 Applying A Normal Map In Blender

### 42 Texture Resolution

+ Understand that resolution will control the level of detail at a particular distance.
+ Realise when a texture is too large or too small.
+ Learn about the power of two (POT) and why and when it is important.
+ (Updated 12/06/2017)

**Power Of Two**

+ Computers work with 1s and 0s, or Binary.
+ A lot of external programs need POT textures.
+ They aren’t necessary in Blender but are a good standard to adhere too, especially when working with external programs.
+ Don’t have to be ‘square’, providing side length is a POT.

**Which Numbers are Power of 2?**  

+ Mathematically they’ll be 2 to the power of n or 2^n. eg. 2^5 = 32
+ If you have been around computers for a while you’ll recognise this sequence: 2, 4, 8, 16, 32, 64, 128, 256, 512,1024, 2048, etc.

**Textures Of Different Sizes.**  

+ Need their own UV Map.
+ Probably not exportable due to multiple UV maps.
+ Best to stick to one texture size for any given unwrap.
+ Larger textures require more memory.

**What Size Textures**  

+ How far away is the camera from the object/texture?
+ How big is the object?
+ What’s the “Retina” Texture level?
+ rTexture = 3266 * Tan(Size/Distance)

### 43 The Multi-Resolution Modifier

+ Learn how to use the multi resolution modifier.
+ See it is similar to the subsurf. modifier and great for multiple resolutions of a single model.
+ Learn to control how sharp edges.
+ Understand that this is best applied to a base mesh that is close to the ‘final’ low-poly version.

### 44 Baking Using The Multires Modifier

+ Learn how bake detail from the higher multires to a lower one.
+ Very similar to before, but this time only one model.

### 45 Copying Mesh Properties

+ Learn how to copy attributes of a mesh object.
+ See this is great when you have lots of components, for e.g. need the same material.
+ Understand it’s a destructive operation e.g. copying materials will overwrite a meshes current materials

### 46 Optimising A UV Map

+ Making your UV map more uniform, minimising distortion and optimising image use.
+ Understand the use of margins
+ Learn more about seams and their placement.

### 47 Texture Painting In The ViewPort

+ Create a hand painted texture directly onto your model
+ Be creating a diffuse map from scratch

### 48 Realistic Lighting Or Fake It?

### 49 Creating a New Scene In Blender

### 50 Section 7 Wrap Up
