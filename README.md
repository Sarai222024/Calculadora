

# PROYECTO CALCULADORA
DISEÑO DEL PROYECTO
El objetivo de este proyecto es desarrollar una calculadora que  permita  realizar  operaciones  
aritméticas  básicas (suma, resta, multiplicación, división, porcentaje) mediante una interfaz 
gráfica de usuarios.




## FUNCIONALIDAD DEL PROYECTO
La calculadora implementa las operaciones básicas de suma, resta, multiplicación, división y 
porcentaje, además de la posibilidad de trabajar con decimales. Las funciones están definidas en la 
clase operaciones, donde cada operación aritmética tiene su propio método.
También la calculadora cuenta con la funcionalidad de eliminar el último carácter ingresado y 
limpiar por completo la entrada.


## CLASE OPERACIONES:
•	MÉTODO SUMAR:
Toma dos números, los suma y devuelve el resultado.
•	MÉTODO RESTAR:
Toma dos números, resta el segundo del primero y devuelve el resultado.
•	MÉTODO MULTIPLICAR:
Toma dos números, los multiplica y devuelve el resultado.
•	MÉTODO DIVIDIR:
Toma dos números, divide el primero entre el segundo y devuelve el resultado. Si el segundo número es 0, muestra un mensaje de error porque no se puede dividir entre cero.
•	MÉTODO PORCENTAJE:
Toma un número y lo divide entre 100 para calcular su porcentaje. Devuelve el resultado como un número decimal.
•	MÉTODO MAIN:
Este es el punto de entrada del programa. Aquí se crean instancias de la clase Operaciones y se llaman los métodos para ver ejemplos de cómo funcionan.
### Ejemplo
```
Sumamos dos números (10 + 5).
Restamos dos números (10 - 5).
Multiplicamos dos números (10 * 5).
Dividimos dos números (10 / 2), o mostramos un error si el divisor es 0.
Calculamos el 50%, que es 0.5.
```

## CLASE CALCULADORA1
Se encarga de gestionar la lógica de inicio de sesión y la apertura de la ventana de la calculadora. 

usuario: Almacena el nombre del usuario que ha iniciado sesión.
METODO CALCULADORA1
-Parámetros:
user: String — El nombre del usuario que ha iniciado sesión. Este parámetro es requerido para identificar al usuario en la aplicación.
Valor de retorno: void (constructor) — No devuelve ningún valor.
-Excepciones:
IOException: Puede lanzarse al intentar abrir la ventana de la calculadora si hay un problema de entrada/salida.
Descripción: Este constructor inicializa la variable usuario y crea una nueva instancia de la ventana de la calculadora.
Ejemplo :

```
Calculadora1 calc = new Calculadora1("usuario123");
main(String[] args)
```
Parámetros:
args: String[] — Un arreglo de cadenas que puede contener argumentos pasados desde la línea de comandos.
Valor de retorno: void — No devuelve ningún valor.
-Excepciones: Ninguna explícita, aunque cualquier excepción no manejada puede causar que el programa termine inesperadamente.
Descripción: Método principal que inicia la aplicación llamando al método launchApp().
### Ejemplo:
Este método se ejecuta automáticamente al iniciar la aplicación y no se llama explícitamente.

```
launchApp()
```

-Parámetros:Ninguno.
Valor de retorno: void — No devuelve ningún valor.
-Excepciones:
No se especifican excepciones en el método, pero puede lanzar cualquier excepción no manejada si la inicialización falla.
Descripción: Crea una instancia de la ventana de inicio de sesión (Loggin) y la hace visible para el usuario.

###Ejemplo:
Este método se llama desde el método main para iniciar el proceso de inicio de sesión:

```
launchApp();

```
Llama al método para abrir la ventana de inicio de sesión.
### Ejemplo: 
Para utilizar esta clase, el usuario puede ejecutarla desde un entorno que soporte aplicaciones Java. 
Se abrirá la ventana de inicio de sesión. Una vez que el usuario se autentique, se abrirá la ventana de la calculadora.


```
public static void main(String[] args) {
    Calculadora1 calc = new Calculadora1("usuario123"); // Inicializa la calculadora con el usuario "usuario123".
}
```


# Clase Archivos
String nombre: Establece el nombre del archivo. 

•	Método create(String ruta):
String ruta: Especifica dónde se creará el archivo.

•	Método registrar(String linea):
String linea: Es la línea de texto que se quiere agregar al archivo. 
•	Método setNombre(String nombre):
String nombre: Cambia el nombre del archivo. 
•	Método setArchivo(File archivo):
File archivo: Establece un nuevo archivo. Valor de Retorno de Cada Método:
•	Método create(String ruta):
No devuelve un valor, pero puede lanzar un error si falla. 
•	Método getNombre():
Devuelve el nombre del archivo como un String.
•	Método registrar(String linea):
Devuelve true si se registró la línea, o false si hubo un error. 
•	Método limpiarArchivo():
Devuelve true si se limpió el archivo, o false si hubo un error. 
•	Método getArchivo():
Devuelve el objeto File que representa el archivo. Excepciones que Puede Lanzar Cada Método:
•	Método create(String ruta):
Lanza IOException si hay un problema al crear el archivo. Método registrar(String linea):
Lanza IOException si hay un problema al escribir en el archivo. Método limpiarArchivo():
Lanza IOException si hay un problema al eliminar el archivo.
### Ejemplos:

```
Archivos archivo = new Archivos("miArchivo.txt");
try {
    archivo.create("ruta/del/archivo/miArchivo.txt");
} catch (IOException e) {
    System.out.println("Error al crear el archivo: " + e.getMessage());
}

```
Registrar una línea:
### Ejemplo


```
boolean exito = archivo.registrar("Esta es una línea de ejemplo.");

```
Limpiar el archivo:
### Ejemplo
```
boolean limpio = archivo.limpiarArchivo();
```
Obtener el nombre del archivo:

### Ejemplo

```
String nombreArchivo = archivo.getNombre();

```

## LA CLASE LOGGIN
Gestiona la interfaz de inicio de sesión, permite a los usuarios ingresar sus credenciales y verificar si son correctas. También permite a los nuevos usuarios registrarse. Si ocurre un error al cargar los usuarios desde el archivo, se maneja de manera adecuada. Parámetros de Cada Método:
Constructor Loggin():
No tiene parámetros. Inicializa la ventana de inicio de sesión y carga los usuarios. Método initComponents():
•	No tiene parámetros. Se encarga de configurar la interfaz gráfica. Método loadUsers():
•	No tiene parámetros. Carga los usuarios desde un archivo de texto. Método actionPerformed(ActionEvent e):
•	Parámetro: ActionEvent e: Representa el evento de acción (como clics en botones). 
•	Método refreshUsers():
•	No tiene parámetros. Recarga la lista de usuarios desde el archivo. Método setVisible(boolean visible):
•	Parámetro: boolean visible: Controla la visibilidad de la ventana. Valor de Retorno de Cada Método:
Constructor Loggin():
No devuelve valor. Método initComponents():
No devuelve valor. Método loadUsers():
No devuelve valor. Método actionPerformed(ActionEvent e):
No devuelve valor. Método refreshUsers():
No devuelve valor. Método setVisible(boolean visible):
No devuelve valor. Excepciones que Puede Lanzar Cada Método:
•	Método loadUsers():
Lanza IOException si hay un problema al leer el archivo de usuarios. Método actionPerformed(ActionEvent e):
Puede lanzar IOException al crear una nueva ventana (ventana) en caso de error.
### Ejemplos:
Creamos una nueva instancia de Loggin:

```
Loggin loggin = new Loggin();

```
 Inicia la ventana de inicio de sesión
Iniciar sesión:
El usuario ingresa su nombre de usuario y contraseña en la interfaz. Al hacer clic en "Acceder", el programa verifica si el usuario existe y si la contraseña es correcta. Registrar un nuevo usuario:
Al hacer clic en "Registrarse", se cierra la ventana de inicio de sesión y se abre la ventana de registro. Cerrar la ventana:
Al hacer clic en "Cancelar", se cierra la ventana de inicio de sesión.


## LA CLASE REGISTER
Gestiona la interfaz para registrar nuevos usuarios. Permite ingresar un nombre de usuario y dos contraseñas, validando que coincidan antes de guardar los datos en un archivo. También proporciona mensajes para informar al usuario sobre el éxito o fallo de la operación.
Constructor Register():
•	No tiene parámetros. Inicializa la ventana de registro y establece la interfaz de usuario. Método actionPerformed(ActionEvent e):
•	Parámetro: ActionEvent e: Representa el evento de acción (como clics en botones). Valor de Retorno de Cada Método:
Constructor Register():
•	No devuelve valor. Método actionPerformed(ActionEvent e):
•	No devuelve valor, pero muestra mensajes de diálogo dependiendo del resultado de la operación (registro exitoso o error). Excepciones que Puede Lanzar Cada Método:
•	Método actionPerformed(ActionEvent e): Lanza IOException si hay un problema al escribir en el archivo de usuarios.
### Ejemplo:
Creamos una nueva instancia de Register:


```
Register registro = new Register();

```
 Inicia la ventana de registro
Registrar un nuevo usuario:
El usuario ingresa su nombre de usuario y contraseña, y luego confirma la contraseña. Al hacer clic en "Guardar", el programa valida que las contraseñas coincidan. Si coinciden, se guarda el nuevo usuario en el archivo y se muestra un mensaje de éxito. Cerrar la ventana:
Al hacer clic en "Cancelar", se cierra la ventana de registro. La clase ventana implementa una calculadora básica en Java utilizando una interfaz gráfica de usuario (GUI). Permite realizar operaciones aritméticas como suma, resta, multiplicación y división, así como registrar operaciones en un archivo.
•	Métodos importantes ventana(String usuario)
•	Parámetros: usuario: Nombre del usuario para personalizar la interfaz. Valor de retorno: Ninguno (constructor). Excepciones: Lanza IOException si hay un problema al crear o cargar archivos.
### Ejemplo:

```
ventana miVentana = new ventana("Juan");
iniciar(String usuario)

```
•	Parámetros: usuario: Nombre del usuario para personalizar la interfaz. Valor de retorno: Ninguno. Excepciones: Lanza IOException si hay un problema al crear el archivo. ###Ejemplo: Podemos invocar dentro del constructor.
actionPerformed(ActionEvent e)

•	Parámetros: e: Evento que contiene información sobre la acción del usuario. Valor de retorno: Ninguno. Excepciones: No lanza excepciones manejadas. Ejemplo de uso: Se ejecuta automáticamente al hacer clic en un botón. calcular()
•	Parámetros: Ninguno. Valor de retorno: Ninguno. Excepciones: Lanza Exception si hay un error al evaluar la expresión. Ejemplo de uso: Se invoca al presionar el botón "=". cargarOperacionesDesdeArchivo()
•	Parámetros: Ninguno. Valor de retorno: Ninguno. Excepciones: Lanza IOException si no puede leer el archivo. Ejemplo de uso: Se invoca al iniciar la ventana. guardarOperacionesEnArchivo()
•	Parámetros: Ninguno. Valor de retorno: Ninguno. Excepciones: Lanza IOException si no puede escribir en el archivo. Ejemplo de uso: Se invoca después de calcular o modificar operaciones. modificarOperacion(int indice, String nuevaOperacion)
•	Parámetros: indice: Índice de la operación a modificar. nuevaOperacion: Nueva operación que reemplazará a la anterior. Valor de retorno: Ninguno. Excepciones: Lanza IndexOutOfBoundsException si el índice es inválido.

### Ejemplo:

```
ventana.modificarOperacion(0, "5 + 3");

```
### Ejemplo:
Para utilizar la calculadora, podemos crear una instancia de la clase ventana pasando el nombre del usuario:

```
public static void main(String[] args) {
    try {
        new ventana("Juan");
    } catch (IOException e) {
        e.printStackTrace();
    }
}

```
Excepciones
IOException: Puede lanzarse en varios métodos si hay problemas al leer o escribir archivos. IndexOutOfBoundsException: Se puede lanzar en modificarOperacion si se intenta modificar una operación con un índice inválido.



## CLASE VENTANA
Constructor: ventana(String usuario)
•	Descripción: Inicializa la ventana de la calculadora y carga las operaciones del archivo asociado al usuario.
•	Parámetros:
o	String usuario: El nombre del usuario, que se utiliza para personalizar la interfaz y gestionar archivos de operaciones.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Puede lanzar IOException si hay problemas al crear archivos o al cargar operaciones.
###	Ejemplo:


```
ventana miVentana = new ventana("Juan");

```
 Método: iniciar(String usuario)
•	Descripción: Configura la interfaz gráfica, creando los componentes necesarios y asignando los eventos de los botones.
•	Parámetros:
o	String usuario: Nombre del usuario para personalizar la ventana.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Puede lanzar IOException si hay problemas al crear archivos.
•	Ejemplo de uso: Este método es llamado automáticamente dentro del constructor.
 Método: actionPerformed(ActionEvent e)
•	Descripción: Maneja las acciones de los botones de la calculadora y actualiza la entrada según la interacción del usuario.
•	Parámetros:
o	ActionEvent e: Evento que indica qué botón fue presionado.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Ninguna esperada.
•	Ejemplo de uso: Este método es invocado automáticamente por el sistema cuando se produce un evento.
 Método: cargarOperacionesDesdeArchivo()
•	Descripción: Carga las operaciones del usuario desde un archivo específico y las añade a la lista de operaciones.
•	Parámetros: Ninguno.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Puede lanzar IOException si hay problemas al leer el archivo.
•	Ejemplo de uso: Llamado automáticamente dentro del constructor.
 Método: guardarOperacionesEnArchivo()
•	Descripción: Guarda la lista actual de operaciones en el archivo correspondiente al usuario.
•	Parámetros: Ninguno.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Puede lanzar IOException si hay problemas al escribir el archivo.
•	Ejemplo de uso: Llamado al final de la operación de cálculo.
 Método: modificarOperacion(int indice, String nuevaOperacion)
•	Descripción: Modifica una operación existente en la lista.
•	Parámetros:
o	int indice: El índice de la operación a modificar.
o	String nuevaOperacion: La nueva cadena que reemplazará la operación existente.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Puede lanzar ArrayIndexOutOfBoundsException si el índice está fuera de rango.
###	Ejemplo:

```
ventana miVentana = new ventana("Juan");
miVentana.modificarOperacion(0, "5 + 3 = 8");

```
 Método: mostrarOperaciones()
•	Descripción: Muestra un diálogo con la lista de operaciones realizadas y permite modificar o eliminar.
•	Parámetros: Ninguno.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Ninguna esperada.
### Ejemplo:

```
miVentana.mostrarOperaciones();

```
Método: calcular()
•	Descripción: Evalúa la expresión matemática ingresada y actualiza el resultado.
•	Parámetros: Ninguno.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Puede lanzar ArithmeticException si hay un error de cálculo (como división por cero) o NumberFormatException si hay problemas al convertir los números.
•	Ejemplo:

```
miVentana.calcular();

```
 Método: registrarActividad(String registro)
•	Descripción: Registra una operación realizada por el usuario en el archivo de actividades.
•	Parámetros:
o	String registro: La operación que se va a registrar.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones: Puede lanzar IOException si hay problemas al escribir en el archivo.
### Ejemplo:


```
Ventana.registrarActividad("5 + 3 = 8");


```
 Métodos para operaciones matemáticas (sumar, restar, multiplicar, dividir)
•	Descripción: Cada uno de estos métodos realiza la operación matemática correspondiente entre dos números.
•	Parámetros: Ninguno, pero utilizan el texto del campo de entrada.
•	Valor de retorno: Ninguno (tipo void).
•	Excepciones:
o	NumberFormatException si los números no pueden ser convertidos a enteros.
o	IOException si hay problemas al registrar la operación en el archivo.
### 	Ejemplo:

```
miVentana.sumar();


```
LA CLASE BOTONCIRCULAR
Extiende JButton para crear un botón con forma circular. Personaliza la apariencia del botón, incluyendo su fondo, borde y el área que responde a los clics.
•	Métodos importantes botonCircular(String texto)
•	Parámetros: texto: El texto que se mostrará en el botón. Valor de retorno: Ninguno (constructor). Excepciones: No lanza excepciones. Ejemplo de uso:
botonCircular miBoton = new botonCircular
paintComponent(Graphics g)

•	Parámetros: g: Objeto gráfico para dibujar en el botón. Valor de retorno: Ninguno. Excepciones: No lanza excepciones manejadas. Descripción: Personaliza el color de fondo del botón según su estado (normal o presionado) y dibuja un óvalo que representa el botón. Ejemplo de uso: Se llama automáticamente cuando se necesita redibujar el botón. paintBorder(Graphics g)
•	Parámetros: g: Objeto gráfico para dibujar el borde del botón. Valor de retorno: Ninguno. Excepciones: No lanza excepciones. Descripción: Dibuja el borde del botón en forma de óvalo. Ejemplo de uso: Se llama automáticamente al dibujar el borde del botón. getPreferredSize()
•	Parámetros: Ninguno. Valor de retorno: Dimension - Tamaño preferido del botón. Excepciones: No lanza excepciones. Descripción: Ajusta el tamaño preferido del botón para que sea cuadrado, usando el mayor de sus dimensiones. Ejemplo de uso: Se invoca automáticamente para obtener el tamaño ideal del botón. contains(int x, int y)
•	Parámetros: x: Coordenada X del punto. y: Coordenada Y del punto. Valor de retorno: boolean - Verdadero si el punto está dentro del área del botón. Excepciones: No lanza excepciones. Descripción: Verifica si las coordenadas dadas están dentro del área circular del botón. Ejemplo de uso: Se llama automáticamente para determinar si el cursor está sobre el botón. Ejemplo de uso general Para utilizar el botón circular, puedes crear una instancia de la clase botonCircular y añadirla a un panel o marco:
### Ejemplo:

```

public static void main(String[] args) {
    JFrame frame = new JFrame("Ejemplo de botón circular");
    botonCircular miBoton = new botonCircular("Clic aquí");
    frame.add(miBoton);
    frame.setSize(200, 200);
    frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    frame.setVisible(true)
}

```










