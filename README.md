#Калькулятор +/-
def calculator():
    while True:
        usl = input("Введите операцию (+ для сложения, - для вычитания): ")

        if usl not in ['+', '-']:
            print("Ошибка! Некорректная операция.")
            continue

        try:
            num = int(input ("Введите первое чисто: "))
            num2 = int(input ("Введите второе число: "))


            if usl == '+':
                res = num + num2
                print ("Сумма чисел равна ", res)
            elif usl == '-':
                res = num - num2
                print( "Разница чисел равна ",  res)
        except ValueError:
            print("Ошибка! Введите числа корректно.")


        choice = input("Хотите продолжить? (да/нет): ")
        if choice.lower() != 'да':
            break

calculator()
