# 🍕 Pizza-Track – Sistema Undo/Redo con Pilas en Java

## 📌 Objetivo
Comprender el concepto de **pila (stack)** y su estructura lógica mediante la implementación de un simulador de gestión de pedidos para una pizzería, aplicando las operaciones **Undo (Deshacer)** y **Redo (Rehacer)**.  
El proyecto utiliza **pilas manuales basadas en listas ligadas**, arreglos de tamaño fijo y buenas prácticas de programación en Java.

---

## 🛠️ Tecnologías Utilizadas
- Lenguaje: **Java**
- Entorno: **Consola**
- Editor: **VS Code / Editor en línea**
- Control de versiones: **GitHub**

---

## 🧱 Arquitectura del Sistema

El sistema está compuesto por:

### 🔹 Clase Pizza
- Representa un pedido.
- Contiene:
  - Nombre de la pizza
  - Arreglo fijo de **3 ingredientes**

### 🔹 Pila Manual (Lista Ligada)
Implementada desde cero sin usar `java.util.Stack`.

Métodos implementados:
- `push()` → Inserta una pizza en el tope
- `pop()` → Elimina y retorna la pizza del tope
- `peek()` → Muestra la pizza del tope sin eliminarla
- `isEmpty()` → Verifica si la pila está vacía

### 🔹 Dos Pilas
- **Pila Principal (Undo):** almacena los pedidos activos
- **Pila Secundaria (Redo):** almacena los pedidos deshechos

---

## 📋 Funcionalidades del Menú

1. **Registrar Pizza**  
   Permite ingresar el nombre de la pizza y 3 ingredientes.  
   Se guarda en la pila principal.

2. **Deshacer (Undo)**  
   Elimina el último pedido registrado y lo mueve a la pila secundaria.

3. **Rehacer (Redo)**  
   Recupera el último pedido deshecho y lo devuelve a la pila principal.

4. **Mostrar Pedido Actual**  
   Muestra la pizza que está en el tope de la pila principal.

0. **Salir**
