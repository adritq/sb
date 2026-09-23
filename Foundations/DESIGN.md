---
version: alpha
name: Core Foundations
description: Fundamentos compartilhados por Core Web e Core App.
omitted:
  - components
---

# Core Foundations

## Overview

Core Foundations define a linguagem visual e semântica comum às bibliotecas Core Web e Core App. Não descreve componentes de plataforma; descreve as decisões que devem permanecer consistentes entre superfícies.

### Princípios globais de design

Estes princípios orientam decisões quando um token, componente ou precedente não oferece uma resposta clara. Eles valem para Web e App e vão além da expressão visual da marca.

#### Simples

Reduzimos esforço, ruído e escolhas desnecessárias. Cada tela prioriza a tarefa principal, apresenta informação em uma ordem compreensível e revela complexidade apenas quando ela é necessária.

- Prefira o caminho mais direto para concluir uma tarefa.
- Use linguagem clara, rótulos específicos e ações reconhecíveis.
- Agrupe informações relacionadas e elimine elementos sem função.

#### Moderno

Expressamos tecnologia por meio de clareza, precisão, fluidez e qualidade de acabamento — não por decoração ou novidade pela novidade.

- Use componentes, tokens e padrões consistentes para produzir uma experiência confiável.
- Faça estados, carregamentos e transições parecerem intencionais e contínuos.
- Adote novos padrões somente quando melhorarem a compreensão, eficiência ou acessibilidade.

#### Universal

Projetamos para a maior variedade possível de pessoas, contextos, dispositivos, habilidades, idiomas e níveis de familiaridade digital.

- Ofereça mais de uma forma de perceber e operar informações e controles.
- Não presuma visão, precisão motora, conexão estável, contexto silencioso ou conhecimento prévio.
- Preserve a tarefa e o significado quando a interface for ampliada, traduzida, reduzida ou usada com tecnologia assistiva.

### Fontes de verdade

- [Biblioteca de tokens](https://www.figma.com/design/ZPWfhmidgyfkok9RYa6QWE/Design-Tokens)
- [Biblioteca de assets](https://www.figma.com/design/fu1sRTGOuDJj2ZLkV8lSX1/Assets?node-id=209-36)
- [SB-Mural](https://www.figma.com/design/7R9SXfp0vhVqh8hSBtpQRr/SB-Mural?node-id=22-5108)

Os tokens publicados são valores normativos. Para automação futura, sincronize o YAML dos documentos de plataforma a partir do Figma em vez de manter valores duplicados manualmente.

## Colors

- Global Tokens são a fundação, nos modos Value, Aurora e Floqui.
- Alias Tokens comunicam intenção, nos modos Light, Dark, Aurora e Floqui.
- Prefira aliases semânticos, como action/primary/bg, text color/heading, surface/bg base, selected/border e negative/label.

Use Global Tokens diretamente apenas quando não houver alias adequado. No frame raiz, Global Tokens e Alias Tokens devem apontar para o modo da mesma marca.

## Typography

Os estilos Core são semânticos. Use o estilo publicado que corresponde à função do texto, sem sobrescrever família, tamanho, peso ou line-height.

- Heading XL: título principal de página ou tarefa.
- Heading LG, MD, SM e XS: níveis sucessivos de agrupamento.
- Paragraph: conteúdo principal e explicações.
- Description: contexto, metadados e informação secundária.

## Layout

Use variáveis publicadas em gap, padding, raio, fundo e borda. Valor manual, ainda que igual visualmente, não é aplicação do token. Cada plataforma detalha seus grids, safe areas e regras de navegação.

## Elevation & Depth

A definição normativa de superfícies, bordas e elevação pertence aos tokens e componentes publicados. Registre aqui somente decisões compartilhadas que não possam ser expressas por eles.

## Shapes

Use raios, ícones, logos e assets publicados. Brand é a forma padrão de exibir identidade de marca.

## Do's and Don'ts

- Use tokens e estilos publicados; não use valores repetíveis soltos.
- Não use cor como único indicador de estado.
- Todo controle interativo precisa de nome acessível.
- Labels explicam o dado solicitado; placeholder não substitui label.
- Erros devem explicar como corrigir o problema.

### Padrão de qualidade

O objetivo mínimo de acessibilidade para produtos Web é WCAG 2.2 nível AA. Os mesmos princípios devem orientar o Core App, complementados pelas diretrizes nativas de cada plataforma. A validação deve combinar checagens automatizadas com revisão humana de fluxos reais.

### Checklist de usabilidade e acessibilidade

#### Perceptível

- Texto comum deve manter contraste mínimo de 4,5:1; texto grande, 3:1. Elementos de interface e indicadores visuais relevantes também precisam de contraste suficiente.
- Toda imagem informativa precisa de alternativa textual equivalente; imagens decorativas não devem criar ruído para tecnologia assistiva.
- Não use somente posição, cor, forma ou som para comunicar uma instrução ou estado.
- O conteúdo deve suportar zoom, aumento de texto e reflow sem perda de informação ou de tarefa.

#### Operável

- Toda funcionalidade Web deve ser operável por teclado, com ordem de foco lógica, foco visível e sem aprisionamento de foco.
- O elemento focado não pode ficar coberto por cabeçalho fixo, modal, teclado virtual ou outro conteúdo.
- Controles devem ter área de toque de pelo menos 24 × 24 px CSS; para ações importantes ou isoladas, prefira uma área mais generosa.
- Gestos de arrastar, hover, movimento ou pressionamento prolongado precisam ter alternativa simples de toque, clique ou teclado.
- Dê controle para pausar, reduzir ou evitar movimento não essencial; não use flashes que possam provocar desconforto.

#### Compreensível

- Use linguagem direta, títulos descritivos, rótulos consistentes e ação previsível.
- Preserve o contexto e não dispare mudanças inesperadas ao receber foco ou preencher um campo.
- Mostre validação perto do campo, explique como corrigir e mantenha valores já preenchidos quando possível.
- Em fluxos financeiros, legais, destrutivos ou difíceis de desfazer, ofereça revisão, confirmação e possibilidade de correção.
- Mostre estados de carregamento, vazio, sucesso, erro, indisponibilidade e offline quando forem relevantes.

#### Robusto

- Componentes interativos precisam expor nome, função, estado e valor de forma programática.
- Use componentes semânticos e padrões nativos antes de criar equivalentes customizados.
- Mensagens de status, erro e sucesso devem ser anunciáveis por tecnologia assistiva sem deslocar inesperadamente o foco.

### Critérios de revisão antes da entrega

1. A tarefa principal, ação primária e próximo passo estão claros em poucos segundos?
2. O fluxo funciona com teclado, aumento de texto e leitor de tela?
3. Há contraste, foco, estados e mensagens de erro/sucesso suficientes?
4. A tela funciona em dimensões menores, com teclado virtual e em conexão instável quando aplicável?
5. Alguma exceção a token, componente ou acessibilidade foi registrada com motivo e plano de correção?
