# Plano de estudo

**Ritmo:** 2 horas por dia.
**Foco atual:** aprender a programar em GDScript na Godot 4. Arte fica para depois; até lá, assets gratuitos prontos.

As durações são estimativas. Só avance de fase quando o "pronto quando" estiver cumprido, mesmo que leve mais dias.

## Como usar as 2 horas

| Tempo | Atividade |
|---|---|
| 15 min | Reler o que fez ontem e rodar o projeto |
| 30 min | Estudar o conteúdo novo do dia (ler ou assistir) |
| 60 min | Praticar: digitar o código, mudar valores, quebrar e consertar |
| 15 min | Anotar o que aprendeu e as dúvidas, e fazer o commit no Git |

Regra principal: **digite o código, não copie e cole**. E depois de cada tutorial, mude alguma coisa por conta própria.

## Fase 0: Preparação (1 dia)

- [ ] Baixar a Godot 4 estável (versão padrão, não a ".NET") em godotengine.org
- [ ] Instalar o Git e criar conta no GitHub
- [ ] Criar um projeto de teste na Godot e rodar uma cena vazia
- [ ] Ler o `guia-inicial.md` desta pasta

**Pronto quando:** a Godot abre, um projeto roda e o primeiro commit existe.

## Fase 1: GDScript e o editor (cerca de 2 semanas)

Objetivo: entender a linguagem e como a Godot pensa (nós, cenas, sinais).

- [ ] Dias 1–5: curso gratuito "Learn GDScript From Zero" (GDQuest, roda no navegador)
- [ ] Dias 6–8: documentação oficial, seção "Getting started > Step by step" (nós, cenas, scripts, sinais)
- [ ] Dias 9–10: exercícios próprios, sem tutorial:
  - [ ] Um sprite que se move com as setas
  - [ ] Um contador na tela que aumenta ao apertar uma tecla
  - [ ] Um botão que emite um sinal e muda um texto
  - [ ] Uma lista de itens (Array) e um dicionário de quantidades, impressos no console

**Pronto quando:** você escreve, sem consultar, um script que move um nó e reage a um sinal.

## Fase 2: Primeiro jogo completo (cerca de 1 semana)

- [ ] Tutorial oficial "Your first 2D game" (Dodge the Creeps), do início ao fim
- [ ] Três mudanças suas: por exemplo vida extra, inimigo mais rápido com o tempo, tela de recorde

**Pronto quando:** o jogo roda do menu ao game over e tem as suas três mudanças.

## Fase 3: Base do nosso jogo (cerca de 3 semanas)

Aqui começa o projeto de verdade, dentro desta pasta.

- [ ] Personagem com visão de cima andando em 4 direções (`CharacterBody2D`)
- [ ] Animações de andar e parar
- [ ] Mapa com tiles (`TileMapLayer`) usando um pacote gratuito
- [ ] Colisão com paredes, árvores e água
- [ ] Câmera seguindo o personagem
- [ ] Trocar de área (sair de casa, entrar em casa)

**Pronto quando:** dá para andar por um mapa pequeno sem atravessar obstáculos.

## Fase 4: O dia (cerca de 4 semanas)

- [ ] Relógio do jogo e ciclo dia/noite (com a tela escurecendo)
- [ ] Objetos coletáveis no mapa
- [ ] Inventário com slots e interface
- [ ] Crafting simples: recurso vira poção de vida
- [ ] Barra de vida e usar a poção

**Pronto quando:** você coleta, crafta uma poção e a usa, e o dia vira noite.

## Fase 5: A noite (cerca de 4 semanas)

- [ ] Inimigo que persegue o jogador
- [ ] Dano, morte e reinício
- [ ] Ataque do jogador
- [ ] Inimigos só aparecem à noite
- [ ] Experiência por sobreviver e subir de nível

**Pronto quando:** a "primeira versão jogável" do `ideia-do-jogo.md` está completa.

## Fase 6 em diante: Crescer o jogo

A ordem será decidida quando chegarmos lá:

- Salvar e carregar o jogo
- Cidade, NPCs e diálogos
- Missões
- Dinheiro e loja
- Plantio
- Construção da área
- Mais inimigos e o chefão
- Som e música
- Arte própria

## Diário

Uma linha por dia: o que fiz, o que travou.

| Data | O que fiz | Dúvidas |
|---|---|---|
| | | |
