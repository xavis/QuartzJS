QuartzJS
========

Light and simple WebGL motor
Uses K3D.js and GL-MATRIX

This is a little project for creating a light webgl library for web and smartphone use.
It is easy to use, the scene is based in a tree structure where the nodes represents transformations, shapes, lights...

Here a simple example where we load an object and traslate and rotate it:

  	var root = QUARTZ.getRoot();
  
  	var trans = QUARTZ.createTransform();
  	trans.setTraslation(0,0,-7);
  	trans.addRotation(90, [1,0,0]);
  	trans.setScale(2);
  
  	var shape = QUARTZ.createMesh();
  	shape.loadModel("Object.obj);
  	shape.color = [1,0,0,1]; //RGBA
  	shape.loadTexture("texture.png");
  
  	var light = QUARTZ.createLight();
	light.setLight([0.2,0.2,0.2],[0.2,0.2,0.2],0.4,[0,0,0],[-4.4,10,-5],20); //(AMBIENTAL COLOR, DIFFUSE COLOR, SPECULAR FACTOR, DIRECTION, POSITION, INTENSITY)
  
  	QUARTZ.addLight(light,root);
  
  	var transNode = QUARTZ.addTransform(trans,root);
  
  	var shapeNode = QUARTZ.addMesh(shape,root);
  
  	QUARTZ.init("webGL"); // "webGL" is canvas ID attribute value
  
  

QuartzJS is open for anyone who wants help me with it to join QuartzJS project.

Website: quartzjs.javiersr.com

Email: info@javiersr.com
