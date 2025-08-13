# Webots Generic Mesh Loader

This repository contains a Webots PROTO definition for importing and displaying 3D mesh files in Webots simulations.

## Overview
The `GenericMesh.proto` file allows you to load any supported mesh file into Webots with adjustable position, rotation, and scale.  
It is designed to be reusable — you only need to change the `meshUrl` field to point to your model file.


## File Extensio
Webots PROTO files use the `.proto` extension. Mesh files may use `.stl`, `.obj`.

## Usage
1. Place your `.proto` file inside your Webots project `protos/` directory.
2. Place your mesh file (e.g., `model.STL`) in the same directory or update the `meshUrl` path accordingly.
3. In your Webots world, **Add → PROTO nodes (Current Project)** → select your PROTO.
4. Adjust the `meshUrl`, `translation`, `rotation`, and `scale` fields in the node inspector.

## Example
```vrml
GenericMesh {
  meshUrl [ "my_model.STL" ]
  translation 0 0 0
  rotation 0 1 0 0
  scale 0.001 0.001 0.001
}
