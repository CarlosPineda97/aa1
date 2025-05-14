<!DOCTYPE html>
<html lang="es">
    <head>

        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Fuerza De Seguridad Privada</title>
        <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
        
        <style>

            body { /*Fondo del Formulairo*/
                font-family: 'Poppins', sans-serif;
                background-color: #1e5fa0;
                display: flex;
                flex-direction: column;
                align-items: center;
                height: 100vh;
                margin: 5;               
                text-align: center;
                overflow-x: hidden;
            }

            .navbar {
                width: 100%; /* Esto hace que ocupe todo el ancho de la pantalla */
                background: #FFC107;
                padding: 10px;
                text-align: center;
                box-shadow: 1px 4px 6px rgba(10, 10, 10, 0.1); /* Corrige el valor de opacidad */
                position: absolute; /* Para que se quede fija en la parte superior */
                top: 0; /* Ajusta la barra a la parte superior */
                left: 0; /* Asegura que ocupe todo el ancho */
            }


            .navbar a {/* Letras de la Franja*/
                color: #000000;
                text-decoration: none;
                margin: 0 20px;
                font-size: 18px;
                font-weight: 600;
            }

            .navbar a:hover {
                text-decoration: underline;
            }

            .container {
                padding: 15px;
                border-radius: 5px;
                box-shadow: 0 4px 15px rgba(17, 255, 9, 0.3);
                width: 90%; /* Aumenta el ancho relativo */
                max-width: 1000px; /* Aumenta el ancho máximo permitido */
                margin-top: 70px;
                color: rgb(0, 0, 0);
                text-align: center;
                background: #ffffff;
            }


            h2 {
                text-align: center;
                font-weight: 600;
            }

            input, select, button, textarea {/* Tamañno y forma de los formularios*/
                width: 85%;
                padding: 10px;
                margin: 8px 0;
                border: 2px solid  #FFC107;
                border-radius: 10px;
                font-size: 15px;
            }

            button {
                background: #0839ea;
                color: rgb(255, 255, 255);
                border: none;
                cursor: pointer;
                font-size: 14px;
                padding: 10px;
                border-radius: 8px;
                transition: 0.5s;
                width: 200px;
                
            }

            button:hover { /*Cuando se selecciona el boton*/
                background-color: #FFC107;
                color: rgb(0, 0, 0);                
            }         

            .dropdown {
                position: relative;
                display: inline-block;
            }
                
            .dropdown-content {
                display: none;
                position: absolute;
                background-color: white;
                min-width: 200px;
                box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2);
                padding: 10px;
                border-radius: 5px;
            }
                
            .dropdown:hover .dropdown-content {
                display: block;
            }
                
            label {
                display: block;
                cursor: pointer;
            }
                
            .selected-items {
                display: block;
                margin-top: 10px;
                font-weight: bold;
            }

        </style>

    </head>
    <body>
       
        
        <div class="navbar">            
            <a href="listado.html">Listado</a>
            <a href="armas.html">Armas</a>
            <a href="Quejas.html">Quejas de Guardias</a>
            <a href="Papeleria.html">Papeleria Importante</a>
             <a href="Guardia.html">Buscar Guardia</a>
            
        </div>
        
        <div class="container">
            <img src="img-FUSEPRI.jpg" alt="Logo" style="width: 200px; height: 200px; object-fit: cover; border-radius: 10px;">

            <form method="post" action="https://script.google.com/macros/s/AKfycbxD4MIUYEuKwYqqwKE-rJxi3MKMKU8F3EnccIvn2lxte55qfdg6WrQjHPDkxzw7T6zZYQ/exec">
                <input type="hidden" name="formulario" value="personas">                           
                
                <h2>Formulario Guardias</h2>

                <label>Nombre completo:</label>
                <input type="text" name="nombre">
              
                <label>ID:</label>
                <input type="number" name="cedula">
              
                <label>Teléfono:</label>
                <input type="number" name="telefono">
              
                <label>Dirección:</label>
                <input type="text" name="direccion">
              
                <label>Fecha de ingreso:</label>
                <input type="date" name="fecha" required>
              
                <label>Puesto asignado:</label>
                <select name="puesto" required>
                  <option value="" disabled selected hidden>Seleccione el puesto</option>
                  <option>Halcón 1</option>
                  <option>Halcón 2</option>
                  <option>Halcón 3</option>
                </select>
              
                <label>Número de emergencia:</label>
                <input type="number" name="emergencia" placeholder="Número">
                <input type="text" name="pertenece" placeholder="Pertenece a">

                <label>Número de emergencia:</label>
                <input type="number" name="emergencia1" placeholder="Número">
                <input type="text" name="pertenece1" placeholder="Pertenece a">

                <label>Número de emergencia:</label>
                <input type="number" name="emergencia2" placeholder="Número">
                <input type="text" name="pertenece2" placeholder="Pertenece a">
              
                <label>Estado civil:</label>
                <select name="estado">
                  <option value="" disabled selected hidden>Seleccione estado civil</option>
                  <option>Soltero</option>
                  <option>Casado</option>
                  <option>Unión libre</option>
                </select>
              
                <label>Tiene hijos</label>
                <select name="tieneHijos" onchange="toggleHijos(this)">
                  <option value="" disabled selected hidden>Seleccione</option>
                  <option>Sí</option>
                  <option>No</option>
                </select>
              
                <div id="cantidadHijos" style="display:none">
                  <label>¿Cuántos hijos?</label>
                  <input type="number" name="cantidadHijos" min="0">
                </div>
              
                <label>Papeles pendientes:</label>
                <select name="papeles">
                  <option value="" disabled selected hidden>Papeles pendientes</option>
                  <option>Ninguno</option>
                  <option>Policiales</option>
                  <option>Penales</option>
                  <option>Ambos</option>
                </select>
              
                <label>Descripción adicional:</label>
                <textarea name="descripcion" rows="3"></textarea>
                <button type="submit">Guardar Información</button>
              
                
            </form>

                        

        </div>     
       
    </body>
</html>
