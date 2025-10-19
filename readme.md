#BibleAddon


BibleAddon es un cmplemento que te permite a través de una interfaz facíl e intuitiva leer un libro por capitulos ya sea del antiguo o nuevo testamento, cargando para ello en memoria el texto biblico desde una base de datos SQLite.

Inicialmente este complemento no tiene asignada una combinación de teclas para llamarlo, para asignarle una de esta, hacer lo siguiente:

* ir al menú de NVDA  submenú Preferencias y seleccionar Gestos de entrada.
* Bajar hasta ubicar BibleAddon y con flecha derecha expandir este item.
* Bajar a "Llama al complemento BibleAddon".
* Tabula hasta  posicionarte en "Añadir" y presiona enter.
* En el cuadro de diálogo, presionar las teclas que serán usadas para llamar el BibleAddon, se desplegará  un cuadro de lista, baja para que selecciones el tipo de teclado a usar y presiona enter.
* Tabula hasta "Aceptar" y habrás creado la combinación de teclas para llamar a BibleAddon.


## ¿Cómo usarlo?
Al abrir  por primera vez el complemento, pordrás leer con flecha arriba o abajo los versículos del primer capítulo del libro de Génesis,  de allí en adelante al abrirlo,  leerás  los versículos del último libro seleccionado antes de salir del complemento. 
Si pulsas la tecla "Tab" o "Tabulador" una vez, te posicionarás en el botón "Siguiente". Este botón al pulsarlo avanza un capítulo en el libro seleccionado y te posiciona nuevamente en el   texto Biblico.
Si vuelves a tabular estarás ahora en el botón "Anterior". Este botón al pulsarlo retrocede un capítulo en el libro seleccionado y te posiciona nuevamente en el   texto Biblico.
Si tabulas nuevamente estarás en el botón "salir" que al pulsarlo cerrará el complemento.

Estando en el cuadro de texto de lectura del texto Biblico, puedes usar los siguientes atajo de teclado:

* Alt mas 1: te lleva a la lista desplegable para seleccionar un testamento
* Alt mas 2: te lleva a la lista desplegable para seleccionar un libro
* Alt mas flecha derecha: Avanza un capítulo en el libro seleccionado
* Alt mas flecha izquierda: retrocede un capítulo en el libro seleccionado
* Tecla "Esc" o "Escape": Cierra el complemento
* Alt mas Tecla "i": Para saber en que libro y capítulo estás

Estando en el cuadro de texto de lectura de los versículos, si quieres ir a un capítulo en particular del libro actual, pulsa la tecla "Shift" mas "Tabulador" y luego escribe un número de capítulo valido.

También puedes desde el cuadro de texto de lectura presionar Alt más 1 para que selecciones un testamento, luego puedes tabular para que selecciones un libro, nuevamente tabulas y ahora puedes escribir o selecionar un capítulo y al presionar enter volverás al cuadro de texto de lectura para leer el capítulo ahora seleccionado.

Y en general, puedes moverte por toda la interfaz gráfica con tabulador o Shift mas tabulador.


## Su interfaz Gráfica.
Es de forma rectangular, más ancha que alta, tiene   3 secciones organizadas como cabezera, principal y pie, es decir una debajo de otra, y dentro de cada sección sus componentes se organizan de forma horizontal. 
La primera sección   contiene los siguientes objetos:

* Una lista desplegable para seleccionar el testamento
* Una lista desplegable que se llena  con los nombre de los libros según el testamento seleccionado
* Un combo list que carga los capítulos según el libro seleccionado
* Un botón "Ir" que carga los versículos del capítulo seleccionado

Estos objetos conforman la barra de búsqueda del libro a leer.

La segunda sección contiene solo un cuadro de texto multilínea de solo lectura que ocupa todo el ancho disponible, con todos los versículos que correspondan al libro seleccionado. 

La tercera sección contiene los siguientes objetos: 

* Un botón "Siguiente", que te lleva un capítulo adelante del libro seleccionado
* Un botón "Anterior", que te lleva un capítulo Atrás del libro seleccionado
* Y finalmente un botón "Salir" que ciera el complemento.

## Información Técnica
El complemento por ahora gestiona Biblias cristianas protestantes que contienen 66 libros a diferencia de las cristianas católicas que están formadas por 72 libros.

El texto biblico se encuentra almacenado en un archivo de base de datos sqlite la cual contiene 2 tablas, una llamada Bible y otra llamada Details, en la tabla Bible se encuentra todos los versículos que contiene una Biblia de 66 libros, cada versículo es un registro en la tabla, mientras que en la tabla Details solo hay un registro con información adicional acerca de esa versión de La Biblia.

Con sqlite3 desde el cmd puedes gestionar el archivo con extensión bbl con todos los comandos que te ofrece este gestor de base de datos. Siempre toma la precaución de respaldar tu archivo bbl antes de manipularlo desde este gestor. 

Cabe mencionar que el texto o los versículos están almacenados junto con caracteres especiales que le dan formato RTF, por razones de accesibilidad, no se usó un wx widget que soportara este formato, así que antes de colocar el texto en el cuadro de texto para su lectura, este es procesado para eliminar en lo posible todo formato RTF. 

Este complemento puede leer una Biblia siempre y cuando el nombre del archivo de base de datos sqlite tenga extensión bbl y el esquema de base de datos sea el correcto. Viene por defecto con La Biblia "Nueva traducción Viviente" cuyo nombre de archivo es NTV.bbl.
Para cargar una versión distinta debes ir a la carpeta BibleAddon, mover a otra carpeta el archivo NTV.bbl y luego copiar el archivo bbl que contiene la versión de La Biblia que deseas leer, luego deberás reiniciar NVDA y cargar nuevamente el complemento.


## Descarga del complemento.
Puedes  descargar este  complemento haciendo [click aquí][1].  


[1]: https://drive.google.com/uc?export=download&id=1tqTPs5Ldeco92ip6M9hDlgpA-IQQ_mUL
