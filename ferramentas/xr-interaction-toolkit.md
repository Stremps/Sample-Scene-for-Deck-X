---
layout: default
title: "XR Interaction Toolkit"
parent: "Ferramentas e plataformas"
nav_order: 2
---

## Visão geral
O **XR Interaction Toolkit (XRIT)** é um conjunto de componentes para criar interações em XR (seleção, manipulação, UI, locomoção) diretamente no Unity, reduzindo a necessidade de código de baixo nível. A versão adotada neste projeto é **2.5.4**. O XRIT não tem escopo limitado a um tipo de produto: pode ser aplicado a protótipos, aplicações educacionais, industriais ou experiências imersivas completas.

## Elementos fundamentais
Para dar apoio à leitura das demais páginas, seguem conceitos-chave usados pelo XRIT. 
- **XR Origin**: rig que representa câmera e origem do usuário na cena; 
- **Interactors**: objetos que iniciam interações (ex.: *Ray Interactor* para apontar à distância; *Direct Interactor* para contato próximo); 
- **Interactables**: alvos de interação (ex.: *XR Grab Interactable* para agarrar/soltar, *XR Simple Interactable* para cliques/ativação);
- **Locomotion System**: provê provedores de movimento/rotação (teleporte, movimentação contínua, giro). 
- **Interaction Layer Masks**: filtros que definem quais *interactors* podem agir sobre quais *interactables*;
- **XR Device Simulator** (opcional): simula entradas de dispositivo no Editor para testes rápidos.

## Integração mínima
A instalação ocorre via **Package Manager** (página *Unity e módulos* detalha pré-requisitos). Após instalar, adicionar um **XR Origin** à cena, configurar *interactors* conforme a necessidade (raio ou direto) e marcar os objetos alvo com componentes *interactable*. Em projetos que utilizam **OpenXR**, assegurar que o *XR Plug-in Management* esteja habilitado e que os perfis/extensões necessários estejam selecionados nas configurações correspondentes. Ajustes de camadas de interação e de entrada devem ser validados no Editor antes dos *builds*.

Leitura recomendada  
- [Documentação do XR Interaction Toolkit 2.5](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/index.html)  
- [Samples do XR Interaction Toolkit 2.5](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/samples.html)  
- [API do pacote (2.5)](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/api/)
