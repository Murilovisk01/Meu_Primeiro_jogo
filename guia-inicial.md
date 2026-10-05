# Guia inicial

Referência rápida de tecnologia, instalação e GDScript para quem vem de Python e Java.

## Decisões de tecnologia

| Item | Escolha | Motivo |
|---|---|---|
| Engine | Godot 4 (estável, versão padrão) | Gratuita, leve, feita para 2D |
| Linguagem | GDScript | Sintaxe parecida com Python, integrada ao editor |
| Versionamento | Git + GitHub | Histórico e backup desde o primeiro dia |
| Arte | Assets gratuitos por enquanto | O foco agora é programação |

## Instalação

1. **Godot**: baixar em godotengine.org, extrair o `.zip` e abrir o executável. Não tem instalador.
2. **Git**: baixar em git-scm.com e instalar com as opções padrão.
3. **GitHub**: criar a conta e um repositório privado para o jogo.

Ao criar o projeto na Godot, o renderizador "Compatibilidade" é suficiente para 2D e roda em qualquer PC.

## Conceitos da Godot

- **Nó (Node)**: a peça básica. Cada nó faz uma coisa: mostrar um sprite, detectar colisão, tocar um som.
- **Cena (Scene)**: uma árvore de nós salva em arquivo. O jogador é uma cena, um inimigo é outra, o mapa é outra.
- **Script**: código anexado a um nó para dar comportamento a ele.
- **Sinal (Signal)**: aviso que um nó emite ("fui clicado", "algo entrou em mim") e outros nós escutam.

Para quem vem de Java: uma cena é parecida com uma classe, e colocar a cena no jogo é parecido com instanciar um objeto.

## GDScript para quem sabe Python

### O que é igual
Indentação define blocos, `if / elif / else`, `for x in lista`, `while`, `and / or / not`, `#` para comentários.

### O que muda

| Python | GDScript |
|---|---|
| `x = 10` | `var x = 10` |
| `x: int = 10` | `var x: int = 10` |
| `PI = 3.14` | `const PI = 3.14` |
| `def somar(a, b):` | `func somar(a, b):` |
| `def f(a: int) -> int:` | `func f(a: int) -> int:` |
| `True / False / None` | `true / false / null` |
| `self.vida` | `vida` (ou `self.vida`) |
| `class Jogador(Base):` | `extends Base` na primeira linha do arquivo |
| `print(f"vida: {vida}")` | `print("vida: %d" % vida)` |
| `len(lista)` | `lista.size()` |
| `lista.append(x)` | `lista.append(x)` |
| `{"a": 1}` | `{"a": 1}` |

Cada arquivo `.gd` é uma classe. Não existe `import`: os outros scripts e cenas são carregados com `preload("res://caminho")`.

### Funções especiais da Godot

```gdscript
extends Node2D

func _ready() -> void:
	# roda uma vez, quando o nó entra na cena
	print("pronto")

func _process(delta: float) -> void:
	# roda a cada quadro; delta é o tempo em segundos desde o último quadro
	pass

func _physics_process(delta: float) -> void:
	# roda em ritmo fixo; é aqui que fica movimento e colisão
	pass
```

### Anotações mais usadas

```gdscript
@export var velocidade: float = 120.0   # aparece no editor para ajustar sem mexer no código
@onready var sprite = $Sprite2D          # pega um nó filho quando a cena fica pronta
```

`$NomeDoNo` é um atalho para `get_node("NomeDoNo")`.

### Sinais

```gdscript
signal vida_mudou(nova_vida: int)

var vida: int = 100

func levar_dano(valor: int) -> void:
	vida -= valor
	vida_mudou.emit(vida)
```

Em outro script, para escutar:

```gdscript
func _ready() -> void:
	jogador.vida_mudou.connect(_ao_mudar_vida)

func _ao_mudar_vida(nova_vida: int) -> void:
	print("vida agora: %d" % nova_vida)
```

### Primeiro personagem andando

Script para um nó `CharacterBody2D`, visão de cima:

```gdscript
extends CharacterBody2D

@export var velocidade: float = 120.0

func _physics_process(delta: float) -> void:
	var direcao := Input.get_vector("ui_left", "ui_right", "ui_up", "ui_down")
	velocity = direcao * velocidade
	move_and_slide()
```

## Onde estudar

- **Learn GDScript From Zero** (GDQuest): curso gratuito e interativo no navegador. Ponto de partida da Fase 1.
- **Documentação oficial**: docs.godotengine.org. Há tradução parcial em português; o inglês é o mais completo.
- **"Your first 2D game"**: tutorial oficial dentro da documentação, usado na Fase 2.
- **Ajuda dentro do editor**: `F1` ou `Ctrl + clique` em qualquer função abre a documentação dela.

## Assets gratuitos

- **Kenney** (kenney.nl): pacotes grandes, licença livre.
- **Sprout Lands** (itch.io): pacote de fazenda no estilo Stardew Valley.
- **itch.io**, seção de assets gratuitos: sempre confira a licença de cada pacote.

## Organização sugerida da pasta

Quando o projeto do jogo for criado na Fase 3:

```
Meu_Primeiro_jogo/
├── primeiroContato.md
├── ideia-do-jogo.md
├── plano-de-estudo.md
├── guia-inicial.md
└── jogo/              <- projeto da Godot
    ├── cenas/
    ├── scripts/
    ├── assets/
    └── project.godot
```
