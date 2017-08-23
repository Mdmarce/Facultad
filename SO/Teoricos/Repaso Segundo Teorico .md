# Sistemas Operativos 

## Segundo Parcial Teórico Repaso


***


		FALSO. -> Todas las syscall se redirigen a un mismo procesador (el maestro) y el resto de los procesadores (esclavos) corren procesos de usuario.


		VERDADERO -> al tener cada CPU su conjunto de procesos, se produce un desbalance de cargas de trabajo.
		

		FALSO -> SMP (Multiprocesadores simetricos) Hay una unica copia del SO en memoria, y cualquier CPU puede ejecutarlo. Por lo tanto, para que muchos CPU usen el mismo codigo se necesita exclusión mutua entre ellas para no generar conflictos.
		

		FALSO -> TSL (test set lock) es un sistema para garantizar exclusion mutua, prueban y establecen el bloqueo. El problema son los multiprocesadores que pueden llegar a obtener acceso al CPU al mismo tiempo.
		Para tratar de solucionar se bloquea el acceso al bus, lo cual necesita apoyo del hardware y a su vez desperdicia tiempo de CPU.
		Para solcionar esto se pueden utilizar caches para evitar el uso del BUS, pero esto genera mas problemas manteniendo la consistencia de los datos (lo cual requiere al fin y al cabo uso de BUS).
		

		FALSO -> La planificacion tiene que ser adaptada para optimizar la utilizacion en multiples procesadores en vez de uno solo.
		

		FALSO -> Al ser distribuidos, no es necesario que los SO sean los mismos pero si hace falta que compartan algun protocolo de comunicacion, de manera que puedan entenderse entre ellas.
		

		VERDADERO -> Una multicomputadora, son varios pares CPU-memoria interconectados pasandose mensajes.
		
  
		a. Memoria Compartida X -> ! no tienen memoria compartida
 		b. Pasajes de Mensajes O -> Correcta.
 		c. RPC  X
 		d. Ninguna X
 		 		

		VERDADERO. -> se maneja por mensajes, solo necesita que el protocolo se respete entre las diferentes computadoras.
		

		DUDOSO -> En el power no menciona Grids en ningun lado, y hay muchos tipos de computadoras conectadas en forma de grid. Deberia ser mas especifico para saber a que se refiere.
		
		Segun Wiki:
		Grid computing is the collection of computer resources from multiple locations to reach a common goal. The grid can be thought of as a distributed system with non-interactive workloads that involve a large number of files. Grid computing is distinguished from conventional high performance computing systems such as cluster computing in that grid computers have each node set to perform a different task/application. Grid computers also tend to be more heterogeneous and geographically dispersed (thus not physically coupled) than cluster computers.[1] Although a single grid can be dedicated to a particular application, commonly a grid is used for a variety of purposes. Grids are often constructed with general-purpose grid middleware software libraries. 
		

		DUDOSO -> Yo diria que si, el nombre te dice que es una capa intermedia entre 2 cosas. Pero otra vez, en las diapositivas no se menciona ni una sola vez la palabra middleware.
		
		Segun Wiki:
		"The software layer that liesbetween the operating system and applications on each side of a distributed computing system in a network."
		
		
		VERDADERO -> ELF (Formato de Linkeo y ejecutable).
		Segun lo que dice el documento:
		ELF (Executable and Linking Format). There are three main types of object files.
		
			
			
		

		VERADERO
		

		VERDADERO -> An object file segment contains one or more sections.
		

		DUDOSO -> Las secciones TIENEN un FLAG, y el mismo puede indicar varias cosas. Entre ellas hay una que se llama WRITE, que especifica:
		"SHF_WRITE The section contains data that should be writable during process execution."
		

		FALSO -> Nos permite relacionar la direccion de memoria con el valor del programa.
		

		VERDADERO -> La seccion de exports, contiene informacion de codigos o datos que pueden ser exportados desde el archivo. Se tratan de nombres de variables o funciones que pueden ser referenciados desde otros PE Los elementos que se exportan se denominan 'simbolos'.
		

		DUDOSO -> No encontre nada que diga que esto sea verdadero asi que lo tomo por falso.
		

		VERDADERO -> El campo para indicar la cantidad de secciones de 2bytes y el maximo numero de secciones es de 96.
		

		FALSO -> segun wikipedia: "...the .text section (which holds program code)..."
		

		VERDADERO -> Un dominio es un conjunto de pares {Objeto, Derecho} cada par especifica un objeto y un subconjunto de operaciones que se pueden realizar con el.
		

		VERDADERO -> hay muchos dominios dentro de los cuales se ejecutan los procesos.
		

		VERDADERO
		
24. El derecho copy se asocia a un objeto, y permite que un proceso en ese dominio pueda copiar los derechos de ese objeto dentro de su columna.

		DUDOSO -> en principio la parte de que 'permite que un proceso en ese dominio pueda copiar los derechos de ese objeto dentro de su columna' es verdad. Pero en la diapo aparece como que el derecho copy se asocia a un elemento access (i,j) de la matriz, y no 'a un objeto'.
		

		VERDADERO -> Para poder cambiar de un dominio a otro se debe habilitar la operación switch sobre un objeto.
		

		VERDADERO -> Transferencia: si un derecho se copia desde matriz(i,j) a matriz(k,j), el derecho desaparece para matriz(i,j), o sea, el derecho fue transferido.
		

		CREO QUE ES FALSO -> Si matriz(i,j) incluye el derecho de owner entonces un proceso ejecutándose en el dominio Di puede agregar y borrar cualquier entrada en la columna j.
		

		VERDADERO
		
29. Un proceso en el dominio i puede remover cualquier derecho del j, si tiene habilitada la operación control en su dominio.

		DUDOSO -> es VERDADERO si la matriz es (i,j). porque: "Si matriz (i,j) incluye el derecho de control, entonces un proceso ejecutándose en el dominio Di puede remover cualquier derecho de acceso dentro de la fila j." Si la matriz no es asi, entonces es FALSO.
		

		FALSO -> La matriz de acceso puede implementarse como una lista de acceso a objetos, para optimizarla.
		

		FALSO -> Primero las politicas, luego los mecanismos.
		

		VERDADERO (supongo, no lo encontre en las diapos)

		CREO QUE FALSO -> yo diría qeu la privacidad es lo anterior, y lo confidencial es informacion sensible, que por alguna razon no debe ser expuesta al publico general y debe ser protegida de alguna manera.
		

		FALSO -> Identificarse hace referencia a decir quien somos, y autenticarse hace referencia a demostrar que somos quien decimos ser.
		

		VERDADERO
		

		FALSO -> es una amenaza a la Integridad de los datos.
		

		FALSO -> igual creo que se equivocaron de palabra diciendo 'invención'
		

		NI IDEA. Si declaras un buffer como solo lectura, como lo usas como buffer??
		

		Se puede sobreescribir la dirección de retorno de printf y saltar donde quiera. 
		Si el programa se ejecuta con SETUID root, se podría saltar a un Shell code que se ejecute con esos privilegios.