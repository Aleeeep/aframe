<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Mi primer mundo 3D</title>
    <script src="https://aframe.io/releases/1.4.2/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-event-set-component@3.0.3/dist/aframe-event-set-component.min.js"></script>

  </head>
  <body>
   
    <a-scene>
      <!--<a-box position="-1 0.5 -3" color="#4CC3D9" rotation="0 45 0"></a-box>-->
      <a-box
        position="-2 0.5 -2"
        color="#4CC3D9"
        event-set__click="color: #ff0000"
        animation__click="property: scale; to: 1.5 1.5 1.5; startEvents: click; dur: 300">
      </a-box>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"
           event-set__enter="_event: mouseenter; color: #8FF7FF"
           event-set__leave="_event: mouseleave; color: #ff0000"></a-box>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"
                event-set__enter="_event: mouseenter; _target: #cylinderText; visible: true"
                event-set__leave="_event: mouseleave; _target: #cylinderText; visible: false">
        <a-text id="cylinderText" value="Hola Hola" align="center" color="#FFF" visible="false" position="0 -0.55 0.55"
              geometry="primitive: plane; width: 1.75" material="color: #333"></a-text>
      </a-cylinder>
      <a-assets>
        <a-asset-item id="cityModel" src="https://cdn.aframe.io/test-models/models/glTF-2.0/virtualcity/VC.gltf"></a-asset-item>
      </a-assets>
      <a-entity gltf-model="#cityModel" modify-materials></a-entity>
     
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
      <a-plane rotation="-90 0 0" width="10" height="10" color="#7BC8A4"></a-plane>
      <!--<a-sky color="#ECECEC"></a-sky>-->
      <a-sky src="passendorf_snow.webp"></a-sky>
      <a-camera>
        <a-cursor></a-cursor>
      </a-camera>
         <a-assets>
        <a-asset-item id="cityModel" src="https://cdn.aframe.io/test-models/models/glTF-2.0/virtualcity/VC.gltf"></a-asset-item>
      </a-assets>
      <a-entity gltf-model="#cityModel" modify-materials></a-entity>

    </a-scene>  </body>
</html>
