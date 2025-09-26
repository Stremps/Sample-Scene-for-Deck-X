---
layout: default
title: "Cena de amostra"
nav_order: 5
has_children: true
description: "Panorama da cena de amostra: propósito, conceitos básicos e mapa das estações para exploração prática."
---

## Propósito
Esta cena funciona como um **laboratório guiado** para experimentar padrões essenciais de interação em XR no contexto do **Deck X** (HMD *optical see-through*). O objetivo é permitir observação, comparação e validação de comportamentos sem exigir configuração extensa. A cena foi construída no **Unity**, utilizando os pacotes **XR Interaction Toolkit (2.5.4)** e **XR Hands**; **scripts adicionais** foram criados apenas para enriquecer a visualização e a ergonomia de testes, sem introduzir novas funcionalidades XR proprietárias. Quando um exemplo depender de lógica própria, a página indicará o script correspondente e a seção **[Scripts utilitários](../scripts/)**.

<p align="center">
  <img src="{{ '/assets/img/cena-amostra/panorama.png' | relative_url }}" alt="Panorama das estações da cena de amostra" />
</p>

## Como explorar localmente
Para abrir a cena no Editor e executar os exemplos, **siga o passo-a-passo da seção Instalação**, que explica como **clonar o repositório**, a **versão recomendada do Unity** e demais preparos (OpenXR e Leap Motion):  
**[Instalação e configuração](../instalacao/)**

## Conceitos de referência
Nesta documentação, os termos são usados de forma objetiva:
- **Interação**: o conjunto de ações e respostas da interface que permitem realizar tarefas (por exemplo, apontar, selecionar, pegar, soltar, “poking”, “gaze”).  
- **Interface**: a camada visível/auditiva de controle e feedback (controles de UI, indicadores em mundo, estados visuais).  
- **Navegação**: mecanismos que mantêm **orientação** e **deslocamento** do usuário no espaço de tarefas (por exemplo, alternar entre alcance direto e *raycast*, ou usar *gaze* quando um alvo está fora de alcance).

Para aprofundamento teórico e boas práticas, consulte os materiais em **Leitura recomendada** ao final desta página.

## Mapa das estações
A cena organiza exemplos em estações independentes. Cada página explica objetivo, componentes relevantes e parâmetros sugeridos de exploração.

- **[Hands (Gestures & Visualizer)](./hands)** — gestos detectáveis com XR Hands e personalização visual das mãos virtuais.
- **[UI & Poke](./ui-poke)** — UI com **Poke** (e compatível com **Raycast**) em botões, *toggle*, *slider*, *dropdown* e exemplo de manipulação por toque.
- **[Manipulation](./manipulation)** — `XR Grab Interactable` com contato direto e *raycast*, *attach points*, ajustes dinâmicos e *resize*.
- **[Socket Interactor](./socket-interactor)** — comparação entre socket **específico** (filtrado) e **geral**.
- **[Gaze Interactable Objects](./gaze-objects)** — *hover*, seleção temporizada e *auto-deselect* por gaze.
- **[Movement Types](./movement-types)** — diferenças práticas entre **Kinematic**, **Instantaneous** e **Velocity Tracked**.
- **[Debug Console](./debug-console)** — painel de logs dentro do HMD para depuração sem sair da experiência.

## Leitura recomendada
> Fontes para aprofundar conceitos e boas práticas de **interface**, **interação** e **navegação** em XR, além das bases usadas na implementação desta cena.

- **[Interaction fundamentals (Mixed Reality)](https://learn.microsoft.com/en-us/windows/mixed-reality/design/interaction-fundamentals)** — princípios de modelos de interação (mãos, *gaze*, combinações)  
- **[Gaze & commit](https://learn.microsoft.com/en-us/windows/mixed-reality/design/gaze-and-commit) / [Gaze & dwell](https://learn.microsoft.com/en-us/windows/mixed-reality/design/gaze-and-dwell) (Mixed Reality)** — quando e como empregar *gaze* como mecanismo de entrada  
- **XR Interaction Toolkit 2.5.4 (Unity)** — [visão geral](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/) e [general setup](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/general-setup.html) 
- **[XR Hands (Unity)](https://docs.unity3d.com/Packages/com.unity.xr.hands@1.4/)** — acesso a dados de rastreamento das mãos e provedores  