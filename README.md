# Geopandas - Visualización con Python

### Requisitos
Instalar las siguientes librerías:
+ geopandas
+ descartes

Instalar Descartes en windowns porque para hacer ploting Geopandas necesita de esa libreria para dibujar poligonos vectoriales. Sin embargo, puede que en otros sistemas operativos no sea necesario.

```cmd
conda install geopandas
conda install -c conda-forge descartes
```
Se puede instalar con pip ambas librerias, pero para evitar errores es recomendable usar conda.

##### Importar librerias en el entorno de trabajo

Para hacer ploteo se necesita la librería matplotlib, esta libreria es muy conocida para hacer graficos al igual que pandas que es muy util para manejar dataframes y adicionalmente permite plotear. Anaconda ya los trae instalados.

```python
%matplotlib inline
import pandas as pd
import matplotlib.pyplot as plt
import geopandas as gpd
```

### Noteboks con Mapas en Python

+ [Notebook Mapa Mundial](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/geopandas_world.ipynb)

![alt text](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/data/images/world.png)

+ [Notebook Regiones del Perú](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/geopandas_regions.ipynb)

Regiones del Perú

![alt text](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/data/images/regiones.png)

+ [Notebook Provincias del Perú](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/geopandas_provinces.ipynb)

Provincias del departamento de Cusco

![alt text](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/data/images/provincias.png)

+ [Notebook Distritos del Perú](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/geopandas_districts.ipynb)

Distritos de la provincia de Calca del departamento de Cusco

![alt text](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/data/images/distritos.png)
