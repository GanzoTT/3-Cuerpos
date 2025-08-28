# 🌌 Simulación del Problema de los Tres Cuerpos en Python

Este proyecto implementa una simulación numérica del **Problema de los Tres Cuerpos** utilizando el método de **Euler explícito**.  
El objetivo es modelar las trayectorias de tres masas que interactúan gravitacionalmente entre sí y visualizar su evolución en el tiempo.

---

## 📖 Descripción

El **Problema de los Tres Cuerpos** es un clásico de la mecánica celeste que estudia el movimiento de tres cuerpos bajo la acción de la **gravitación universal de Newton**.  
A diferencia del problema de dos cuerpos, no existe una solución analítica general, por lo que recurrimos a métodos numéricos y simulaciones computacionales para aproximar sus trayectorias.

---

## ⚙️ Funcionamiento del Código

1. **Definición de parámetros iniciales**
   - Constante gravitacional `G = 1.0` (valor simplificado).
   - Masas de los tres cuerpos (`m1, m2, m3`).
   - Posiciones iniciales (`r1, r2, r3`).
   - Velocidades iniciales (`v1, v2, v3`).

2. **Cálculo de aceleraciones**
   - La función `acceleration()` calcula la aceleración sobre cada cuerpo aplicando la **Ley de Gravitación Universal**:
     \[
     \vec{F}_{ij} = G \cdot \frac{m_j}{|\vec{r}_j - \vec{r}_i|^3} (\vec{r}_j - \vec{r}_i)
     \]

3. **Integración temporal (Euler)**
   - Actualización de velocidades:
     \[
     \vec{v}_{t+dt} = \vec{v}_t + \vec{a}_t \cdot dt
     \]
   - Actualización de posiciones:
     \[
     \vec{r}_{t+dt} = \vec{r}_t + \vec{v}_{t+dt} \cdot dt
     \]

4. **Simulación**
   - Se ejecuta un bucle de `steps = 5000` iteraciones.
   - Se almacenan las posiciones de cada cuerpo en listas para su posterior visualización.

5. **Visualización**
   - Se grafican las trayectorias con **Matplotlib**.
   - Se usan escalas iguales en los ejes para representar fielmente el movimiento.

---

## 🚀 Ejecución

Clona este repositorio y ejecuta el script principal:

``bash
python tres_cuerpos.py



Esto generará una gráfica con las trayectorias simuladas.

Ejemplo de salida:

<img width="509" height="405" alt="image" src="https://github.com/user-attachments/assets/6981c1b5-7957-4af2-8c2f-900bbcf33ea3" />

---

## 📊 Resultados

El resultado es una gráfica que muestra las trayectorias de los tres cuerpos interactuando entre sí.  
Dependiendo de las condiciones iniciales, se pueden observar comportamientos como:
- Órbitas cerradas.
- Trayectorias caóticas.
- Escape de uno de los cuerpos.

---

## 📦 Requisitos

El proyecto está desarrollado en **Python 3** y requiere las siguientes librerías:

- `numpy`
- `matplotlib`

Puedes instalarlas con:

```bash
pip install numpy matplotlib
