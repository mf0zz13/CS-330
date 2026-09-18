# Interactive OpenGL 3D Scene

![Rendered 3D scene with a bookcase, books, display case, and framed picture](FinalProjectScene.png)

> **Status:** Completed academic scene with source and a captured final render. The repository is not a self-contained build because it depends on course-provided libraries and utility files that are not included.

This CS-330 project builds an interactive indoor scene from reusable geometric meshes. The composition uses transformed planes, boxes, prisms, and cylinders to construct a bookcase, books, a display case, a picture frame, walls, and flooring. Textures, material properties, multiple light sources, and a movable camera provide the final presentation.

## What the project demonstrates

- C++ application structure separated into scene, view, and startup responsibilities
- OpenGL rendering through GLFW and GLEW, with GLM for transformations and camera math
- Translation, rotation, and scaling of reusable meshes
- Texture loading and UV scaling for wood, wall, plastic, logo, and picture assets
- Material definitions and four configured light sources
- Perspective and orthographic projections with keyboard and mouse camera controls
- Iterative visual testing while composing a scene from simple shapes

## Controls

| Input | Action |
| --- | --- |
| `W` / `S` | Move the camera forward / backward |
| `A` / `D` | Move left / right |
| `Q` / `E` | Move up / down |
| Mouse movement | Change the viewing direction in perspective mode |
| Mouse wheel | Adjust camera zoom |
| `P` | Select the perspective view and its preset camera position |
| `O` | Select the orthographic view and its preset camera position |
| `Esc` | Close the window |

## Repository layout

- [`Source/MainCode.cpp`](Source/MainCode.cpp) initializes OpenGL and runs the render loop.
- [`Source/SceneManager.cpp`](Source/SceneManager.cpp) loads textures and materials, configures lighting, and composes the scene.
- [`Source/ViewManager.cpp`](Source/ViewManager.cpp) handles the window, camera input, and projection matrices.
- [`FinalProjectScene.png`](FinalProjectScene.png) records the completed scene used for visual review.
- [`Design Decisions_Mike_Foster.docx`](Design%20Decisions_Mike_Foster.docx) contains the accompanying design discussion.

## Build requirements and limitation

The committed solution targets Visual Studio 2022's `v143` C++ toolset, Win32, and the Windows SDK. Its project file expects the following course support folders two levels above this repository:

```text
Libraries/GLEW
Libraries/GLFW
Libraries/glm
Utilities
3DShapes
```

Those folders provide shader code, camera and shader helpers, mesh implementations, and third-party headers/libraries. They are absent from this repository, so a fresh clone cannot be built as-is. The screenshot above is existing visual evidence; this documentation pass did not reproduce the build or run an automated graphics test suite.

## Academic context and contribution

This project was completed for SNHU CS-330: Computational Graphics and Visualization. The scene and view framework in the source credits SNHU instructor Brian Battersby. The coursework applied that framework to scene composition, transformations, texture and material selection, lighting, and interactive camera behavior.

<details>
<summary>Course reflection</summary>

### How do I approach designing software?

This project reinforced modular design by separating shapes, textures, lighting, and camera behavior into manageable components. I followed an iterative process: plan the layout, assemble objects from basic shapes, apply textures, and then tune the lighting. Breaking a larger goal into smaller improvements is a process I can reuse in other software projects.

### How do I approach developing programs?

This was my first graphical scene, so development required frequent visual checks in addition to normal debugging. Each course milestone added another part of the final result. As the scene became more complex, I tested more often so I could isolate problems sooner.

### How can computer science help me reach my goals?

The course provided my first academic introduction to linear algebra and showed how mathematical transformations become visible behavior. It also strengthened the problem-solving and debugging skills that transfer to software engineering work outside graphics.

</details>
