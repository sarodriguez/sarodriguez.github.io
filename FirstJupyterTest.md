

```python
#Primer Test de Jupyter Notebooks en Azure
```


```python
import pandas as pd
import numpy as np
vinc=pd.read_excel("vinculacion.xls")
vinc["INGRESO"] = vinc["INGRESO"].apply(pd.to_numeric, errors='coerce')
vinc=vinc.groupby(["PROGRAMA",'AÑO']).agg({'INGRESO': {'avg': np.mean}})
vinc=vinc.reset_index()
# writer = pd.ExcelWriter('pandas_simple.xlsx', engine='xlsxwriter')
# vinc.to_excel(writer, sheet_name='Vinculacion')
# write.save()
print(vinc)

```

                                                 PROGRAMA   AÑO       INGRESO
                                                                          avg
    0                          ACTIVIDAD FISICA Y DEPORTE  2014  0.000000e+00
    1                                         ACUICULTURA  2006  1.587043e+06
    2                                         ACUICULTURA  2007  9.614805e+05
    3                                         ACUICULTURA  2008  7.410000e+05
    4                                         ACUICULTURA  2009  9.766154e+05
    5                                         ACUICULTURA  2010  6.545556e+05
    6                                         ACUICULTURA  2011  8.467500e+05
    7                                         ACUICULTURA  2012  5.895000e+05
    8                                         ACUICULTURA  2013  7.907663e+05
    9                                         ACUICULTURA  2014  1.173088e+06
    10                                     ADMINISTRACION  2006  1.603605e+06
    11                                     ADMINISTRACION  2007  8.114120e+05
    12                                     ADMINISTRACION  2008  1.514468e+06
    13                                     ADMINISTRACION  2009  1.261080e+06
    14                                     ADMINISTRACION  2010  1.524314e+06
    15                                     ADMINISTRACION  2011  1.285001e+06
    16                                     ADMINISTRACION  2012  1.477559e+06
    17                                     ADMINISTRACION  2013  2.081731e+06
    18                                     ADMINISTRACION  2014  1.343408e+06
    19                        ADMINISTRACION  EMPRESARIAL  2006  1.162373e+06
    20                         ADMINISTRACION  FINANCIERA  2008  9.748333e+05
    21                         ADMINISTRACION  FINANCIERA  2009  1.085667e+06
    22                         ADMINISTRACION  FINANCIERA  2010  2.058800e+06
    23                         ADMINISTRACION  FINANCIERA  2012  1.336500e+06
    24                         ADMINISTRACION  FINANCIERA  2013  1.922695e+06
    25                         ADMINISTRACION  FINANCIERA  2014  1.116392e+06
    26                         ADMINISTRACION AERONAUTICA  2007  0.000000e+00
    27                         ADMINISTRACION AERONAUTICA  2010  7.736020e+05
    28                         ADMINISTRACION AERONAUTICA  2011  0.000000e+00
    29                        ADMINISTRACION AGROPECUARIA  2006  9.871549e+05
    ...                                               ...   ...           ...
    24294                                  TRABAJO SOCIAL  2014  1.352802e+06
    24295               TRADUCCION INGLES-FRANCES-ESPAÑOL  2006  1.135497e+06
    24296               TRADUCCION INGLES-FRANCES-ESPAÑOL  2007  1.035633e+06
    24297               TRADUCCION INGLES-FRANCES-ESPAÑOL  2008  1.173400e+06
    24298               TRADUCCION INGLES-FRANCES-ESPAÑOL  2009  1.337952e+06
    24299               TRADUCCION INGLES-FRANCES-ESPAÑOL  2010  1.091938e+06
    24300               TRADUCCION INGLES-FRANCES-ESPAÑOL  2011  1.454924e+06
    24301               TRADUCCION INGLES-FRANCES-ESPAÑOL  2012  1.237637e+06
    24302               TRADUCCION INGLES-FRANCES-ESPAÑOL  2013  1.689598e+06
    24303               TRADUCCION INGLES-FRANCES-ESPAÑOL  2014  1.243486e+06
    24304                           TRADUCCION SIMULTANEA  2007  1.505000e+06
    24305                           TRADUCCION SIMULTANEA  2008  1.542000e+06
    24306                           TRADUCCION SIMULTANEA  2009  1.119500e+06
    24307                           TRADUCCION SIMULTANEA  2011  1.749940e+06
    24308                           TRADUCCION SIMULTANEA  2012  7.090000e+05
    24309                                         TURISMO  2012  7.885417e+05
    24310                                         TURISMO  2013  9.408331e+05
    24311                                         TURISMO  2014  1.021607e+06
    24312        TÉCNICA PROFESIONAL EN MERCADEO Y VENTAS  2014  8.696809e+05
    24313  TÉCNICA PROFESIONAL EN OPERACIONES COMERCIALES  2014  1.681923e+06
    24314  TÉCNICA PROFESIONAL EN RECONOCIMIENTO ADUANERO  2014  1.356338e+06
    24315                                       ZOOTECNIA  2006  1.041873e+06
    24316                                       ZOOTECNIA  2007  1.035596e+06
    24317                                       ZOOTECNIA  2008  1.047495e+06
    24318                                       ZOOTECNIA  2009  9.137103e+05
    24319                                       ZOOTECNIA  2010  1.084533e+06
    24320                                       ZOOTECNIA  2011  1.101485e+06
    24321                                       ZOOTECNIA  2012  1.214882e+06
    24322                                       ZOOTECNIA  2013  1.313775e+06
    24323                                       ZOOTECNIA  2014  1.337175e+06
    
    [24324 rows x 3 columns]

