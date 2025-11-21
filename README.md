<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cartel: Juego Limpio Dentro y Fuera de la Cancha</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }
        
        .poster {
            width: 100%;
            max-width: 1000px;
            background-color: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            position: relative;
        }
        
        .header {
            background: linear-gradient(to right, #1a2a6c, #b21f1f);
            color: white;
            padding: 25px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                to bottom right,
                rgba(255,255,255,0) 0%,
                rgba(255,255,255,0.1) 50%,
                rgba(255,255,255,0) 100%
            );
            transform: rotate(30deg);
            animation: shine 8s infinite linear;
        }
        
        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(30deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(30deg); }
        }
        
        .header h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            position: relative;
        }
        
        .header p {
            font-size: 1.2rem;
            font-weight: 300;
            position: relative;
        }
        
        .content {
            display: flex;
            flex-wrap: wrap;
            padding: 20px;
        }
        
        .section {
            flex: 1;
            min-width: 300px;
            padding: 20px;
            border-radius: 10px;
            margin: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .section::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                to bottom right,
                rgba(255,255,255,0) 0%,
                rgba(255,255,255,0.3) 50%,
                rgba(255,255,255,0) 100%
            );
            transform: rotate(30deg);
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }
        
        .section:hover::after {
            opacity: 1;
            animation: sectionShine 1.5s;
        }
        
        @keyframes sectionShine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(30deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(30deg); }
        }
        
        .section h2 {
            color: #1a2a6c;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #fdbb2d;
        }
        
        .equidad {
            background-color: #e8f4f8;
        }
        
        .valores {
            background-color: #f0f8e8;
        }
        
        .protocolos {
            background-color: #f8e8f0;
        }
        
        .icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            display: inline-block;
            width: 100%;
        }
        
        .icon:hover {
            transform: scale(1.1) rotate(5deg);
            filter: drop-shadow(0 0 8px rgba(253, 187, 45, 0.7));
        }
        
        ul {
            list-style-type: none;
            padding-left: 0;
        }
        
        li {
            margin-bottom: 12px;
            padding-left: 25px;
            position: relative;
        }
        
        li:before {
            content: "•";
            color: #b21f1f;
            font-weight: bold;
            position: absolute;
            left: 0;
        }
        
        .footer {
            background-color: #1a2a6c;
            color: white;
            text-align: center;
            padding: 20px;
            font-size: 1.1rem;
            position: relative;
            overflow: hidden;
        }
        
        .footer::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                to bottom right,
                rgba(255,255,255,0) 0%,
                rgba(255,255,255,0.1) 50%,
                rgba(255,255,255,0) 100%
            );
            transform: rotate(30deg);
            animation: shine 10s infinite linear;
        }
        
        .footer p {
            position: relative;
        }
        
        .images-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 20px 0;
            padding: 15px;
            background-color: #f5f5f5;
            border-radius: 10px;
        }
        
        .image-item {
            text-align: center;
            margin: 10px;
            flex: 1;
            min-width: 200px;
            transition: all 0.3s ease;
        }
        
        .image-item:hover {
            transform: translateY(-5px);
        }
        
        .image-placeholder {
            width: 150px;
            height: 150px;
            background-color: #ddd;
            border-radius: 50%;
            margin: 0 auto 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: #666;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .image-placeholder::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                to bottom right,
                rgba(255,255,255,0) 0%,
                rgba(255,255,255,0.4) 50%,
                rgba(255,255,255,0) 100%
            );
            transform: rotate(30deg);
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .image-placeholder:hover::after {
            opacity: 1;
            animation: iconShine 1s;
        }
        
        @keyframes iconShine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(30deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(30deg); }
        }
        
        .equality-icon {
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            color: white;
        }
        
        .ethics-icon {
            background: linear-gradient(45deg, #45b7d1, #96ceb4);
            color: white;
        }
        
        .sports-icon {
            background: linear-gradient(45deg, #f093fb, #f5576c);
            color: white;
        }
        
        .contributors {
            background: linear-gradient(to right, #fdbb2d, #b21f1f);
            color: white;
            padding: 20px;
            text-align: center;
        }
        
        .contributors h3 {
            margin-bottom: 15px;
            font-size: 1.5rem;
        }
        
        .contributors-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin-top: 10px;
        }
        
        .contributor {
            background-color: rgba(255, 255, 255, 0.2);
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .contributor:hover {
            background-color: rgba(255, 255, 255, 0.3);
            transform: scale(1.05);
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
        }
        
        @media (max-width: 768px) {
            .content {
                flex-direction: column;
            }
            
            .header h1 {
                font-size: 2rem;
            }
            
            .contributors-list {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="poster">
        <div class="header">
            <h1>JUEGO LIMPIO DENTRO Y FUERA DE LA CANCHA</h1>
            <p>Promoviendo la equidad, los valores éticos y las prácticas seguras en el deporte</p>
        </div>
        
        <div class="images-container">
            <div class="image-item">
                <div class="image-placeholder equality-icon">⚖️</div>
                <p><strong>Equidad de Género</strong></p>
            </div>
            <div class="image-item">
                <div class="image-placeholder ethics-icon">🌟</div>
                <p><strong>Principios Éticos</strong></p>
            </div>
            <div class="image-item">
                <div class="image-placeholder sports-icon">⚽</div>
                <p><strong>Protocolos Deportivos</strong></p>
            </div>
        </div>
        
        <div class="content">
            <div class="section equidad">
                <div class="icon">👥</div>
                <h2>EQUIDAD DE GÉNERO</h2>
                <ul>
                    <li>Igualdad de oportunidades para todos los géneros en la práctica deportiva</li>
                    <li>Reconocimiento equitativo del talento sin distinción de género</li>
                    <li>Promoción de equipos mixtos y liderazgo femenino</li>
                    <li>Eliminación de estereotipos y prejuicios en el deporte</li>
                    <li>Acceso igualitario a recursos, instalaciones y entrenamiento</li>
                </ul>
            </div>
            
            <div class="section valores">
                <div class="icon">💖</div>
                <h2>PRINCIPIOS ÉTICOS Y MORALES</h2>
                <ul>
                    <li><strong>Respeto:</strong> Por compañeros, rivales, árbitros y público</li>
                    <li><strong>Justicia:</strong> Jugar limpio y aceptar las reglas</li>
                    <li><strong>Integridad:</strong> Honestidad en cada acción y decisión</li>
                    <li><strong>Responsabilidad:</strong> Asumir las consecuencias de nuestros actos</li>
                    <li><strong>Solidaridad:</strong> Apoyar al equipo, especialmente en la derrota</li>
                    <li><strong>Tolerancia:</strong> Aceptar la diversidad y diferencias</li>
                </ul>
            </div>
            
            <div class="section protocolos">
                <div class="icon">📋</div>
                <h2>PROTOCOLOS DEPORTIVOS</h2>
                <ul>
                    <li><strong>Antes del juego:</strong>
                        <ul>
                            <li>Calentamiento y estiramiento adecuado</li>
                            <li>Revisión del equipo e instalaciones</li>
                            <li>Establecimiento claro de reglas</li>
                        </ul>
                    </li>
                    <li><strong>Durante el juego:</strong>
                        <ul>
                            <li>Seguir indicaciones del entrenador</li>
                            <li>Hidratación constante</li>
                            <li>Respeto a las decisiones arbitrales</li>
                        </ul>
                    </li>
                    <li><strong>Después del juego:</strong>
                        <ul>
                            <li>Enfriamiento y estiramiento</li>
                            <li>Saludo deportivo al rival</li>
                            <li>Evaluación constructiva del desempeño</li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
        
        <div class="contributors">
            <h3>Contribuyeron en este proyecto:</h3>
            <div class="contributors-list">
                <span class="contributor">Juan Cardona</span>
                <span class="contributor">Juan Cardona</span>
                
            </div>
        </div>
        
        <div class="footer">
            <p>¡Construyamos un deporte mejor para todos! | #EquidadDeportiva #JuegoLimpio #DeporteSeguro</p>
        </div>
    </div>
</body>
</html>
