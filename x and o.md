mas = [[" ", 0, 1, 2], [0, "-", "-", "-"], [1, "-", "-", "-"], [2, "-", "-", "-"]]
n=0

for b in range(9):
    for i in range(0, len(mas)):
        for i2 in range(0, len(mas[i])):
            print(mas[i][i2], end=' ')
        print()
    a = int(input("введите координат a "))
    b = int(input("введите координат b "))
    if (a<0)or(b<0)or(a>2)or(b>2):
        print("ты играешь не по правилам, я с тобой не играю")
    else:
        if mas[a + 1][b + 1] != "x" and mas[a + 1][b + 1] != "o":
            if n%2 ==0:
                mas[a+1][b+1]="x"
            else:
                mas[a+1][b+1] = "o"
        else:
            print("здесь уже есть знак. так не честно, я с тобой не играю")
            break
    n+=1
    if n>4:
        if ((mas[1][1]=="x" and mas[1][2]=="x" and mas[1][3]=="x") or
            (mas[2][1]=="x" and mas[2][2]=="x" and mas[2][3]=="x") or
            (mas[3][1] == "x" and mas[3][2] == "x" and mas[3][3] == "x") or
            (mas[1][1] == "x" and mas[2][1] == "x" and mas[3][1] == "x") or
            (mas[1][2] == "x" and mas[2][2] == "x" and mas[3][2] == "x") or
            (mas[1][3] == "x" and mas[2][3] == "x" and mas[3][3] == "x") or
            (mas[1][1] == "x" and mas[2][2] == "x" and mas[3][3] == "x") or
            (mas[1][3] == "x" and mas[2][2] == "x" and mas[3][1] == "x")):
            for i in range(0, len(mas)):
                for i2 in range(0, len(mas[i])):
                    print(mas[i][i2], end=' ')
                print()
            print("победил игрок x")
            break

        elif (mas[1][1]=="o" and mas[1][2]=="o" and mas[1][3]=="o" or
            mas[2][1]=="o" and mas[2][2]=="o" and mas[2][3]=="o" or
            mas[3][1] == "o" and mas[3][2] == "o" and mas[3][3] == "o" or
            mas[1][1] == "o" and mas[2][1] == "o" and mas[3][1] == "o" or
            mas[1][2] == "o" and mas[2][2] == "o" and mas[3][2] == "o" or
            mas[1][3] == "o" and mas[2][3] == "o" and mas[3][3] == "o" or
            mas[1][1] == "o" and mas[2][2] == "o" and mas[3][3] == "o" or
            mas[1][3] == "o" and mas[2][2] == "o" and mas[3][1] == "o"):
            for i in range(0, len(mas)):
                for i2 in range(0, len(mas[i])):
                    print(mas[i][i2], end=' ')
                print()
            print("победил игрок o")
            break

    if n==9:
        for i in range(0, len(mas)):
            for i2 in range(0, len(mas[i])):
                print(mas[i][i2], end=' ')
            print()
        print("ничья")
