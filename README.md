# test1

#3: Создайте программу “Медицинская анкета”, где вы запросите у пользователя следующие данные: имя, фамилия, возраст и вес.
#Выведите результат согласно которому:
#Пациент в хорошем состоянии, если ему до 30 лет и вес от 50 и до 120 кг,
#Пациенту требуется заняться собой, если ему более 30 и вес меньше 50 или больше 120 кг
#Пациенту требуется врачебный осмотр, если ему более 40 и вес менее 50 или больше 120 кг.
#Все остальные варианты вы можете обработать на ваш вкус и полет фантазии.
#(Формула не соответствует реальной действительности и здесь используется только ради примера)
#Примечание: при написание программы обратите внимание на условия в задаче и в вашем коде.  Протестируйте программу несколько раз и убедитесь, что проверки срабатывают верно. В случае ошибок, уточните условия для той или иной ситуации.
#Пример: Вася Пупкин, 29 год, вес 90 - хорошее состояние
#Пример: Вася Пупкин, 31 год, вес 121 - следует заняться собой
#Пример: Вася Пупкин, 31 год, вес 49 - следует заняться собой
#Пример: Вася Пупкин, 41 год, вес 121 - следует обратится к врачу!
#Пример: Вася Пупкин, 41 год, вес 49 - следует обратится к врачу!

print("Hello!")
answer = ''
while answer != 'N':
    answer = input("Do you wont to create a new medical questionnaire? (Y/N)")
    if answer == 'Y':
        name = input("What is your name?")
        surname = input("What is your surname?")
        years = int(input("How old are you?"))
        weight = int(input("What is your weight?"))
        range = bool(50 < weight < 120)

        print("Your medical results:")
        if years < 30 and range:
            print('Your name:', name, ', Your surname:', surname, ', Your weight:', weight, ', Your age:', years, " - You have a nice healths")
        elif years < 40 and not range:
            print('Your name:', name, ', Your surname:', surname, ', Your weight:', weight, ', Your age:', years, " - You need a survey")
        elif years > 40 and range:
            print('Your name:', name, ', Your surname:', surname, ', Your weight:', weight, ', Your age:', years, " - You need a hospitalization")
        else:
            print('Your name:', name, ', Your surname:', surname, ', Your weight:', weight, ', Your age:', years, " - You have a bad healths")
    elif answer == 'N':
        print("Good bye!")
