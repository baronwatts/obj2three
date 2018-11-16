# obj2three
mrdoob's three.js blender exporter
Steps to use:
1) Put this script and your .obj and .mlt in the same folder<br>
2) Open your terminal in that same folder and type: <b>python conversion.py -i yourfilename.obj -o yourfilename.js -b</b> <br>
3) Just substitute <b>yourfilename</b> with the name of you file<br>

<script src="https://threejs.org/examples/js/loaders/AssimpJSONLoader.js"></script><br>
var loader = new THREE.JSONLoader();<br>
loader.load('yourfilename.js', function (geometry, materials) {<br>
    var matt = new THREE.MeshLambertMaterial( { vertexColors: THREE.FaceColors, side: THREE.DoubleSide } );<br>
    var obj =  new THREE.Mesh(geometry, matt);<br>
    obj.position.set(0, 0, 0 );<br>
    obj.scale.set(1,1,1);<br>
    scene.add(obj);<br>
 });
