# ==========================================
# PROBLEMA 3 - AUDITORÍA DE INVENTARIO
# Curso: Fundamentos de Programación
# ==========================================

# Matriz de inventario
# [Código, Nombre, Stock Actual, Stock Mínimo]

inventario = [
    ["A001", "Teclado", 3, 10],
    ["A002", "Mouse", 15, 10],
    ["A003", "Monitor", 2, 5],
    ["A004", "USB", 20, 15],
    ["A005", "Impresora", 1, 4]
]

# ==========================================
# Función para calcular cantidad a pedir
# ==========================================

def calcular_pedido(stock_actual, stock_minimo):

    if stock_actual < stock_minimo:
        cantidad_pedir = stock_minimo - stock_actual
    else:
        cantidad_pedir = 0

    return cantidad_pedir


# ==========================================
# Mostrar reporte de pedidos
# ==========================================

print("====================================")
print("   REPORTE DE REABASTECIMIENTO")
print("====================================")

for articulo in inventario:

    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    pedido = calcular_pedido(stock_actual, stock_minimo)

    print("------------------------------------")
    print("Código:", codigo)
    print("Artículo:", nombre)
    print("Stock actual:", stock_actual)
    print("Stock mínimo:", stock_minimo)
    print("Cantidad a pedir:", pedido)

print("------------------------------------")
print("Fin del reporte")
