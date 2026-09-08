using System;

class Program
{
    static void Main()
    {
        string[] nombres = { "David", "Luis", "Carlos", "Diego", "Maria" };
		int[] vidas = {5, 3, 2, 4, 4 };
		int[] puntos = {201, 333, 405, 240, 199 };
		int[] velocidad = {1, 3, 2, 5, 4 };
		bool[] tienellave = {true, false, true, false, false};
		bool[] estaenpuerta = {false, true, true, false, false};
		
		Console.WriteLine("Selecciona tu perfil con un número. 0. David 1.Luis 2.Carlos 3.Diego 4.Maria");
		String Perfil = Console.ReadLine();
		if (int.TryParse(Perfil, out int perfilnumero))
			{
			}
		else 
		{
			Console.WriteLine("Error. Por favor reinicie y seleccione un número válido.");
		}
		
	
			Console.WriteLine("Ha seleccionado a " + nombres[perfilnumero]);
			Console.WriteLine("Este perfil tiene " + vidas[perfilnumero] + " vidas y ");
		    Console.WriteLine(puntos[perfilnumero] + " puntos");
			Console.WriteLine("La velocidad de este jugador es nivel" + velocidad[perfilnumero]);
			
		if (tienellave[perfilnumero] && estaenpuerta[perfilnumero])
		{
			Console.WriteLine("El jugador ya ha abierto la puerta.");
		}
		else if (tienellave[perfilnumero] && estaenpuerta[perfilnumero]!)
		{
			Console.WriteLine("El jugador tiene una llave, pero no ha llegado a la puerta");
		}
		else
		{
			Console.WriteLine("El jugador no tiene una llave aun");
		}

    }
}


