# Mobile Developer : Jogos
## Fundamentos de Programação com Node
## Simulador de Corridas do Mario Kart com Node.js

### Author: Macedo, Glener Diniz - Desenvolvedor Full Stack
### Data.: 22 de julho de 2025.

### Orientador:

Felipe Aguiar - Tech Educator, DIO

<p align="center">
  <img src="https://raw.githubusercontent.com/gdmacedo/Nodes.js/refs/heads/main/imagens/NodeJs.png" alt="">
</p>


### Desafio de Projeto:
O desafio foi desenvolver um simulador de corridas inspirado em Mario Kart utilizando Node.js, onde toda a lógica do jogo será executada no terminal. O jogador controlará um personagem e participará de corridas, podendo usar itens clássicos do universo Mario Kart. A movimentação e interação ocorrerão por meio de entradas no console, com o simulador calculando os resultados da corrida, uso de itens e posicionamento dos competidores. O foco do projeto está no desenvolvimento da lógica de jogo no backend, com a execução e simulação acontecendo no ambiente do terminal.


<p align="center">
  <img  src="https://raw.githubusercontent.com/gdmacedo/Glener-Talk/main/developer-MacedoGDiniz.jpg" alt="Macedo, Glener Diniz">
</p>

  <table>
        <tr>
            <td>
                <img src="./docs/header.gif" alt="Mario Kart" width="200">
            </td>
            <td>
                <b>Objetivo:</b>
                <p>Mario Kart é uma série de jogos de corrida desenvolvida e publicada pela Nintendo. Nosso desafio será criar uma lógica de um jogo de vídeo game para simular corridas de Mario Kart, levando em consideração as regras e mecânicas abaixo.</p>
            </td>
        </tr>
    </table>

<h2>Players</h2>
      <table style="border-collapse: collapse; width: 800px; margin: 0 auto;">
        <tr>
            <td style="border: 1px solid black; text-align: center;">
                <p>Mario</p>
                <img src="./docs/mario.gif" alt="Mario Kart" width="60" height="60">
            </td>
            <td style="border: 1px solid black; text-align: center;">
                <p>Velocidade: 4</p>
                <p>Manobrabilidade: 3</p>
                <p>Poder: 3</p>
            </td>
             <td style="border: 1px solid black; text-align: center;">
                <p>Peach</p>
                <img src="./docs/peach.gif" alt="Mario Kart" width="60" height="60">
            </td>
            <td style="border: 1px solid black; text-align: center;">
                <p>Velocidade: 3</p>
                <p>Manobrabilidade: 4</p>
                <p>Poder: 2</p>
            </td>
              <td style="border: 1px solid black; text-align: center;">
                <p>Yoshi</p>
                <img src="./docs/yoshi.gif" alt="Mario Kart" width="60" height="60">
            </td>
            <td style="border: 1px solid black; text-align: center;">
                <p>Velocidade: 2</p>
                <p>Manobrabilidade: 4</p>
                <p>Poder: 3</p>
            </td>
        </tr>
        <tr>
            <td style="border: 1px solid black; text-align: center;">
                <p>Bowser</p>
                <img src="./docs/bowser.gif" alt="Mario Kart" width="60" height="60">
            </td>
            <td style="border: 1px solid black; text-align: center;">
                <p>Velocidade: 5</p>
                <p>Manobrabilidade: 2</p>
                <p>Poder: 5</p>
            </td>
            <td style="border: 1px solid black; text-align: center;">
                <p>Luigi</p>
                <img src="./docs/luigi.gif" alt="Mario Kart" width="60" height="60">
            </td>
            <td style="border: 1px solid black; text-align: center;">
                <p>Velocidade: 3</p>
                <p>Manobrabilidade: 4</p>
                <p>Poder: 4</p>
            </td>
            <td style="border: 1px solid black; text-align: center;">
                <p>Donkey Kong</p>
                <img src="./docs/dk.gif" alt="Mario Kart" width="60" height="60">
            </td>
            <td style="border: 1px solid black; text-align: center;">
                <p>Velocidade: 2</p>
                <p>Manobrabilidade: 2</p>
                <p>Poder: 5</p>
            </td>
        </tr>
    </table>

<p></p>

<h3>🕹️ Regras & mecânicas:</h3>

<b>Jogadores:</b>

<input type="checkbox" id="jogadores-item" />
<label for="jogadores-item">O Computador deve receber dois personagens para disputar a corrida em um objeto cada</label>

<b>Pistas:</b>

<ul>
  <li><input type="checkbox" id="pistas-1-item" /> <label for="pistas-1-item">Os personagens irão correr em uma pista aleatória de 5 rodadas</label></li>
  <li><input type="checkbox" id="pistas-2-item" /> <label for="pistas-2-item">A cada rodada, será sorteado um bloco da pista que pode ser uma reta, curva ou confronto</label>
    <ul>
      <li><input type="checkbox" id="pistas-2-1-item" /> <label for="pistas-2-1-item">Caso o bloco da pista seja uma RETA, o jogador deve jogar um dado de 6 lados e somar o atributo VELOCIDADE, quem vencer ganha um ponto</label></li>
      <li><input type="checkbox" id="pistas-2-2-item" /> <label for="pistas-2-2-item">Caso o bloco da pista seja uma CURVA, o jogador deve jogar um dado de 6 lados e somar o atributo MANOBRABILIDADE, quem vencer ganha um ponto</label></li>
      <li><input type="checkbox" id="pistas-2-3-item" /> <label for="pistas-2-3-item">Caso o bloco da pista seja um CONFRONTO, o jogador deve jogar um dado de 6 lados e somar o atributo PODER, quem perder, perde um ponto</label></li>
      <li><input type="checkbox" id="pistas-2-3-item" /> <label for="pistas-2-3-item">Nenhum jogador pode ter pontuação negativa (valores abaixo de 0)</label></li>
    </ul>
  </li>
</ul>

<b>Condição de vitória:</b>

<input type="checkbox" id="vitoria-item" />
<label for="vitoria-item">Ao final, vence quem acumulou mais pontos</label>



#### Conteúdo:
- Introdução
- Regras De Negócio
- Demonstração
- Setup
- Objetos
- Roll Dice (Async Functions)
- Main (Auto Invoke)
- Start (Template String)
- Race Engine (Functions Chains)
- Rounds (For)
- Blocks (Switch Case)
- Convenções
- Testando Blocos (If)
- Escopo De Variaveis
- Log Roll (Encapsulate)
- Javascript Expressions
- Winner - (Else If's)
- Diminuindo Ifs (If Ternario)
- Condição Dupla (If Combinado)
- Game Over (Clean Ifs)
- Conclusão
- Projeto Base
- Entendendo o Desafio


####Como Executar o seu Projeto
1. Baixe o repositório:

https://github.com/gdmacedo/Nodes.js/tree/main/Simulador%20de%20Corridas%20do%20Mario%20Kart



2. Navegue até o diretório/pasta do seu projeto clonado:

cd nome-do-seu-repositorio



3. Em seu terminal e na pasta do projeto

node src/index.js
