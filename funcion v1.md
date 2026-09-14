using System;

static int ManejarLinea(string texto, int numeroSalto)
	{
    Console.WriteLine(texto);

  	  if (numeroSalto == 1)
  	  {
        return 1; // esta línea es un final: hay que terminar el cuento
 	   }

  	  if (numeroSalto == 0)
  	  {
        return 0; // esta línea no era una decisión, no hay nada más que hacer
  	  }

   	 string entrada = Console.ReadLine();

   	 if (entrada == "1")
   	 {
        return 0; // opción 1: seguir la secuencia normal
   	 }

   	 if (entrada == "2")
   	 {
        return numeroSalto; // opción 2: saltar a la línea indicada
  	  }

  	  return 0; // valor por defecto: si el usuario escribió algo inválido, seguimos normal
	}

static void Main()
{
    string [] textos = {"Bogotá amanece gris. Miras el celular: 7:18 a.m.", "La clase empieza a las 8:00. Sales corriendo a la calle.", "Llegas a la esquina. 1) Tomar el camino conocido. 2) Tomar un atajo.","Caminas por la ruta de siempre, pasando la panadería.","Llegas a clase justo a tiempo. FINAL: LLEGASTE.","Entras por el atajo. Al fondo hay una construcción bloqueando el paso.","1) Rodear por el andén. 2) Cruzar la calle rápidamente.","Rodeas con cuidado y llegas a clase apenas a tiempo. FINAL: LLEGASTE.","Cruzas justo cuando pasa una moto. FINAL: NO LLEGASTE."};
	int [] saltos = {0, 0, 5, 0, 1,0, 8, 1, 1};
	
	for (int i = 0; i < textos.Length; i++){
			int resultado = ManejarLinea(textos[i], saltos[i]);

			if (resultado == 1)
			{
				break;
			}

			else if (resultado != 0)
			{
				i = resultado - 1; // nos ubicamos justo antes de la línea destino...
			}
		}
}
Main ();
