Gestión de la Demanda en Supply Chain

Descripción

Este proyecto aplica técnicas de Supply Chain Analytics para analizar la gestión de la demanda a partir de un dataset de ventas. Incluye análisis exploratorios y modelos que permiten identificar patrones de consumo, segmentar clientes y evaluar la relación precio–volumen de ventas.

Análisis incluidos

Ventas por producto / categoría (SKU): identificación de los más y menos vendidos.
Top & Bottom products: ranking de SKUs según unidades vendidas.
Relación Precio vs Volumen: exploración de elasticidad y sensibilidad de la demanda.
Segmentación de clientes: agrupación por variables demográficas y de compra.

🎯 Problemas que resuelve

Detectar productos estratégicos para la planeación de inventarios.
Identificar productos de baja rotación que impactan la rentabilidad.
Medir cómo el precio afecta las ventas para apoyar decisiones comerciales.
Definir estrategias diferenciadas para segmentos de clientes.

🛠️ Tecnologías usadas
Python (pandas, numpy, matplotlib, seaborn, scikit-learn)

Excel / Power BI (para reportes complementarios)

1. Gestión de la Demanda

1️⃣ Análisis de ventas por producto, categoría o SKU

Problema: No se sabe qué productos son los que más aportan a las ventas totales.

Qué resolvemos:
Identificar productos “estrella” vs. “cola larga” (pocos ingresos).
Priorización de portafolio.
Enfocar esfuerzos comerciales en productos de alto impacto.


<img width="856" height="480" alt="image" src="https://github.com/user-attachments/assets/20563b73-a8cb-49c2-8ea4-9fe809c79846" />

•	Hallazgo: Por ejemplo, cosmetics11 destaca con ventas y revenue elevados, mientras otros como cosmetics13 muestran menor rotación.

•	Interpretación:
o	Ya puedes identificar productos estrella (alto revenue y volumen).
o	Los de menor aporte son candidatos a revisión: o bien estrategias de marketing específicas, o posible descontinuación.
o	Te da un mapa claro para priorizar el portafolio.


2️⃣ Identificación de productos más vendidos y menos vendidos

Problema: Recursos de marketing y producción se asignan sin priorización clara.

Qué resolvemos:
Evitar invertir en productos de bajo desempeño.
Detectar candidatos para descontinuación o promoción.
Optimizar espacio en inventario y canales de venta.

<img width="854" height="477" alt="image" src="https://github.com/user-attachments/assets/0b54b2dd-8d84-40ad-9827-ca0b5447f820" />

Hallazgos:
•	Más vendidos: skincare6, cosmetics25, skincare5, etc., con volúmenes cercanos a 1000 unidades.
•	Menos vendidos: algunos haircare y cosmetics con ventas mínimas (<30 unidades), aunque generan altos ingresos unitarios.

•	Interpretación:
o	Los “menos vendidos” no siempre son poco rentables: algunos tienen precios altos y revenue relevante (ej. haircare2).
o	Esto indica que no solo debes mirar unidades, sino también margen y contribución al revenue.
o	Estrategia: mantener estos productos como premium o reposicionarlos.

3️⃣ Relación entre precio y volumen de ventas

Problema: Desconocimiento de la elasticidad precio–demanda.

Qué resolvemos:
Ajustar estrategias de precios.
Detectar si un precio bajo realmente impulsa la venta o solo reduce margen.
Identificar productos “premium” que venden bien aún con precio alto.

<img width="921" height="523" alt="image" src="https://github.com/user-attachments/assets/3088f556-c7b3-43fc-80ba-acb236880aa0" />

•	Resultados:
o	Pendiente ≈ 0.056, R² ≈ 0.00003 → prácticamente sin relación lineal.
o	Elasticidad ≈ 0.02 → demanda casi inelástica (cambios en precio no afectan el volumen significativamente).

•	Interpretación:
o	A nivel agregado, el precio no es un driver principal de la demanda.
o	Esto sugiere que otros factores (marca, categoría, promoción, disponibilidad) influyen más en las ventas.
o	Acción: analizar elasticidad por subcategorías o segmentos de producto, ya que en el promedio global se pierde información.

4️⃣ Segmentación de clientes (Customer demographics)

Problema: Estrategias comerciales generalistas que no consideran perfil del cliente.

Qué resolvemos:
Conocer qué segmentos de clientes generan mayor revenue.
Diseñar promociones específicas (ej. campañas por género, edad, ubicación).
Detectar nichos de mercado desatendidos.

<img width="921" height="519" alt="image" src="https://github.com/user-attachments/assets/acf3056a-03c9-4377-9960-81a34623e090" />

•	Resultados:
o	Segmento Unknown = mayor volumen y revenue.
o	Female y Male generan ingresos relevantes y estables.
o	Non-binary con menor revenue, pero aún significativo.

•	Interpretación:
o	El segmento Unknown probablemente agrupe clientes sin clasificación → puede ocultar insights importantes (ej. falta de calidad en los datos).
o	Los segmentos Female y Male son claros objetivos de campañas personalizadas.
o	Estrategia: mejorar la captura de datos de clientes para reducir la categoría Unknown y diseñar acciones diferenciadas de marketing.

