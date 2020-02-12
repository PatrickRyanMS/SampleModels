# Bench

Interactive sample available at https://playground.babylonjs.com/#6NK2T6
## Screenshot
<img src = "https://raw.githubusercontent.com/PatrickRyanMS/SampleModels/master/bench/images/benchRender.png" />

## Description
- 3408 triangles with 1760 vertices which emphasizes the amount of resolution needed to hold a silhouette on curved surfaces. Normal map used to bake in edge bevels and rounding rather than put it in the low-poly asset to save on mesh weight.
- Mesh was scaled at real world size.
- All transforms were reset and history erased and all meshes were combined into one mesh for export.
- Mesh was raised so that the bottom sits at 0 on the Y axis (Maya) and the pivot point was set to world 0 which is a requirement for many AR applications.
- All textures baked in a non-square 1x2 format, in this case 1024x2048. This maximizes texel density and UV spacedue to the longer pieces in this model.
- Slats share UV space with some other slats that aren't adjacent to increase texel density while reducing overall coverage in UV space.
- All UV islands are aligned to horizontal and vertical directions. This will help textures appear higher resolution because any straight lines traversing the UVs will not render at an angle. This can reduce the apparent resolution of a texture as the line will need to hop pixels based on the angle it crosses UV space.
- All UV edges straightened to allow for a tighter pack and for the textures to follow the curve of the mesh, even when using a texture that has a straight flow like wood grain. This helped particularly for the sides of the slats where the grain reads as layers of laminate bent around a curve. 
  
### Pipeline
- Maya for modeling and UV mapping
- Substance Designer to bake normals and create custom concrete material
- Substance Painter to bake mesh maps for procedural texturing and applying materials to mesh
- Substance Painter to export glTF and glb with base color, normal, and packed ORM textures at 1024 x 2048 

## License Information

Donated by Microsoft as a sample model of the glTF creation pipeline

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)  
To the extent possible under law, Microsoft has waived all copyright and related or neighboring rights to this asset.