[index.html](https://github.com/user-attachments/files/26729302/index.html)
# clase-6<!doctype html>
<html lang="es">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>Un fetch</title>
        <style>
            body {
                font-family: Helvetica, Arial, sans-serif;
            }
			table {
			border-collapse: collapse;
			text-align: left;
			}
			td, th{
			border:1px solid black;
			padding: 1 rem;
			}
        </style>
    </head>
    <body>
        <h1>Mis electivos 𖤐</h1>
		<table>
		<thead>
		<tr>
		<th>Asignatura<th>
		<th>Grupo<th>
		<th>Enfoque<th>
		</thead>
		<tbody></tbody>
		</table>

        <script>
            const t= document.querySelector("tbody");
			
			
			const URL = "https://api.myjson.online/v1/records/3fadbf5e-b32a-462f-8264-e317a5672946";
            fetch(URL)
                .then((respuesta) => {
                    if (!respuesta.ok) {
                        throw new Error("Error HTTP: " + respuesta.status);
                    }
                    return respuesta.json();
                })

                .then((datos) => {
                    var trabajo = datos;
                    console.log("Datos recibidos:", trabajo);
                })

                .catch((error) => {
                    console.error("Algo salió mal:", error);
                });
        </script>
    </body>
</html>
