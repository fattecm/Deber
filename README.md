Deber
=====

Deberes de Web
<!DOCTYPE html>
<!--
Esta página va a indicar si el dato introducido es primo, o no primo.
-->
<html>
    <head>
        <title>Primo o No Primo</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <h1><center>Verificación de número primo</center></h1>
    </head>
    <body>
     
         <div id="divContenido"> </div>
         <h3>Ingrese un número para comprobar si es primo </h3>
        <!-- insertamos un cuadro tipo texto para introducir el dato a validar -->
        <input type="text" id="txtdato" name="txtdato" /> 
        <!-- insertamos un boton para llamar a la función -->
        <input type="button" name="btn_verificar" id="btn_verificar" value="Obtener Resultado" onClick="esPrimoMio()" />
        <!-- Otro cuadro tipo texto, para mostrar el mensaje si es primo o no -->
        <br/>Resultado <input type="text" name="resultado" id="resultado"/>
    </body>
    <footer>
			<small>
                            <br/>
                            <br/>
                            <br/>
				Documento realizado 27 de Abril del 2014 <br/>
				Autor Fátima Carrillo Morán
			</small>
    </footer>
</html>
<!-- Scritp q cmprueba si un numero es primo, es decir si es divisible
por uno y por si mismo unicamente -->

<script>
function esPrimoMio()
{
    var dato="";
    //guardamos en la variable dato, lo que se haya introducido en txtdato
    dato=document.getElementById("txtdato").value;
    //convertimos dato a entero
    dato=parseInt(dato);
    //declaramos e inicializamos la varible divisores, para ir guardando cuantas
    //veces se divide el dato 
    var divisores = 2;
    for ( j = 2; j<dato ; j++){
        if (dato%j == 0){
        divisores++;
        break;
        }
    }
    //Si divisores=2, quiere decir que si es primo, ya que se divide por si mismo
    // y por la unidad
    if (divisores == 2){
        document.getElementById('resultado').value = 'ES primo';
    //caso contrario no es primo
    }else{
            document.getElementById('resultado').value = 'NO es primo';
         }
}

</script>
