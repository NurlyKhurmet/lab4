# lab4
lab 4
#4
unique = set()
nounique = []

a = input(" элементы через запятую: ")

b = a.split(", ")

for item in b:
    if item not in unique:
        unique.add(item)
    else:
        nounique.append(item)

print("уникальные items:", unique)
print("неповторяющиеся items:", tuple((item, nounique.count(item)) for item in set(nounique)))
#2 

print(" типы операций:")
print("1. cложение")
print("2. умножение")
print("3. деление")
print("4. возведение в степень")

vybor = int(input("(1/2/3/4): "))

n = input("2 числа через запятую: ").split(',')

if len(n) != 2:
    print("неверно")
else:
    a, b = map(float, n)
    
    if vybor == 1:
        result = a + b
    elif vybor == 2:
        result = a * b
    elif vybor == 3:
        result = a / b
    elif vybor == 4:
        result = a ** b
    else:
        print("веверный выбор.Выбери от 1 до 4.")
    
    print("результат:", result)

#1
a = input("имя:")

salaryInput = input(" желаемая зарплата: ")

try:
    zp = int(salaryInput)
    print(f"{a}, уровень налога: {zp * 0.2}")
except ValueError:
    print(f"{a}, введите как число.")
