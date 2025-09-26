---
layout: default
title: "Manipulation"
parent: "Cena de amostra"
nav_order: 3
description: "Manipulação de objetos com XR Grab Interactable usando Direct Interactor e Ray Interactor; attach points, dinâmica e resize."
---

## Objetivo
Esta estação demonstra **manipulação de objetos** com o **XR Interaction Toolkit 2.5.4**, comparando **contato direto (Direct Interactor)** e **alcance à distância (Ray Interactor)** no mesmo conjunto de alvos. Também inclui exemplos com **attach points**, ajustes de **dinâmica/física** e **resize/duas mãos** para observar como cada opção afeta a sensação de controle.


<p align="center">
  <img src="{{ '/assets/img/cena-amostra/manipulation.png' | relative_url }}" alt="Manipulation — detalhe de alvos e componentes" />
</p>

## Direct vs. Ray — quando usar cada um
**Direct Interactor (contato próximo)**  
Interações feitas “com a mão no objeto”. Em AR **optical see-through** (Deck X), favorece **propriocepção** e leitura intuitiva de peso/posição, funcionando bem em tarefas de **pegar, posicionar, ajustar finamente** e em controles in-world. A percepção de precisão costuma ser maior em curtas distâncias e em alvos com boa ancoragem visual.

**Ray Interactor (à distância)**  
Permite **alcançar** objetos fora do volume de toque confortável, atrás de outros elementos ou em áreas estreitas. É útil para **selecionar, puxar, alinhar** e iniciar manipulações quando o acesso direto está obstruído. Em AR, o ray ajuda a **reduzir movimentos amplos do braço**, melhora a ergonomia e facilita operar objetos pequenos ou distribuídos no espaço.

> Em muitas aplicações XR, ambos coexistem: **Direct** para ações precisas e de curta distância; **Ray** para seleção e pré-posicionamento à distância, antes de refinar com contato.

## Componentes-chave
**XR Grab Interactable** (alvo manipulável) • **XR Direct Interactor** (contato) • **XR Ray Interactor** (distância) • **Attach Transform** (ponto de acoplamento) • **Interaction Layer Masks** (filtragem de quem pode pegar o quê).  
Recursos adicionais exemplificados: **manipulação a duas mãos/resize** (quando habilitado) e parâmetros de **dinâmica** (acoplamento, soltura, *smoothing*).  
> Observação. Ajustes detalhados de **Movement Type** (Kinematic/Instantaneous/Velocity Tracked) são explorados na estação **[Movement Types](./movement-types)**.

## Como experimentar
1. **Contato direto**: agarre um objeto com a mão (Direct), mova e solte. Observe a aderência ao ponto de contato e a resposta ao soltar.  
2. **A distância**: selecione o mesmo objeto com o **Ray** e agarre mantendo o gatilho. Compare suavidade e controle ao transladar/rotacionar.  
3. **Attach points**: ative objetos com *Attach Transform* distinto (ex.: pegadas centradas vs. laterais) e avalie como o acoplamento muda o pivô de manipulação.  
4. **Dinâmica e resize**: teste o objeto configurado para **duas mãos/resize** (quando disponível) e verifique o comportamento ao variar a distância entre as mãos; experimente soltar com movimento rápido para notar diferença de *throwing*.

## Parâmetros para explorar
- **Attach Transform**: posição/rotação do acoplamento; influencia pivô e conforto.  
- **Interaction Layer Masks**: restrinja quais interatores podem pegar cada alvo.  
- **Smoothing / Ease-in/out**: transição ao acoplar; reduz saltos bruscos.  
- **Throw On Detach / Velocity settings**: controla impulso ao soltar.  
- **(Opcional) Duas mãos/resize**: habilite conforme a variante do exemplo ou script utilitário.

Leitura recomendada  
- [XR Interaction Toolkit 2.5 — Índice](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/index.html)  
- [XR Interaction Toolkit 2.5 — Samples](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/manual/samples.html)  
- [API — XR Grab Interactable (2.5)](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.5/api/UnityEngine.XR.Interaction.Toolkit.XRGrabInteractable.html)
