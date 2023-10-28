# 1TUP9-2023-GRUPO1
UTN - 1TUP9 - PROGRAMACION1 - GRUPO1 - TP1
Algoritmo TP_Programacion1_grupo1
	Definir menu, ruta,ruta2,op1,contador Como Entero;
	Definir ord, list, descRuta Como Caracter;
	Definir arregloBB, arregloBS,arregloRB, arregloMPM Como Caracter;
	Definir costoPas como real;
	Definir contadorBB, contadorBS, contadorRB,contadorMM,i Como Entero;
	definir arreglo Como Caracter;
	
	// Listado de pasajeros Ruta:Buenos Aires-Bariloche
	Dimension arregloBB[120,8];
	
	// Listado de pasajeros Ruta:Buenos Aires-Salta
	Dimension arregloBS[120,8];
	
	// Listado de pasajeros Rosario-Buenos Aires
	Dimension arregloRB[80,8];
	
	// Listado de pasajeros Mar del Plata-Mendoza
	Dimension arregloMPM[80,8];
	
	contadorBB=0;
	contadorBS=0;
    contadorRB=0;
	contadorMM=0;
	
	
	repetir
		
		Escribir "¡Bienvenido a la pagina oficial de nuestra aerolinea!";
		Escribir "-----------------------------------------------------";
		Escribir "Seleccione la operacion que desee realizar: ";
		Escribir "1-Venta de pasajes";
		Escribir "2-Buscar un pasaje ";
		Escribir "3-Buscar un pasajero";
		Escribir "4-Ordenar y mostrar lista de pasajeros";
		Escribir "5-Listado/s";
		escribir "6-salir";
		Escribir "-----------------------------------------------------";
		
		
		Leer menu;
		Segun menu Hacer
			1:
				repetir
					Escribir "Venta de pasajes: ";
					Escribir "Seleccione la ruta aerea que desea tomar: ";
					Escribir "1-Buenos Aires-Bariloche";
					Escribir "2-Buenos Aires-Salta";
					Escribir "3-Rosario-Buenos Aires";
					Escribir "4-Mar del Plata-Mendoza";
					Escribir "5-Volver a menú principal";					
					Leer ruta;
					
					Segun ruta Hacer
						1:
							descRuta="Ruta:Buenos Aires-Bariloche";
							Escribir descRuta;							
							cargaDatos(arregloBB, ruta, descRuta,contadorBB);
						2:
							descRuta= "Ruta:Buenos Aires-Salta";
							Escribir descRuta;
							cargaDatos(arregloBS, ruta, descRuta,contadorBS);
							
						3:
							descRuta= "Ruta:Rosario-Buenos Aires";
							Escribir descRuta;
							cargaDatos(arregloRB, ruta, descRuta,contadorRB);
						4:
							descRuta="Ruta:Mar del Plata-Mendoza";
							Escribir descRuta;
							cargaDatos(arregloMPM, ruta, descRuta,contadorMM);
							
						5: 
							escribir "Volver";  // volver al menú anterior
							
						De Otro Modo:
							Escribir "Solo existen 4 rutas de vuelo,por el momento, actualizaremos la pagina cuando se agregue alguna. Por favor, ingrese un numero entre 1 y 4.";
					FinSegun
				hasta que ruta = 5
				
			2:
				repetir 
					Escribir "Busqueda de pasajes por pasaje(nro de asiento): ";				
					Escribir "Seleccione la ruta aerea que desea tomar: ";
					Escribir "1-Buenos Aires-Bariloche";
					Escribir "2-Buenos Aires-Salta";
					Escribir "3-Rosario-Buenos Aires";
					Escribir "4-Mar del Plata-Mendoza";
					Escribir "5-Volver a menú principal";					
					Leer ruta;
					Segun ruta Hacer
						1:
							descRuta="Ruta:Buenos Aires-Bariloche";
							Escribir descRuta;						
							busquedaPorAsiento(arregloBB,contadorBB);
						2:
							descRuta= "Ruta:Buenos Aires-Salta";
							Escribir descRuta;
							busquedaPorAsiento(arregloBS, contadorBS);
							
						3:
							descRuta= "Ruta:Rosario-Buenos Aires";
							Escribir descRuta;
							busquedaPorAsiento(arregloRB,contadorRB);
						4:
							descRuta="Ruta:Mar del Plata-Mendoza";
							Escribir descRuta;
							busquedaPorAsiento(arregloMPM, contadorMPM);
							
						5: 
							escribir "Volver"; 
							
						De Otro Modo:
							Escribir "Solo existen 4 rutas de vuelo,por el momento, actualizaremos la pagina cuando se agregue alguna. Por favor, ingrese un numero entre 1 y 4.";
					FinSegun
				hasta que ruta = 5
				
				
			3:
				
				repetir 
					Escribir "Busqueda de pasajes por pasajero(nombre y apellido): ";				
					Escribir "Seleccione la ruta aerea que desea tomar: ";
					Escribir "1-Buenos Aires-Bariloche";
					Escribir "2-Buenos Aires-Salta";
					Escribir "3-Rosario-Buenos Aires";
					Escribir "4-Mar del Plata-Mendoza";
					Escribir "5-Volver a menú principal";					
					Leer ruta;
					Segun ruta Hacer
						1:
							descRuta="Ruta:Buenos Aires-Bariloche";
							Escribir descRuta;						
							busquedaPorPasajero(arregloBB,contadorBB);
						2:
							descRuta= "Ruta:Buenos Aires-Salta";
							Escribir descRuta;
							busquedaPorPasajero(arregloBS, contadorBS);
							
						3:
							descRuta= "Ruta:Rosario-Buenos Aires";
							Escribir descRuta;
							busquedaPorPasajero(arregloRB,contadorRB);
						4:
							descRuta="Ruta:Mar del Plata-Mendoza";
							Escribir descRuta;
							busquedaPorPasajero(arregloMPM, contadorMPM);
							
						5: 
							escribir "Volver"; 
							
						De Otro Modo:
							Escribir "Solo existen 4 rutas de vuelo,por el momento, actualizaremos la pagina cuando se agregue alguna. Por favor, ingrese un numero entre 1 y 4.";
					FinSegun
				hasta que ruta = 5
				
				
				
			4:
				Escribir "Ordenar y mostrar lista de pasajeros: ";
						
				repetir 					
					Escribir "Seleccione la ruta aerea que desea ordenar: ";
					Escribir "1-Buenos Aires-Bariloche";
					Escribir "2-Buenos Aires-Salta";
					Escribir "3-Rosario-Buenos Aires";
					Escribir "4-Mar del Plata-Mendoza";
					Escribir "5-Volver a menú principal";					
					Leer ruta;
					Segun ruta Hacer
						1:
							descRuta="Ruta:Buenos Aires-Bariloche";
							Escribir descRuta;					
							Escribir "a-Orden ascendente";
							Escribir "b-Orden descendente";				
							
							Repetir
								leer ord;				
							Hasta Que ord="a" o ord="A" o ord="b" o ord="B"
							
							Listado(arregloBB,contadorBB);
							
							si ord = "a" o ord ="A" entonces
								ordenamientoAscendente(arregloBB,contadorBB);
							SiNo
								ordenamientoDescendente(arregloBB,contadorBB);
							FinSi
							
							Listado(arregloBB,contadorBB);
						2:
							descRuta= "Ruta:Buenos Aires-Salta";
							Escribir descRuta;
							Escribir "a-Orden ascendente";
							Escribir "b-Orden descendente";				
							
							Repetir
								leer ord;				
							Hasta Que ord="a" o ord="A" o ord="b" o ord="B"
							
							si ord = "a" o ord ="A" entonces
								ordenamientoAscendente(arregloBS,contadorBS);
							SiNo
								ordenamientoDescendente(arregloBB,contadorBB);
							FinSi
							
							Listado(arregloBS,contadorBS);
							
						3:
							descRuta= "Ruta:Rosario-Buenos Aires";
							Escribir descRuta;
							Escribir "a-Orden ascendente";
							Escribir "b-Orden descendente";				
							
							Repetir
								leer ord;				
							Hasta Que ord="a" o ord="A" o ord="b" o ord="B"
							
							si ord = "a" o ord ="A" entonces
								ordenamientoAscendente(arregloRB,contadorRB);
							SiNo
								ordenamientoDescendente(arregloBB,contadorBB);
							FinSi
							
							Listado(arregloRB,contadorRB);
						4:
							descRuta="Ruta:Mar del Plata-Mendoza";
							Escribir descRuta;
							Escribir "a-Orden ascendente";
							Escribir "b-Orden descendente";				
							
							Repetir
								leer ord;				
							Hasta Que ord="a" o ord="A" o ord="b" o ord="B"
							
							si ord = "a" o ord ="A" entonces
								ordenamientoAscendente(arregloMPM,contadorMPM);
							SiNo
								ordenamientoDescendente(arregloBB,contadorBB);
							FinSi
							
							Listado(arregloMPM,contadorMPM);
							
						5: 
							escribir "";  // volver al menú anterior
							
						De Otro Modo:
							Escribir "Solo existen 4 rutas de vuelo,por el momento, actualizaremos la pagina cuando se agregue alguna. Por favor, ingrese un numero entre 1 y 4.";
					FinSegun
				hasta que ruta = 5
				
				
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
					FinSegun
				Hasta Que list="a" o list="A" o list="b" o list="B"
				
			6: escribir "salir";
				
			De Otro Modo:
				Escribir "ingrese un numero valido(entre 1 y 6)";
		FinSegun
	mientras que menu <> 6
	
FinAlgoritmo


//------------------------------------------------------------------------------------------//
//ventas de pasajes BB
SubProceso cargaDatos(arreglo,ruta,descRuta,contador Por Referencia)
	
	arreglo[contador,0]=descRuta;
	
	escribir "ingrese el nombre y apellido";
	leer arreglo[contador,1];
	arreglo[contador,1] <- Minusculas(arreglo[contador,1]);
	
	escribir "ingrese dni";
	leer arreglo[contador,2];
	
	escribir "ingrese telefono";
	leer arreglo[contador,3];
	
	repetir
		escribir "Ingrese si tiene equipaje en bodega (si/no): ";
		leer arreglo[contador, 4];
		arreglo[contador, 4]<- Minusculas(arreglo[contador, 4]);
		
		Si arreglo[contador,4] = "si" Entonces
			escribir "Usted tiene equipaje en bodega: verdadero";
		Sino
			Si arreglo[contador,4]= "no"  Entonces
				escribir "Usted no tiene equipaje en bodega: falso";
			SiNo
				escribir "Entrada inválida. Debe ingresar si o no";
			FinSi
			
		FinSi
	hasta que arreglo[contador, 4]="si" o arreglo[contador, 4] ="no"
	
	escribir "ingrese numero de pasajero frecuente";
	leer arreglo[contador,5];
	
	// Nro de asiento
	arreglo[contador,6]=ConvertirATexto(contador+1);
	
	arreglo[contador,7]=ConvertirATexto(valorPasaje(ruta,contador));
	
	muestraDatos(arreglo,contador);
	contador=contador+1;
	
FinSubProceso

//------------------------------------------------------------------------------------------//
Funcion return<-valorPasaje(ruta,contador)
	 definir return como entero;
	 Segun ruta Hacer
		1:
			return=150000;
			si contador>20 y contador<=60 Entonces
				return=165000;
			SiNo
				si contador>60 Entonces
					return=180000;
				FinSi
			FinSi
		2:
			return=120000;
			si contador>20 y contador<=60 Entonces
				return=132000;
			SiNo
				si contador>60 Entonces
					return=150000;
				FinSi
			FinSi
			
		3:
			return=70.000;
			si contador>10 y contador<=40 Entonces
				return=80500;
			SiNo
				si contador>40 Entonces
					return=95000;
				FinSi
			FinSi
		4:
			return=95.000;
				si contador>10 y contador<=40 Entonces
					return=109250;
				SiNo
					si contador>40 Entonces
						return=125000;
					FinSi
				FinSi;
				
	FinSegun
FinFuncion

//-------------------------------------------------------------------------------------------------------------//
//mostrar datos de las ventas
SubProceso muestraDatos(arreglo,contador)
	
	Escribir " ";
    Escribir "Datos ingresados:";
    Escribir "Ruta: " ,arreglo[contador,0];	
	escribir "Nombre y apellido: ", arreglo[contador,1];		
	escribir "Dni: ", arreglo[contador,2];		
	escribir "Telefono: ", arreglo[contador,3];		
		
	Si arreglo[contador,4] = "si" Entonces
			escribir "Usted tiene equipaje en bodega: verdadero";
	Sino
			escribir "Usted no tiene equipaje en bodega: falso";
	FinSi
	
	escribir "numero de pasajero frecuente: " , arreglo[contador,5];
	Escribir "Nro de asiento: " ,arreglo[contador,6];
	Escribir "Valor Pasaje: ", arreglo[contador,7];
	Escribir "";
FinSubProceso

//-------------------------------------------------------------------------------------------------------------//
//mostrar datos ordenamiento
SubProceso Listado(arreglo,contador)
	definir i como entero;
	para i <- 0 hasta contador-1 con paso 1 hacer
	Escribir " ";
    Escribir "Listado de pasajeros:";
    Escribir "Ruta: " ,arreglo[i,0];	
	escribir "Nombre y apellido: ", arreglo[i,1];		
	escribir "Dni: ", arreglo[i,2];		
	escribir "Telefono: ", arreglo[i,3];		
	
	Si arreglo[i,4] = "si" Entonces
		escribir "Usted tiene equipaje en bodega: verdadero";
	Sino
		escribir "Usted no tiene equipaje en bodega: falso";
	FinSi
	
	escribir "numero de pasajero frecuente: " , arreglo[i,5];
	Escribir "Nro de asiento: " ,arreglo[i,6];
	Escribir "Valor Pasaje: ", arreglo[i,7];
	Escribir "";
FinPara

FinSubProceso


//------------------------------------------------------------------------------------------//
//busqueda de pasajero por asiento
SubProceso busquedaPorAsiento(arreglo,contador)
	definir i como entero;
	definir datoABuscar Como Entero;
	definir encontrado como logico;

	escribir "ingresa el nro de asiento que buscas";
	leer datoABuscar;
	encontrado<- Falso;
	
	i=0;
	mientras  (no encontrado) y (i < contador) hacer		
		
		Si arreglo[i,6] == ConvertirATexto(datoABuscar) Entonces			
            encontrado <- Verdadero;
		SiNo
			i=i+1;
		FinSi
		
	Finmientras
	
	Si (no encontrado) Entonces
		escribir "Pasajero no encontrado";
	sino			
		Escribir "Nombre y apellido: " , arreglo[i,1];
		escribir "Ruta: " , arreglo[i,0];
		Escribir "Dni: " , arreglo[i,2];
	FinSi
FinSubProceso

//----------------------------------------------------------------------------------------
//busqueda de pasajero por nombre y apellido 
SubProceso busquedaPorPasajero(arreglo,contador)
	definir i como entero;
	definir datoABuscar Como caracter;
	definir encontrado como logico;
	
	escribir "ingresa el nombre y apellido que buscas: ";
	leer datoABuscar;
	encontrado<- Falso;
	
	i=0;
	mientras  (no encontrado) y (i < contador) hacer		
		
		Si arreglo[i,1] == datoABuscar Entonces			
            encontrado <- Verdadero;
		SiNo
			i=i+1;
		FinSi
		
	Finmientras
	
	Si (no encontrado) Entonces
		escribir "Pasajero no encontrado";
	sino			
		Escribir "Nombre y apellido: " , arreglo[i,1];
		escribir "Ruta: " , arreglo[i,0];
		Escribir "Dni: " , arreglo[i,2];
	FinSi
FinSubProceso


//---------------------------------------------------------------------------------------

subproceso ordenamientoAscendente(arreglo,contador)
	definir i, j Como Entero;
	definir aux Como Caracter;
	
	
	para i=0 hasta contador-2 con paso 1 Hacer		
		para j=i+1 hasta contador-1  con paso 1 Hacer			
			si arreglo[i,6] > arreglo[j,6] Entonces  // convertir a numero
				aux <- arreglo[i,6];
				arreglo[i,6] <- arreglo[j,6];
				arreglo[j,6] <- aux;
				
				aux <- arreglo[i,0];
				arreglo[i,0] <- arreglo[j,0];
				arreglo[j,0] <- aux;
				
				aux <- arreglo[i,1];
				arreglo[i,1] <- arreglo[j,1];
				arreglo[j,1] <- aux;
				
				aux <- arreglo[i,2];
				arreglo[i,2] <- arreglo[j,2];
				arreglo[j,2] <- aux;
				
				aux <- arreglo[i,3];
				arreglo[i,3] <- arreglo[j,3];
				arreglo[j,3] <- aux;
				
				aux <- arreglo[i,4];
				arreglo[i,4] <- arreglo[j,4];
				arreglo[j,4] <- aux;
				
				aux <- arreglo[i,5];
				arreglo[i,5] <- arreglo[j,5];
				arreglo[j,5] <- aux;
				
				
			FinSi
		FinPara
	FinPara
	
	
FinSubProceso


//----------------------------------------------------------------------------------------------------------------
subproceso ordenamientoDescendente(arreglo,contador)
	definir i, j Como Entero;
	definir aux Como Caracter;
	
	para i=0 hasta contador-2 Hacer
		para j=i+1 hasta contador-1 Hacer
			si arreglo[i,6] < arreglo[j,6] Entonces  // convertir a numero
				aux <- arreglo[i,6];
				arreglo[i,6] <- arreglo[j,6];
				arreglo[j,6] <- aux;
				
				aux <- arreglo[i,0];
				arreglo[i,0] <- arreglo[j,0];
				arreglo[j,0] <- aux;
				
				aux <- arreglo[i,1];
				arreglo[i,1] <- arreglo[j,1];
				arreglo[j,1] <- aux;
				
				aux <- arreglo[i,2];
				arreglo[i,2] <- arreglo[j,2];
				arreglo[j,2] <- aux;
				
				aux <- arreglo[i,3];
				arreglo[i,3] <- arreglo[j,3];
				arreglo[j,3] <- aux;
				
				aux <- arreglo[i,4];
				arreglo[i,4] <- arreglo[j,4];
				arreglo[j,4] <- aux;
				
				aux <- arreglo[i,5];
				arreglo[i,5] <- arreglo[j,5];
				arreglo[j,5] <- aux;
				
				
			FinSi
		FinPara
	FinPara
	
	
FinSubProceso
	
