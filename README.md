# =====================================================
# PROBLEMA 3 - AUDITORÍA DE INVENTARIO
# Curso: Fundamentos de Programación
# Autor: [Tu Nombre]
# =====================================================

# -----------------------------------------------------
# MATRIZ DE INVENTARIO
# [Código, Nombre, Stock Actual, Stock Mínimo]
# -----------------------------------------------------

inventario = [
    ["A001", "Teclado", 3, 10],
    ["A002", "Mouse", 15, 10],
    ["A003", "Monitor", 2, 5],
    ["A004", "USB", 20, 15],
    ["A005", "Impresora", 1, 4]
]

# =====================================================
# FUNCIÓN: calcular_pedido()
# Objetivo:
# Determinar la cantidad exacta a solicitar
# según el stock actual y el stock mínimo.
# =====================================================

def calcular_pedido(stock_actual, stock_minimo):

    # Validar si el stock es insuficiente
    if stock_actual < stock_minimo:
        return stock_minimo - stock_actual

    # Si el stock es suficiente
    return 0


# =====================================================
# REPORTE DE REABASTECIMIENTO
# =====================================================

print("\n==========================================")
print("      REPORTE DE REABASTECIMIENTO")
print("==========================================")

# Recorrer cada artículo de la matriz
for articulo in inventario:

    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    # Llamado a la función
    cantidad_pedir = calcular_pedido(stock_actual, stock_minimo)

    # Mostrar información del artículo
    print("\n------------------------------------------")
    print(f"Código: {codigo}")
    print(f"Artículo: {nombre}")
    print(f"Stock actual: {stock_actual}")
    print(f"Stock mínimo: {stock_minimo}")
    print(f"Cantidad a pedir: {cantidad_pedir}")

# Mensaje final
print("\n==========================================")
print("        FIN DEL REPORTE")
print("==========================================")
