---
layout: default
title: "OpenXR"
parent: "Ferramentas e plataformas"
nav_order: 3
---

## Visão geral

<p align="center">
  <img src="{{ '/assets/img/ferramentas/openxr.jpg' | relative_url }}" alt="Leap Motion Controller — visão geral" width="400"/>
</p>

**OpenXR** é uma especificação aberta, mantida pelo Khronos Group, que padroniza a interface entre aplicações XR e os *runtimes* dos dispositivos/plataformas. Em termos práticos, fornece um único conjunto de APIs para VR/AR, reduzindo a fragmentação e facilitando a manutenção do código. Para uma descrição completa, recomenda-se consultar a documentação oficial.

## Princípio e benefícios
O princípio central é **um caminho único de integração**: a aplicação conversa com o *runtime* por meio de uma API comum, em vez de múltiplos SDKs específicos de cada fabricante. Isso melhora a compatibilidade entre diferentes contextos e dispositivos **sem necessidade de camadas adicionais de abstração** na aplicação. Recursos específicos de hardware continuam possíveis via **extensões** do OpenXR, preservando o núcleo padronizado.

## Uso com Unity (contexto deste projeto)
No Unity, o suporte ocorre via **OpenXR Plugin** (Package Manager) e **XR Plug-in Management** (Project Settings). A seleção de *features* e perfis/extensões deve acompanhar as necessidades do dispositivo-alvo. Os passos de ativação e validação estão detalhados nas seções de Instalação.

Leitura recomendada  
- [Portal oficial do OpenXR (Khronos)](https://www.khronos.org/OpenXR)  
- [Guia do plugin OpenXR para Unity](https://docs.unity3d.com/Packages/com.unity.xr.openxr@1.15/manual/index.html)
