
# Manipulación de Datos con Pandas
Bienvenidos a Mi Diario Python. Mi nombre es Luis y es un placer estar nuevamente aquí. 

En el articulo de hoy veremos algunos ejemplos para la manipulación de datos, creación de DataFrame y archivos CSV. 
Todo esto lo haremos con ayuda de la libreria Pandas, la cual puedes descargar ingresando al siguiente enlace: 

O introduciendo el siguiente comando en tu consola: pip install pandas

Antes de proseguir dejame invitarte ha hechar un vistazo a nuestro curso para __Aprender Python__ y nuestros articulos __Ejercicios de Programación__ en el cual podras reforzar todas tus habilidades como programador.

# Manipulación de Datos - Pandas:
Pandas es una libreria escrita en python utiliza para el analisis de datos y la estadistica. Pandas nos permite crear DataFrames, los cuales son tablas de datos ordenados por columnas. El formato CSV es el más para guardar y leer conjuntos de datos, pandas nos permite leer este tipo de archivo de manera muy sencilla.

¿Que les parece si damos los primeros pasos con pandas?. Crearemos nuestro primero DataFrame.

## Creación de un DataFrame:
Para crear nuestro DataFrame, lo primero que haremos sera importar la libreria Pandas y escoger los datos que queremos guardar en el.



```python
import pandas as pd # importamos pandas

columnas = ['Nombre', 'Edad', 'Genero', 'Id'] # Columnas del DataFrame

datos = pd.DataFrame([['Carmen', 26, 'F', 1743],
                      ['Pedro', 39, 'M', 9264],
                      ['Maria', 28, 'F', 8362],
                      ['Julio', 35, 'M', 2537]],
                      columns=columnas)
print(datos)
```

       Nombre  Edad Genero    Id
    0  Carmen    26      F  1743
    1   Pedro    39      M  9264
    2   Maria    28      F  8362
    3   Julio    35      M  2537
    

Y como pueden observar, el resultado son nuestros datos ordenado. Genial ¿No lo crees?.

No nos limitemos a crear un solo DataFrame. Podemos crear todos los que deseemos.


```python
import pandas as pd # importamos pandas

columnas = ['Nombre', 'Edad', 'Genero', 'Id'] # Columnas del DataFrame

datos_0 = pd.DataFrame([['Carmen', 26, 'F', 1743],
                      ['Pedro', 39, 'M', 9264],
                      ['Maria', 28, 'F', 8362],
                      ['Julio', 35, 'M', 2537]],
                      columns=columnas)

datos_1 = pd.DataFrame([['Rodrigo', 43, 'M', 8374],
                      ['Jose', 21, 'M', 8329],
                      ['Ramon', 29, 'M', 9236],
                      ['Susana', 34, 'F', 9836]],
                      columns=columnas)

datos_2 = pd.DataFrame([['Gabriela', 27, 'F', 1736],
                      ['Carlos', 36, 'M', 3524],
                      ['Samuel', 22, 'M', 9837],
                      ['Jhon', 29, 'M', 7367]],
                      columns=columnas)

print(datos_2)
```

         Nombre  Edad Genero    Id
    0  Gabriela    27      F  1736
    1    Carlos    36      M  3524
    2    Samuel    22      M  9837
    3      Jhon    29      M  7367
    

Como pueden observar, podemos tener todas las tablas que querramos. 
En muchas ocasiones, tendremos muchos DataFrame. ¿Que pasaria si quisieramos concatenarlos a toddos?.
Para esto tendremos que utilizar el metodo "concat()" ypasarle como argumento los DataFrame en una lista.


```python
datos_concatenados = pd.concat([datos_0, datos_1, datos_2])
print(datos_concatenados)
```

         Nombre  Edad Genero    Id
    0    Carmen    26      F  1743
    1     Pedro    39      M  9264
    2     Maria    28      F  8362
    3     Julio    35      M  2537
    0   Rodrigo    43      M  8374
    1      Jose    21      M  8329
    2     Ramon    29      M  9236
    3    Susana    34      F  9836
    0  Gabriela    27      F  1736
    1    Carlos    36      M  3524
    2    Samuel    22      M  9837
    3      Jhon    29      M  7367
    

Como pueden observar, el resultado es un DataFrame con toda la información de los creados anteriormente.

# Leer y Crear archivos CSV
Una vez que tengamos los DataFrames con todos los datos, necesitaremos guardarlos para su uso posterior.


```python
import pandas as pd

datos = pd.read_csv('./iris.csv')
datos.head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>150</th>
      <th>4</th>
      <th>setosa</th>
      <th>versicolor</th>
      <th>virginica</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>



Con esto, podres ver las primeras 5 columnas del archivo. El archivo que estoy utilizando como ejemplos es el conjunto de datis "iris", uno muy usado para probar algoritmos clasificiación y el analisis de datos.

Bueno, con lo aprendido hoy, ya puedes crear tus propios conjuntos de datos y leer de manera muy facil.

¿Alguna duda? ¿Con ganas de más? Dejanos tu comentario.

Mi nombre es Luis, y fue un placer compartir mis conocimientos con todos ustedes :D.
