---
layout: default
title: "Ferramentas e plataformas"
nav_order: 3
has_children: true
description: "Panorama das tecnologias de software e hardware utilizadas na cena de amostra, com encaminhamento para leitura detalhada e páginas de instalação."
---

Esta seção apresenta, em nível introdutório, as tecnologias de **software** e **hardware** empregadas na cena de amostra. O objetivo é situar o leitor antes dos procedimentos de instalação e dos guias práticos, destacando o papel de cada ferramenta no projeto e apontando para as páginas específicas quando houver necessidade de configuração.

O escopo aqui cobre **contexto, propósito e termos básicos**. Passos operacionais, configurações detalhadas e solução de problemas permanecem nas seções adequadas do site. A ordem de leitura sugerida é: Unity → XR Interaction Toolkit (2.5.4) → OpenXR → Deck X → Leap Motion. Para executar tarefas, consulte **[Instalação e configuração](../instalacao/)**.

---

## Panorama

- **[Unity](./unity)** — IDE base para compor e validar a cena no Editor, com *Play Mode*, pipeline de *build* e gestão de dependências via Package Manager. Introduz conceitos essenciais (Projeto, Cena, GameObject, Componentes, Prefabs) e como eles aparecem nesta documentação.

- **[XR Interaction Toolkit 2.5.4](./xr-interaction-toolkit)** — Conjunto de componentes para interações em XR (seleção, manipulação, UI, locomoção). Apresenta noções de **XR Origin**, **Interactors/Interactables**, camadas de interação e uso do **XR Device Simulator** para testes no Editor.

- **[OpenXR](./openxr)** — Especificação aberta do Khronos que padroniza a interface entre aplicações XR e *runtimes*. Explica o princípio de um único caminho de integração e os benefícios de compatibilidade no Unity por meio do **OpenXR Plugin**.

- **[Deck X (hardware)](./deckx-hardware)** — Variante do ecossistema **Project North Star** (optical see-through) mantida pela comunidade Combine Reality, com diferenciais de integração e canais de participação (Discord).

- **[Leap Motion (hardware)](./leapmotion-hardware)** — Sensor de **rastreamento de mãos** utilizado como entrada principal de interação na cena, com nota sobre habilitação do perfil correspondente no **OpenXR** para reconhecimento do input manual no Unity.

---

## Quando consultar a documentação oficial
Cada página desta seção oferece um bloco **Leitura recomendada** com as fontes primárias (manuais oficiais, portais e APIs). Esse material complementa o site com detalhes que evoluem com as versões das ferramentas. A proposta desta documentação é **contextualizar e encaminhar**: sempre que houver conteúdo mais completo mantido pelos autores das tecnologias, o leitor será direcionado para lá.

---

## Próximos passos
- Para executar tarefas: **[Instalação e configuração](../instalacao/)** (versão do Editor, módulos, OpenXR e Leap Motion).  
- Para experimentar a experiência: **[Cena de amostra](../cena-amostra/)** (Interface, Navegação, Interação).  
- Para utilidades do projeto: **[Scripts utilitários](../scripts/)**.
