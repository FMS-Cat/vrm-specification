# VRMC_materials_mtoon

## Contributors

* TODO: Name, affiliation, and contact info for each contributor

## Status

Draft

## Dependencies

Written against the glTF 2.0 spec.

## Overview

This extension defines an use of toon material called MToon that can be used as a glTF 2.0 material, as an alternative to the PBR shading models provided by the core specification.
The material MToon was originally intended to be used with an extension [`VRMC_vrm`](../VRMC_vrm-1.0_draft/README.md) which enables us to describe a glTF asset as a VR avatar, but it can be used with any glTF models.
The motivation of this extension is to provide artists various way to express toon-like materials that are not covered by PBR materials or Unlit materials by the extension [`KHR_materials_unlit`](https://github.com/KhronosGroup/glTF/tree/master/extensions/2.0/Khronos/KHR_materials_unlit).

### MToon

MToon is an implementation of toon material.
MToon is originally implemented for Unity, then ported to various platforms.
MToon has following various features:

- Toon shading, to render models in various styles of toon shading using detailed parameters.
- MatCap, provides an easy way to simulate environment lighting.
- Parametric Rim Lighting, provides an easy way to express glossy materials.
- Outlines, to draw outline of models.
- UV Animation, to render animated textures.

## Extending Materials

The parameters of an MToon material will be stored in the extension `VRMC_materials_mtoon` of glTF materials.
When the extension is present, it indicates that the material should be rendered in MToon material.

```json
{
    "materials": [
        {
            "name": "MyMToonMaterial",
            "pbrMetallicRoughness": {
                "baseColorFactor": [ 1.000, 1.000, 1.000, 1.0 ]
            },
            "extensions": {
                "VRMC_materials_mtoon": {
                    "shadeFactor": [ 1.000, 0.831, 0.831, 1.0 ],
                    "shadingToonyFactor": 0.5
                }
            }
        }
    ]
}
```

## Properties

TODO

### JSON Schema

TODO: Links to the JSON schema for the new extension properties.

## Known Implementations

* TODO: List of known implementations, with links to each if available.

## Resources

* TODO: Resources, if any.
