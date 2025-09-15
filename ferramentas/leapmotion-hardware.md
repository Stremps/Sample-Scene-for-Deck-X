---
layout: default
title: "Leap Motion (hardware)"
parent: "Ferramentas e plataformas"
nav_order: 5
description: "Sensor de rastreamento de mãos utilizado como entrada principal de interação; relação com Unity, OpenXR e o Deck X."
---

## Visão geral
**Leap Motion** é um sensor de rastreamento de mãos em tempo real, capaz de estimar posição e orientação de mãos e dedos para produzir gestos e **interações manuais** naturais em XR. Em experiências de realidade aumentada, atua como fonte de **input** sem controladores físicos, favorecendo manipulação direta de elementos virtuais.

<p align="center">
  <img src="{{ '/assets/img/ferramentas/LeapMotionController.jpg' | relative_url }}" alt="Leap Motion Controller — visão geral" width="400"/>
</p>


## Papel na aplicação (contexto Deck X)
No contexto da cena de amostra para o **Deck X** (HMD optical see-through), o Leap Motion opera como **modalidade primária de entrada**: deteta as mãos do usuário e fornece eventos para **seleção, ativação e manipulação** de objetos virtuais no campo de visão do headset. O comportamento percebido depende de fatores como **posicionamento do sensor na estrutura do HMD**, **alinhamento com o volume de trabalho** à frente do usuário e **condições de iluminação** do ambiente. Recomenda-se validar o enquadramento das mãos no Editor antes de realizar *builds*.

<p align="center">
  <img src="{{ '/assets/img/ferramentas/LeapMotionArOvelay.jpg' | relative_url }}" alt="Leap Motion Controller — visão geral" width="500"/>
</p>

## Uso no Unity e relação com OpenXR
A integração ocorre no Unity por meio do pacote do fornecedor e/ou de recursos de **OpenXR Hand Tracking**. Para que o input de mãos seja reconhecido, é necessário **habilitar o recurso/perfil correspondente no OpenXR** (*Project Settings → XR Plug-in Management → OpenXR*) e importar os componentes do fornecedor quando aplicável. O detalhamento dos passos de importação, habilitação e validação está em:  
**Instalação e configuração → [Leap Motion no Unity](../instalacao/leapmotion-unity)**.

Leitura recomendada  
- [Documentação do Leap Motion / Ultraleap](https://docs.ultraleap.com/)
