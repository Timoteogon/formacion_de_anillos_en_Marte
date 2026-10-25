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

### 3. Límite de Roche
El límite de Roche define la distancia crítica donde las fuerzas de marea superan la autogravitación del satélite. Para un cuerpo rígido:

$$d_R = R_{\text{Marte}} \left( 2 \frac{\rho_{\text{Marte}}}{\rho_{\text{Fobos}}} \right)^{1/3}$$

### 4. Tiempo de Colapso Orbital
La solución analítica para el tiempo $t$ en función del radio orbital $r$ hasta alcanzar la disrupción es:

$$t(r) = t_0 + \frac{2 Q}{13 k_2} \frac{M_{\text{Marte}}}{m_{\text{Fobos}}} \sqrt{\frac{1}{G M_{\text{Marte}}}} \frac{1}{R_{\text{Marte}}^5} \left( a_0^{13/2} - r^{13/2} \right)$$

## Estructura del Repositorio

```text
.
├── notebooks/         # Jupyter Notebooks con las simulaciones y análisis
├── src/               # Módulos y funciones auxiliares en Python
├── data/              # Datos orbitales e hiperparámetros
└── README.md          # Documentación principal del proyecto
```

---

### 2. Cómo ejecutar las simulaciones (Uso)
Explica brevemente cómo clonar el repositorio y correr los archivos.

```markdown
## Uso

1. Clona este repositorio en tu máquina local:
   ```bash
   git clone [https://github.com/mateocgonzalez07/formacion_de_anillos_en_Marte.git](https://github.com/mateocgonzalez07/formacion_de_anillos_en_Marte.git)

```
