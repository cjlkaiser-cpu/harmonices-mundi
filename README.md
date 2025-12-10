# Harmonices Mundi

**La Música de las Esferas — Sistema Solar sonificado según la visión de Johannes Kepler (1619)**

Simulación interactiva que convierte las órbitas planetarias en música. Cada planeta genera un tono basado en su velocidad orbital, siguiendo los principios que Kepler describió en su tratado *Harmonices Mundi*.

## Demo

**[Ver Demo en Vivo](https://cjlkaiser-cpu.github.io/harmonices-mundi/)**

**[Tutorial Interactivo](https://cjlkaiser-cpu.github.io/harmonices-mundi/tutorial.html)**

## Características

### Física Orbital Real
- **8 planetas** con parámetros orbitales reales (semieje mayor, excentricidad, período)
- **Ecuación de Kepler** resuelta con Newton-Raphson para posiciones precisas
- **Leyes de Kepler**: velocidad orbital variable (más rápido en perihelio, más lento en afelio)
- Escalas de tiempo ajustables (1-365 días/segundo)

### Sonificación
- **Modo Kepler 1619**: Frecuencias basadas en los ratios armónicos originales de Kepler
- **Modo Tiempo Real**: Frecuencia proporcional a la velocidad orbital instantánea
- **Modo Musical**: Mapeo a escalas musicales occidentales

### Interfaz
- **Mixer planetario**: Control individual de volumen por planeta
- **Presets armónicos**: Coro completo, planetas rocosos, gigantes gaseosos, tríadas
- **Analizador FFT**: Visualización del espectro en tiempo real
- **Concert Hall**: Modo inmersivo de pantalla completa
- **Fecha simulada**: Seguimiento temporal de la simulación

## Tecnologías

| Tecnología | Uso |
|------------|-----|
| Canvas 2D | Renderizado del sistema solar |
| Web Audio API | Síntesis de sonido y análisis FFT |
| Newton-Raphson | Resolución de ecuación de Kepler |
| Ecuación de Kepler | M = E - e·sin(E) |

## Física

### Ecuación de Kepler
```
M = E - e·sin(E)
```
Donde:
- **M** = Anomalía media (posición temporal)
- **E** = Anomalía excéntrica (posición geométrica)
- **e** = Excentricidad orbital

### Tercera Ley de Kepler
```
T² = a³
```
El período orbital al cuadrado es proporcional al cubo del semieje mayor.

### Velocidad Orbital
```
v = √(GM(2/r - 1/a))
```
La velocidad varía según la distancia al Sol (ecuación vis-viva).

## Uso Local

```bash
# Clonar repositorio
git clone https://github.com/cjlkaiser-cpu/harmonices-mundi.git

# Abrir directamente o con servidor local
python -m http.server 8000
# Navegar a http://localhost:8000
```

## Estructura

```
harmonices-mundi/
├── index.html      # Simulación principal
├── tutorial.html   # Tutorial interactivo
├── README.md
└── LICENSE
```

## Contexto Histórico

En 1619, Johannes Kepler publicó *Harmonices Mundi* (La Armonía del Mundo), donde propuso que los planetas producen "música" basada en sus velocidades orbitales. Kepler asignó intervalos musicales a cada planeta según la relación entre sus velocidades en el afelio y perihelio:

| Planeta | Intervalo (Kepler) |
|---------|-------------------|
| Saturno | Tercera mayor |
| Júpiter | Tercera menor |
| Marte | Quinta |
| Tierra | Semitono (mi-fa) |
| Venus | Diesis |
| Mercurio | Décima menor |

Esta simulación hace audible esa visión, 400 años después.

## Licencia

**Código:** MIT License
**Contenido educativo:** CC BY 4.0

Ver [LICENSE](LICENSE) para detalles.

---

*Parte de [Physics Sound Lab](https://github.com/cjlkaiser-cpu/physics-sound-lab) — Simulaciones donde la física genera música*
