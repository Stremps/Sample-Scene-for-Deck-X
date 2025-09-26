---
layout: default
title: "Socket Interactor"
parent: "Cena de amostra"
nav_order: 4
description: "Encaixe de objetos em soquetes: comparação entre sockets específicos (filtrados) e sockets gerais; feedback de aceitação e parâmetros de snap."
---

## Objetivo
Esta estação apresenta o **encaixe de objetos** com o **XR Socket Interactor**, contrastando **sockets específicos** (que aceitam apenas certos alvos) e **sockets gerais** (que aceitam qualquer alvo compatível). O foco é observar **feedback de aceitação/rejeição**, comportamento de **snap** e como filtros e camadas determinam o que pode ser acoplado.


<div style="
    width: 780px; 
    height: 350px; 
    overflow: hidden; 
    margin: 20px auto;
    border: 1px solid #333; /* Opcional: para ver o limite do corte */
">
    <img src="{{ '/assets/img/cena-amostra/UI_Socket.png' | relative_url }}" 
         alt="Parte de Socket Interactor" 
         style="
            display: block; 
            position: relative; 
            top: -255px; /* Desloca a imagem 300px para cima */
            margin: 0 auto;
         " />
</div>

## O que este exemplo mostra
- **Socket específico (filtrado)** — aceita apenas objetos que atendem a critérios (camada de interação, tag/filtro, tipo). Ao aproximar um alvo inválido, o socket **rejeita** a seleção (sem snap), exibindo apenas *hover* genérico ou nenhum feedback, conforme sua configuração.  
- **Socket geral** — aceita qualquer **XR Grab Interactable** compatível. Ao entrar no volume do socket, o objeto **encaixa** no **Attach Transform** do soquete e fica **selecionado** por ele, liberando a mão do usuário.  
- **Feedbacks** — diferenciação de *hover* (cor/retículo), “fantasma”/*ghost* opcional do alvo no socket, e mudança de estado ao **Select Enter/Exit**.  
- **Desencaixe** — retirar o objeto puxa-o para a mão (ou volta ao estado anterior), conforme as preferências do socket e do interactor que o remove.

## Aplicações em RA
Em AR **optical see-through**, sockets são úteis para **acoplagem sem ambiguidade**: montagem de componentes, **slots** de inventário ou ferramentas, **estações de docking** (carregar, calibrar, posicionar) e interfaces que exigem **estado discreto** (encaixado / não encaixado). Sockets específicos oferecem **segurança semântica** (apenas a peça certa encaixa), enquanto sockets gerais aceleram **protótipos** e **exploração livre**. A combinação de filtros e *layer masks* ajuda a **guiar a ação do usuário** e reduzir erros de manipulação.

## Componentes-chave
**XR Socket Interactor** (soquete) • **XR Grab Interactable** (alvo) • **Attach Transform** (pivô do snap) • **Interaction Layer Masks** (quais alvos cada socket aceita) • **Filtros** (critérios adicionais de seleção) • **Eventos** *Hover/Select* para acionar feedback visual/sonoro.

## Como experimentar
1. **Aproxime** um objeto do **socket geral** até entrar no volume do soquete; observe o **snap** para o **Attach Transform** e a transferência de seleção para o socket.  
2. Repita com o **socket específico** usando primeiro um objeto **válido** (deverá encaixar) e depois um **inválido** (deverá rejeitar). Compare feedbacks de *hover* e o estado final.  
3. **Remova** o objeto do socket (puxe com a mão ou use o Ray) e note o comportamento de desencaixe (retém orientação? volta ao estado anterior?).  
4. Ajuste a distância/ângulo de aproximação para perceber tolerâncias de encaixe.

## Parâmetros para explorar
- **Interaction Layer Masks**: delimita quais objetos o socket aceita.  
- **Attach Transform**: posição/rotação do pivô de encaixe (conforto e previsibilidade).  
- **Starting Selected Interactable**: opcionalmente iniciar com um objeto já encaixado.  
- **Preferências de Snap / Smoothing**: suavidade na transição ao acoplar/desacoplar.  
- **Filtros adicionais**: aceitar por tag/tipo ou lógica custom (quando aplicável).

Leitura recomendada  
- [XR Interaction Toolkit 2.5 — Índice](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/index.html)  
- [API — XR Socket Interactor (2.5)](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/api/UnityEngine.XR.Interaction.Toolkit.XRSocketInteractor.html)  
- [XR Interaction Toolkit 2.5 — Samples](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/samples.html)
