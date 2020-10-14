Volumetric Performance Toolbox
=====

> How can artists create new live performances during the time of COVID-19? Volumetric Performance Toolbox empowers creators to perform from their own living spaces for a virtual audience. Movement artist Valencia James performed publicly with the Toolbox for the first time on September 24, 2020 in the Mozilla Hubs virtual social space. The project is a collaboration between Valencia James, Glowbox and Sorob Louie as part of Eyebeam’s Rapid Response for a Better Digital Future fellowship.

More information on the Volumetric Performance Toolbox here:

https://valenciajames.com/volumetric-performance/

https://www.glowbox.io/work/volumetric-performance/

This is a fork of the Hubs Exporter for Blender, it introduces a few custom components to stream volumnetric video.


# Hubs Exporter for Blender

This addon extends the glTF 2.0 exporter to support the `MOZ_hubs_components` and `MOZ_lightmap` extensions allowing you to add behavior to glTF assets for [Mozilla Hubs](https://hubs.mozilla.com).

# Adding Components

To add components, go to the "Hubs" section of the properties panel for the thing you want to add a component to. Currently adding components is supported on Scenes, Objects, Bones, and Materials.

<img src="https://user-images.githubusercontent.com/130735/84547528-97440a00-acb8-11ea-9f07-24c919796a3c.png" width="300px"/>

Click "Add Component" and select the component you wish to add from the list. Only components appropriate for the object type you are currently editing and have not already been added will be shown.

# Using Lightmaps

To use a lightmap, create a `MOZ_lightamp` node from the `Add > Hubs` menu and hook up a image texture to the `Lightmap` input. Use a `UV Map` node to control what UV set should be used for the lightmap, as you would any other texture in Blender. 

![lightmap node](https://user-images.githubusercontent.com/130735/83931408-65c7bd80-a751-11ea-86b9-a2ae889ec5df.png)

Note that for use in Hubs, you currently **MUST** use the second UV set, as ThreeJS is currently hardcoded to use that for lightmaps. This will likely be fixed in the future so the exporter does not enforce this.

![setting bake UV](https://user-images.githubusercontent.com/130735/83697782-b9e96b00-a5b4-11ea-986b-6690c69d8a3f.png)

# Exporting

This addon works in conjunction with the official glTF exporter, so exporting is done through it. Select "File > Export > glTF 2.0" and then ensure "Hubs Components" is enabled under "Extensions".

![gltf export window](https://user-images.githubusercontent.com/130735/84547591-be9ad700-acb8-11ea-8c58-7b1104f0a3a7.png)
