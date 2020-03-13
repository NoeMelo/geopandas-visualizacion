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

### Noteboks con Mapas en Python

##### Importar librerias en el entorno de trabajo

Para hacer ploteo se necesita la librería matplotlib, esta libreria es muy conocida para hacer graficos al igual que pandas que es muy util para manejar dataframes y adicionalmente permite plotear. Anaconda ya los trae instalados.

```python
%matplotlib inline
import pandas as pd
import matplotlib.pyplot as plt
import geopandas as gpd
```

+ [Notebook Mapa Mundial](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/geopandas_world.ipynb)

```python
url_geojson = "geojson/countries.geojson"
world_geojson = gpd.read_file(url_geojson)
```
```python
ax = world_geojson.plot(figsize=(20,20),edgecolor=u'gray', cmap='Pastel1')
plt.ylabel('Latitude')
plt.xlabel('Longitude')
plt.show()
```

![alt text](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/data/images/world.png)

+ [Notebook Regiones del Perú](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/geopandas_regions.ipynb)

```python
url_geojson = "geojson/peru_departamental_simple.geojson"
region_geojson = gpd.read_file(url_geojson)
```
```python
ax = region_geojson.plot(figsize=(20,20),edgecolor=u'gray', cmap='Pastel1')
plt.ylabel('Latitude')
plt.xlabel('Longitude')
plt.show()
```
![alt text](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/data/images/regiones.png)

+ [Notebook Provincias del Perú](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/geopandas_provinces.ipynb)

```python
url_geojson = "geojson/peru_provincial_simple.geojson"
provinces_geojson = gpd.read_file(url_geojson)
```
```python
ax = provinces_geojson[provinces_geojson.FIRST_NOMB=='CUSCO'].plot(figsize=(20,20),edgecolor=u'gray', cmap='Pastel1')
plt.ylabel('Latitude')
plt.xlabel('Longitude')
ax.axis('scaled')
plt.show()
```

![alt text](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/data/images/provincias.png)

+ [Notebook Distritos del Perú](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/geopandas_districts.ipynb)

```python
url_geojson = "geojson/peru_distrital_simple.geojson"
districts_geojson = gpd.read_file(url_geojson)
```
```python
ax = districts_geojson[districts_geojson.NOMBPROV=='CALCA'].plot(figsize=(10,10),edgecolor=u'gray', cmap='Pastel1')
plt.ylabel('Latitude')
plt.xlabel('Longitude')
ax.axis('scaled')
plt.show()
```

![alt text](https://github.com/NoeMelo/geopandas-visualizacion/blob/master/data/images/distritos.png)
