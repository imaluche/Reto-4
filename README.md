# Reto-4
reto usando condicionales if

1.número correspondiente al código ASCII de una vocal minúscula
------------
    x:int=int(input("(numero chistoso)x:"))
    conjunto_vocales= (97,101,105,11,117)
    if x in conjunto_vocales:
    print("su valor en ASCII corresponde a una vocal minuscula")
    else:
    print("su valor en ASCII no corresponde a una vocal minuscula")
    EXPLICACION:
    los numeros dentro del conjunto declarado son los correspondiente al codigo ASCII de a,e,i,o,u. 
    Sabiendo esto simplemente evaluamos si el valor entrado esta dentro del conjunto, en caso de que si corresponda podemos saber
    que es una vocal minuscula
    en caso de que no este dentro no corresponde a las vocales minusculas
2.determine si el código ASCII de la primera letra de una cadena de longitud 1 es par o no
--------------
    cadena:str=str(input("cadena a evaluar:"))
    caracter= cadena[0]
    pariedad_cadena= ord(cadena)
    if len(cadena)>1:
    print("cadena muy larga")
    else:
    if pariedad_cadena/2==pariedad_cadena//2:
        print("su ASCII es par")
    else:
        print("su ASCII es impar")
        print("su primera letra es "+ str(caracter)+" obviamente porque solo acepta 1 letra xd")

        EXPLICACION:
        -Ademas de declarar una variable para entrar la cadena declaramos una segunda variable que represente unicamente 
        el primer caracter de la cadena (se le denomina con 0 porque en las cadenas siempre empiezan a contar desde el 0)
        -Declaramos una variable que represente el caracter transformado en valor ASCII, creando despues una condicional
        en la cual lo dividamos entre 2 y comparamos con su division exacta.
        Si este hecho se cumple el numero es par, pues la division entre 2 de un par entero siempre sera otro par entero
        (los valores ASCII siempre son enteros)
3.determinar si un carácter es un dígito o no.
------------
       cadena:str=str(input("cadena a evaluar:"))
       caracter= cadena[0]
       ASCII_cadena= ord(cadena)
       if len(cadena)>1:
    print("cadena muy larga")
    else:
    if ASCII_cadena<=57 and ASCII_cadena>=48:
        print("su caracter es un digito")
    else:
        print("su caracter no es un digito")
        print("se limita a solo una letra para obtener solo un valor evaluable")
        EXPLICACION: 
        -Realizamos el mismo proceso del punto 2 en cuanto a variables 
        -La diferencia consiste en esta vez crear la condicional teniendo en cuenta el intervalo [48,57] (digitos del 0 al 9).
        Si esta dentro del intervalo podemso estar seguro que sera un digito, en caso contrario no lo sera.
4.Dado un número real x. Determinar si el número es positivo, negativo o cero.
------------
      x:float=float(input("numero real a evaluar:"))
      if x>0:
    print("x es positivo")
    if x<0:
    print("x es negativo")
    if x==0:
    print("x es neutro para la suma")
    EXPLICACION: En este caso tan solo se necesita hacer 3 condicionales comparandolo con 0, siempre que sea un valor numerico
    x estara dentro de alguna de las 3 comparaciones
5.Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.
------------
     centrox:float=float(input("valor centro de la circunferencia en x:"))
     centroy:float=float(input("valor centro de la circunferencia en y:"))
     radio: float=float(input("radio de la circunferencia:"))
     x:float=float(input("valor en x del punto:"))
     y:float=float(input("valor en y del punto:"))
     primera_mitad= (x-centrox)**2
     segunda_mitad= (y-centroy)**2
     tercera_mitad=radio**2
     circunferencia=primera_mitad+segunda_mitad<=tercera_mitad
     if circunferencia :
    print("el punto esta dentro de la circunferencia")
    else:
    print("el punto no esta dentro de la circunferencia")
    EXPLICACION: para poder comprobar correctamente que el punto este dentro pedimos 5 variables basicas, estas son:
    . Un punto del centro (centro x, centro y) que represente el centro de la circunferencia
    . El radio que tendra la circunferencia (importante para evaluar que esta dentro)
    . Punto a evaluar (x,y)
    -Para que este dentro de la circunferencia necesitamos que la ecuacion canonica [(x-centrox)**2+(y-centroy)**2] sea
    menor o igual al radio (no es extrictamente igual porque un radio menor tambien se encuentra dentro de la circunferencia)
    .Si la desigualdad descrita en el codigo como la variable circunferencia es verdadera podemos estar seguro que el punto se
    encuentra dentro de la circunferencia
6.Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.
------------
     a:float=float(input("valor de la longitud 1:"))
     b:float=float(input("valor de la longitud 2:"))
     c:float=float(input("valor de la longitud 3:"))
     condicion_a:bool=False
     condicion_b:bool=False
     condicion_c:bool=False
     if a+b>c:
    condicion_a=True
    if a+c>b:
    condicion_b=True
    if b+c>a:
    condicion_c=True    
    if ((condicion_a)== True) and (condicion_b==True) and (condicion_c== True):
     print("se puede hacer un triangulo")
     else:
    print("no se puede hacer un triangulo")
    EXPLICACION: 
    -Creamos las 3 variables que se introducen por teclado, pero tambien creamos otras 3 variables booleanas para confirmar la 
    verdad del hecho fundamental que nos confirme que se puede crear un triangulo.
    -Hacemos 3 condicionales if separadas usando en cada una una de las 3 desigualdades triangulares para cambiar el estado de las
    variables booleanas a verdadero, estas desigualdades son necesarias para construir cualquier triangulo pues sin ellas no se podra
    formar por exceso o falta de longitud.
    -Por ultimo hacemos un cuarto condicional al que solo se pueda acceder si las 3 condiciones anteriores son verdad, en tal caso 
    podemos estar
    ACLARACION: (realmente si no se quieren usar booleanos puede hacerse con variables numericas, pero usar booleanos es mas facil de
    entender para quien quiera entender el codigo)
    seguros que se puede hacer un triangulo.
