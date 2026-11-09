# STREET DRIFT — Mobile 3D driving prototype

This is a playable first build: 3D city road, directional sunlight, shadow maps, procedural sports coupe, traffic, touch steering, accelerator, brake, nitro, speed HUD, drift score, menu, garage paint switch.

## Run locally
```bash
npm install
npm run dev
```
Open the Vite URL in a modern browser. Internet is needed to load Three.js from jsDelivr in this version.

## Build Android APK
Recommended: use GitHub Actions (workflow included). Push this folder to a GitHub repository, then open **Actions → Build Android APK**. Download the `street-drift-debug-apk` artifact after the workflow succeeds.

## Termux (Git workflow)
```bash
pkg update -y
pkg install git nodejs-lts -y
git clone https://github.com/YOUR-USERNAME/street-drift.git
cd street-drift
npm install
npm run build
```
For APK creation, push to GitHub and use the included Actions workflow. A full Android SDK/Gradle setup directly inside Termux is not assumed.

## Important asset note
The uploaded `New Project 15.obj` file was inspected and is a packaged project archive, not a plain Wavefront OBJ text mesh. The current prototype uses a built-in procedural car until you provide/export the vehicle as `.glb` or `.gltf`. Replaceable textures can go in `assets/`.

## Performance
Shadow maps and antialiasing are enabled. Performance depends on device GPU; the renderer caps pixel ratio at 1.7 for mobile stability. This is a prototype foundation, not a finished commercial racing game.
