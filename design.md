---
version: alpha
name: Core Design System
description: Linguagem visual e regras de uso compartilhadas pelos produtos Web e App.
omitted:
  - Elevation & Depth
  - Shapes
---

# Core Design System

## Overview

Este é o documento consolidado e autocontido do Core Design System. Use-o ao fornecer contexto para uma LLM ou para qualquer pessoa que precise tomar decisões de interface sem consultar os documentos internos do repositório.

O sistema possui duas bibliotecas de componentes:

- **Core Web:** componentes e padrões para produtos web.
- **Core App:** componentes e padrões para aplicativos móveis.

Elas compartilham identidade de marca, Global Tokens, Alias Tokens, assets, tipografia e princípios de experiência. Componentes, navegação, comportamento e composição podem ser específicos da plataforma.

### Princípios globais de design

#### Simples

Reduzimos esforço, ruído e escolhas desnecessárias. Cada tela prioriza a tarefa principal, apresenta informação em ordem compreensível e revela complexidade apenas quando necessária.

- Prefira o caminho mais direto para concluir uma tarefa.
- Use linguagem clara, rótulos específicos e ações reconhecíveis.
- Agrupe informações relacionadas e elimine elementos sem função.

#### Moderno

Expressamos tecnologia por clareza, precisão, fluidez e qualidade de acabamento — não por decoração ou novidade.

- Use componentes, tokens e padrões consistentes para criar confiança.
- Faça estados, carregamentos e transições parecerem intencionais e contínuos.
- Adote novos padrões apenas quando melhorarem compreensão, eficiência ou acessibilidade.

#### Universal

Projetamos para diferentes pessoas, habilidades, dispositivos, contextos, idiomas e níveis de familiaridade digital.

- Ofereça mais de uma forma de perceber e operar informações e controles.
- Não presuma visão, precisão motora, conexão estável, contexto silencioso ou conhecimento prévio.
- Preserve tarefa e significado quando a interface for ampliada, traduzida, reduzida ou usada com tecnologia assistiva.

### Fontes de verdade

- [Biblioteca de tokens](https://www.figma.com/design/ZPWfhmidgyfkok9RYa6QWE/Design-Tokens)
- [Biblioteca de assets](https://www.figma.com/design/fu1sRTGOuDJj2ZLkV8lSX1/Assets?node-id=209-36)
- [Biblioteca Core Web](https://www.figma.com/design/emMSpxSdN92klss1Vh1ou6/Core-Web?node-id=1-8)
- [Biblioteca Core App](https://www.figma.com/design/RXrjdZA9A3xqRGaUr2U3Ek/SB-Core-App?node-id=53-4420&p=f&t=DvbzE2OsMGjtGWvL-0)
- [SB-Mural](https://www.figma.com/design/7R9SXfp0vhVqh8hSBtpQRr/SB-Mural?node-id=22-5108)

Em caso de conflito, aplique esta prioridade: tokens publicados → componente publicado da plataforma → este documento → página correspondente no Mural → especificação da tela.

## Colors

Os valores exatos são definidos na Biblioteca de Tokens. Use os nomes semânticos abaixo; não invente cores, opacidades ou variações locais quando um token publicado atender à intenção.

- **Global Tokens:** valores de fundação, nos modos Value, Aurora e Floqui.
- **Alias Tokens:** intenção semântica, nos modos Light, Dark, Aurora e Floqui.

Prefira Alias Tokens, como action/primary/bg, text color/heading, surface/bg base, selected/border e negative/label. Use Global Tokens diretamente apenas quando não houver alias adequado.

Aurora e Floqui são modos do mesmo sistema, não sistemas independentes. No frame raiz, Global Tokens e Alias Tokens devem apontar para o modo da mesma marca.

Use cor para reforçar significado, nunca como único indicador de estado. Estados de sucesso, erro, seleção, aviso ou indisponibilidade também precisam de texto, ícone, padrão ou outro sinal compreensível.

## Typography

Use os estilos semânticos publicados. Não sobrescreva manualmente família, tamanho, peso, espaçamento ou line-height.

- **Heading XL:** título principal de página, fluxo ou tarefa; use uma vez por área principal.
- **Heading LG:** título de seção principal sob um Heading XL.
- **Heading MD:** título de seção, card, painel ou etapa.
- **Heading SM:** título de agrupamento local.
- **Heading XS:** título de subgrupo compacto.
- **Paragraph:** conteúdo principal, explicação e orientação em sequência.
- **Description:** contexto breve, metadado e informação secundária.

Todo texto autoral fora de uma instância de componente deve receber um desses estilos. Cor aplicada isoladamente não substitui um estilo tipográfico.

## Layout

### Regras compartilhadas

Use variáveis publicadas em gap, padding, raio, fundo e borda. Um valor digitado manualmente, mesmo que visualmente igual ao token, não conta como aplicação do sistema.

Uma boa composição:

- parte da tarefa da pessoa usuária, não do componente disponível;
- torna conteúdo, ação primária e ações secundárias inequívocos;
- mantém contraste e densidade apropriados ao dispositivo;
- prevê carregamento, vazio, erro, sucesso e indisponibilidade quando aplicável;
- preserva contexto, retorno e progresso em fluxos longos.

### Core Web

Use a página Web do SB-Mural como precedente para arquitetura de navegação, hierarquia, desktop e responsividade. Para área logada desktop, o precedente é a composição Home área logada: navegação global superior, painel de abertura, indicadores e seções de acompanhamento.

Projete reflow e zoom sem perda de informação ou tarefa. Todo fluxo deve funcionar por teclado, com foco visível, ordem de foco lógica e foco não coberto por cabeçalho fixo, modal ou outro conteúdo.

### Core App

Use a página App do SB-Mural como precedente para hierarquia, densidade, estados e transições mobile.

- Considere safe areas, teclado virtual e zonas de toque desde o início.
- Priorize uma tarefa principal por tela.
- Defina comportamento para conteúdo longo, rolagem, orientação, offline, carregamento, vazio e erro.
- Use navegação, sheets, drawers e tabs somente nas variantes publicadas na Core App.

## Components

### Regras comuns

Use componentes públicos e suas variantes publicadas. Itens iniciados por ponto são internos e não devem ser inseridos diretamente em telas. Preserve propriedades, tokens e estilos das instâncias.

Ícones em ações devem usar Button Icon; quando o significado não for inequívoco, complemente com Tooltip. Use Brand para logos e identidade de marca, nunca arquivos soltos quando o componente existir.

### Core Web

#### Ações

- **Button:** executa ação no contexto atual; não use para navegação.
- **Button Icon:** ação por ícone em espaço reduzido; não use para ações primárias ou ambíguas.
- **Link Icon:** navegação ou ação textual de baixa hierarquia; não use para operação local principal.

#### Conteúdo, identidade e dados

- **Accordion:** revela conteúdo complementar; não esconda conteúdo essencial.
- **Brand:** exibe identidade institucional; não é ornamento ou avatar.
- **Avatar:** representa pessoa ou perfil; não use para logo ou ação.
- **Currency e Sale Currency:** exibem valores monetários; não capturam valor.
- **Icon:** representa conceito visual; ícone isolado não é controle interativo.
- **Image:** reserva mídia em proporção previsível; não use para avatar ou logo.
- **Badge:** indica contador ou status numérico sobre outro elemento.
- **Tag:** classifica status ou categoria por texto curto; não é interativa.

#### Containers e overlays

- **Card:** agrupa conteúdo relacionado.
- **Clickable Card:** transforma toda a superfície em uma única ação; não use quando houver várias ações internas.
- **Selectable Card:** permite escolha visualmente rica; prefira Radio Button ou Checkbox quando o controle compacto atender.
- **Popover:** conteúdo complementar ancorado; não é menu, tooltip ou feedback.
- **Popover Menu:** lista contextual de ações; seus subcomponentes iniciados por ponto são internos.
- **Tooltip:** explicação breve; nunca contém informação essencial.

#### Formulários, navegação e feedback

- **Input Text, Password e Text Area:** capturam texto curto, sensível e longo, respectivamente.
- **Input Select:** escolhe um valor de formulário; não use para navegação ou múltipla seleção.
- **Input Date e Date Picker:** o calendário acompanha o campo; Date Picker não é inserido isoladamente.
- **Checkbox:** múltiplas escolhas independentes.
- **Radio Button:** uma escolha em grupo pequeno.
- **Switch:** ativação binária com efeito imediato.
- **Dropdown:** agrupa links ou ações; não substitui Input Select.
- **Progress Stepper:** mostra fluxo sequencial de etapas, não navegação livre.
- **Alert:** situação persistente que pede atenção ou ação.
- **Toast:** resultado breve e temporário de uma ação.
- **Skeleton:** estrutura de carregamento; não é estado permanente.

### Core App

Use apenas componentes publicados na Core App para interação móvel. Documente e use os padrões móveis de navegação, inputs, seleção, sheets, dialogs, alerts e feedback conforme a biblioteca.

Não adapte componentes Web para mobile sem variante publicada. Ao escolher um componente, priorize alcance, legibilidade, toque, contexto de navegação e continuidade de tarefa.

## Do's and Don'ts

### Usabilidade e acessibilidade

O alvo mínimo para produtos Web é WCAG 2.2 nível AA. Os mesmos princípios orientam Core App, complementados pelas diretrizes nativas de cada plataforma.

#### Perceptível

- Texto comum requer contraste de pelo menos 4,5:1; texto grande, 3:1.
- Imagens informativas precisam de alternativa textual equivalente; decoração não deve gerar ruído para leitor de tela.
- Suporte aumento de texto, zoom e reflow sem perda de conteúdo ou tarefa.
- Não dependa exclusivamente de cor, posição, forma ou som para comunicar instrução ou estado.

#### Operável

- Toda funcionalidade Web deve funcionar por teclado, sem aprisionamento de foco.
- Todo controle precisa de foco visível e de área de toque de pelo menos 24 × 24 px CSS; prefira áreas mais generosas para ações importantes ou isoladas.
- Gestos de arrastar, hover, movimento ou pressionamento longo devem oferecer alternativa simples de toque, clique ou teclado.
- Permita reduzir, pausar ou evitar movimento não essencial; não use flashes que possam provocar desconforto.

#### Compreensível

- Use linguagem direta, títulos descritivos, rótulos consistentes e ações previsíveis.
- Não dispare mudanças inesperadas ao receber foco ou preencher um campo.
- Mostre erro próximo ao campo, explique a correção e preserve valores já preenchidos quando possível.
- Para ações financeiras, legais, destrutivas ou difíceis de desfazer, ofereça revisão, confirmação e correção.
- Apresente estados de carregamento, vazio, sucesso, erro, indisponibilidade e offline quando relevantes.

#### Robusto

- Controles interativos devem expor nome, função, estado e valor para tecnologia assistiva.
- Prefira elementos semânticos e padrões nativos a equivalentes customizados.
- Mensagens de status, erro e sucesso devem ser anunciáveis sem deslocar inesperadamente o foco.

### Gate de entrega

Antes de concluir uma tela:

1. Confirme os modos de Global Tokens e Alias Tokens no frame raiz.
2. Verifique vínculo de variável em todo fundo, borda, gap, padding e raio autoral.
3. Verifique estilo semântico em todo texto autoral.
4. Confirme instâncias e variantes públicas adequadas.
5. Teste tarefa, teclado, foco, contraste, estados e responsividade.
6. Registre exceções, motivo e plano de correção.

### Manutenção

Este arquivo é a versão de distribuição. Mantenha as decisões de origem em Foundations, Core Web e Core App e atualize este documento consolidado sempre que uma regra compartilhada ou de plataforma mudar.
