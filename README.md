# Escuchaton

<img width="561" height="251" alt="image" src="https://github.com/user-attachments/assets/c82b7e08-a433-47d1-bc51-6279117433f4" />

Jornada de verificación de predicciones en el marco del programa Conserva Aves. 


- La carpeta [detacciones_crudas](https://github.com/sanruizguz/Escuchaton/tree/main/Detecciones_crudas) contiene las detecciones sin estandarizar
- La carpeta [detacciones_estandarizadas](https://github.com/sanruizguz/Escuchaton/tree/main/Detecciones_estandarizadas) contiene las detecciones corregidas bajo el mismo formato

- La carpeta [detacciones_filtradas](https://github.com/sanruizguz/Escuchaton/tree/main/Detecciones_filtradas) contiene un archivo csv por cada especie incluida en la lista de [especies objetivo](https://github.com/sanruizguz/Escuchaton/blob/main/especies_objetivo.csv) con el mismo número de grabaciones, por ejemplo (basado en el puntaje de detección arrojado por BirdNET). Estos últimos son los que deben ser descargados para iniciar el proceso de verificación. 


### Descripción de las columnas 

| Columna           | Descripción |
|--------------------|-------------|
| **mediaID** | Nombre del audio, el formato usualmente se compone de 3 partes divididas por "_" (`A6B8FF18_20250131_105500.WAV`):<br> - Identificador único de la grabadora usada (usualmente las letras están asociadas con el tipo de grabadora y los números con el ID).<br> - Fecha en formato Año-mes-día.<br> - Hora del día en formato Hora-minuto-segundo. |
| **eventStart** | Tiempo inicial (en segundos) de la predicción de BirdNET. |
| **eventEnd** | Tiempo final (en segundos) de la predicción de BirdNET. |
| **speciesName** | Nombre científico de la especie detectada (siguiendo la taxonomía de Clements 2024). |
| **confidence** | Puntaje de detección generado por BirdNET que se puede interpretar como la “confianza” que tiene el modelo de que una predicción dada sea correcta. |
| **classifiedBy** | Nombre y versión del modelo de clasificación automática, ej: *BirdNET v2.3*. |
| **recorderID** | Código único de la grabadora (de cada punto). |
| **recorderModel** | Modelo de la grabadora, incluyendo la marca y versión (ej. *SMM2 para Song Meter Micro 2*). |
| **locality** | Intermedio entre punto y municipio; puede interpretarse como nombre del predio o vereda. |
| **projectName** | Nombre del proyecto; a veces puede contener información geográfica o temporal (ej. *GEOPARK_PUTUMAYO_2024*). |
| **municipality** | Municipio. |
| **latitude** | Latitud en formato de coordenadas geográficas (números decimales). |
| **longitude** | Longitud en formato de coordenadas geográficas (números decimales). |
| **setupBy** | Nombre y apellido de la persona que instaló la grabadora en cada punto. |
| **deploymentStart** | Fecha de inicio del despliegue de la grabadora en formato DD/MM/AAAA. |
| **deploymentEnd** | Fecha de término del despliegue de la grabadora en formato DD/MM/AAAA. |
| **deploymentGroups** | Nombre del despliegue (ej. número del despliegue dentro de la misma localidad). |
| **timestamp** | Fecha y hora de la predicción en formato AAAA-MM-DD HH:MM:SS. |
| **segmentID** | Identificador de la predicción de BirdNET; se compone del MediaID + eventStart + eventEnd. |
