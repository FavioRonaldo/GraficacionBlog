---
title: Formulario
---

<html lang="en">
<head>
 
</head>
<body>

<p>FORMULARIO: </p>

Nombre: <input type="text" id="fname" onkeyup="myFunction()">
<p id="nombre" style="color:Tomato;"></p>
Apellido: <input type="text" id="fapellido" onkeyup="myFunction2()">
<p id="apellido" style="color:Tomato;"></p>
Email: <input type="text" id="femail" onkeyup="email()">
<p id="email" style="color:Tomato;"></p>
Fecha Nacimiento: <input type="date" name="user_date" id="user_date" value="1995-01-01" />
<p>SEXO: </p>
<select id="mySelect" size="2" >
  <option>Masculino</option>
  <option>Femenino</option>
</select>
<p id="demo">
Ingrese el mesaje: </p>
<textarea id="msj" name="msj" requiered></textarea>


<script>
function myFunction() {
  var name = document.getElementById("fname").value;
  
  if (!(/^([a-zA-Z])*$/.test(name)))  {
  	if(!(/^([a-zA-Z]+ +[a-zA-Z]{3,10})*$/.test(name))){
  	document.getElementById("nombre").innerHTML = "Error en el campo nombre";
  	document.getElementById("nombres").style.color="red";
  	/*document.getElementById("nombre").style.="red";*/
  }else
 	document.getElementById("nombre").innerHTML ="";	
 }
}

function myFunction2() {
var apellido = document.getElementById("fapellido").value;
if (!(/^[a-zA-Z]*$/.test(apellido))){
      if(!(/^([a-zA-Z]+ +[a-zA-Z]{3,10})*$/.test(apellido))){
  document.getElementById("apellido").innerHTML = "Error en Campo Apellido";
 
/*txt = "Error en Campo Apellido";*/
}else
  document.getElementById("apellido").innerHTML ="";
}
}
function email(){
	var valor = document.getElementById("femail").value;
if( !(/^\w+([-+.']\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/.test(valor)) ) {
  document.getElementById("email").innerHTML = "Error en Campo Apellido";
}else
    	document.getElementById("email").innerHTML ="";

}
</script>

</body>
</html>