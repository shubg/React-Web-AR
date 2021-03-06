# Introduction

**Augmented Reality** is projection of virtual world but fused with reality which makes it different from **Virtual Reality** where the actual environment is hidden and it simulates a physical presence in virtual environment.

> Given below is an abstract from a document which you can find [here](http://www.vtt.fi/inf/pdf/science/2012/S3.pdf).

Augmented Reality combines real world and digital data or you can say that it combines the field of **computer vision** and **computer graphics**. Computer vision applies to **marker detection**, **tracking the position of the marker** and **motion detection** whereas computer graphics applies to the **photometric registration** (matching the appearance of 3D objects in virtual environment to the actual environment) and **interactive animations**.

## Architecture

<p align="center">
  <img src="./architecture.png">
</p>

The **capturing module** captures the **image** from the **camera**. The **tracking module** calculates the correct location and orientation for virtual overlay. The **rendering module** combines the original image and the **virtual components** using the calculated **pose** and then renders the **augmented image** on the display.

The tracking module is the important and heart of the architecture. It calculates the relative pose of the camera in real time. The term pose means the **six degrees of freedom position** i.e **3D orientation and 3D location of an object**. It also enables the system to add virtual components as part of the real scene.

Now to calculate the pose, markers are used along with the **projective geometry**.

This project aims to bridge AR with React to create AR on the web. It uses AR.js behind the scenes to describe the **AR context** and configure the **AR controller** which we will cover in more detail in [concepts](./concepts.md) section.

> If you're interested then you can read the document linked above about the theory of augmented reality.

## Why React?

* Components makes it easy to reason about a scene.
* Clean and minimal API.
* Declaratively controlling the render loop (for threejs renderer).
* Easy to create AR content that can be used and integrated in a React app.

## What it tries to solve?

This project is based on [AR.js](https://github.com/jeromeetienne/AR.js). It provides an abstraction over artoolkit and also enables composition with the custom React components so that you can create AR content on web with ease. Also, its difficult to use the `AR.js` APIs because they aren't well documented and its only possible to learn them by looking at each example (which isn't convenient) and analysing the program structure.

So this project tries to eliminate the learning curve for the APIs and provides an abstraction over the artoolkit core components so that you can understand and create AR content on the web.

## Future

* [webxr-api proposal](https://github.com/mozilla/webxr-api)
* [WebAssembly](http://webassembly.org/)
* Marker less detection

[Continue to concepts section](./concepts.md)
