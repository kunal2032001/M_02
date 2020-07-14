# M_02


Welcome to M_02

 
Life Saving Application For Public Tansportation

Project scope
IBM cloud
Create node-red service
Using MIT app inventor
Model building
Application building
App is completed
code for making Registration form using IBM Node-Red
:[{"id":"1bb3e4ac.a9bc03","type":"tab","label":"cloudant","disabled":false,"info":""},{"id":"1baea7c.3d87dd8","type":"ui_form","z":"1bb3e4ac.a9bc03","name":"","label":"","group":"693597ca.ce9c78","order":0,"width":0,"height":0,"options":[{"label":"Enter Name","value":"Name","type":"text","required":true,"rows":null},{"label":"Enter email","value":"email","type":"email","required":true,"rows":null},{"label":"Enter Password","value":"pwd","type":"password","required":true,"rows":null},{"label":"Enter phone number","value":"phno","type":"number","required":true,"rows":null},{"label":"Enter the gender","value":"gender","type":"text","required":true,"rows":null}],"formValue":{"Name":"","email":"","pwd":"","phno":"","gender":""},"payload":"","submit":"submit","cancel":"cancel","topic":"","x":210,"y":140,"wires":[["3ec41889.d304a8","2ab04229.26784e"]]},{"id":"135b856.180037b","type":"cloudant out","z":"1bb3e4ac.a9bc03","name":"","cloudant":"","database":"tushar","service":"node-red-tsshw-cloudant-1591678574539-2509","payonly":true,"operation":"insert","x":500,"y":60,"wires":[]},{"id":"3ec41889.d304a8","type":"function","z":"1bb3e4ac.a9bc03","name":"","func":"msg.payload = {\n    _id:msg.payload.email,\n    Name:msg.payload.name,\n    Gender:msg.payload.gender,\n    Phonenumber:msg.payload.phno,\n    Password:msg.payload.pwd,\n    \n    \n    \n    \n}\nreturn msg;","outputs":1,"noerr":0,"x":340,"y":60,"wires":[["135b856.180037b"]]},{"id":"2ab04229.26784e","type":"function","z":"1bb3e4ac.a9bc03","name":"","func":"msg.payload= \"Hey\"+msg.payload.name+\". Registration is successful\"\nreturn msg;","outputs":1,"noerr":0,"x":300,"y":240,"wires":[["c57b85d0.1e0318"]]},{"id":"c57b85d0.1e0318","type":"ui_text","z":"1bb3e4ac.a9bc03","group":"693597ca.ce9c78","order":1,"width":0,"height":0,"name":"","label":"text","format":"{{msg.payload}}","layout":"row-spread","x":500,"y":220,"wires":[]},{"id":"693597ca.ce9c78","type":"ui_group","z":"","name":"ragistration","tab":"fbd49a34.ae3ad","order":1,"disp":true,"width":"6","collapse":false},{"id":"fbd49a34.ae3ad","type":"ui_tab","z":"","name":"student","icon":"dashboard","disabled":false,"hidden":false}]
