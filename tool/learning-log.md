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

<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
