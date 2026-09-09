using System;
class Program
{
 static void Main()
	{
		//Arrays de preguntas
		string[] herramienta = {"Poción", "Espada", "Arco", "Bardo"};
	 	bool [] prefieredia = {true, false};
	 	string [] poder = {"agua", "plantas", "sanación", "furgo", "batalla", "oscuridad"};
	 
		//Nombre
		Console.WriteLine("¿Cuál es el nombre de tu personaje?");
		string nombre = Console.ReadLine();
	 
	 	//Elección 1: herramienta
		Console.WriteLine("Elige tu herramienta:");
		Console.WriteLine("1. Poción     2.Espada");
	 	Console.WriteLine("3. Arco       4.Bardo");
	 	string herramientaselect = Console.ReadLine();
	 	int herramientanum = int.Parse (herramientaselect)-1;
	 	Console.WriteLine("elegiste " + herramienta[herramientanum]);
	 
	    //Elección 2: dia o noche
		Console.WriteLine("¿Qué prefieres?");
		Console.WriteLine("1. El día    2. La Noche");
	 	string prefierediaselect = Console.ReadLine();
	 	int prefieredianum = int.Parse (prefierediaselect)-1;
	 
	    //Elección 3: color
		Console.WriteLine("Elige un color");
		Console.WriteLine("1. azul    2. verde	 3. blanco");
		Console.WriteLine("4. rojo    5. amarillo 6. gris");
	 	string colorselect = Console.ReadLine();
	 	int colornum = int.Parse (colorselect)-1;
	 
	 
	 //Arrays de roles y magias
	 	bool [] esheroe = {false, true, true, false};
	 	String [] especie = {"Elfo", "Vampiro", "humano", "hombre lobo"};
		int [] espvelocidad = {50, 100, 50, 75};
		int [] espfuerza = {50, 75, 60, 100};
	 	int [] espresistencia = {75, 75, 100, 50};
		int [] esphabilidadmagica = {100, 50, 75, 35};
	 	int [] espvida = {100, 90, 75, 50};
	 
	 
	 // variables
	 int especienum = 0;
	 int rangonum = 0;
	 string [] rango = {" de asistencia", " héroe"};
		
	 //procesando personaje
	 if (colornum <=3 && prefieredia[prefieredianum])
	 {
	 especienum = especienum + 1;
	 }
	  else if (prefieredia[prefieredianum]! && colornum>3)
	 {
		especienum = especienum + 2; 
	 }
	 else if (prefieredia[prefieredianum] && colornum>3)
	 {
		especienum = especienum + 3; 
	 }
	 else 
	 {
		 especienum = especienum + 4;
	 }
	 
	 if (esheroe[herramientanum])
				 { 
					rangonum = rangonum +1;
				  }
	 else
	 {
	 }
				 
				 
	 
	// Info final
	 Console.Write(nombre + "es un: ");
	 Console.Write(especie [ especienum ] + rango [rangonum]);
	 
}
}



V2



using System;
class Program
{ 
	static void Main()
	{
	//Arrays de preguntas
	
		string[] herramienta = {"Poción", "Espada", "Arco", "Bardo"};
		bool [] prefieredia = {true, false};
		string [] poder = {"agua", "plantas", "sanación", "fuego", "batalla", "oscuridad"};

	//Nombre
	Console.WriteLine("¿Cuál es el nombre de tu personaje?");
	string nombre = Console.ReadLine();
 
 	//Elección 1: herramienta
	Console.WriteLine("Elige tu herramienta:");
	Console.WriteLine("1. Poción     2.Espada");
 	Console.WriteLine("3. Arco       4.Bardo");
 	string herramientaselect = Console.ReadLine();
 	int herramientanum = int.Parse (herramientaselect)-1;
 	Console.WriteLine("elegiste " + herramienta[herramientanum]);
 
    //Elección 2: dia o noche
	Console.WriteLine("¿Qué prefieres?");
	Console.WriteLine("1. El día    2. La Noche");
 	string prefierediaselect = Console.ReadLine();
 	int prefieredianum = int.Parse (prefierediaselect)-1;
 
    //Elección 3: color
	Console.WriteLine("Elige un color");
	Console.WriteLine("1. azul    2. verde	  3. blanco");
	Console.WriteLine("4. rojo    5. amarillo 6. gris");
 	string colorselect = Console.ReadLine();
 	int colornum = int.Parse (colorselect)-1;
 
 
 //Arrays de roles y magias
 	bool [] esheroe = {false, true, true, false};
 	String [] especie = {"Elfo", "Vampiro", "humano", "hombre lobo"};
	int [] espvelocidad = {50, 100, 50, 75};
	int [] espfuerza = {50, 75, 60, 100};
 	int [] espresistencia = {75, 75, 100, 50};
	int [] esphabilidadmagica = {100, 50, 75, 40};
 	int [] espvida = {100, 90, 75, 75};
 
 
 // variables
 int especienum = 0;
 int rangonum = 0;
 string [] rango = {" de asistencia", " héroe"};
 bool prefierenoche = prefieredia[prefieredianum]!;
	
 //procesando personaje
 if (colornum <=2 && prefieredia[prefieredianum])
 {
	 especienum = 0;
 }
  else if (prefierenoche && colornum<=2)
 {
	especienum = 3; 
 }
 else if (prefieredia[prefieredianum] && colornum>2)
 {
	especienum = 2; 
 }
 else 
 {
	 especienum = 1;
 }
 
 if (esheroe[herramientanum])
			 { 
				rangonum = rangonum +1;
	 			espvida [especienum] = espvida [especienum] -20;
	 			esphabilidadmagica [especienum] = esphabilidadmagica [especienum] +10;
	 			espfuerza [especienum] = espfuerza [especienum] +20;
			  }
 else
 {
 }
			 
			 
 
// Info final
	Console.Write(nombre + " es un ");
	Console.Write(especie [ especienum ] + rango [rangonum]);
	Console.WriteLine(" esto significa que sus stats son:");
	Console.WriteLine("Vida: " + espvida [especienum]);
	Console.WriteLine("Velocidad: " + espvelocidad [especienum]);
	Console.WriteLine("Fuerza: " + espfuerza [especienum]);
	Console.WriteLine("Resistencia: " + espresistencia [especienum]);
	Console.WriteLine("Habilidad mágica: " + esphabilidadmagica [especienum]);
	Console.WriteLine(" ");
	Console.WriteLine("Su poder mágico es " + poder [colornum]);
	Console.WriteLine("Y su herramienta es " + herramienta [herramientanum]);
} }
