## Chess System

**Chess System** é um jogo de xadrez baseado em console, implementado em Java, que simula as regras completas do xadrez clássico. O projeto foi desenvolvido durante um estágio de desenvolvimento de software e evoluiu para suportar movimentos de todas as peças, gerenciamento de turnos, captura, detecção de xeque e outras mecânicas fundamentais.

---

## Índice

* [Visão Geral](#visão-geral)
* [Funcionalidades](#funcionalidades)
* [Pré-requisitos](#pré-requisitos)
* [Instalação e Uso](#instalação-e-uso)
* [Estrutura do Projeto](#estrutura-do-projeto)
* [Como Jogar](#como-jogar)

---

## Visão Geral

O Chess System fornece:

* Representação do tabuleiro de xadrez em formato de matriz 8x8.
* Classes de peça (`Pawn`, `Rook`, `Knight`, `Bishop`, `Queen`, `King`), cada uma com regras de movimentação válidas.
* Controle de turnos entre jogadores (Brancas e Pretas).
* Gerenciamento de capturas e contagem de movimentos.
* Detecção de condições de xeque.
* Tratamento de exceções específicas de xadrez (`ChessException`, `BoardException`).

---

## Funcionalidades

1. **Inicialização do Tabuleiro**: Posicionamento automático de todas as peças na configuração inicial.
2. **Movimentação de Peças**: Cálculo de movimentos válidos para cada tipo de peça, com restrições de rota livre quando aplicável.
3. **Captura de Peças**: Remoção de peças capturadas do tabuleiro.
4. **Alternância de Turnos**: Controle automático de quem joga a cada turno.
5. **Detecção de Xeque**: Verificação se o rei de um jogador está em perigo.
6. **Contagem de Movimentos**: Registro do número de movimentos realizados em cada partida.

---

## Pré-requisitos

Antes de começar, verifique se você tem instalado:

* Java Development Kit (JDK) 8 ou superior
* Terminal (Linux/macOS) ou Prompt de Comando (Windows)

---

## Instalação e Uso

1. Clone este repositório:

   ```bash
   git clone https://github.com/murilosolino/chess-system.git
   ```
2. Navegue até a pasta do projeto:

   ```bash
   cd chess-system/src
   ```
3. Compile todas as classes Java:

   ```bash
   javac *.java
   ```
4. Execute a aplicação:

   ```bash
   java Main
   ```

> **Nota**: Ajuste o nome da classe principal (`Main`) se estiver diferente no código-fonte.

---

## Estrutura do Projeto

```
chess-system/
├── src/
│   ├── Board.java          # Lógica de criação e impressão do tabuleiro
│   ├── Piece.java          # Classe abstrata base para peças
│   ├── Pawn.java           # Implementação de Peão
│   ├── Rook.java           # Implementação de Torre
│   ├── Knight.java         # Implementação de Cavalo
│   ├── Bishop.java         # Implementação de Bispo
│   ├── Queen.java          # Implementação de Rainha
│   ├── King.java           # Implementação de Rei e lógica de xeque
│   ├── ChessException.java # Exceções específicas do jogo
│   ├── ChessPosition.java  # Conversão de coordenadas de tabuleiro
│   └── Main.java           # Ponto de entrada da aplicação
└── .gitignore              # Arquivos e pastas ignoradas pelo Git
```

---

## Como Jogar

Após iniciar a aplicação, o tabuleiro será exibido no console com coordenadas:

```text
  a b c d e f g h
8 ♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜ 8
7 ♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟ 7
...                   
1 ♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖ 1
  a b c d e f g h
```

1. **Entradas**: Informe a posição de origem e destino no formato padrão (ex: `e2 e4`).
2. **Movimento**: O sistema valida e executa o movimento, mostrando o tabuleiro atualizado.
3. **Captura**: Se houver peça adversária na posição de destino, ela será capturada.
4. **Fim de Jogo**: O jogo detecta xequemate ou saída manual.

---
