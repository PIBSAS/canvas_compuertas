# canvas_compuertas

Código canvas que dibuja las compuertas.

# PARTE HTML:
````
<canvas id="COMPUERTA"></canvas>
  <script>
    const canvas = document.getElementById('COMPUERTA');
    const ctx = canvas.getContext('2d');
	
	// EXPANDIR LIENZO SEGUN PANTALLA
    canvas.width = window.innerWidth * window.devicePixelRatio;
    canvas.height = window.innerHeight * window.devicePixelRatio;
    ctx.scale(window.devicePixelRatio, window.devicePixelRatio);

  <CÓDIGO CANVAS>
</script>
````

# IF:
````bash
  ctx.lineWidth = ANCHO DE LINEA EN PX;
	ctx.strokeStyle = '#000000';
	
	//BASE
	ctx.beginPath();
	ctx.moveTo(X, Y);
	ctx.lineTo(X, Y);
	ctx.lineTo(X, Y);
	ctx.closePath();
	ctx.stroke();
	
	//Z 
	ctx.beginPath();
	ctx.moveTo(X, Y);
	ctx.lineTo(X, Y);
	ctx.stroke();
	
	//ENTRADA
	ctx.beginPath();
	ctx.moveTo(X, Y);
	ctx.lineTo(X, Y);
	ctx.stroke();
</script>
````
	
# COMPUERTA NOT:
````bash
	ctx.lineWidth = 2;
	ctx.strokeStyle = '#000000';
	
	//BASE
	ctx.beginPath();
	ctx.moveTo(60, 610);
	ctx.lineTo(60, 650);
	ctx.lineTo(100, 630);
	ctx.closePath();
	ctx.stroke();
	
	// NOT
    ctx.beginPath();
    ctx.arc(105, 630, 5, 0, 2 * Math.PI);
    ctx.stroke()
	
	//Z 
	ctx.beginPath();
	ctx.moveTo(110, 630);
	ctx.lineTo(130, 630);
	ctx.stroke();
	
	//ENTRADA
	ctx.beginPath();
	ctx.moveTo(30, 630);
	ctx.lineTo(60, 630);
	ctx.stroke();
````

# COMPUERTA AND:
````bash
	ctx.lineWidth = 2;
    ctx.strokeStyle = '#000000';
	// BASE
	ctx.beginPath();
    ctx.moveTo(60, 390);
    ctx.lineTo(60, 450);
	ctx.lineTo(90, 450);
	ctx.moveTo(60, 390);
	ctx.lineTo(90, 390);
	ctx.arc(90, 420, 30, 1.5*Math.PI, 0.5*Math.PI);
    ctx.stroke();
	
	// entradas
	ctx.beginPath();
	ctx.moveTo(30, 400);
	ctx.lineTo(60, 400);
	ctx.moveTo(30, 440);
	ctx.lineTo(60, 440);
	ctx.stroke();
	
	//Z 
	ctx.beginPath();
	ctx.moveTo(120, 420);
	ctx.lineTo(140, 420);
	ctx.stroke();
 ````

# COMPUERTA NAND:
````bash
	ctx.lineWidth = 2;
    ctx.strokeStyle = '#000000';
	// BASE
	ctx.beginPath();
    ctx.moveTo(60, 470);
    ctx.lineTo(60, 530);
	ctx.lineTo(90, 530);
	ctx.moveTo(60, 470);
	ctx.lineTo(90, 470);
	ctx.arc(90, 500, 30, 1.5*Math.PI, 0.5*Math.PI);
    ctx.stroke();
	
	// entradas
	ctx.beginPath();
	ctx.moveTo(30, 480);
	ctx.lineTo(60, 480);
	ctx.moveTo(30, 520);
	ctx.lineTo(60, 520);
	ctx.stroke();
	
	// NOT
    ctx.beginPath();
    ctx.arc(125, 500, 5, 0, 2 * Math.PI);
    ctx.stroke();
	
	//Z 
	ctx.beginPath();
	ctx.moveTo(130, 500);
	ctx.lineTo(150, 500);
	ctx.stroke();
````

# COMPUERTA OR:
````bash
    ctx.lineWidth = 2;
    ctx.strokeStyle = '#000000';

//  ARCOS
    ctx.beginPath();
    ctx.moveTo(60, 230);
    ctx.quadraticCurveTo(100, 260, 60, 290);
    ctx.stroke();

// PERFILES
    ctx.beginPath();
    ctx.moveTo(59.5, 230);
    ctx.lineTo(80, 230);
    ctx.moveTo(59.5, 290);
    ctx.lineTo(80, 290);
    ctx.stroke();

// ESCUDO
    ctx.beginPath();
    ctx.moveTo(80, 230);
    ctx.quadraticCurveTo(110, 230, 130, 260);
	ctx.moveTo(80, 290)
	ctx.quadraticCurveTo(110,290, 130,260);
    ctx.stroke();

// Z
    ctx.beginPath();
    ctx.moveTo(130, 260);
    ctx.lineTo(150, 260);
    ctx.stroke();

// entradas
    ctx.beginPath();
    ctx.moveTo(30, 240);
    ctx.lineTo(70, 240);
    ctx.moveTo(30, 280);
    ctx.lineTo(70, 280);
    ctx.stroke();
````

# COMPUERTA NOR
````bash
    ctx.lineWidth = 2;
    ctx.strokeStyle = '#000000';

//  ARCOS
    ctx.beginPath();
    ctx.moveTo(60, 310);
    ctx.quadraticCurveTo(100, 340, 60, 370);
    ctx.stroke();

// PERFILES
    ctx.beginPath();
    ctx.moveTo(59.5, 310);
    ctx.lineTo(80, 310);
    ctx.moveTo(59.5, 370);
    ctx.lineTo(80, 370);
    ctx.stroke();

// ESCUDO
    ctx.beginPath();
    ctx.moveTo(80, 310);
    ctx.quadraticCurveTo(110, 310, 130, 340);
	ctx.moveTo(80, 370)
	ctx.quadraticCurveTo(110,370, 130,340);
    ctx.stroke();

// NOT
    ctx.beginPath();
    ctx.arc(135, 340, 5, 0, 2 * Math.PI);
    ctx.stroke();
	

// Z
    ctx.beginPath();
    ctx.moveTo(140, 340);
    ctx.lineTo(160, 340);
    ctx.stroke();

// entradas
    ctx.beginPath();
    ctx.moveTo(30, 320);
    ctx.lineTo(70, 320);
    ctx.moveTo(30, 360);
    ctx.lineTo(70, 360);
    ctx.stroke();
````

# COMPUERTA XOR:
````bash
    ctx.lineWidth = 2;
    ctx.strokeStyle = '#000000';

//  ARCOS
    ctx.beginPath();
    ctx.moveTo(50, 150);
    ctx.quadraticCurveTo(100, 180, 50, 210);
    ctx.moveTo(60, 150);
    ctx.quadraticCurveTo(100, 180, 60, 210);
    ctx.stroke();

// PERFILES
    ctx.beginPath();
    ctx.moveTo(59.5, 150);
    ctx.lineTo(80, 150);
    ctx.moveTo(59.5, 210);
    ctx.lineTo(80, 210);
    ctx.stroke();

// ESCUDO
    ctx.beginPath();
    ctx.moveTo(80, 150);
    ctx.quadraticCurveTo(110, 150, 130, 180);
	ctx.moveTo(80, 210)
	ctx.quadraticCurveTo(110,210, 130,180);
    ctx.stroke();

// Z
    ctx.beginPath();
    ctx.moveTo(130, 180);
    ctx.lineTo(150, 180);
    ctx.stroke();

// entradas
    ctx.beginPath();
    ctx.moveTo(30, 160);
    ctx.lineTo(65, 160);
    ctx.moveTo(30, 200);
    ctx.lineTo(65, 200);
    ctx.stroke();
  ````

# COMPUERTA XNOR:
````bash
    ctx.lineWidth = 2;
    ctx.strokeStyle = '#000000';

//  ARCOS
    ctx.beginPath();
    ctx.moveTo(50, 70);
    ctx.quadraticCurveTo(100, 100, 50, 130);
    ctx.moveTo(60, 70);
    ctx.quadraticCurveTo(100, 100, 60, 130);
    ctx.stroke();

// PERFILES
    ctx.beginPath();
    ctx.moveTo(59.5, 70);
    ctx.lineTo(80, 70);
    ctx.moveTo(59.5, 130);
    ctx.lineTo(80, 130);
    ctx.stroke();

// ESCUDO
    ctx.beginPath();
    ctx.moveTo(80, 70);
    ctx.quadraticCurveTo(110, 70, 130, 100);
	ctx.moveTo(80, 130)
	ctx.quadraticCurveTo(110,130, 130,100);
    ctx.stroke();
// NOT
    ctx.beginPath();
    ctx.arc(135, 100, 5, 0, 2 * Math.PI);
    ctx.stroke();

// Z
    ctx.beginPath();
    ctx.moveTo(140, 100);
    ctx.lineTo(160, 100);
    ctx.stroke();

// entradas
    ctx.beginPath();
    ctx.moveTo(30, 80);
    ctx.lineTo(65, 80);
    ctx.moveTo(30, 120);
    ctx.lineTo(65, 120);
    ctx.stroke();
	````
