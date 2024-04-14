# Entry 5: Learning A-Frame
##### 4/8/24

### A-Frame
Throughout the *LOYO* (Learn On Your Own) process, I have learned a lot more about my tool, **A-Frame**, and the way it works. I mainly used the [**A-Frame**](https://aframe.io/docs/1.5.0/introduction/) documents and watched [this](https://www.youtube.com/playlist?list=PLP3KjR1TMw7ekqC4o5gy0rR4odw7Jga84) tutorial series to figure out how **A-Frame** works. The main documents I used were "[Building a Basic Scene](https://aframe.io/docs/1.5.0/guides/building-a-basic-scene.html)", "[HTML & Primitives](https://aframe.io/docs/1.5.0/introduction/html-and-primitives.html)", "[Entity-Component-System](https://aframe.io/docs/1.5.0/introduction/entity-component-system.html)", and "[Mixins](https://aframe.io/docs/1.5.0/core/mixins.html)". The main videos that helped me from the tutorial series were "[Transformations, Primitives & Textures](https://www.youtube.com/watch?v=mETucqeOmXA&list=PLP3KjR1TMw7ekqC4o5gy0rR4odw7Jga84&index=2)", "[ECS Architecture](https://www.youtube.com/watch?v=qB8Ejh_QdpE)", "[Cursor and Gaze Controls](https://www.youtube.com/watch?v=r_pq9EuE-o0&list=PLP3KjR1TMw7ekqC4o5gy0rR4odw7Jga84&index=11)", and "[Mixins](https://www.youtube.com/watch?v=UjvvtIQwaqo&list=PLP3KjR1TMw7ekqC4o5gy0rR4odw7Jga84&index=11)". The documents helped me understand how to incorporate different things and make them function and the videos showed me how to write the code and understand more. I learned many things about **A-Frame** such as how to incorporate `assets`(textures/images for the background or scene), add `text` to the scene, and use `entities`, `primitives`, and `components`. Other useful things I learned were how to `animate` entities and use `id`s to make entities similar but different and created scenes on [*Glitch*](https://glitch.com/).

I tried to create my own scene using spheres, a ring, a box, a octahedron, and using animations.
```HTML
<a-scene>
  <a-box position="0 -1.5 0" rotation="0 45 0" color="#4CC3D9"></a-box>
  <a-ring color="teal" radius-inner="0.5" radius-outer="1" position="0 0 0" width="20"></a-ring>
  <a-octahedron color="red" radius="1" position="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000"></a-  octahedron>
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

Another thing I learned was how to use `mixins` which are used to set `id`s for entities that you want to be the same or have similar properties. I made this scene using `mixins` and other properties:
```HTML
<a-scene>
  <a-camera position="0 1 3"
    ><a-entity
      cursor="fuse: true; fuseTimeout: 1000;"
      geometry="primitive: box; width: 0.1; height:0.1; depth:0.5;"
      material="color: pink;"
      position="0 0 -2"
      animation__fusing="property: scale; from: 1 1 1; to: 0.5 0.5 0.5; startEvents: fusing;"
      animation__reset="property: scale; to: 1 1 1; startEvents: mouseleave"
    ></a-entity
  ></a-camera>
  <a-assets>
    <a-mixin id="red" material="color: red"></a-mixin>
    <a-mixin id="blue" material="color: blue"></a-mixin>
    <a-mixin id="cube" geometry="primitive: box"></a-mixin>
    <a-mixin id="sphere" geometry="primitive: sphere"></a-mixin>
    <a-mixin
      id="cylinder"
      geometry="primitive: cylinder; height: 1.5;"
    ></a-mixin>
  </a-assets>

  <a-entity
    mixin="red cube"
    position="0 -0.5 -3"
    animation="property:rotation; from: 0 0 0; to: 0 360 0; dur: 2000; startEvents: click;"
  ></a-entity>
  <a-entity
    mixin="blue sphere"
    animation="property: position; from: 0 0 0; to: 0 0 -6; dur: 5000; startEvents: click;"
  ></a-entity>
  <a-entity
    mixin="red cylinder"
    position=" 3 0 -3"
    animation="property: rotation; from: 0 0 0; to: 360 0 0; dur: 2000; startEvents:click;"
  ></a-entity>
  <a-entity
    mixin="red blue cylinder"
    position=" -3 0 -3"
    animation="property: position; from: -3 0 -3; to: 3 0 -3; dur: 5000; startEvents: click;"
  ></a-entity>
  <a-entity mixin="blue red cylinder sphere" position="0 0 -6"></a-entity>

  <a-plane
    position="0 -1 -3"
    rotation="-90 0 0"
    width="10"
    height="10"
    color="#7BC8A4"
  ></a-plane>
</a-scene>
```


### Skills
A skill I have improved on while learning **A-Frame** is **Attention to detail**. When coding, it was very important to spell everything correct or else it won't work or appear in the preview. I misspelled some words which made me think that I used the wrong code. After looking back at the videos and examples, I realized that I didn't spell things like `property` correctly or I was missing a `;` so I fixed it and made sure everything was good.

Another skill I have developed more is **Organization**. While learning **A-Frame**, we had to keep track of the resources we used and what we changed/tinkered with. We did this in a file (*learning-log.md*) and I used bullet points and indented the information that was part of the bullet point. I also labeled the day I tinkered and kept *code snippets* of what I made in each day.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
