# Calculo-de-errores

Para usar la función Error(variables,ec,vals,errores)

La función espera en "variables" un array de numpy con las letras que aparecen en la ecuación a propagar, por ejemplo, si tenemos la ecuación del gas ideal y queremos calcular P a partir de los otros parámetros, sería

variables = np.array(['n','R','T','V'])

La ecuación tiene que ir como un string, y se escribe solo el lado derecho:

ec = 'n*R*T/V'


En "vals" van los datos que se midieron y que se reemplazan en la ecuación. La función espera recibir un solo array en el que estos estén agrupados, de forma que si se tiene una columna de datos de numpy para n, otra para R, otra para T y otra para V, hay que hacer

vals = np.array([n,R,T,V])

Y de la misma forma con los errores:

errores = np.array([errn,errR,errT,errV])



A esta evaluación la función devuelve un array con los errores listos para graficar, y la expresión propagada.
