# Formación de anillos en Marte

**Autor:** Mateo C. Gonzalez  
*Universidad de Antioquia — Medellín, Colombia*  
**GitHub:** [@mateocgonzalez07](https://github.com/mateocgonzalez07)  
**Contacto:** `mateo.chavarriag@udea.edu.co`

Proyecto de mecánica celeste y ciencias planetarias para estudiar la evolución orbital de Fobos y su posible fragmentación en el límite de Roche.

## Etapas del proyecto

- **Etapa I:** Modelo kepleriano del problema de dos cuerpos e integración numérica.
- **Etapa II:** Evolución orbital por disipación mareal.
- **Etapa III:** Límite de Roche y simulación de anillos.

## Requisitos

El proyecto utiliza librerías de Python para cálculo científico y astrodinámica:
- `numpy`
- `matplotlib`
- `pymcel`
- `spiceypy`

## Modelo Físico y Ecuaciones

### 1. Integración Numérica (Método de Delambre-Verlet)
Para resolver la ecuación de movimiento bajo una aceleración gravitacional central, se utiliza el esquema de segundo orden:

$$\vec{r}_{n+1} = 2\vec{r}_n - \vec{r}_{n-1} + \vec{a}_n \Delta t^2$$

### 2. Disipación Mareal
La evolución temporal del semieje mayor $a(t)$ debido al torque mareal de Marte se modela con la siguiente expresión:

$$\frac{da}{dt} = -\frac{3 k_2}{Q} \frac{m_{\text{Fobos}}}{M_{\text{Marte}}} \left( \frac{R_{\text{Marte}}}{a} \right)^5 \sqrt{\frac{G M_{\text{Marte}}}{a}}$$
