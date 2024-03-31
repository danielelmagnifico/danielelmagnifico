import matplotlib.pyplot as plt
import numpy as np

# Datos
costo_fijo = 4000000
costo_variable = 150
precio_venta = 350

# Calculamos el punto de equilibrio
Q = costo_fijo / (precio_venta - costo_variable)

# Generamos una lista de unidades vendidas
unidades = np.linspace(0, 2*Q, 1000)

# Calculamos los costos totales e ingresos para cada cantidad de unidades vendidas
costos_totales = costo_fijo + costo_variable * unidades
ingresos = precio_venta * unidades

# Creamos el gráfico
plt.figure(figsize=(10, 6))
plt.plot(unidades, costos_totales, label='Costos Totales')
plt.plot(unidades, ingresos, label='Ingresos')
plt.xlabel('Unidades Vendidas')
plt.ylabel('Pesos')
plt.title('Gráfico de Equilibrio')
plt.legend()
plt.grid(True)
plt.show()
