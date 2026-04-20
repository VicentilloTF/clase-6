<!doctype html>

<title>Un fetch</title> <style> body { font-family: Helvetica, Arial, sans-serif;
        }
		
		table {
			border-collapse: collapse;
			text-align:left
			
		}
		
		td, th{
			border:1px solid black; 
			padding: 1 rem;
		}
    </style>
</head>
<body>
    <h1>MIS ELECTIVOS</h1>
	<table>
		<thead>
			<tr>
				<th>Código</th>
				<th>Asignatura</th>
				<th>Nivel</th>
				<th>Mención</th>
				<th>Grupo</th>
				<th>Enfoque</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<th>AUD5V027</th>
				<th>Diseño y visualización de información</th>
				<th>Troncal</th>
				<th>V y M</th>
				<th>Comunicación y Gestión del Diseño</th>
				<th>Comunicación Visual Estratégica</th>
			</tr>
			<tr>
				<th>AUD6V020</th>
				<th>Diseño editorial y publicación</th>
				<th>Troncal</th>
				<th>V y M</th>
				<th>Comunicación y Gestión del Diseño</th>
				<th>Gestión de publicidades</th>
			</tr>
			<tr>
				<th>AUD7V021</th>
				<th>Diseño de interacción y experiencia</th>
				<th>Troncal</th>
				<th>V y M</th>
				<th>Comunicación y Gestión del Diseño</th>
				<th>Diseño de Servicios y Experiencia</th>
			</tr>
			<tr>
				<th>AUDIV025</th>
				<th>La interacción del Color; su anatomía y lenguaje</th>
				<th>Abierto</th>
				<th>Ambas</th>
				<th>Morfología</th>
				<th>Teoría y Aplicación del Color (CMF)</th>
			</tr>
			<tr>
				<th>AUD7V015</th>
				<th>Ilustración editorial</th>
				<th>Abierto</th>
				<th>V y M</th>
				<th>Morfología</th>
				<th>Composición Editorial y Tipográfica</th>
			</tr>
		</tbody>
	</table>

    <script>
	
		const t = document.querySelector("table");
		
        const URL = "https://api.myjson.online/v1/records/7325f0a0-fa43-4e9b-bc5d-069ce1ca5c80";
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
				trabajo.forEach((x) => {
					if(x.ok == 1 1){
						t.innerHTML += `<tr><td>${x.name}</td><td>${x.group}</td><td>${focus}</td><tr>´ ;
					}
				}};
            })

            .catch((error) => {
                console.error("Algo salió mal:", error);
            });
    </script>
</body>

