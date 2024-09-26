import random

def generar_contrasena(longitud):
    """
    Genera una contraseña aleatoria de la longitud especificada.

    Args:
        longitud (int): La longitud deseada de la contraseña.

    Returns:
        str: La contraseña generada.
    """

    # Todos los caracteres posibles para la contraseña
    caracteres = "+-/*!&$#?=@abcdefghijklnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890"

    # Inicializar la contraseña vacía
    contrasena = ""

    # Generar cada carácter de la contraseña
    for _ in range(longitud):
        indice_aleatorio = random.randint(0, len(caracteres) - 1)
        caracter_aleatorio = caracteres[indice_aleatorio]
        contrasena += caracter_aleatorio

    return contrasena

# Pedir al usuario la longitud de la contraseña
longitud = int(input("Ingrese la longitud deseada para la contraseña: "))

# Generar y mostrar la contraseña
contrasena_generada = generar_contrasena(longitud)
print("La contraseña generada es:", contrasena_generada)de-Dylan-.
