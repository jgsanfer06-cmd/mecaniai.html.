# mecaniai.html.
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>MecaniAI - Diagnóstico Inteligente</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f1f1f1;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 700px;
            background: white;
            padding: 20px;
            border-radius: 15px;
            margin: auto;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        textarea {
            width: 100%;
            height: 120px;
            padding: 10px;
            border-radius: 10px;
            border: 1px solid #ccc;
            font-size: 16px;
        }
        button {
            width: 100%;
            padding: 12px;
            background: #007bff;
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            cursor: pointer;
        }
        button:hover {
            background: #0056b3;
        }
        .resultado {
            margin-top: 20px;
            padding: 15px;
            background: #e9f5ff;
            border-left: 5px solid #007bff;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>MecaniAI</h1>
        <p>Ingresa los síntomas de la máquina para obtener un diagnóstico inteligente.</p>

        <textarea id="inputSintomas" placeholder="Ejemplo: vibración fuerte y ruido metálico..."></textarea>
        <br><br>
        <button onclick="diagnosticar()">Diagnosticar</button>

        <div id="resultado" class="resultado" style="display:none;"></div>
    </div>

    <script>
        function diagnosticar() {
            const texto = document.getElementById('inputSintomas').value.toLowerCase();
            let fallo = "No se pudo determinar el fallo con la información proporcionada.";
            let recomendacion = "Intenta describir más síntomas.";

            if (texto.includes("vibra") && texto.includes("ruido")) {
                fallo = "Desgaste en rodamientos";
                recomendacion = "Lubricar o reemplazar rodamientos y verificar alineación del eje.";
            }
            else if (texto.includes("temperatura") || texto.includes("calienta")) {
                fallo = "Sobrecalentamiento del motor";
                recomendacion = "Revisar ventilación, carga mecánica y sistema eléctrico.";
            }
            else if (texto.includes("potencia") || texto.includes("fuerza")) {
                fallo = "Pérdida de eficiencia o desgaste interno";
                recomendacion = "Revisar transmisión, bandas, y nivel de lubricación.";
            }
            else if (texto.includes("chispa") || texto.includes("eléctrico")) {
                fallo = "Falla eléctrica o cortocircuito";
                recomendacion = "Inspeccionar cableado, aislamiento y fusibles.";
            }

            document.getElementById('resultado').style.display = 'block';
            document.getElementById('resultado').innerHTML = `
                <h3>Diagnóstico Probable:</h3>
                <p><strong>${fallo}</strong></p>
                <h3>Recomendación:</h3>
                <p>${recomendacion}</p>
            `;
        }
    </script>
</body>
</html>
