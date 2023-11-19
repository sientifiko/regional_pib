# regional_pib
Datos con PIB regionales de Chile 

Este es un empalme propio y aunque lo hice con toda la rigurosidad que pude, las fuentes antes del 2000 no son del todo confiables.
Por lo que antes de usarlos, hagan el ejercicio de validar con otros datos que tengan. 

El dataset contiene un panel de las 13 regiones clásicas de Chile, y su PIB por cada sector. El valor del PIB no está armonizado, 
presentando distintas unidades de medida según la fuente (ver txt de fuentes de datos). Por lo tanto su empalme no es válido y como 
mucho puede ser interpretado longitudinalmente en función de alguna transformación o cálculo a nivel regional como porcentajes, 
Gini, desviación estándar u otro similar. 

DICCIONARIO DE DATOS:
**region**: 13 regiones armonizadas. Para las series de Badia-Miró usé el criterio que presenta en su paper del 2015
(ver txt de fuentes). Para el periodo actual, colapsé Arica y Parinacota con Tarapacá, Ñuble con Biobio, y Los Ríos con Los Lagos. 

**anio**: año de la medición/estimación

**sector**: sector económico pseudoarmonizado. Se toman todos los sectores económicos declarados en la fuente original, y se
armonizan entre ellos. Esta armonización es principalmente por diferencias de escritura (un mismo sector con o sin una coma, 
o la referencia a un mismo sector, pero con una palabra ligeramente distinta). 

**pib**: PIB nominal no arminizado, según la fuente original. Dependiendo la fuente están a pesos de distintos años. 

**origen**: fuente de la cual se extrae el PIB. Considerar que los PIB del Banco Central tienen pesos a distintos años base
por lo que no son empalmables entre sí. Los PIB de Badia-Miró y del Mideplan sí

**sector2**: sector económico armonizado. Se usaron los 4 sectores de Badia-Miró. Este colapso es totalmente arbitrario y
aún no lo he validado, por lo que debe ser tomado con precaución

**pobla**: población regional según los Censos y el INE, ver txt de fuentes

**pobla_hat**: población regional imputada por medio de filtro de Kalman. 






