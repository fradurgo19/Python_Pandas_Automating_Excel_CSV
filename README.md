# Python_Automating_Excel_CSV

Pandas is an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language. 

## Pasos 🚀

1. Leer todos los archivos 
2. Concatenar archivos
3. Eliminar datos nulos de archivos
4. Leer xlsx y convertir a csv archivos
5. cambiar nombre de columna
6. Filtrar archivos 
7. Unir archivos
8. Selecionar informacion
9. Convertir a CSV y xlsx para informe

## Importar librerías 🔧

    import pandas as pd
    import numpy as np
    import matplotlib.pyplot as plt
    import statsmodels.api as sm
    import glob
    import os
    import openpyxl
    import pdfkit

## 1. Leer todos los archivos  📋

    todos=[]
    for f in glob.glob(os.path.join("ubicaciòn archivos")):
    df=pd.read_excel(f)
    todos.append(pd.read_excel(f))

## 2. Concatenar arvhivos ⌨️

    df = pd.concat(todos,ignore_index="True")

## 3. Eliminar datos nulos de archivos ⚙️

    df = df.fillna(0)

## 4. Leer Excel y convertir a CSV archivoss  📖

    df.to_excel("ubicacion.xlsx", index = None, header=True)
    todosne = pd.read_excel(r"ubicacion.xlsx")
    todosne.to_csv(r"Ubicacion_final", index = None,  header=True) 

## 5. cambiar nombre de columna 🖇️

    df1.rename(columns={'CodigoBus': 'Bus'}, inplace=True)

## 6. Filtrar archivos 7. Unir archivos 📦

    filtrado = df[(df.Responsable == "Cop") & (df.Observación == "F2 inicio_fin Ruta") | (df.Observación == "Estados de Localización")]

    output1 = pd.merge(df1, filtrado, on = ['Bus','ViajeLinea','ServicioBus','Coche'], how ='inner') 
    
## 8. Selecionar informacion 🔩

      derived_df = output1.filter(['Fecha_y', 'Operador', 'NumeroBus',
       'NumEventosBus', 'Linea', 'OrdenViaje', 'IDViaje', 'Tipo', 'Nodo',
       'Descripcion', 'HoraTeorica', 'HoraReferencia', 'HoraLlegada',
       'HoraSalida', 'Evento', 'TiempoRegulacion', 'Alarma',
       'TiempoAperturaPuertas', 'Conductor', 'NombreConductor'])

## 9. Convertir a CSV y xlsx para informe 🔩
    
    df.to_xlsx()
    df.to_csv()
    
## Autor ✒️
    
⭐️ [fradurgo19](https://github.com/fradurgo19)
