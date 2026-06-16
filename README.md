#  Food Store – Sistema de Gestión de Pedidos

Trabajo Práctico Integrador – Programación 2  
Tecnicatura Universitaria en Programación – UTN

---

## Descripción

Aplicación de consola desarrollada en Java 21 que permite gestionar categorías, productos, usuarios y pedidos de un negocio de comidas. Toda la información se almacena en memoria mediante Colecciones durante la ejecución del programa.

---

## Requisitos

- Java 21 o superior
- IDE recomendado: NetBeans o Eclipse (o cualquier IDE con soporte Java)

Verificar versión de Java instalada:
```bash
java -version
```

---

## Estructura del proyecto

```
src/
└── integrado/prog2/
    ├── Main.java
    ├── entities/
    │   ├── Base.java
    │   ├── Calculable.java         ← interfaz
    │   ├── Categoria.java
    │   ├── Producto.java
    │   ├── Usuario.java
    │   ├── Pedido.java
    │   └── DetallePedido.java
    ├── enums/
    │   ├── Estado.java
    │   ├── FormaPago.java
    │   └── Rol.java
    ├── exception/
    │   ├── EntidadNoEncontradaException.java
    │   ├── StockInvalidoException.java
    │   └── ValidacionException.java
    ├── service/
    │   ├── CategoriaService.java
    │   ├── ProductoService.java
    │   ├── UsuarioService.java
    │   └── PedidoService.java
    └── ui/
        ├── Consola.java
        ├── MenuCategorias.java
        ├── MenuProductos.java
        ├── MenuUsuarios.java
        └── MenuPedidos.java
```

---

## Cómo ejecutar el proyecto

### Opción 1 – NetBeans (recomendado)

1. Abrir NetBeans
2. Seleccionar **File > Open Project**
3. Seleccionar la carpeta raíz del proyecto
4. Asegurarse de que el JDK esté configurado en **Java 21 o superior**  
   (clic derecho en el proyecto > Properties > Libraries > Java Platform)
5. Clic derecho sobre `Main.java` → **Run File**

### Opción 2 – Eclipse

1. Abrir Eclipse
2. Ir a **File > Import > Existing Projects into Workspace**
3. Seleccionar la carpeta raíz del proyecto
4. Hacer clic derecho sobre `Main.java` → **Run As > Java Application**

---

## Uso del sistema

Al iniciar, se muestra el menú principal:

```
========================================
   SISTEMA DE PEDIDOS (FOOD STORE)
========================================
1. Categorias
2. Productos
3. Usuarios
4. Pedidos
0. Salir
Seleccione:
```

Cada opción abre un submenú con operaciones CRUD. Se recomienda seguir este orden para probar el sistema:

1. Crear una **Categoría**
2. Crear un **Producto** (asociado a la categoría)
3. Crear un **Usuario**
4. Crear un **Pedido** (asociado al usuario, con productos como detalles)

---

## Funcionalidades principales

- CRUD completo de Categorías, Productos, Usuarios y Pedidos
- Baja lógica (soft delete) en todas las entidades
- Validaciones de entrada (precio, stock, mail único, campos obligatorios)
- Excepciones propias: `EntidadNoEncontradaException`, `StockInvalidoException`, `ValidacionException`
- Cálculo automático de totales mediante la interfaz `Calculable`
- Filtro de pedidos por usuario
- Filtro de productos por categoría

---

## Video demostrativo

🎥 [https://www.youtube.com/watch?v=JvGN0OzYxjI&t=51s](https://www.youtube.com/watch?v=JvGN0OzYxjI&t=51s)

---

## Repositorio en GitHub

🔗 [https://github.com/ghernanc/Trabajo_practico_integrador_2](https://github.com/ghernanc/Trabajo_practico_integrador_2)

---

## Autor

**Gustavo Campestre**  
Tecnicatura Universitaria en Programación  
Universidad Tecnológica Nacional (UTN)  
Programación 2

---

## Conceptos aplicados

- Programación Orientada a Objetos (POO)
- Herencia mediante la clase abstracta `Base`
- Encapsulamiento
- Polimorfismo
- Interfaces (`Calculable`)
- Enumeraciones (`Rol`, `Estado`, `FormaPago`)
- Manejo de Excepciones Personalizadas
- Colecciones (`ArrayList`)
- Baja lógica (Soft Delete)
