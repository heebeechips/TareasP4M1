using System;

class Program
{
    static void Main()
    {
		//J1
		Console.WriteLine("Ingrese el nombre del Jugador 1");
		String jugador1 = Console.ReadLine();
		Console.WriteLine("Ingrese la cantidad de vidas de "+ jugador1) ;
		int j1vida = int.Parse(Console.ReadLine());
		Console.WriteLine("Ingrese el puntaje de "+ jugador1) ;
		int j1puntos= int.Parse(Console.ReadLine());
		Console.WriteLine("Ingrese la veloocidad de "+ jugador1) ;
		int j1velocidad = int.Parse(Console.ReadLine());
	//J2
		Console.WriteLine("Ingrese el nombre del Jugador 2");
		String jugador2 = Console.ReadLine();
		Console.WriteLine("Ingrese la cantidad de vidas de "+ jugador2) ;
		int j2vida = int.Parse(Console.ReadLine());
		Console.WriteLine("Ingrese el puntaje de "+ jugador2) ;
		int j2puntos= int.Parse(Console.ReadLine());
		Console.WriteLine("Ingrese la veloocidad de "+ jugador2) ;
		int j2velocidad = int.Parse(Console.ReadLine());
		
		//J3
		Console.WriteLine("Ingrese el nombre del Jugador 3");
		String jugador3 = Console.ReadLine();
		Console.WriteLine("Ingrese la cantidad de vidas de "+ jugador3) ;
		int j3vida = int.Parse(Console.ReadLine());
		Console.WriteLine("Ingrese el puntaje de "+ jugador3) ;
		int j3puntos= int.Parse(Console.ReadLine());
		Console.WriteLine("Ingrese la veloocidad de "+ jugador3) ;
		int j3velocidad = int.Parse(Console.ReadLine());
		
		string[] nombres = {jugador1, jugador2, jugador3};
		int[] vidas = {j1vida, j2vida, j3vida};
		int[] puntos = {j1puntos, j2puntos, j3puntos};
		int[] velocidad = {j1velocidad, j2velocidad, j3velocidad};
		
		
		Console.WriteLine("Selecciona tu jugador (escribe 1, 2, o 3)");
		int numerojugador = int.Parse(Console.ReadLine());
		Console.WriteLine("Nombre: " + nombres [numerojugador-1]);
		Console.WriteLine("vidas: " + vidas [numerojugador-1]);
		Console.WriteLine("Nombre: " + puntos [numerojugador-1]);
		Console.WriteLine("Nombre: " + velocidad [numerojugador-1]);
	}	
}
