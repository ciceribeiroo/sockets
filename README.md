# Trabalho-Redes-Socket

Implementação de uma batalha naval utilizando sockets em python para disciplina de Redes.

Tambem disponível no seguinte repositório: [ciceribeiroo](https://github.com/ciceribeiroo/Trabalho-Redes-Socket) 

## Execução

Para rodar o jogo, é necessaria a instalacao de python3 (*pip install python3*).

Para executar a aplicação, servidor deve ser rodado primeiro. Após isso, em outro cmd, o cliente deve ser rodado. As linhas de comando são respectivamente:

Para Linux ou Mac: <br> 
*python3 server.py*<br>
*python3 client.py* <br>

Para Windows: <br>
*py server.py*<br>
*py client.py*<br>

## Jogo

Após isso, cada jogador irá definir a posição de seus navios na malha 10x10 sendo
  - 1 porta avião de tamanho 5
  - 2 navios tanque de tamanho 4
  - 3 contra torpedos de tamanho 3
  - 4 submarinos de tamanho 2

A ideia principal do jogo é que cada jogador tem dois tabuleiros, um seu e um do seu oponente. No seu ele ve as posições atuais dos navios e do oponente ele ve vazio. Na malha os simbolos representam:
  - '-' escondido
  - 'O' seu navio
  - 'X' ataque bem sucedisdo
  - '.' ataque em celula vazia
  
Um jogador faz uma jogada, que é validada. Se essa for correta, ele ira manda-la para o outro jogador, para que as opeações ocorram na matriz completa. Se tem algo, tal marcação sera X e ira retornar true. Se não a marcação é . e retornará true.  Essa marcação volta para o jogador original para que aparecça na malha escondida.

O jogo termina quando um dos jogadores descobrir todas os navios(controlado por um navegador que é incrementado toda vez que algo é atingido).
