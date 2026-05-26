# ♟ Xadrez System — Java

Jogo de xadrez completo para terminal, desenvolvido em **Java puro**. O projeto implementa todas as regras oficiais do xadrez, incluindo jogadas especiais, com interface colorida no console.

## ✨ Funcionalidades

- **Todas as peças**: Rei, Rainha, Torre, Bispo, Cavalo e Peão
- **Jogadas especiais**: Roque (kingside e queenside), En Passant
- **Detecção automática** de Xeque e Xeque-mate
- **Validação de movimentos**: impede jogadas ilegais e auto-xeque
- **Interface no terminal** com cores ANSI e destaque de movimentos possíveis
- **Controle de turnos**: alternância entre jogadores Branco e Preto
- **Exibição de peças capturadas** por cor

## 🏗 Estrutura do Projeto

```
src/
├── application/
│   ├── Program.java          # Ponto de entrada — loop principal do jogo
│   └── UI.java               # Interface do terminal (tabuleiro, cores, input)
├── boardgame/
│   ├── Board.java            # Tabuleiro genérico (matriz de peças)
│   ├── Piece.java            # Peça abstrata do tabuleiro
│   ├── Position.java         # Posição (linha, coluna)
│   └── BoardException.java   # Exceção do tabuleiro
└── chess/
    ├── ChessMatch.java       # Lógica da partida (regras, turnos, xeque)
    ├── ChessPiece.java       # Peça de xadrez (cor, contagem de movimentos)
    ├── ChessPosition.java    # Posição no formato do xadrez (ex: e2)
    ├── ChessException.java   # Exceção de jogada inválida
    ├── Color.java            # Enum de cores (WHITE, BLACK)
    └── pieces/
        ├── King.java         # Rei (inclui roque)
        ├── Queen.java        # Rainha
        ├── Rook.java         # Torre
        ├── Bishop.java       # Bispo
        ├── Knight.java       # Cavalo
        └── Pawn.java         # Peão (inclui en passant)
```

## 🚀 Como Executar

```bash
# Compilar
javac -d bin src/**/*.java

# Executar
java -cp bin application.Program
```

> ⚠️ O terminal deve suportar cores ANSI para a melhor experiência visual.

## 🎮 Como Jogar

1. O jogo inicia com as peças Brancas
2. Digite a **posição de origem** (ex: `e2`)
3. O tabuleiro destaca os movimentos possíveis
4. Digite a **posição de destino** (ex: `e4`)
5. Os turnos alternam automaticamente entre Branco e Preto

## 🛠 Tecnologias

- **Java** (puro, sem frameworks)
- **Programação Orientada a Objetos** — herança, polimorfismo, encapsulamento
- **Padrão em camadas** — separação entre tabuleiro genérico e regras de xadrez
