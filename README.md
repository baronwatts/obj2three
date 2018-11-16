# obj2three
mrdoob's three.js blender exporter
Steps to use:
1) Put this script and your .obj and .mlt in the same folder<br>
2) Open your terminal in that same folder and type: python conversion.py -i <b>yourfilename</b>.obj -o <b>yourfilename</b>.js -b <br>
3) Just substitute <b>yourfilename</b> with the name of you file<br>

loader = new THREE.JSONLoader();
loader.load('yourfile.js', function (geometry, materials) {
    var matt = new THREE.MeshLambertMaterial( { vertexColors: THREE.FaceColors, side: THREE.DoubleSide } );
    var obj =  new THREE.Mesh(geometry, matt);
    obj.position.set(0, 0, 0 );
    obj.scale.set(1,1,1);
    scene.add(obj);
 });
