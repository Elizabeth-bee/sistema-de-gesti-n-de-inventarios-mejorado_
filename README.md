# Documentación del Sistema de Gestión de Inventarios con Manejo de Archivos

## Descripción General

Este sistema de gestión de inventarios permite administrar productos mediante operaciones de **alta**, **actualización**, **eliminación** y **consulta**.  
Las operaciones se reflejan en un archivo de texto (`inventario.txt`), garantizando persistencia de datos entre ejecuciones.  

El sistema implementa **manejo de excepciones** para prevenir errores durante la lectura y escritura de archivos, y ofrece retroalimentación al usuario en la consola.

---

## Clases y Métodos

### Clase `camisa 
Representa un pantalon dentro del inventario.

**Atributos:**
- `id` (int): Identificador único del blusa
- `nombre` (str): Nombre del camisa
- `cantidad` (int): 30 disponible en inventario.
- `precio` (float): 49,99 unitario.

**Métodos:**
- `__str__()`: Devuelve una representación legible del product para mostrar al usuario.

---

### Clase `Inventario`

Gestiona el conjunto de productos y su persistencia en archivos.

**Atributos:**
- `productos` (dict): Diccionario con los productos cargados, donde la clave es el `id`.

**Métodos Principales:**

- `cargar_inventario()`:

- `
- `agregar_camisa)`:  
  - Añade un camisa al inventario y actualiza el archivo.  
  - Notifica en consola el éxito o error de la operación.

- `actualizar_producto(id: int, cantidad: int, precio: float)`:  
  - Modifica atributos de un producto existente.  
  - Persiste los cambios en el archivo.  
  - Informa al usuario si el producto no existe.

- `eliminar_producto(id: int)`:  
  - Elimina un producto por su identificador.  
  - Guarda los cambios en el archivo.  
  - Notifica éxito o fallo.

- `mostrar_inventario()`:  
  - Imprime en consola todos los productos almacenados.

---

## Interfaz de Usuario en Consola

El programa ofrece un menú interactivo con las siguientes opciones:

1. Agregar producto  
2. Actualizar producto  
3. Eliminar producto  
4. Mostrar inventario  
5. Salir  

Cada operación informa al usuario del **resultado de la acción** (ejemplo: *"Producto agregado exitosamente"*, *"Error al guardar archivo: permisos insuficientes"*).

---

## Manejo de Excepciones

El sistema implementa un control robusto para los siguientes casos:

- 

- 

## Ejemplo de Flujo

```text
Bienvenido al Sistema de Inventarios
1. Agregar blusa
2. Actualizar camisa
3. Eliminar jeans
4. Mostrar inventario
5. Salir

Seleccione una opción: 1
Ingrese ID del producto: 101
Ingrese nombre del producto: Teclado
Ingrese cantidad: 20
Ingrese precio: 35.5
Producto agregado exitosamente al inventario y guardado en archivo.
```
 def valor_total(self):
        """
        Calcula el valor total del producto.

        Returns:
            float: Cantidad * precio.
        """
        return self.cantidad * self.precio


class Inventario:
    """
    Gestiona una colección de productos y la persistencia en archivo.

    Atributos:
        productos (list): Lista de objetos Producto.
        archivo (str): Ruta del archivo donde se guarda el inventario.

    Métodos:
        cargar_inventario(): Carga productos desde el archivo, creando el archivo si no existe.
        guardar_inventario(): Guarda productos en el archivo.
        agregar_producto(producto): Añade un producto y actualiza el archivo.
        actualizar_producto(id_producto, nombre=None, cantidad=None, precio=None): Actualiza un producto existente.
        eliminar_producto(id_producto): Elimina un producto por ID.
        listar_productos(): Muestra todos los productos en consola.
    """
    
    def __init__(self, archivo="inventario.txt"):
        """
        Inicializa el inventario y carga los productos desde el archivo.

        Args:
            archivo (str): Ruta del archivo del inventario.
        """
        self.productos = []
        self.archivo = archivo
        self.cargar_inventario()

    def cargar_inventario(self):
        """
        Carga los productos desde el archivo.

        Maneja excepciones:
            FileNotFoundError: Crea el archivo si no existe.
            PermissionError: Notifica que no se tienen permisos de lectura.
            ValueError: Detecta datos corruptos.

        Reconstruye la lista de productos en memoria.
        """
        pass  # Implementación de lectura de archivo con manejo de excepciones

    def guardar_inventario(self):
        """
        Guarda todos los productos en el archivo.

        Maneja excepciones:
            PermissionError: Notifica que no se pueden escribir datos en el archivo.
        """
        pass  # Implementación de escritura de archivo con manejo de excepciones

    def agregar_producto(self, producto):
        """
        Añade un nuevo producto al inventario y actualiza el archivo.

        Args:
            producto (Producto): Producto a añadir.

        Notifica si la operación fue exitosa o fallida.
        """
        pass

    def actualizar_producto(self, id_producto, nombre=None, cantidad=None, precio=None):
        """
        Actualiza los atributos de un producto existente.

        Args:
            id_producto (int): ID del producto a actualizar.
            nombre (str, optional): Nuevo nombre.
            cantidad (int, optional): Nueva cantidad.
            precio (float, optional): Nuevo precio.

        Notifica si la operación fue exitosa o fallida.
        """
        pass

    def eliminar_producto(self, id_producto):
        """
        Elimina un producto del inventario por su ID.

        Args:
            id_producto (int): ID del producto a eliminar.

        
    def listar_productos(self):
        """
        Muestra todos los productos del inventario en consola,
        incluyendo ID, nombre, cantidad, precio y valor total.
        """
--

#
---
