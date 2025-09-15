---
layout: default
title: "Unity"
parent: "Ferramentas e plataformas"
nav_order: 1
---

## Visão geral
Unity é um ambiente de desenvolvimento integrado (IDE) para criação de aplicações interativas em 3D/2D. Oferece um Editor visual com execução em tempo real (*Play Mode*), pipeline de *build* para múltiplas plataformas e um sistema oficial de pacotes. Nesta documentação, Unity é a base para compor a cena de amostra, ajustar propriedades e validar o funcionamento antes de gerar *builds*.

## Instalação base
A instalação é composta por **Unity Hub** (gerenciamento de versões e projetos) e **Unity Editor** em versão **LTS** (*Long Term Support — Suporte de Longo Prazo*, foco em estabilidade). Pelo Hub, adicionam-se módulos de *build* conforme a plataforma alvo e seleciona-se a versão indicada na seção de Instalação. Após a instalação, recomenda-se validar o ambiente abrindo um projeto vazio para verificar importação correta e ausência de erros no Console antes de carregar a cena de amostra.

## Conceitos fundamentais
Para dar apoio à leitura das demais páginas, seguem conceitos-chave usados ao longo da documentação. 
- **Projeto**: diretório que reúne cenas, *assets* e configurações do Editor; 
- **Cena (Scene)**: espaço onde objetos e lógica são organizados para formar um estado do aplicativo; 
- **GameObject**: unidade básica presente na cena (câmeras, luzes, UI, objetos interativos); 
- **Componentes**: comportamentos acoplados a GameObjects (renderização, física, scripts); 
- **Prefabs**: modelos reutilizáveis de GameObjects; alterações no prefab podem propagar para suas instâncias; 
- **Package Manager**: gerenciador para instalar e versionar pacotes oficiais do Unity.

## Relação com XR
A integração com XR no Unity ocorre por meio de pacotes. Neste projeto utilizam-se **OpenXR Plugin** (aderência ao padrão OpenXR) e, quando aplicável, **XR Interaction Toolkit** (componentes de interação). Seleção de versões, habilitação e perfis são detalhados nas seções específicas de Ferramentas e Instalação.

Leitura recomendada  
- [Unity Learn — Introdução e primeiros passos](https://unity.com/pt/learn/get-started)  
- [Manual do Unity (LTS sugerida)](https://docs.unity3d.com/2022.3/Documentation/Manual/UnityManual.html)  
- [Unity Hub — Download e gerenciamento](https://unity.com/download)  
- [Package Manager — Interface e fluxo](https://docs.unity3d.com/Manual/upm-ui.html)
