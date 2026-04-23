# Análisis de Operaciones — MedSupply México (Sector Salud)

## Descripción del Proyecto
MedSupply México es una distribuidora de dispositivos médicos que vende 
a hospitales públicos (IMSS, ISSSTE, SEDESA) y privados (Médica Sur, 
Hospital Ángeles, Christus Muguerza) en 5 regiones del país. Se analizaron 
600 transacciones para entender el desempeño comercial, calcular comisiones 
de representantes de ventas y detectar contratos en riesgo.

## Problema que resolvimos
La directora comercial necesitaba para el viernes:
- Saber si los hospitales públicos o privados eran más rentables
- Un reporte de comisiones del Q1 para pagar a los representantes
- Identificar cuánto revenue estaba en riesgo por contratos inactivos
- Un dashboard interactivo que el director pudiera usar solo

## Lo que hicimos
**Análisis exploratorio y KPIs ejecutivos**
- Resumen ejecutivo automático con métricas clave del negocio
- Revenue total, margen bruto, comisiones totales y estado de contratos

**Análisis con SQL**
- Comparación de revenue y margen entre hospitales públicos y privados
- Ranking de productos por rentabilidad (margen %, no volumen)
- Reporte de comisiones Q1 por representante con ranking de desempeño
- Análisis de contratos inactivos y revenue potencial perdido

**Excel avanzado**
- BUSCARV entre hojas para cruzar datos de hospitales
- SUMAR.SI y CONTAR.SI para resúmenes ejecutivos dinámicos
- Fórmula SI anidada para clasificar representantes (Top/Mid/Low)
- Tabla dinámica con campo calculado de margen %
- Formato condicional con fórmula para resaltar filas completas
- Gráfica dinámica conectada a tabla dinámica

**Dashboard en Tableau Public**
- 4 visualizaciones interactivas conectadas entre sí
- Filtros globales por trimestre y tipo de hospital
- Publicado en línea — accesible sin instalar software

## Hallazgos principales
- Hospitales públicos generan 55% del revenue ($116M MXN) pero los 
  privados tienen 5 puntos más de margen promedio (37% vs 32%)
- El Ventilador Mecánico, Desfibrilador y Cama Hospitalaria lideran 
  en rentabilidad — el equipo de ventas debería priorizarlos
- El representante #1 generó 4 veces más comisión que el último en Q1 — 
  brecha significativa que requiere atención del gerente de ventas
- $54M MXN en revenue potencial en riesgo por 156 contratos inactivos — 
  reactivar contratos con IMSS e ISSSTE es la acción prioritaria

## Recomendación principal
Asignar los top 3 representantes de ventas a la reactivación de contratos 
con hospitales públicos dado su mayor volumen, y establecer un esquema de 
bonos por reactivación para incentivar al equipo.

## Herramientas utilizadas
- **Python** — pandas, matplotlib, seaborn, numpy
- **SQL** — SQLite con GROUP BY, RANK, window functions, filtros compuestos
- **Excel** — BUSCARV, SUMAR.SI, tablas dinámicas, formato condicional 
  con fórmula, gráficas dinámicas
- **Tableau Public** — dashboard interactivo publicado en línea

## Dashboard interactivo
https://public.tableau.com/app/profile/jared.vargas/viz/MedSupplyMxico/Dashboard1
## Archivos
- `Dia3_MedSupply.ipynb` — notebook completo con análisis
- `MedSupply_Data.xlsx` — reporte Excel con formato avanzado
