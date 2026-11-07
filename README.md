#include <stdio.h>

#ifdef _WIN32
    #include <windows.h>
#endif

struct Neurona {
	
float peso1;       	
float peso2; 
float sesgo;
float entrada1;
float entrada2;
float salidaDeseada;
float prediccion;
float error;	
	
};

void configurarConsola () {
	
	#ifdef _WIN32
    
	    SetConsoleOutputCP (CP_UTF8);
	    
	#endif
}

int main () {
	
	configurarConsola();
	
struct Neurona miNeurona; 

miNeurona.peso1 = 0.5f;
miNeurona.peso2 = 0.5f;
miNeurona.sesgo = -0.2f;

printf ("=== NEURONA ARTESANAL EN C (PERCEPTRÓN) === \n");
printf ("Estructura de 8 variables inicializada correctamente. \n");
printf ("Sistema listo para procesar datos lógico y matemático. \n");

printf ("Ingresa el valor para la entrada 1: ");
scanf ("%f",&miNeurona.entrada1);

printf ("Ingresa el valor para la entrada 2: ");
scanf ("%f",&miNeurona.entrada2);

miNeurona.prediccion = (miNeurona.entrada1 * miNeurona.peso1) + 
(miNeurona.entrada2 * miNeurona.peso2) +
miNeurona.sesgo;  

printf ("\n--- RESULTADO DEL CÁLCULO ---\n");
printf ("Predicción de la neurona: %.2f\n",miNeurona.prediccion);                      

getchar ();
getchar ();

return 0; }
