```js
// 1
function cambiar() {
	let titular = document.getElementById('titular');
	titular.innerText = "Hola Mundo con Javascript";
}

// 2
function cambiar() {
	let titular = document.getElementById('titular');
	titular.style.color = "red";
	titular.style.textAlign = "center"
}

// 3
function crearDiv() {
	let txt = document.createTextNode("Javascript permite crear págnas dinámicas");
	let bloque = document.createElement("div");
	bloque.setAttribute("style", 'background:red; color: white; text-align: center')
	bloque.appendChild(txt);
	document.body.appendChild(bloque);
}

// 4
function borrarDiv() {
	let blq = document.getElementById('subtitulo');
		if (blq != null) {
		document.body.removeChild(blq);
		}
}

// 5
function ponerPie(fig) {
	let pie = fig.getElementsByTagName('figcaption')[0];
	let imag = fig.getElementsByTagName('img')[0];
		if (pie.innerText == '') {
			pie.innerText = imag.alt;
		} else {
			pie.innerText = '';
		}
}

// 6
function fuentesImg() {
	let listaImgs = document.getElementsByTagName('img');
	//O: listaImgs = document.Images;
	let salida = document.getElementById('fuentes');
		for (let ind = 0; ind < listaImgs.length; ind++){
		salida.innerHTML += listaImgs[ind].src + "<br>";
	}
}

// 7
function toggle(){
	let encab = document.getElementById('titular');
	encab.classList.toggle('activo');
}

// 8
function intercalar(){
	let miBloque = document.createElement('div');
	let titular = document.getElementById('titular');
	miBloque.innerHTML = "<b>Página Modelo</b>";
	miBloque.classList.add('destacar');
	titular.insertAdjacentElement('afterend', miBloque)
}

// 9
function cambiaImg() {
	let imgs = ['uno.png', 'dos.png', 'tres.png'];
	let car = document.querySelector(".carrusel");
	let indActual = parseInt(car.dataset.img);
	indActual++;
	if (indActual >= imgs.length) {
	indActual = 0;
	}
	car.children[0].src = "/imgs/" + imgs[indActual];
	car.dataset.img = indActual;
}

// 10
function toggle(){
	let barra = document.querySelector(".botones");
	let botones = barra.children;
	let estado = barra.dataset.estado == 'none'?'inline-block':'none';
	for(let i = 1; i < botones.length; i++){
	botones[i].style.display = estado
	}
	barra.dataset.estado = estado;
}

```
