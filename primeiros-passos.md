---
layout: default
title: Primeiros passos
nav_order: 2
description: Caminho rápido para abrir o projeto no Unity e executar o primeiro teste local.
---

# EM CONSTRUÇÃO!

Esta página conduz o leitor ao primeiro contato com a cena de amostra. O objetivo é **abrir o projeto no Unity e executar um teste local**. Os detalhes finos de instalação e variações por hardware ficam na seção [Instalação e configuração](./instalacao/); a exploração pedagógica da experiência está em [Cena de amostra](./cena-amostra/).

## Pré-requisitos
> Nota. Liste aqui os elementos mínimos para o primeiro teste. Mantenha sucinto e aponte detalhes para “Instalação e configuração”.
- **Software**: Unity (versão recomendada), Unity Hub.  
  _Preencher: versão exata do Unity e módulos obrigatórios._
- **Hardware (opcional para este primeiro teste)**: Deck X, Leap Motion.  
  _Preencher: se o primeiro teste exige ou não o hardware conectado._

Leituras de apoio: [Ferramentas e plataformas](./ferramentas/).

## Obter o projeto
> Escolha uma única forma principal de obtenção (ex.: `git clone`) e cite alternativas se necessário.
- _Preencher: URL do repositório e comando `git clone`._
- _Preencher: instruções para baixar ZIP, caso prefira._

## Abrir no Unity Hub
1. Abrir **Unity Hub** → **Open** → selecionar a pasta do projeto.  
2. Confirmar a **versão do Editor** sugerida pelo Hub.  
3. Aguardar a importação inicial.  
   _Preencher: observações específicas de importação (ex.: TMP resources, URP)._

## Carregar a cena principal
- Caminho da cena: `Assets/.../Scenes/Sample.unity`.  
  _Preencher: caminho real e nome canônico da cena._  
- Abrir a cena e aguardar o carregamento.

## Executar o primeiro teste
1. Pressionar **Play** no Editor.  
2. Observar a tela inicial/overlay de status.  
   _Preencher: qual feedback mínimo o usuário deve ver; logs esperados no Console._

Se houver dependência de OpenXR/Leap Motion para este teste, aponte diretamente para:
- [Configurar OpenXR e perfis](./instalacao/openxr-perfis)  
- [Integrar Leap Motion no Unity](./instalacao/leapmotion-unity)

## Validação rápida
> Liste sinais de que “deu certo” e sintomas comuns de erro.
- **Sucesso**: elementos de UI exibidos, mensagem “Hello Deck X” no Console, FPS estável.  
- **Problemas comuns**: versão do Unity incompatível, pacotes faltando, erro de TMP.  
  Consulte [Solução de problemas](./troubleshooting).

## Próximos passos
- Completar a preparação do ambiente em [Instalação e configuração](./instalacao/).  
- Explorar os três eixos da [Cena de amostra](./cena-amostra/) — Interface, Navegação e Interação.  
- Conhecer as bases do projeto em [Ferramentas e plataformas](./ferramentas/).
