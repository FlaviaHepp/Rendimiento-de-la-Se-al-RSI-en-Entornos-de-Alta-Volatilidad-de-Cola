# 📉Rendimiento de la Señal RSI en Entornos de Alta Volatilidad de Cola

## 📌Descripción del Proyecto

Este proyecto evalúa la efectividad real de la señal técnica de sobrecompra (RSI > 70) cuando se aplica exclusivamente en acciones con alto riesgo de cola, medido a través de kurtosis elevada.

La idea central es simple pero potente:
👉 no todas las señales técnicas son iguales en todos los contextos.
Una señal RSI puede funcionar muy distinto en un activo estable que en uno propenso a movimientos extremos.

Este análisis filtra el “ruido técnico” y valida la señal solo donde el riesgo estructural es alto.

## 🎯Objetivo del Insight

Responder a la pregunta:
- ¿Cuál fue el rendimiento promedio a 5 días de una señal de venta (RSI > 70) cuando se produce en acciones con kurtosis elevada (> 5.0)?

Esto permite evaluar la calidad de la señal ajustada al riesgo de cola, algo que la mayoría de los backtests tradicionales ignoran.

## 🧠Hipótesis de Mercado

- Un RSI > 70 indica sobrecompra.

Una kurtosis alta (> 5.0) indica:
- retornos con colas gruesas,
- mayor probabilidad de movimientos extremos,
- estructuras de precio inestables.

En este contexto, una señal de venta debería ser más efectiva (caídas más pronunciadas posteriores).

## 📊Metodología

- Identificación de señales
- RSI de 14 períodos mayor a 70 (zona de sobrecompra).
- Kurtosis mayor a 5.0 (alto riesgo de cola).
- Medición de rendimiento
- Precio de cierre el día de la señal.
- Precio de cierre 5 días después.
- Cálculo del rendimiento porcentual a 5 días.
- Análisis sectorial
- Agrupación por sector.
- Promedio de rendimiento posterior.
- Conteo de señales válidas por sector.

## 🧮Métrica Clave

Rendimiento promedio a 5 días:

Rendimiento = ((Precio 5d - Precio señal)/ precio señal ) * 100

Valores negativos ⇒ señal de venta efectiva

Valores positivos ⇒ señal fallida o contexto no adecuado

## 📌Output del Análisis

El resultado final muestra, por sector:
- Número de señales en entornos de alto riesgo
- Rendimiento promedio a 5 días posterior a la señal
- Ranking de sectores donde la señal RSI fue más efectiva como señal de venta

Los sectores con rendimientos más negativos representan mejores oportunidades de short o salida.

## 💼Valor de Negocio

✅ Mejora la robustez de estrategias RSI

✅ Evita operar señales técnicas en contextos estructuralmente inestables sin filtro

✅ Permite construir estrategias de trading ajustadas al riesgo de cola

✅ Útil para:
 - trading cuantitativo,
 - filtros de riesgo,
 - sistemas de alerta temprana,
 - validación de señales técnicas avanzadas

## ⚠️Consideraciones

- No es un consejo de inversión.

Kurtosis elevada puede implicar:
- gaps,
- iliquidez,
- eventos exógenos.

Recomendado combinar con:
- volumen,
- eventos corporativos,
- análisis de liquidez.

## 🧩Requisitos de Datos

- tickers
- indicadores_tecnicos (RSI, Kurtosis)
- precios_diarios

## 🚀Próximos Pasos Sugeridos

- Comparar contra RSI en entornos de baja kurtosis
- Medir drawdown máximo post-señal
- Extender el horizonte a 10 y 20 días
- Integrar con eventos corporativos

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
***
📉 **No todas las señales RSI son iguales… depende del contexto de riesgo**

El RSI > 70 suele interpretarse como señal de sobrecompra.
Pero en la práctica, muchas de estas señales fallan.

👉 Entonces probé algo distinto:
¿qué pasa si solo consideramos RSI en **entornos de alto riesgo de cola**?

💡 **Insight clave:**
Cuando combinamos **RSI > 70** con **kurtosis elevada (> 5)**, la señal se vuelve mucho más potente.
En estos contextos, las caídas posteriores tienden a ser más pronunciadas.

---

📊 **¿Qué medí?**

* Señales de sobrecompra (RSI > 70)
* Filtrado por activos con alta kurtosis (riesgo de eventos extremos)
* Rendimiento promedio a 5 días post-señal
* Análisis por sector

---

🧠 **¿Cómo interpretarlo?**

* RSI solo → puede generar ruido
* RSI + alto riesgo de cola → señal más selectiva
* Mayor kurtosis → mayor probabilidad de movimientos bruscos (incluyendo caídas)

---

⚡ **¿Por qué importa?**

Porque mejora la calidad de las señales:

* Menos falsos positivos
* Mejor timing en estrategias de reversión
* Integración de **momentum + distribución de retornos**

---

📌 Pregunta para la comunidad:
¿Filtran sus indicadores técnicos con métricas de riesgo (como kurtosis o skewness)… o los usan de forma aislada?

#QuantFinance #Trading #DataScience #StockMarket #RSI #RiskManagement #MachineLearning #Analytics
