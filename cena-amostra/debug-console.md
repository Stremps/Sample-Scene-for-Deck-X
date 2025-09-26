---
layout: default
title: "Debug Console"
parent: "Cena de amostra"
nav_order: 7
description: "Painel de depuração exibido dentro do HMD; implementação com ConsoleToText.cs e VRDebug.cs."
---

## Objetivo
Esta estação adiciona um **console de debug** visível dentro do HMD, permitindo acompanhar mensagens de log sem precisar remover o dispositivo para verificar o Console do Unity. A solução combina dois scripts: **ConsoleToText.cs**, responsável por redirecionar as mensagens, e **VRDebug.cs**, que controla a ativação da interface no espaço da cena.

<p align="center">
  <img src="{{ '/assets/img/cena-amostra/debug.png' | relative_url }}" alt="Debug Console — painel de logs dentro do HMD" />
</p>

## Funcionamento
- **ConsoleToText.cs** intercepta os eventos `Application.logMessageReceived` e renderiza o texto em um componente **TextMeshProUGUI**. Cada nova mensagem aparece no topo, mantendo o histórico abaixo. Opcionalmente, o log pode ser limpo ao desabilitar o objeto.
- **VRDebug.cs** gerencia a ativação do painel de debug por meio de uma **Input Action** configurada no **Input System**. O painel (`UIDebug`) pode ser alternado entre ativo/inativo. Quando reativado, reposiciona-se e reorienta-se de acordo com o **UIAnchor**, garantindo legibilidade no campo de visão.

## Aplicações em RA
Em cenários de **AR optical see-through** (como o Deck X), este console facilita o **desenvolvimento iterativo**: o programador pode verificar **erros, avisos e logs** diretamente no headset, sem alternar entre o dispositivo e o Editor. Isso reduz interrupções no fluxo de testes e acelera ajustes de scripts, interações e configurações.

## Componentes-chave
- **ConsoleToText.cs**: captura mensagens de log (`Debug.Log`, `Debug.Warning`, `Debug.Error`) e exibe em UI.  
- **VRDebug.cs**: alterna a visibilidade e alinha o painel de logs no espaço, ancorado em um objeto de referência (`UIAnchor`).  
- **UIDebug (GameObject)**: painel de UI com componente de texto (TextMeshProUGUI).  
- **UIAnchor (GameObject)**: referência espacial para posicionar e orientar o painel de debug.

## Como experimentar
1. Inicie a cena; o painel de debug (`UIDebug`) deve aparecer ativo.  
2. Interaja com outras estações; observe que mensagens de `Debug.Log` são exibidas diretamente no painel.  
3. Use a **Input Action** configurada (ex.: botão no teclado/controlador) para ocultar e reexibir o painel.  
4. Ao reexibir, note o reposicionamento/alinhamento automático com base no `UIAnchor`.

## Parâmetros para explorar
- **ClearLogOnDisable** (`ConsoleToText.cs`): define se o log é apagado ao desativar o painel.  
- **Posição/orientação do UIAnchor**: ajusta local e ângulo padrão do painel de debug.  
- **InputActionReference** (`VRDebug.cs`): escolha qual botão/gesto alterna a visibilidade do console.

Leitura recomendada  
- [Unity Manual — Debugging](https://docs.unity3d.com/Manual/ManagedCodeDebugging.html)  
- [Unity Scripting API — Application.logMessageReceived](https://docs.unity3d.com/ScriptReference/Application-logMessageReceived.html)  
- [Unity Input System — Manual](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.7/manual/index.html)  
- [TextMeshPro — Manual](https://docs.unity3d.com/Packages/com.unity.textmeshpro@3.0/manual/index.html)
