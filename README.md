# Jogo-de-palavras-secretas
Neste projeto, foi desenvolvido um jogo de palavras secretas como uma forma de iteração nos códigos.
Ultilizando a linguagem de programação Python, que é uma linguagem dinâmica e forte.
Foi usado o módulo os para limpar o terminal automaticamente após o ciclo ser concluído ultilizando 
os.system(cls), que pode se ultilizar 'clear' no Windows e outros sistemas opercionais. Dessa forma, foi o ultilizado o loop principal(while) e subloop (for). Além disso, foi ultilizado (input) para entrada do jogador, validação da entrada do
jogador através do que ele digitou usando 'if' e 'len' para analisar os elemnetos no argumento, con-
strução da palavra ultilizando o método 'for' e 'in' para iterar e pecorrer os elementos, operadores
concicionais como 'if' e 'elif' foram ultilizados também para a construçao da variável (palavra formada).
Assim, sendo True todos esse algoritmos, serão executados e impressos os códigos do último bloco. Da
linha 45 a 51.




import os

palavra_secreta = 'vitor'
letra_acertada = ''
numero_de_tentativas = 0


while True:
    
    letra_digitada = input('Digite uma letra: ')
    numero_de_tentativas += 1
    
    if len(letra_digitada)> 1:
        print('Digite apenas uma letra.')
        continue
    if letra_digitada in palavra_secreta:
        letra_acertada += letra_digitada   # a letra digitada é adicionada à variável vazia (letra acertada)


    palavra_formada = ''

    for letra_secreta in palavra_secreta:  # Para cada letra na palavra secreta
    
        if letra_secreta in letra_acertada:  # Verifica se a letra foi acertada (adiciona a letra correta ns variável (letra_secreta)
            palavra_formada += letra_secreta  # Adiciona a letra acertada da palvra secreta.
        else:
            palavra_formada += '*'  # Adiciona '*' para as letras não acertados.
        
    print( 'Palavra formada: ',palavra_formada)  # Exibe o progresso.
    
    if palavra_formada == palavra_secreta:   # esta ocasião sendo True, executa e imprime os algoritmos abaixo.
        os.system('cls')
        print('Vacê ganhou. Parabéns')
        print('A palavra secreta é:', palavra_secreta)
        print('Número de tentativas:',numero_de_tentativas)
        letra_acertada = ''
        numero_de_tentativas = 0
        
  
