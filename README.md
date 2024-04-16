# Virtual-Try-On-Glasses
Use ARKit to try on glasses

## prepare environment
1. Download 3D Models from [sketchfab](https://sketchfab.com/feed)

2. Install Reality Composer from XCode 14(`Xcode > Open Developer Tool > Reality Composer`)
Then Create a new Document: File > New and choose a Face anchor. It’s up to you if you want to uncheck Use template content — this will just add a “Hello World” thought bubble to your scene.

Once the scene appears with the face anchor, drag your .usdz model file onto the window to add it to the scene. You might need to zoom out to see the model depending on the size. Select it and use the Green, Red & Blue position controls along with the Scale slider in the Transform Pane to move the model into place on the face anchor similar to below.
<img width="630" alt="image" src="https://github.com/fifyrio/Virtual-Try-On-Glasses/assets/8080188/fd71d73b-5500-4124-945f-a4dab048fc6e">


## Create Augmented Reality App project
<img width="889" alt="image" src="https://github.com/fifyrio/Virtual-Try-On-Glasses/assets/8080188/8880abc4-c2e5-4e22-89f6-482d51d43e03">

Drag the `.rcproject` to your project

Load face anchor Reality Composer file
```
let faceAnchor = try! Glasses.loadScene()
```
Set the face tracking configuration to ARView
```
let faceTrackingConfig = ARFaceTrackingConfiguration()
arView.session.run(faceTrackingConfig)
```


| Style 1 | Style 2 |
|----------|----------|
| ![3201713229030_ pic](https://github.com/fifyrio/Virtual-Try-On-Glasses/assets/8080188/3a73761f-f399-4087-b974-eb5c00ec34fa)   | ![3221713251094_ pic](https://github.com/fifyrio/Virtual-Try-On-Glasses/assets/8080188/1b28f6b9-43d8-4151-82eb-04e017e3833e)  |

