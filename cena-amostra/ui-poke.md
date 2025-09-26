---
layout: default
title: "UI & Poke"
parent: "Cena de amostra"
nav_order: 2
description: "Interface de usuário com Poke (toque direto) e compatível com Raycast; exemplos de botões, toggles, slider, dropdown e manipulação por toque."
---

## Objetivo
Esta estação demonstra **UI acionável por Poke** (toque direto do dedo) e, simultaneamente, **compatível com Raycast**. O objetivo é comparar perto e longe no mesmo conjunto de alvos: **botões**, **toggles**, **slider**, **dropdown** e um exemplo de **manipulação por toque** aplicado a objetos/cores. Os exemplos usam o **XR Interaction Toolkit 2.5.4** e o **XR UI Input Module**; scripts do projeto apenas organizam feedbacks e ações simples.

<p align="center">
  <img src="{{ '/assets/img/cena-amostra/ui-poke.png' | relative_url }}" alt="UI & Poke — visão geral da estação" />
</p>

<div style="
    width: 780px; 
    height: 250px; 
    overflow: hidden; 
    margin: 0 auto; 
    border: 1px solid #333; /* Opcional: para ver o limite do corte */
">
    <img src="{{ '/assets/img/cena-amostra/UI_Socket.png' | relative_url }}" 
         alt="Parte de UI Components" 
         style="display: block; margin: 0 auto;" />
</div>

## Comportamento dos componentes apresentados
- **Botões**: com **Poke**, o evento de “press” ocorre quando o dedo cruza o *press threshold* (com feedback visual de *hover/press*); com **Ray**, o botão responde ao *trigger/confirm* do interactor à distância.  
- **Toggles**: alternam estado ao toque direto ou confirmação via Ray; mantêm indicação de ligado/desligado.  
- **Slider**: com **Poke**, o dedo “agarra” a alça e arrasta; com **Ray**, o cursor seleciona e move a alça mantendo o gatilho pressionado.  
- **Dropdown**: abre por Poke ou Ray; a seleção é feita no item da lista com o mesmo mecanismo.  
- **Poke Manipulation (exemplo)**: tocar nas **barras de cor** altera propriedades de materiais em tempo real (mapeamento 1:1 entre alvo tocado e ação do script/handler).  
- **Ações auxiliares (botões dedicados)**: ex.: *Reset Objects*, *Particles* — servem para validar que os eventos chegam e o estado é atualizado.

## Possibilidades em aplicações de RA
Em **AR optical see-through** (como no Deck X), **painéis ancorados no mundo** com **Poke** oferecem controles naturais para ajustes rápidos (parâmetros, modos, filtros), enquanto o **Raycast** amplia o alcance quando o painel está fora da zona de toque confortável. Combinar ambos melhora **acessibilidade** e **ergonomia**: Poke para precisão e confirmação tátil/visual imediata; Ray para alvos distantes, pequenos ou quando o espaço de trabalho está ocupado. O mesmo padrão se aplica a controles in-world (ex.: botões em dispositivos virtuais, seletores de cor/estado, janelas arrastáveis) sem exigir controladores físicos.

## Componentes-chave
**XR Poke Interactor** (entrada por toque próximo) • **XR Ray Interactor** (interação à distância) • **XR Simple/Grab Interactable** quando a UI/objeto é 3D • **XR UI Input Module** (ponte entre XR e eventos de UI) • **Interaction Layer Masks** para isolar o que cada interactor pode acionar.

## Como experimentar
1. Inicie a cena e **toque** nos controles com o dedo (Poke): pressione botões, alterne *toggles*, arraste o *slider*, abra o *dropdown*.  
2. Repita as mesmas ações com o **Ray Interactor** para comparar comportamento e feedback.  
3. Use o painel de **Poke Manipulation** para alterar cores/estados e observar o efeito imediato na cena.  
4. Caso um alvo não responda, verifique **Layer Masks** e o alinhamento do interactor (distância/normal de toque no Poke).

## Parâmetros para explorar
- **Poke**: *press threshold*, *contact offset*, tamanho do *poke volume*, *tween/smoothing*.  
- **Ray**: *max distance*, retículo/linha, gatilho de seleção.  
- **UI**: mapeamentos do **XR UI Input Module** e **Interaction Layer Masks**.

Leitura recomendada  
- [XR Interaction Toolkit 2.5 — Índice](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/index.html)  
- [XR Interaction Toolkit 2.5 — Samples](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/samples.html)  
- [UI (uGUI) — Manual do Unity](https://docs.unity3d.com/Manual/UISystem.html)
