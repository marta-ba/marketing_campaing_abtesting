# **Marketing A/B Testing**

1. Description.

The companies are interested in answering two questions:

1. Would the campaign be successful?
2. If the campaign was successful, how much of that success could be attributed to the ads? 

With the second question in mind, we normally do an A/B test. The majority of the people will be exposed to ads (the experimental group). And a small portion of people (the control group) would instead see a Public Service Announcement (PSA) (or nothing) in the exact size and place the ad would normally be.

The idea of the dataset is to analyze the groups, find if the ads were successful, how much the company can make from the ads, and if the difference between the groups is statistically significant.

**Data dictionary:**

- Index: Row index
- user id: User ID (unique)
- test group: If "ad" the person saw the advertisement, if "psa" they only saw the public service announcement
- converted: If a person bought the product then True, else is False
- total ads: Amount of ads seen by person
- most ads day: Day that the person saw the biggest amount of ads
- most ads hour: Hour of day that the person saw the biggest amount of ads


2. Análisis Exploratorio (EDA)

- Balanceo de grupos: Comparar la proporción de usuarios en psa vs ad. Si hay desbalanceo, considerar técnicas como estratificación.

- Tasa de conversión global y por grupo (ad vs psa).

- Usar un boxplot para detectar usuarios con valores extremos (ej. 72 anuncios vs 2). Decidir si truncar o segmentar.

- Patrones temporales: Analizar si la conversión varía por most ads day o most ads hour (ej. ¿Los usuarios expuestos en horario laboral convierten más?).

3. Estadísticas Descriptivas Clave

- Mediana y media de total_ads por grupo (la media puede ser sensible a outliers).
- Frecuencia de días/horas con mayor actividad.

4. Hipótesis para el A/B Testing

- Hipótesis nula (H₀): No hay diferencia en la tasa de conversión entre psa y ad.

-Hipótesis alternativa (H₁): El grupo ad tiene una tasa de conversión mayor.

5. Métricas a Comparar
Métrica principal: Tasa de conversión (converted).

Métricas secundarias:

Engagement: total_ads (si el grupo ad ve más anuncios, ¿afecta a la conversión?).

Efecto temporal: ¿La hora/día influye en la conversión?