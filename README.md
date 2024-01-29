# Wireframe Viewer
C++ app that allows for viewing 3d .obj models' wireframes

# What is this app
  
![overview](./misc/overview.gif)

## features
 * This app allows 3d models (saved as \*.obj) files be seen in a window  
 * The app offers an ability to move, scale and rotate models
 * App allows for customization of the colors (of the background, edges and points that can be customized too), projection (orthographic or perspective), change the edges to be dashed etc.  
 * App allows for grabbing the framebuffer programmatically i.e. making screenshots
 * ~~App allows for recording gifs of the framebuffer of the desired length~~ is yet to be implemented properly

## support
 * The app supports [wavefront \*.obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file) files, that do not contain negative indexing (some negative indexed models could be parsed correctly, but generally it is not the case)
 * The app supports models with thousands of edges without stutter (it uses OpenGL rendering API)
 * In order to run the application you need OpenGL 3.3 support and Qt dynamic libraries (if you didn't build the app with with staticly built Qt)

## technology
 - Qt 6 frontend
 - OpenGL for rendering
 - written completely in C++ and glsl

# Building

## Requirements
- qt6-qmake
- qt6
- make
- gcc
- stdc++ libs (usually comes bundled with g++)

## build steps
```
cd src
make
```

If you want to statically build the application (without Qt dynamic lib dependencies), you can [add statically configured qt to PATH](https://doc.qt.io/qt-6/linux-deployment.html).

## testing

The testing is quite frankly lacking on this project. However you can run existing tests with the help of [google test](https://github.com/google/googletest) libraries.

```
cd src
make tests
