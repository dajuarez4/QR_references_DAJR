# Problema: Efecto de memoria de forma en un clip de Nitinol

Un clip de Nitinol deformado se encuentra inicialmente a temperatura ambiente:

\[
T_{i,\text{clip}} = 25^\circ C
\]

Para recuperar su forma original, el clip debe alcanzar su temperatura final de austenita:

\[
A_f = 60^\circ C
\]

El clip tiene una masa de:

\[
m_{\text{clip}} = 2.0\,\text{g}
\]

y un calor específico de:

\[
c_{\text{NiTi}} = 0.32\,\frac{\text{J}}{\text{g}\cdot^\circ C}
\]

El clip se coloca dentro de:

\[
m_{\text{agua}} = 100\,\text{g}
\]

de agua caliente, cuyo calor específico es:

\[
c_{\text{agua}} = 4.18\,\frac{\text{J}}{\text{g}\cdot^\circ C}
\]

Suponga que no hay pérdidas de calor al ambiente.

## Pregunta

¿Cuál debe ser la temperatura mínima inicial del agua para que el clip de Nitinol alcance \(A_f\) y recupere su forma original?

La condición física es:

\[
T_{\text{agua}} > A_f
\]

---

# Solución

El clip debe alcanzar:

\[
T_f = A_f = 60^\circ C
\]

El calor ganado por el clip de Nitinol es:

\[
Q_{\text{clip}} = m_{\text{clip}} c_{\text{NiTi}}(T_f - T_{i,\text{clip}})
\]

Sustituyendo los valores:

\[
Q_{\text{clip}} = (2.0)(0.32)(60 - 25)
\]

\[
Q_{\text{clip}} = (2.0)(0.32)(35)
\]

\[
Q_{\text{clip}} = 22.4\,\text{J}
\]

Este calor proviene del agua caliente:

\[
Q_{\text{agua}} = m_{\text{agua}} c_{\text{agua}}(T_{\text{agua}} - T_f)
\]

Por conservación de energía:

\[
Q_{\text{agua}} = Q_{\text{clip}}
\]

Entonces:

\[
m_{\text{agua}} c_{\text{agua}}(T_{\text{agua}} - T_f) = 22.4
\]

Sustituyendo:

\[
(100)(4.18)(T_{\text{agua}} - 60) = 22.4
\]

\[
418(T_{\text{agua}} - 60) = 22.4
\]

\[
T_{\text{agua}} - 60 = \frac{22.4}{418}
\]

\[
T_{\text{agua}} - 60 = 0.0536
\]

\[
T_{\text{agua}} = 60.0536^\circ C
\]

---

# Respuesta final

\[
\boxed{T_{\text{agua}} \approx 60.1^\circ C}
\]

Como:

\[
T_{\text{agua}} > A_f
\]

el clip de Nitinol alcanza la fase austenítica y recupera su forma original.

En un experimento real, el agua debería estar más caliente, por ejemplo:

\[
\boxed{T_{\text{agua}} \approx 70^\circ C}
\]

porque parte del calor se pierde en el vaso, el aire y el ambiente.
