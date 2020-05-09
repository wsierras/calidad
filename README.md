# Tretramino Letra L
![](https://cdn02.nintendo-europe.com/media/images/10_share_images/games_15/wiiu_download_software_5/H2x1_WiiUDS_Tetraminos.jpg) 

** Autores: ** 
Jeisson Ramirez Zorro 				ID 157190
William Dario Sierra Sierra			ID 80817368

###Tetramino Letra L

Para dar inicio daremos a conocer un poco de la historia del tetramino el cual es una forma geométrica compuesta de cuatro cuadrados iguales, conectados entre sí ortogonalmente (lado a lado). Al igual que los dominós y los pentominós, es un tipo particular de poliominó. El policubo correspondiente, llamado tetracubo, es una forma geométrica compuesta por cuatro cubos conectados ortogonalmente (cara a cara).
 
Un uso popular de los tetrominós es la base del videojuego Tetris, en el que las piezas se describen como tetriminos.
Nosotros hemos seleccionado la letra L 
![](https://toppng.com/uploads/preview/wow-l-tetris-block-body-tetris-l-block-11563000592yjhefelupa.png) 
     L: una fila de tres bloques con uno agregado debajo del lado izquierdo. 

La documentación estará disponible en el servidor en la siguiente dirección
http://158.69.63.154/letral/
Requisitos de la Aplicación
•	GIT
•	AngularJS
•	Nodejs
Código Inicial para la pagina
$scope.PageTitle="AngularJS Tetramino Letra L";


Codigo Solución 

•	Inicialización movimientos de la ficha
const L = [
	[
		[0, 1, 0],
		[0, 1, 0],
		[0, 1, 1]
	],
	[
		[0, 0, 0],
		[1, 1, 1],
		[1, 0, 0]
	],	
	[
		[1, 1, 0],
		[0, 1, 0],
		[0, 1, 0]
	],
	[
		[0, 0, 1],
		[1, 1, 1],
		[0, 0, 0]
	],
];
•	Movimientos de la ficha => Girar
function rotar(tablero) {
    for (let c = 0; c < tablero.length; c++) {
      for (let x = 0; x < c; r++) {
        [tablero[r][c], tablero[c][r]] = [tablero[c][r], tablero[r][c]];
      }
    }
    tablero.forEach((row) => row.reverse());
  }

•	Movimiento de la ficha => Posición de la Letra
function movimientoL (direccionr, direccionc) {
    L.pos.r += direcionR;
    L.pos.r = direcconC;
  }

•	Movimiento iniciales del tablero y la posición de la ficha 
app.get("/tablero", (req, res) => {
  res.json(talblero);
});

•	Rotar ficha L
app.get("/rotar", (req, res) => {
  const { pos, tablero } = req.body;
  //console.log(req.body);
  if (pos && tablero) {
    const posicion = { ...req.body };
    rotar(posicion.tablero);
    res.json(posicion);
  }

