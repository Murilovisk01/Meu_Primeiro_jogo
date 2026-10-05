# Ideia do jogo

Documento vivo de design. Organiza o que está em `primeiroContato.md` e cresce conforme o projeto anda.
O `primeiroContato.md` continua sendo o rascunho livre; aqui fica a versão organizada.

## Resumo em uma frase

Jogo 2D de sobrevivência com visão de cima, no clima de Stardew Valley, em que o dia serve para se preparar e a noite para sobreviver.

## O ciclo principal

O jogo gira em dois turnos que se alimentam:

| Turno | O que o jogador faz | Sensação |
|---|---|---|
| **Dia** | Craftar, montar e melhorar sua área, explorar para achar objetos, ganhar experiência | Calma, planejamento |
| **Noite** | Sobreviver, sair para caçar, cumprir missões | Tensão, terror |

O que é feito de dia (poções, equipamentos, defesas) decide o quanto a noite é perigosa.
O que é ganho à noite (experiência, dinheiro, itens raros) abre novas opções para o dia.

## Ambientação

- Mesma linguagem de Stardew Valley: uma cidade, uma fazenda, pessoas com quem interagir.
- À noite o mesmo mundo fica ameaçador: fantasmas, zumbis, bichos.

## Mecânicas

### Dia
- **Crafting**: criar itens a partir de recursos coletados.
- **Construção**: estruturar a própria área.
- **Exploração**: áreas com objetos para coletar.
- **Plantio (secundário)**: poucas sementes, voltadas para utilidade, por exemplo ingredientes de poção de vida.

### Noite
- **Sobrevivência**: inimigos no estilo terror (fantasmas, zumbis, bichos).
- **Caça**: sair atrás de inimigos por recompensa.
- **Missões**: salvar a donzela, levar mantimentos, caçar o chefão.

### Personagem
- **Nível de experiência**: aumenta a vida e os slots de inventário.
- **Dinheiro**: para comprar e trocar.

## Primeira versão jogável (o alvo inicial)

Uma fatia pequena que já mostra o ciclo dia/noite funcionando:

1. Um mapa pequeno com a casa do jogador e uma área para explorar.
2. Personagem que anda, coleta um tipo de recurso e tem barra de vida.
3. Relógio que alterna dia e noite.
4. De dia: craftar uma poção de vida com o recurso coletado.
5. De noite: um tipo de inimigo que persegue e causa dano.
6. Sobreviver até amanhecer dá experiência.

Cidade, NPCs, missões, loja e chefão entram depois que isso estiver divertido.

## Perguntas em aberto

Decisões que ainda precisam ser tomadas. Não precisam de resposta agora.

- **Combate**: o jogador ataca com arma corpo a corpo, à distância, ou só foge e usa armadilhas?
- **Morte**: o que acontece ao morrer à noite? Perde itens, perde o dia, volta para casa?
- **Noite obrigatória?**: o jogador pode ficar em casa em segurança, ou a ameaça vai até ele?
- **Tempo**: quanto dura um dia e uma noite em minutos reais?
- **Mundo**: mapa fixo feito à mão (como Stardew) ou gerado aleatoriamente?
- **História**: por que as noites são perigosas? Existe um objetivo final?
- **Nome do jogo**.

## Ideias soltas

Espaço para anotar qualquer ideia nova antes de decidir se entra no jogo.

-
