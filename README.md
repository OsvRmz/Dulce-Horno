## DULCE HORNO

Dulce Horno es una aplicación diseñada para facilitar la compra de
productos de panadería. Permite a los usuarios registrarse,
explorar un catálogo digital, realizar pedidos, gestionar su carrito
de compras y consultar su historial de compras. Su objetivo es
optimizar la experiencia del cliente al ofrecer una plataforma
rápida, clara y funcional, construida sobre JAVA. 

. Inicio de sesión y registro de usuarios.
- Catálogo de productos con buscador y filtros por tipo (pan dulce,
galletas, bebidas, etc.).
- Carrito de compras con cálculo automático del total y costo de
envío.
- Ventana emergente de ubicación para definir la dirección de
entrega.
- Historial de recibos con detalles de pedidos anteriores.


## CÓMO EJECUTARLO

1. Descargar el repositorio.
2. El archivo MyApp.java contiene una utl base para hacer las solicitudes http, ejecutar la API rest de https://github.com/OsvRmz/Dulce-Horno-Server.git, al ejecutarla, el puerto en el que esté lanzado debe colocarse en la variable BASE_URL al final de la cadena, para que las solicitudes vayan al puerto correcto
   ```java
   package com.example.dulcehorno;

   import android.app.Application;

   public class MyApp extends Application {
    private static MyApp instance;

    // Base URL de tu API
    private final String BASE_URL = "https://dulcehorno.onrender.com/api/";

    @Override
    public void onCreate() {
        super.onCreate();
        instance = this;
    }

    public static MyApp getInstance() {
        return instance;
    }

    public String getBaseUrl() {
        return BASE_URL;
    }
   }

   ```
3. Ejecutar la aplicación en el emulador, así las request http van a ser capaces de llegar a la API anteriormente ejecutada. 
