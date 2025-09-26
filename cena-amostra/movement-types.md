---
layout: default
title: "Movement Types"
parent: "Cena de amostra"
nav_order: 6
description: "Comparação prática dos modos de movimento do XR Grab Interactable: Kinematic, Instantaneous e Velocity Tracked."
---

## Objetivo
Esta estação compara os **Movement Types** do `XR Grab Interactable` — **Kinematic**, **Instantaneous** e **Velocity Tracked** — no mesmo conjunto de alvos, para observar diferença de sensação, estabilidade e resposta ao soltar. O foco é ajudar a escolher o modo mais adequado ao tipo de tarefa em **AR optical see-through** (Deck X).

<div style="
    width: 780px; 
    height: 350px; 
    overflow: hidden; 
    margin: 20px auto;
    border: 1px solid #333; /* Opcional: para ver o limite do corte */
">
    <img src="{{ '/assets/img/cena-amostra/gaze_movement.png' | relative_url }}" 
         alt="Parte de Socket Interactor" 
         style="
            display: block; 
            position: relative; 
            top: -255px; /* Desloca a imagem 300px para cima */
            margin: 0 auto;
         " />
</div>

## Modos e características
**Kinematic**  
O objeto acompanha o interactor por atualização direta da pose (física limitada). Oferece **controle previsível** e **boa precisão** em ajustes finos, com baixa inércia aparente. Útil para ferramentas, widgets e operações que exigem estabilidade visual.

**Instantaneous**  
Atualiza a pose do objeto de forma imediata a cada frame (teletransporte pequeno e contínuo para a nova pose). Transmite sensação de **resposta muito rápida**, mas pode evidenciar “saltos” em movimentos bruscos ou em taxas de quadro irregulares. Adequado para **UI in-world** e objetos leves.

**Velocity Tracked**  
O objeto segue com **modelo físico** (velocidade e aceleração derivadas do movimento do interactor). Proporciona **inércia** e **lançamento natural** ao soltar (throw). Indicado para objetos que se beneficiam de **feedback físico** (brincáveis, arremessos, simulações).

> Em aplicações XR, é comum combinar: **Kinematic** para precisão e estabilidade perto do usuário; **Velocity Tracked** para sensação “física” e arremesso; **Instantaneous** quando a prioridade é resposta visual imediata em elementos leves.

## Componentes-chave
**XR Grab Interactable** (alvo) • **XR Direct/Ray Interactor** (entrada) • Propriedades do `XR Grab Interactable` relacionadas a movimento (*Movement Type*, *Smoothing*, *Velocity/Angular Velocity Scale*, *Throw On Detach*).  
> Dica. O comportamento também é influenciado por **Attach Transform** (pivô) e por camadas de colisão/física do projeto.

## Como experimentar
1. Pegue o objeto configurado como **Kinematic**; faça microajustes, rotações lentas e solte suavemente. Note a **estabilidade** e a baixa inércia.  
2. Repita com **Instantaneous**; realize movimentos curtos e rápidos. Observe a **imediaticidade** e eventuais “saltos” em trajetórias.  
3. Por fim, use **Velocity Tracked**; mova e **arremesse**. Compare a continuidade do movimento após o **detach** e a **trajetória** no ar.  
4. Teste com **Direct** e **Ray** para perceber diferenças de controle em curta vs. longa distância.

## Parâmetros para explorar
- **Movement Type**: Kinematic / Instantaneous / Velocity Tracked.  
- **Smoothing** (*ease in/out*): transições mais suaves ao acoplar/desacoplar.  
- **Throw On Detach** + **Velocity / Angular Velocity Scale**: intensidade do impulso ao soltar.  
- **Attach Transform**: define pivô de manipulação (conforto e previsibilidade).  
- **Collision/Física**: massa, arrasto e camadas influenciam contato e trajetória.

Leitura recomendada  
- [XR Interaction Toolkit 2.5 — Índice](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/index.html)  
- [API — XR Grab Interactable (2.5)](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/api/UnityEngine.XR.Interaction.Toolkit.XRGrabInteractable.html)  
- [XR Interaction Toolkit 2.5 — Samples](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/samples.html)
