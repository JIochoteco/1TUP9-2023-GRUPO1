# 1TUP9-2023-GRUPO1
UTN - 1TUP9 - PROGRAMACION1 - GRUPO1 - TP1
Algoritmo TP_Programacion1_grupo1
	Definir menu, ruta,op1 Como Entero;
	Definir ord, list Como Caracter;
	Definir arregloBB, arregloBS,arregloRB, arregloMPM Como Caracter;
	Definir costoPas como real;
	
	Dimension arregloBB[120,8];
	Dimension arregloBS[120,8];
	Dimension arregloRB[80,8];
	Dimension arregloMPM[80,8];
	
	
	Escribir "¡Bienvenido a la pagina oficial de nuestra aerolinea!";
	Escribir "-----------------------------------------------------";
	Escribir "Seleccione la operacion que desee realizar: ";
	Escribir "1-Venta de pasajes";
	Escribir "2-Buscar un pasaje ";
	Escribir "3-Buscar un pasajero";
	Escribir "4-Ordenar y mostrar lista de pasajeros";
	Escribir "5-Listado/s";
	Escribir "-----------------------------------------------------";
	
	repetir
	 Leer menu;
	 Segun menu Hacer
		 1:
			 Escribir "Venta de pasajes: ";
			Escribir "Seleccione la ruta aerea que desea tomar: ";
			Escribir "1-Buenos Aires-Bariloche";
			Escribir "2-Buenos Aires-Salta";
			Escribir "3-Rosario-Buenos Aires";
			Escribir "4-Mar del Plata-Mendoza";
			
			repetir
				Leer ruta;
				Segun ruta Hacer
					1:
						
						Escribir "Ruta:Buenos Aires-Bariloche";
						
					2:
						Escribir "Ruta:Buenos Aires-Salta";
						
					3:
						Escribir "Ruta:Rosario-Buenos Aires";
						
					4:
						Escribir "Ruta:Mar del Plata-Mendoza";
						
					De Otro Modo:
						Escribir "Solo existen 4 rutas de vuelo,por el momento, actualizaremos la pagina cuando se agregue alguna. Por favor, ingrese un numero entre 1 y 4.";
				FinSegun
			hasta que ruta=1 o ruta=2 o ruta=3 o ruta=4
			
		2:
			Escribir "Buscar un pasaje: ";
			
		3:
			Escribir "Buscar pasajero: ";
			// SubProceso/s busqueda de pasajero
			
			
		4:
			Escribir "Ordenar y mostrar lista de pasajeros: ";
			Escribir"a-Orden ascendente";
			Escribir"b-Orden descendente";
			
			
				Repetir
					leer ord;
					Segun ord Hacer
					"a":
						Escribir "se eligio orden ascendente";
						//SubProceso de orden ascendente
					"b":
						Escribir "se eligio orden descendente";
						//SubProceso de orden descendente 
					De Otro Modo:
						Escribir "Solo se pueden seleccionar las letras a o b. Ingrese de nuevo, por favor ";
					Fin Segun
			
				Hasta Que ord="a" o ord="A" o ord="b" o ord="B"
		
		5:	
			Escribir "Listados/s: ";
			Escribir "a-Cantidad de pasajes vendidos por ruta aerea";
			Escribir "b-Porcentaje de ventas por ruta aerea";
				repetir
				leer list;
				Segun list Hacer
					"a":
						escribir "se eligio cantidad de pasajes vendidos por ruta aerea";
						//SubProceso cantidad de pasajes vendidos por ruta aerea
					"b":
						Escribir "se eligio se eligio porcentaje de ventas por ruta aerea";
						//SubProceso porcentaje  de ventas por ruta aerea
					De Otro Modo:
						Escribir "Solo se pueden seleccionar las letras a o b. Ingrese de nuevo, por favor";
				Fin Segun
				Hasta Que list="a" o list="A" o list="b" o list="B"
		De Otro Modo:
			Escribir "ingrese un numero valido(entre 1 y 5)";
		FinSegun
	Hasta Que menu=1 o menu=2 o menu=3 o menu=4 o menu=5
	
FinAlgoritmo
