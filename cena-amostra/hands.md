---
layout: default
title: "Hands (Gestures & Visualizer)"
parent: "Cena de amostra"
nav_order: 1
description: "Gestos detectáveis com XR Hands e personalização visual das mãos virtuais na cena de amostra."
---

## Objetivo
Esta estação demonstra **gestos** detectáveis pelo **XR Hands** e oferece **personalização visual** das mãos virtuais (cores/materiais, juntas ou malha completa). Os scripts do projeto aqui servem apenas para facilitar a visualização e o ajuste — não adicionam novas capacidades XR além das fornecidas pelos pacotes. Para conhecer a **lista completa de gestos**, critérios e configurações, recomenda-se **ler a documentação oficial do XR Hands** e explorar os exemplos indicados em *Leitura recomendada*.

<p align="center">
  <img src="{{ '/assets/img/cena-amostra/hands.png' | relative_url }}" alt="XR Hands — demonstração de gestos" />
</p>

## Componentes-chave
**XR Hands** como provedor de entrada de mãos (subsystem/provider).  
**Hand Pose assets** para detecção de posturas (ex.: *fist*, *thumb up*, *point*, *shaka*).  
**Hand Visualizer (script do projeto)** para alternar materiais/cores e a forma de renderização (juntas vs. mão completa).  
**`MaterialColorChange.cs` (script utilitário)**: altera cores/material da mão virtual nesta estação; listado em **[Scripts utilitários](../scripts/)**.

## Como experimentar
1. Inicie a cena no Editor com o hardware preparado (ver **Instalação e configuração**).  
2. Traga as mãos para o volume de rastreamento e observe a **detecção de gestos** na grade.  
3. No painel do **Visualizer**, altere materiais/cores (via `MaterialColorChange.cs`) e troque entre **joints** e **virtual hand** para comparar legibilidade.  
4. Caso algum gesto não acione, ajuste enquadramento e iluminação e repita o teste.

## Parâmetros para explorar
- **Modo de visualização**: juntas vs. malha completa.  
- **Materiais/cores**: contraste confortável no HMD (controlado por `MaterialColorChange.cs`).  
- **Sensibilidade/limiares** (quando expostos pelo provider).

Leitura recomendada  
- [XR Hands — Manual (Unity)](https://docs.unity3d.com/Packages/com.unity.xr.hands@1.4/manual/index.html)  
- [XR Interaction Toolkit 2.5 — Índice](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/index.html)
