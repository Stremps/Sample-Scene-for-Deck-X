---
layout: default
title: "Gaze Interactable Objects"
parent: "Cena de amostra"
nav_order: 5
description: "Interação por gaze com hover, seleção temporizada (dwell) e auto-deselect; usos práticos em AR optical see-through."
---

## Objetivo
Esta estação demonstra **interação por gaze** em objetos simples, incluindo **hover**, **seleção por dwell** (temporizada) e **auto-deselect**. O exemplo é derivado/adaptado dos *samples* do **XR Interaction Toolkit 2.5.4**, ajustado para observação rápida dos estados visuais e do tempo até seleção.

<div style="
    width: 780px; 
    height: 200px; 
    overflow: hidden; 
    margin: 0 auto; 
    border: 1px solid #333; /* Opcional: para ver o limite do corte */
">
    <img src="{{ '/assets/img/cena-amostra/gaze_movement.png' | relative_url }}" 
         alt="Gaze Interactable Objects — detalhe de estados e retículo" 
         style="display: block; margin: 0 auto;" />
</div>


## Comportamento apresentado
- **Hover por gaze**: ao alinhar o olhar, o alvo indica foco (ex.: realce/halo).  
- **Seleção temporizada (dwell)**: manter o olhar por um período dispara o **Select** sem clique.  
- **Auto-deselect**: ao desviar o olhar, o alvo retorna ao estado neutro após um atraso configurável.  
- **Feedback**: retículo/indicador de progresso sinaliza o tempo restante para seleção.

## Aplicações em RA
Em **AR optical see-through** (Deck X), o gaze é útil quando **as mãos estão ocupadas**, quando se deseja **reduzir gestos** para ações simples (confirmar, avançar, realçar um alvo), ou em **alvos pequenos/distantes**. Combinar **gaze + dwell** com outros métodos (ex.: **gaze + gesto** ou **gaze + ray**) ajuda a evitar o problema do “toque de Midas” (seleções acidentais) e melhora a **ergonomia**: usa-se dwell para ações de baixo risco e um gesto/confirm para ações críticas.

## Componentes-chave
**Gaze Interactor** (fonte de foco pelo olhar) • **Gaze Assisted** (auxílio de seleção) • Alvos com **XR Simple/Grab Interactable** (conforme o tipo de resposta) • **Reticle/Progress** (feedback) • Temporizadores de **dwell** e **auto-deselect**.  

## Como experimentar
1. Entre em Play e **fixe o olhar** em um alvo até aparecer o **hover**.  
2. Mantenha o gaze até o **dwell** completar e observe o **Select** (mudança de estado).  
3. **Desvie o olhar** para notar o **auto-deselect** após o atraso configurado.  
4. Repita em alvos com tempos de dwell diferentes para comparar responsividade e risco de seleção acidental.

## Parâmetros para explorar
- **Dwell time** (tempo para selecionar)  
- **Auto-deselect delay** (tempo para sair do estado selecionado)  
- **Reticle/Progress** (formato, tamanho, visibilidade)  
- **Interaction Layer Masks** (quais objetos respondem ao gaze)

Leitura recomendada  
- [XR Interaction Toolkit 2.5 — Índice](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/index.html)  
- [XR Interaction Toolkit 2.5 — Samples](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/samples.html)
