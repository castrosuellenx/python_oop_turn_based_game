# Python OOP Turn-Based Game

![Python](https://img.shields.io/badge/python-3.x-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

A simple turn-based battle game implemented in Python using Object-Oriented Programming principles.

## Introduction

This Python OOP Turn-Based Game is a command-line application that simulates a battle between a hero and an enemy. It demonstrates the use of classes, inheritance, and encapsulation in Python while providing an interactive gaming experience.

## Features

- Turn-based combat system
- Hero and Enemy classes with unique attributes
- Special abilities for the Hero
- Random damage calculation based on character level
- Interactive command-line interface

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/castrosuellenx/python_oop_turn_based_game.git
   ```
2. Navigate to the project directory:
   ```
   cd python_oop_turn_based_game
   ```
3. Ensure you have Python 3.x installed on your system.

## Usage

Run the game by executing the `main.py` file:

```
python main.py
```

Follow the on-screen prompts to play the game. You'll control the Hero character and choose between normal attacks and special abilities to defeat the Enemy.

## Game Structure

The game is structured using the following classes:

- `Personagem`: Base class for all characters
- `Heroi`: Subclass of `Personagem`, representing the player-controlled hero
- `Inimigo`: Subclass of `Personagem`, representing the computer-controlled enemy
- `Jogo`: Orchestrator class that manages the game flow

### Example Code Snippet

```python
class Heroi(Personagem):
    def __init__(self, nome, vida, nivel, habilidade) -> None:
        super().__init__(nome, vida, nivel)
        self.__habilidade = habilidade

    def ataque_especial(self, alvo):
        dano = random.randint(self.get_nivel() * 5, self.get_nivel() * 8)
        alvo.receber_ataque(dano)
        print(f"{self.get_nome()} usou sua habilidade especial {self.get_habilidade()} em {alvo.get_nome()} e causou {dano} de dano!")
```

## License

This project is open source and available under the [MIT License](LICENSE).