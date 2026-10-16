# TP N° 5: Lógica de Primer Orden y Programación Lógica

**Institución:** Universidad Católica de Santiago del Estero (UCSE) — Departamento Académico San Salvador (DASS)  
**Carrera:** Tecnicatura Universitaria en Automatización y Robótica / Informática  
**Asignatura:** Laboratorio I (Inteligencia Artificial y Agentes Racionales)  
**Ciclo Lectivo:** 2026  
**Docente / JTP:** Ing. Fabio D. Argañaraz  
**Organización Oficial:** [UCSE-Laboratorio-I](https://github.com/UCSE-Laboratorio-I)

---

## 🎯 Objetivos del Trabajo Práctico
- Comprender el **compromiso ontológico** de la Lógica de Primer Orden (LPO) modelando mundos con objetos, relaciones y funciones.
- Dominar la **sintaxis formal de LPO** diferenciando constantes, variables, funciones, predicados y términos de sentencias atómicas y compuestas.
- Interpretar la **semántica formal** y las condiciones de verdad en modelos formalizados.
- Aplicar correctamente la **cuantificación universal (∀)** y **existencial (∃)**, dominando los conectivos canónicos (⇒ y ∧) y evitando errores comunes de formulación.
- Manejar las propiedades algebraicas, no conmutatividad de cuantificadores mixtos y las leyes de dualidad de De Morgan para cuantificadores.
- Emplear el símbolo de **igualdad (=)** en la ingeniería del conocimiento para dominios de parentesco y relaciones familiares.
- Analizar los métodos y limitaciones de la **reducción a inferencia proposicional** (Instanciación Universal, Skolemización y universos de Herbrand infinitos).
- Formalizar bases de conocimiento complejas mediante cláusulas de primer orden (caso canónico del **Coronel West y los misiles de Nono**).
- Contrastar los mecanismos de **Encadenamiento hacia Adelante (Data-Driven)** y **Encadenamiento hacia Atrás (Goal-Driven)** con unificación.
- Conocer los fundamentos de la **Programación Lógica en Prolog**, la ecuación de Kowalski (*Algoritmo = Lógica + Control*), las cláusulas de Horn y la negación como falla (*Closed World Assumption*).

---

## 📚 Bibliografía y Referencias Obligatorias
1. **Russell, Stuart & Norvig, Peter:** [*Inteligencia Artificial: Un Enfoque Moderno*](http://jdelagarza.fime.uanl.mx/IA/Libros/inteligencia-artificial-un-enfoque-moderno-stuart-j-russell.pdf) (AIMA, 2da / 3ra Edición):
   - **Capítulo 8:** Lógica de Primer Orden (Sintaxis, Semántica, Cuantificadores, Igualdad, Dominio Familia).
   - **Capítulo 9:** Inferencia en Lógica de Primer Orden (Proposicionalización, Unificación, Encadenamiento hacia adelante y atrás, Programación lógica).
2. **Presentación Oficial de Clase:**
   - `6 - Lógica de Primer Orden.pptx` (Diapositivas de cátedra - Ing. Fabio D. Argañaraz).

---

## 🔗 Puente hacia la Próxima Clase (Clase 7 / TP6: SWI-Prolog)
Los conceptos formalizados en este TP5 constituyen la base directa del taller práctico de la **Clase 7 (Lógica aplicada en PROLOG)**:
- **El Árbol Genealógico:** Las definiciones lógicas de $Abuelo(x, y)$ y $Hermano(x, y)$ con exclusión de identidad $\neg(x = y)$ del Ejercicio 6 serán programadas como reglas ejecutables en SWI-Prolog (`abuelo(X, Y) :- padre(X, Z), progenitor(Z, Y).` y `hermano(X, Y) :- progenitor(P, X), progenitor(P, Y), X \= Y.`) para resolver el árbol propuesto en clase.
- **Motor de Inferencia y Backtracking:** El Encadenamiento hacia Atrás (Ejercicio 9) y las Cláusulas de Horn con Negación como Falla / Supuesto de Mundo Cerrado (Ejercicio 10) cobrarán vida interactiva mediante el intérprete y la consola `?-` de SWI-Prolog.

---

## 🚀 Guía de Resolución y Entrega (Git / GitHub)

Este Trabajo Práctico es 100% interactivo y autoevaluable. Sigue estos pasos para resolverlo y acreditar tu entrega:

1. **Bifurcación (Fork):** Ingresa al repositorio oficial [UCSE-Laboratorio-I/TP5](https://github.com/UCSE-Laboratorio-I/TP5) y haz clic en **Fork** (o **Use this template**) para crear tu copia personal en tu cuenta de GitHub.
2. **Clonación local:** Clona tu repositorio bifurcado en tu estación de trabajo:
   ```bash
   git clone https://github.com/TU_USUARIO/TP5.git
   cd TP5
   ```
3. **Resolución Interactiva en el Navegador:** Abre el archivo `index.html` con doble clic en tu navegador preferido (Chrome, Edge, Firefox, Brave). Resuelve los 10 ejercicios interactivos. Tu avance se almacena automáticamente en `localStorage`.
4. **Exportar JSON de Respuestas:** Al alcanzar el 100% de progreso, haz clic en **`💾 Exportar JSON`** (o en el botón al pie de página). Guarda el archivo `respuestas_tp5.json` en la raíz de tu repositorio local.
5. **Autoevaluación Local (Recomendada):** Con Python 3 instalado, verifica tu calificación antes de realizar la entrega final:
   ```bash
   python autograder_tp5.py respuestas_tp5.json
   ```
   *Deberás obtener `100 / 100 pts [■■■■■■■■■■]`.*
6. **Confirmación y Entrega con Git:**
   ```bash
   git add respuestas_tp5.json
   git commit -m "Entrega final TP5 - [Tu Nombre y Apellido]"
   git push origin main
   ```
7. **Notificación:** Envía la URL de tu repositorio personal de GitHub a través del canal formal de la cátedra para su registro.
