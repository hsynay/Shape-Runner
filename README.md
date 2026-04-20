<img width="480" height="873" alt="17p-shaperunner" src="https://github.com/user-attachments/assets/8b5e6727-6aef-4e12-8b8f-251027ff636a" /># Shape Runner 🏃‍♂️💨

![Unity](https://img.shields.io/badge/Unity-100000?style=for-the-badge&logo=unity&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)

**Shape Runner** is a fast-paced, endless runner 3D mobile game developed with Unity. The core mechanic relies on quick reflexes and hand-eye coordination, requiring the player to dynamically change their shape (Cube, Sphere, or Cylinder) to pass through matching obstacle gates while maintaining speed.

> 🎮 **[Download and Play on Google Play Store] (https://play.google.com/store/apps/details?id=com.KNKStudios.ShapeRunner)**

## 📸 Gameplay Preview
*(Add a GIF or 2-3 screenshots of your game here to grab attention instantly!)*
<br>
<img width="483" height="863" alt="18p-shaperunner" src="https://github.com/user-attachments/assets/fb80976f-ac70-44f3-ad65-9c184d3980d0" />
[Uploading 17p-shaperunner.png…]()
<img width="492" height="875" alt="16p-shaperunner" src="https://github.com/user-attachments/assets/11c45bd0-7be1-43c1-8607-e63644e4f2db" />
<img width="492" height="866" alt="14p-shaperunner" src="https://github.com/user-attachments/assets/0ef93816-3a35-44ea-918e-0c44255f76b5" />
<img width="492" height="871" alt="13p-shaperunner" src="https://github.com/user-attachments/assets/4959e32f-d680-43e3-b862-f4477535d2b6" />
<img width="494" height="873" alt="12p-shaperunner" src="https://github.com/user-attachments/assets/62df31d6-7fa0-441a-84fc-d63111512039" />
<img width="489" height="870" alt="19p-shaperunner" src="https://github.com/user-attachments/assets/dac5be28-770e-4b7b-9742-644afc8795a2" />


## 🚀 Key Features
* **Dynamic Shape-Shifting Mechanic:** Instantly transform the player character to match the upcoming gate's shape.
* **Progressive Difficulty:** The game speed and obstacle frequency increase dynamically as the player progresses.
* **Procedural Level Generation:** Endless track generation using custom `ChunkSpawner` logic to spawn grounds, obstacles, and collectible coins infinitely.
* **Coin Collection & Scoring:** Integrated coin collecting system to track the highest score.
* **Optimized for Mobile:** Simple swipe controls and lightweight performance tailored for Android devices.

## 🧠 Technical Highlights & Problem Solving
As a Computer Engineering student, this project was a great opportunity to implement structural game architecture and solve mathematical/physics-based problems in the Unity Engine:

* **Dynamic Collider Management:** Instead of destroying and instantiating colliders (which causes physics engine spikes), the game holds `BoxCollider`, `SphereCollider`, and `CapsuleCollider` simultaneously. The `PlayerShapeController` script dynamically enables the exact collider and adjusts its scale 1:1 with the visual mesh to ensure pixel-perfect collision detection without performance drops.
* **Procedural Spawning & Memory Management:** Implemented a robust `ChunkSpawner` that calculates the `Vector3.forward` position of the last spawned ground block to seamlessly attach the next one. Older chunks are systematically destroyed once they pass a certain distance behind the player to keep memory allocation low and maintain 60 FPS.
* **Scale & Pivot Optimization:** Resolved non-uniform scale distortion issues (especially with rotating coin objects) by nesting visual models and scripts under normalized empty root objects (`Vector3.one` scale and `0,0,0` origin).
* **End-to-End Deployment:** Successfully navigated the full Android deployment pipeline, including Keystore signing, `.aab` building, and navigating the Google Play Console Closed Testing policies.

## 🛠️ Built With
* **Game Engine:** Unity 3D
* **Language:** C#
* **Target Platform:** Android

---
### 👨‍💻 About the Developer
**Hüseyin Ay**
*3rd-Year Computer Engineering Student*
* Passionate about software engineering, full-stack development, and game design.
* Always eager to solve complex problems and learn new technologies.

[LinkedIn]((https://www.linkedin.com/in/h%C3%BCseyin-ay01/) | [Email](huseyin_1153@hotmail.com)
