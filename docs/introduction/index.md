<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Model with A-Frame</title>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <style>
        body { margin: 0; }
        #model { width: 100%; height: 100vh; }
    </style>
</head>
<body>
    <a-scene id="model">
        <a-assets>
            <!-- Загрузка модели в формате GLTF или OBJ -->
            <a-asset-item id="my-model" src="path/to/your/model.gltf"></a-asset-item>
        </a-assets>

        <!-- Добавление модели в сцену -->
        <a-entity gltf-model="#my-model" position="0 1.5 -3" scale="1 1 1"></a-entity>

        <!-- Освещение -->
        <a-light type="ambient" color="#FFFFFF"></a-light>
        <a-light type="directional" position="-1 1 1" intensity="0.5"></a-light>

        <!-- Камера -->
        <a-entity camera look-controls position="0 1.6 0"></a-entity>
        
        <!-- Земля (можно убрать или изменить) -->
        <a-plane position="0 0 -4" rotation="-90 0 0" width="10" height="10" color="#7BC8A4"></a-plane>
    </a-scene>
</body>
</html>
