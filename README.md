# practica-css-pokedex
Practica 1 de CSS y Modelo de caja
# Reporte Técnico: El Arquitecto Visual - CSS y Modelo de Caja

## 1. Inspección en el Mundo Real
A continuación se presenta la captura del Modelo de Caja inspeccionado desde el navegador:

![Diagrama del Modelo de Caja](caja.png)

* **Margin (lo exterior):** 0px en los cuatro lados.
* **Padding (Seria como el espaciado interior):** Arriba, izquierda y derecha esta en 0px, pero abajo esta a 30px.

---

## 2. La parte de Auditoria Manual y la Correccion al archivo CSS.
Durante la revisión del archivo de estilos se identificaron los siguientes 3 errores de sintaxis:
1. **Unidad de medida ausente:** La propiedad `width: 300;` no tenía unidad; se corrigió a `width: 300px;`.
2. **Valor inválido en español:** La propiedad `text-align: centro;` utilizaba el idioma español; se corrigió a `text-align: center;`.
3. **Punto y coma faltante:** Faltaba el `;` al final de `border-style: solid`, lo que rompía las reglas posteriores. Se refactorizó todo el borde a `border: 2px solid black;`.

---

## 3. Investigación Técnica: Tipografía
* **Diferencia entre Serif y Sans-Serif:** Las fuentes *Serif* tienen remates decorativos en los extremos de las letras, mientras que las *Sans-Serif* son completamente limpias.
* **Recomendación para pantallas:** Recomiendo **Sans-Serif** para dispositivos digitales, ya que su diseño facilita la visión para las pantallas que son reducidas.

---

## 4. Reto del Modelo de Caja
Para solucionar el problema del texto pegado al borde, se agregó la propiedad **`padding`** (el que agregue es `padding: 20px;`) dentro del selector `.tarjeta-pokemon`. A diferencia del `margin` el `padding` genera espacio interno entre el contenido y el borde del contenedor.

---

## 5. Conclusión
Separar el contenido (HTML) de la presentación (CSS) mediante archivos externos es fundamental. Permite mantener un código limpio y mantenible, evita la duplicación de estilos y facilita el trabajo colaborativo, aumenta la rapidez en la creación de proyectos y es bastante flexible.
