# Problema: Efecto de memoria de forma en un clip de Nitinol

Un clip de Nitinol deformado se encuentra inicialmente a temperatura ambiente:

$$
T_{i,\mathrm{clip}} = 25^\circ \mathrm{C}
$$

Para recuperar su forma original, el clip debe alcanzar su temperatura final de austenita:

$$
A_f = 60^\circ \mathrm{C}
$$

El clip tiene una masa de:

$$
m_{\mathrm{clip}} = 2.0\,\mathrm{g}
$$

y un calor específico de:

$$
c_{\mathrm{NiTi}} = 0.32\,\frac{\mathrm{J}}{\mathrm{g}\cdot^\circ \mathrm{C}}
$$

El clip se coloca dentro de:

$$
m_{\mathrm{agua}} = 100\,\mathrm{g}
$$

de agua caliente, cuyo calor específico es:

$$
c_{\mathrm{agua}} = 4.18\,\frac{\mathrm{J}}{\mathrm{g}\cdot^\circ \mathrm{C}}
$$

Suponga que no hay pérdidas de calor al ambiente.

## Pregunta

¿Cuál debe ser la temperatura mínima inicial del agua para que el clip de Nitinol alcance \(A_f\) y recupere su forma original?

La condición física es:

$$
T_{\mathrm{agua}} > A_f
$$

---

# Solución

El clip debe alcanzar:

$$
T_f = A_f = 60^\circ \mathrm{C}
$$

El calor ganado por el clip de Nitinol es:

$$
Q_{\mathrm{clip}} = m_{\mathrm{clip}} c_{\mathrm{NiTi}}(T_f - T_{i,\mathrm{clip}})
$$

Sustituyendo los valores:

$$
Q_{\mathrm{clip}} = (2.0)(0.32)(60 - 25)
$$

$$
Q_{\mathrm{clip}} = (2.0)(0.32)(35)
$$

$$
Q_{\mathrm{clip}} = 22.4\,\mathrm{J}
$$

Este calor proviene del agua caliente:

$$
Q_{\mathrm{agua}} = m_{\mathrm{agua}} c_{\mathrm{agua}}(T_{\mathrm{agua}} - T_f)
$$

Por conservación de energía:

$$
Q_{\mathrm{agua}} = Q_{\mathrm{clip}}
$$

Entonces:

$$
m_{\mathrm{agua}} c_{\mathrm{agua}}(T_{\mathrm{agua}} - T_f) = 22.4
$$

Sustituyendo:

$$
(100)(4.18)(T_{\mathrm{agua}} - 60) = 22.4
$$

$$
418(T_{\mathrm{agua}} - 60) = 22.4
$$

$$
T_{\mathrm{agua}} - 60 = \frac{22.4}{418}
$$

$$
T_{\mathrm{agua}} - 60 = 0.0536
$$

$$
T_{\mathrm{agua}} = 60.0536^\circ \mathrm{C}
$$

---

# Respuesta final

$$
\boxed{T_{\mathrm{agua}} \approx 60.1^\circ \mathrm{C}}
$$

Como:

$$
T_{\mathrm{agua}} > A_f
$$

el clip de Nitinol alcanza la fase austenítica y recupera su forma original.

En un experimento real, el agua debería estar más caliente, por ejemplo:

$$
\boxed{T_{\mathrm{agua}} \approx 70^\circ \mathrm{C}}
$$

porque parte del calor se pierde en el vaso, el aire y el ambiente.
