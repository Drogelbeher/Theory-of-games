import random
from math import sqrt
def generator(p):
    if random.random() <= p:
        result = 0
    else:
        result = 1
    return result
def math_exp(p1,p2):
    result = 2*p1*p2 - 3*p1*(1 - p2) - (1 - p1)*p2 + 2*(1 - p1)*(1 - p2)
    return result
def disp(p1,p2):
    result = 4*p1*p2 + 9*p1*(1 - p2) + (1 - p1)*p2 + 4*(1 - p1)*(1 - p2) - (math_exp(p1,p2))**2
    return result
def msq(game_n,sum_n):
    result = 0
    for x in game_n:
        result += (board[x[0]][x[1]] - sum_n/100)**2
    result = sqrt(result/100)
    return result
board = [[2,-3],[-1,2]]
#game_1
p1 = 0.5
p2 = 0.5
game_1 = []
for x in range(100):
    game_1.append((generator(p1),generator(p2)))
sum_1 = 0
for x in game_1:
    sum_1 += board[x[0]][x[1]]
print("Сценарий 1:")
print("Общий выигрыш: ", sum_1)
print("Средний выигрыш: ", sum_1/100)
print("Математическое ожидание: ", math_exp(p1,p2))
print("Эксперементальное среднее квадратичное отклонение: ", msq(game_1,sum_1))
print("Дисперсия: ", disp(p1,p2))
print("Теоретическое среднее квадратичное отклонение: ", sqrt(disp(p1,p2)))
#game_2
p1 = 0.5
p2 = 0.25
game_2 = []
for x in range(100):
    game_2.append((generator(p1),generator(p2)))
sum_2 = 0
for x in game_2:
    sum_2 += board[x[0]][x[1]]
print("Сценарий 2:")
print("Общий выигрыш: ", sum_2)
print("Средний выигрыш: ", sum_2/100)
print("Математическое ожидание: ", math_exp(p1,p2))
print("Эксперементальное среднее квадратичное отклонение: ", msq(game_2,sum_2))
print("Дисперсия: ", disp(p1,p2))
print("Теоретическое среднее квадратичное отклонение: ", sqrt(disp(p1,p2)))
#game_3
p2 = 0.25
game_3 = []
red = 10
blue = 10
for x in range(100):
    p1 = red/(blue + red)
    colour = generator(p1)
    game_3.append((colour,generator(p2)))
    if board[game_3[len(game_3)-1][0]][game_3[len(game_3)-1][1]] > 0:
        if colour == 0:
            red += 2
        else:
            blue += 2        
p1 = red/(blue + red)
game_3 = []
for x in range(100):
    game_3.append((generator(p1),generator(p2)))
sum_3 = 0
for x in game_3:
    sum_3 += board[x[0]][x[1]]
print("Сценарий 3:")
print("Общий выигрыш: ", sum_3)
print("Средний выигрыш: ", sum_3/100)
print("Математическое ожидание: ", math_exp(p1,p2))
print("Эксперементальное среднее квадратичное отклонение: ", msq(game_3,sum_3))
print("Дисперсия: ", disp(p1,p2))
print("Теоретическое среднее квадратичное отклонение: ", sqrt(disp(p1,p2)))
#game_4
p2 = 0.25
game_4 = []
red = 100
blue = 100
for x in range(100):
    p1 = red/(blue + red)
    colour = generator(p1)
    game_4.append((colour,generator(p2)))
    if board[game_4[len(game_4)-1][0]][game_4[len(game_4)-1][1]] < 0:
        if colour == 0:
            red -= 3
        else:
            blue -= 1        
p1 = red/(blue + red)
game_4 = []
for x in range(100):
    game_4.append((generator(p1),generator(p2)))
sum_4 = 0
for x in game_4:
    sum_4 += board[x[0]][x[1]]
print("Сценарий 4:")
print("Общий выигрыш: ", sum_4)
print("Средний выигрыш: ", sum_4/100)
print("Математическое ожидание: ", math_exp(p1,p2))
print("Эксперементальное среднее квадратичное отклонение: ", msq(game_4,sum_4))
print("Дисперсия: ", disp(p1,p2))
print("Теоретическое среднее квадратичное отклонение: ", sqrt(disp(p1,p2)))
#game_5
game_5 = []
red_A = 10
blue_A = 10
red_B = 10
blue_B = 10
for x in range(100):
    p1 = red_A/(blue_A + red_A)
    p2 = red_B/(blue_B + red_B)
    colour_A = generator(p1)
    colour_B = generator(p2)
    game_5.append((colour_A,colour_B))
    if board[game_5[len(game_5)-1][0]][game_5[len(game_5)-1][1]] > 0:
        if colour_A == 0:
            red_A += 2
        else:
            blue_A += 2
    else:
        if colour_B == 0:
            red_B += 2
        else:
            blue_B += 2
p1 = red_A/(blue_A + red_A)
p2 = red_B/(blue_B + red_B)
game_5 = []
for x in range(100):
    game_5.append((generator(p1),generator(p2)))
sum_5 = 0
for x in game_5:
    sum_5 += board[x[0]][x[1]]
print("Сценарий 5:")
print("Общий выигрыш: ", sum_5)
print("Средний выигрыш: ", sum_5/100)
print("Математическое ожидание: ", math_exp(p1,p2))
print("Эксперементальное среднее квадратичное отклонение: ", msq(game_5,sum_5))
print("Дисперсия: ", disp(p1,p2))
print("Теоретическое среднее квадратичное отклонение: ", sqrt(disp(p1,p2)))

