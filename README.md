# perro
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Animación de un Perro</title>
</head>
<body>
    <div class="perro">
        <div class="cuerpo"></div>
        <div class="cabeza"></div>
        <div class="oreja izquierda"></div>
        <div class="oreja derecha"></div>
        <div class="pata izquierda"></div>
        <div class="pata derecha"></div>
    </div>
</body>
</html>
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #e0f7fa;
    margin: 0;
}

.perro {
    position: relative;
    animation: mover 2s linear infinite;
}

@keyframes mover {
    0% { transform: translateX(0); }
    50% { transform: translateX(20px); }
    100% { transform: translateX(0); }
}

.cuerpo {
    width: 100px;
    height: 50px;
    background-color: brown;
    border-radius: 25px;
    position: relative;
}

.cabeza {
    width: 40px;
    height: 40px;
    background-color: brown;
    border-radius: 20px;
    position: absolute;
    top: -20px;
    left: 10px;
}

.oreja {
    width: 15px;
    height: 25px;
    background-color: brown;
    border-radius: 10px;
    position: absolute;
}

.oreja.izquierda {
    top: -15px;
    left: 0;
    transform: rotate(-30deg);
}

.oreja.derecha {
    top: -15px;
    right: 0;
    transform: rotate(30deg);
}

.pata {
    width: 15px;
    height: 30px;
    background-color: brown;
    border-radius: 10px;
    position: absolute;
}

.pata.izquierda {
    bottom: -30px;
    left: 10px;
}

.pata.derecha {
    bottom: -30px;
    right: 10px;
}
