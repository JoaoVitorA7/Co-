repetir = True
while repetir:
    print("Para a matriz ser feita digite cada linha por vez, sem espaços entre os caracteres, lembrando que os pontos de entrega são representados por letras, o ponto de partida é representado por #, os pontos vazioz são representados por '.'")
    n, m = list(map(int, input("Digite o número de linhas e colunas da matriz, respectivamente (com um espaço entre ambos): ").split()))
    matriz = list(range(m))
    matriz1 = list(range(m))
    matriz = [matriz]
    for l in range(n-1):
        matriz = matriz + [matriz1]
    for i in range(n):
        matriz[i] = list(input("Digite a %s° linha da matriz: " %(i+1)).swapcase())
    matrizPontos = []
    linha = 0
    pontoAtual = ["",0,0]
    for l in range(n):
        for c in range(m):
            if matriz[l][c] != ".":
                if matriz[l][c] == "#":
                    pontoAtual[0] = "#"
                    pontoAtual[1] = l  
                    pontoAtual[2] = c 
                else: 
                    matrizPontos = matrizPontos + [["",0,0]] 
                    matrizPontos[linha][0] = matriz[l][c]
                    matrizPontos[linha][1] = l 
                    matrizPontos[linha][2] = c
                    linha += 1
    menorLinha = 0
    checkLinhas = -1
    checkList = 0
    menor = (n - 1) + (m - 1) + 1
    listSaida = list(range(len(matrizPontos)))

    while listSaida[len(listSaida)-1] == len(listSaida) - 1:    
        checkLinhas += 1 
        if (abs(pontoAtual[1] - matrizPontos[checkLinhas][1])) + (abs(pontoAtual[2] - matrizPontos[checkLinhas][2])) < menor and matrizPontos[checkLinhas][0] not in listSaida:
            menorLinha = checkLinhas
            menor = (abs(pontoAtual[1] - matrizPontos[checkLinhas][1])) + (abs(pontoAtual[2] - matrizPontos[checkLinhas][2]))
            listSaida[checkList] = matrizPontos[checkLinhas][0]                
            
        if checkLinhas == len(matrizPontos) - 1:        
            pontoAtual[0] = matrizPontos[menorLinha][0]
            pontoAtual[1] = matrizPontos[menorLinha][1]
            pontoAtual[2] = matrizPontos[menorLinha][2]
            checkLinhas = -1
            checkList += 1
            menor = (n - 1) + (m - 1) + 1
        
    print("A sequência de pontos de entrega são: ",listSaida)
    repetirCheck = input("Gostaria de checar outra matriz? Digite 'SIM' ou 'NAO': ")
    if repetirCheck == "SIM":
        repetir = True
    else:
        break
