# Tool Learning Log

Tool: **A-Frame**

---

2/26/24:
* [This](https://aframe.io/docs/1.5.0/guides/building-a-basic-scene.html) shows how to build a basic scene
  * Helped understand how to add text to a scene
  * Incorporate links for the possibility of different scenarios
* [This](https://aframe.io/docs/1.5.0/introduction/html-and-primitives.html) helped me understand primitives and entity components.
* Next I plan to try to create my own scene


3/4/24:
* Today I tried using different primitives
```HTML
<a-scene>
 <a-box color="red" position="-1 0.5 -3"></a-box>
 <a-tetrahedron color="red" position="0 0 0" radius="5"></a-tetrahedron>
 <a-octahedron color="#FF926B" material.height="1" material.width="1" radius="5"></a-octahedron>
 <a-plane color="#CCC" height="10" width="20"></a-plane>
 <a-plane src="#ground" height="20" width="30" position="1 1 1" rotation="-90 0 0"></a-plane>
 
 <a-camera position="0 0 0"></a-camera>
</a-scene>
```

3/10/24:
* I tried adding some different components
```HTML
<a-scene fog="type: linear; color: #AAA">
 <a-entity light="color: #AFA; intensity: 1.5" position="-1 1 0"></a-entity>
 <a-box position="-1 0.5 -3" rotation="0 45 0" color="black"></a-box>
 <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
 <a-cylinder
    position="1 0.75 -3"
    radius="0.5"
    height="1.5"
    color="#FFC65D"
 ></a-cylinder>
 <a-plane
    position="0 0 -4"
    rotation="-90 0 0"
    width="4"
    height="4"
    color="#7BC8A4"
 ></a-plane>
</a-scene>
```
3/11/24:
* I added animated boxes and a ground
```HTML
  <a-scene>
      <a-cylinder id="ground" src="https://cdn.aframe.io/a-painter/images/floor.jpg" radius="100" height="0.1"></a-cylinder>
      <a-assets>
      <img id="texture" src="texture.png">
      </a-assets>

      <a-box src="#texture" position="0 1 0" ></a-box>
      <a-box position="0 1 0" animation="property: position; to: 0 1 5; dur: 2000; easing: linear; loop: true" color="green"></a-box>
      <a-box position="0 1 0" animation="property: position; to: 0 1 -5; dur: 2000; easing: linear; loop: true" color="red"></a-box>
      <a-box position="0 1 0" animation="property: position; to: -5 1 0; dur: 2000; easing: linear; loop: true" color="black"></a-box>
      <a-box position="0 1 0" animation="property: position; to: 5 1 0; dur: 2000; easing: linear; loop: true" color="white"></a-box>
    
  </a-scene>

```

3/17/24:
* I tried to create my own scene using spheres, a ring, a box, a octahedron, and animated them.
```HTML
    <a-scene>
      <a-box position="0 -1.5 0" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-ring color="teal" radius-inner="0.5" radius-outer="1" position="0 0 0" width="20"></a-ring>
      <a-octahedron color="red" radius="1" position="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000"></a-octahedron>
      <a-ring color="teal" radius-inner="9.7" radius-outer="11" position="0 0 0"></a-ring>
      
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 0 0" color="blue"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 5 0" color="orange"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 5 5" color="white"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="0 0 5" color="red"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="0 5 5" color="green"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 0 5" color="yellow"></a-sphere>
      </a-entity>

      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="-5 0 0" color="blue"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="-5 5 0" color="orange"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="-5 5 -5" color="white"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="0 0 -5" color="red"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="0 5 -5" color="green"></a-sphere>
      </a-entity>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="-5 0 -5" color="yellow"></a-sphere>
      </a-entity>
      
      <a-plane
        position="0 -2 0"
        rotation="-90 0 0"
        width="19"
        height="17"
        color="black"
      ></a-plane>

      <a-sky color="grey"></a-sky>
    </a-scene>
```

3/18/24:
* Today I watched this [video](https://www.youtube.com/watch?v=mETucqeOmXA&list=PLP3KjR1TMw7ekqC4o5gy0rR4odw7Jga84&index=2).
  * It showed me how I can add assets like textures and images
  * It also showed me how to open the inspector for A-Frame (ctrl + alt + i).
  * How to make some components the child of others
```HTML
      <a-octahedron color="red" radius="1" position="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-ring color="teal" radius-inner="0.8" radius-outer="1.2" position="0 0 0" width="20" material="side: double"></a-ring>
      </a-octahedron>
```
* This made the ring rotate and move with the octahedron

3/23/24:
* I watched [this](https://www.youtube.com/watch?v=qB8Ejh_QdpE) video and read [this](https://aframe.io/docs/1.5.0/introduction/entity-component-system.html) document on the Entity-Component-System
  * Entity - containers that require things like components and give more flexibility than primitives.
  * Component - reusable modules that provide appearance, behavior, and functionality.

4/1/24:
* I tried using the `<a-entity>` tag.
```HTML
      <a-entity geometry="primitive:box" material="color:red" position="0 1 -2"></a-entity>
      <a-entity geometry="primitive:box" material="color:green" position="0 2 -2"></a-entity>
      <a-entity geometry="primitive:box" material="color:orange" position="0 3 -2"></a-entity>
      <a-entity geometry="primitive:box" material="color:yellow" position="0 4 -2"></a-entity>
      <a-entity geometry="primitive:box" material="color:pink" position="0 5 -2"></a-entity>
      <a-entity geometry="primitive:box" material="color:purple" position="0 6 -2"></a-entity>
      <a-entity geometry="primitive:box" material="color:gray" position="0 7 -2"></a-entity>
      <a-entity geometry="primitive:box" material="color:cyan" position="0 8 -2"></a-entity>

```


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
