<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mensaje Especial</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #ffdde1, #ee9ca7);
            font-family: 'Arial', cursive;
            overflow: hidden;
            color: #333;
            position: relative;
        }

        /* Envelope animation */
        #envelope {
            cursor: pointer;
            width: 120px;
            height: 100px;
            position: relative;
            background-color: #fff;
            border: 2px solid #ff6f91;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5em;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
            transition: transform 0.5s ease;
        }

        #envelope:hover {
            transform: scale(1.05);
        }

        .hidden-messages {
            display: none;
            max-width: 85%;
            text-align: center;
            background-color: #ffffffcc;
            padding: 15px;
            border-radius: 10px;
            border: 2px solid #ff6f91;
            box-shadow: 0px 4px 15px rgba(255, 111, 145, 0.3);
            animation: slideDown 1s forwards;
        }

        .message-box {
            display: none;
            font-size: 1.8em;
            color: #5c5c5c;
            margin: 20px auto;
            padding: 15px;
            width: 100%;
        }

        #next-button {
            cursor: pointer;
            font-size: 1.2em;
            color: #fff;
            background-color: #333;
            padding: 10px 20px;
            border: none;
            border-radius: 20px;
            margin-top: 20px;
            transition: background-color 0.3s ease;
            display: none;
        }

        #next-button:hover {
            background-color: #ff6f91;
        }

        /* Animations */
        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInText {
            from {
                opacity: 0;
                transform: scale(0.95);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }
    </style>
</head>
<body>
    <div id="envelope" onclick="openEnvelope()">📨</div>

    <div id="messages-container" class="hidden-messages">
        <div id="message1" class="message-box">Oye, hoy quiero hablarte con el corazón en la mano… pulsa aquí.</div>
        <div id="message2" class="message-box">Desde que apareciste en mi vida, siento que hasta el aire es distinto.</div>
        <div id="message3" class="message-box">Eres mi sorpresa favorita, y agradezco al destino cada día por cruzarnos.</div>
        <div id="message4" class="message-box">Cuando pienso en ti, no solo me siento feliz; siento que mi vida está mejor enfocada.</div>
        <div id="message5" class="message-box">Tú le das sentido a los pequeños momentos, y eso es un regalo raro y valioso.</div>
        <div id="message6" class="message-box">Hay días en que me asombra cómo una persona puede hacer que el mundo se sienta en calma.</div>
        <div id="message7" class="message-box">No sabes el orgullo que siento de coincidir contigo; eres de esas personas que no se encuentran dos veces.</div>
        <div id="message8" class="message-box">Ser testigo de tu vida y de tu fuerza es uno de mis mayores privilegios.</div>
        <div id="message9" class="message-box">Si alguien merece lo mejor en este mundo, eres tú, por lo especial y auténtica que eres.</div>
        <div id="message10" class="message-box">Mi Yavi, por más lejos que estés, sigues siendo esa persona que le da sentido a todo. Te quiero y me siento bendecido de ser parte de tu historia. 🫶</div>
        
        <button id="next-button" onclick="showNextMessage()">Pulsa aquí para descubrir más</button>
    </div>

    <script>
        let currentMessage = 1;

        function openEnvelope() {
            document.getElementById("envelope").style.display = "none";
            document.getElementById("messages-container").style.display = "block";
            document.getElementById("next-button").style.display = "inline-block";
            showNextMessage();
        }

        function showNextMessage() {
            // Oculta el mensaje anterior si existe
            if (currentMessage > 1) {
                document.getElementById(message${currentMessage - 1}).style.display = 'none';
            }
            // Muestra el mensaje actual
            document.getElementById(message${currentMessage}).style.display = 'block';
            currentMessage++;
            
            // Oculta el botón después del último mensaje
            if (currentMessage > 10) {
                document.getElementById("next-button").style.display = 'none';
            }
        }
    </script>
</body>
</html>
