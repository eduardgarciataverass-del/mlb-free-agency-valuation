# Modelo de Valoración Sabermétrica de Agentes Libres de la MLB 2027

<img src="banner.jfif" width="100%">

## 📌 Descripción General

Este proyecto implementa un modelo de **Ciencia de Datos aplicado a la Gerencia Deportiva (Sabermetría y Finanzas de Béisbol)** para optimizar la toma de decisiones en la adquisición de agentes libres para la temporada 2027 de la MLB.

A diferencia de los análisis tradicionales que solo evalúan la producción bruta del pasado, este modelo cuantifica la **incertidumbre futura** combinando proyecciones de rendimiento avanzado (fWAR) con variables financieras corporativas. El objetivo es identificar **ineficiencias de mercado**, encontrando jugadores que ofrecen el mayor **Superávit de Valor Presente Neto (VPN)** ajustado por riesgo.

---

## 📊 Principales Hallazgos del Modelo

*Visualización de Cuadrantes: Costo Anual (AAV) vs Superávit de VPN Esperado. La línea roja marca el punto de equilibrio financiero.*

### Insights Ejecutivos:

1.  **Teruaki Sato (3B):** Se consolida como la **joya del mercado**. Su proyección de rendimiento de superestrella frente a un AAV proyectado razonable genera un **superávit neto de ~$87M VPN** con una probabilidad de éxito financiero del 100% en todos los escenarios simulados[cite: 1, 6].
2.  **Luis Arraez (2B):** Representa un **piso financiero seguro**. Su bajo costo proyectado ($12.5M AAV) minimiza el riesgo, generando más de **$58M de superávit VPN**. Es el fichaje de menor riesgo por millón invertido[cite: 1, 6].
3.  **El Dilema de Tarik Skubal (SP):** Aunque es el lanzador más dominante en fWAR crudo, un contrato proyectado de 8 años y $352M destruye el valor financiero a largo plazo. El modelo revela un **superávit negativo de -$11M VPN**, debido a la penalización por edad en los años finales y el riesgo financiero de inmovilizar presupuesto. **El mejor jugador no siempre es la firma más inteligente.**

---

## 🛠️ Stack Tecnológico y Metodología

### Tecnologías Utilizadas:
*   **Python 3.x**
*   **Pandas & NumPy**
*   **Matplotlib & Seaborn**

### Metodología Avanzada:
1.  **Modelo Estocástico de Monte Carlo (10,000 Escenarios):** Simulamos 10,000 temporadas futuras por cada jugador basándonos en la distribución normal de su fWAR base y su volatilidad proyectada[cite: 2, 6].
2.  **Curvas de Envejecimiento por Posición (*Aging Curves*):** Aplicamos penalizaciones de rendimiento anuales basadas en la edad y posición del jugador[cite: 2].
3.  **Valor Presente Neto (VPN) del Contrato:** Descontamos los flujos de efectivo futuros de valor generado (USD) a una tasa de descuento financiera del 5% para evaluar la rentabilidad del contrato al valor de hoy[cite: 2].

---

## 🚀 ¿Cómo usar este repositorio?

1.  **Código Fuente:** Todo el análisis está autocontenido en el archivo `.ipynb` de este repositorio.
2.  **Ejecución:** Puedes descargar el archivo y ejecutarlo en Google Colab o Jupyter Notebook. Los datos de los principales agentes libres están integrados en el código.

---

Este modelo proporciona una herramienta cuantitativa para gerentes generales que buscan maximizar la eficiencia de nómina y la rentabilidad financiera en el mercado abierto.
