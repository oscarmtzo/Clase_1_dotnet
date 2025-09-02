# Introducción a la Programacion Paralela en .NET

![diagrama excalidraw](./diagramas/diagrama_1.excalidraw)

## Usos de Clase Thread

```csharp
using System;
using System.Threading;

class Program
{
    static void Main()
    {
        Thread hilo = new Thread(Mensaje);
        hilo.Start();

        Console.WriteLine("Mensaje desde el hilo principal.");
        hilo.Join(); // Espera a que el hilo secundario termine
    }

    static void Mensaje()
    {
        Console.WriteLine("Mensaje desde el hilo secundario.");
    }
}


```

