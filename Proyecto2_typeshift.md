#Proyecto: TypeShift
#Autor: Ronaldo Barrios and Bryan Sajché
#Carnet: 1660520 y 1530420
#Adivinar Las palabras que hay en cada nivel

from screen import clear
from time import sleep
from random import randint
Licenciatura = ['colas', 'toros', 'agudo', 'agata', 'Agita', 'rugby', 'yagas', 'pegar', 'salta', 'tonos', 'timon', 'limon', 'Bocas', 'pumas', 'letra', 'tenis', 'joyas', 'panty', 'hobby', 'mayas']
Maestría = ['pelotas', 'cabello', 'cabañas', 'echamos', 'cabezal', 'gabacha', 'fabulas', 'xilemas', 'vaciado', 'ubicada', 'taberna', 'sabanas', 'toreada', 'peloton', 'sabados', 'rabanal', 'quebrar', 'quijada', 'pachuco', 'pacayas']  
Doctorado= ['danig', 'desactivar', 'buscador', 'medicina', 'abejorro', 'gabachas', 'siquinala', 'barberena', 'colores', 'botellas', 'moderno', 'confiable', 'volcanes', '', 'espacios', 'penales', 'piochas', 'internet', 'témperas', 'movistar']
A1 = ('Ronaldo')
A2 = ('Bryan')
title =('Proyecto Typeshift')
res='si'
inicicar = True

print('Hola! Espero que tengas un excelente y que te vaya muy bién :)')
nombre = input('Ingrea tu nombre por favor: ')

while inicicar:
    palzarlic = randint(0, len(Licenciatura)- 1)  # Se genera la palabra al azar
    pal1 = Licenciatura[palzarlic]
    pal1.sort(reverse=True)

    palzarmae = randint(0, len(Maestría)- 1)  # Se genera la palabra al azar
    pal2 = Maestría[palzarmae]
    pal2.sort(reverse=True)

    palzardoc = randint(0, len(Doctorado)- 1)  # Se genera la palabra al azar
    pal3 = Doctorado[palzardoc]
    pal3.sort(reverse=True)

    punteo=0#por c/p adivinada se le sumaran 3, 5, 7 pts importando el orden de los niveles
    fallos= 0
    palabras_Escri=[]
    adivinado1 = []
    adivinado2 = []
    adivinado3 = []

    while True: 
        nivel = input("""¿Qué opción te atreves a escoger?  
        1. Licenciatura -> fácil
        2. Maestría -> Intermedio
        3. Doctorado -> Dificil
        """)
        nivel = int(nivel)
        clear() 
        sleep(1.5)

        if nivel == 1 :
            print(str(pal1)#Aquí se va a mostrar la palabra escogida al azar
            word1 = input('Escribe la palabra' + nombre + ' que crees que sea: ') #aqui me da error inge lo tira en blue
            palabras_Escri.append(word1)#Aqui se va a guardar todas las palabras escritas por el usuario
            if word1 == pal1:
                punteo += 3
                adivinado1.append(word1)
                print('Descubriste la palabra bravo, sigue así')
                sleep(2)
                clear()  
            else:
                fallos += 1
                print('Recuerda que solo tienes 7 intentos para fallar')
                sleep(2)
                clear()
            
            if fallos == 7:
                print('Perdiste :,v)
                print('Para una próxima, suerte crack')
                sleep(2)
                clear()
                break
            if adivinado1 == Licenciatura and punteo == 60:#Si las palabras adivinadas son = a las del arreglo terminara 
                print('Congratulations haz adivinado todo')#el juego y le dira si quiere volver a jugar
                sleep(2)
                clear()  
                break
            
        if nivel == 2 : #Puede ser que sea un elif
            print(str(pal2))#Aquí se va a mostrar la palabra escogida al azar
            word2 = input('Escribe la palabra' + nombre + ' que crees que sea: ')#aqui me da error inge lo tira en blue
            palabras_Escri.append(word2)#Aqui se va a guardar todas las palabras escritas por el usuario
            if word2 == pal2:
                punteo += 5
                adivinado2.append(word1)
                print('Descubriste la palabra bravo, sigue así')
                sleep(2)
                clear()  
            else:
                fallos += 1
                print('Recuerda que solo tienes 5 intentos para fallar')
                sleep(2)
                clear()
            
            if fallos == 5:
                print('Perdiste :,v)
                print('Para una próxima, suerte crack')
                sleep(2)
                clear()
                break
            if adivinado2 == Maestría and punteo == 100:#Si las palabras adivinadas son = a las del arreglo terminara 
                print('Congratulations haz adivinado todo')#el juego y le dira si quiere volver a jugar
                sleep(2)
                clear()  
                break

        if nivel == 3 : #Y este un else
            print(str(pal3))#Aquí se va a mostrar la palabra escogida al azar
            word3 = input('Escribe la palabra' + nombre + ' que crees que sea: ')#aqui me da error inge lo tira en blue
            palabras_Escri.append(word3)#Aqui se va a guardar todas las palabras escritas por el usuario
            if word3 == pal3:
                punteo += 7
                adivinado3.append(word3)
                print('Descubriste la palabra bravo, sigue así')
                sleep(2)
                clear()  
            else:
                fallos += 1
                print('Recuerda que solo tienes 3 intentos para fallar')
                sleep(2)
                clear()
            
            if fallos == 3:
                print('Perdiste :,v)
                print('Para una próxima, suerte crack')
                sleep(2)
                clear()
                break
            if adivinado3 == Doctorado and punteo == 140:#Si las palabras adivinadas son = a las del arreglo terminara 
                print('Congratulations haz adivinado todo')#el juego y le dira si quiere volver a jugar
                sleep(2)
                clear()  
                break
    print(nombre + 'Tu puntajes es de: ' + str(punteo) + ' pts.' )
    print('Y las palabras que escribiste son: ')
    print(*palabras_Escri, sep=' , ')
    sleep(2)
    clear()
    sleep(2)

    print('Quieres volver a jugar')
    res = input('si/no ')
    sleep(2)
    clear()
    if res =='no':
        break     

director= 'Realizado por: \'{A1} y {A2} los autores legitimos\''#aqui me da error inge lo tira en blue
pana = title.strip().upper().center(80,'*')#aqui me da error inge lo tira en blue
lucha = director.format(A1 = A1,  A2=A2).center(80)#aqui me da error inge lo tira en blue
print(pana)
print(lucha)
print('*' *80)
input('')