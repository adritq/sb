---
version: alpha
name: Core Web
description: Sistema semântico para interfaces Core Web, com tokens, componentes públicos e regras de composição publicados no Figma.
omitted:
  - Elevation & Depth
  - Shapes
---

# Design System — Core Web

## Overview

Esta é a referência semântica do Design System Core Web: explica **por que**, **quando** e **como** usar os recursos publicados no Figma. O Figma é a fonte visual e normativa de variantes, propriedades e valores; este arquivo documenta as decisões de uso para design, produto e engenharia.

### Fontes de verdade

- [Biblioteca de componentes](https://www.figma.com/design/emMSpxSdN92klss1Vh1ou6/Core-Web?node-id=1-8)
- [Biblioteca de assets](https://www.figma.com/design/fu1sRTGOuDJj2ZLkV8lSX1/Assets?node-id=209-36)
- [Biblioteca de tokens](https://www.figma.com/design/ZPWfhmidgyfkok9RYa6QWE/Design-Tokens)
- [Mural de composições e casos de uso](https://www.figma.com/design/7R9SXfp0vhVqh8hSBtpQRr/SB-Mural?node-id=22-5108)

Em caso de conflito: tokens publicados → componente publicado → este documento → mural de composições → especificação de tela.

### Princípios de uso

1. Comece pela intenção da interface, não pela aparência desejada.
2. Escolha o componente na categoria semântica correta e use apenas propriedades e variantes publicadas.
3. Combine componentes públicos; itens iniciados por `.` são internos e não entram diretamente em telas.
4. Use tokens, nunca valores soltos, para decisões repetíveis.

### Mural de composições

O [SB-Mural](https://www.figma.com/design/7R9SXfp0vhVqh8hSBtpQRr/SB-Mural?node-id=22-5108) é a referência de experiência para combinar componentes, tokens e assets em contextos reais. Ele não substitui as regras semânticas dos componentes.

Use-o para definir hierarquia, combinações de componentes, densidade, responsividade e estados de onboarding, autenticação, busca, formulários, drawers, headers, listas, seleção, navegação e conclusão de tarefa. Use precedentes equivalentes como ponto de partida — referência, não cópia — e adicione ao mural novos casos recorrentes bem resolvidos.

Uma boa composição parte da tarefa da pessoa usuária, prioriza conteúdo e ações de forma inequívoca, prevê estados relevantes (carregamento, vazio, erro, sucesso e indisponibilidade), preserva contraste e densidade adequados e mantém contexto, retorno e progresso ao longo do fluxo. Sempre que o mural contiver imagens, crie imagens alinhadas ao guia de marca do tema.

## Colors

Os valores de cor são normativos na [Biblioteca de tokens](https://www.figma.com/design/ZPWfhmidgyfkok9RYa6QWE/Design-Tokens); não os replique como valores locais neste arquivo. Quando valores CSS forem consolidados, publique-os no front matter como `colors`.

- **Global Tokens:** 145 tokens base, nos modos `Value`, `Aurora` e `Floqui`.
- **Alias Tokens:** 127 tokens semânticos, nos modos `Light`, `Dark`, `Aurora` e `Floqui`.
- Prefira aliases semânticos como `action/primary/bg`, `text color/heading`, `surface/bg base`, `selected/border` e `negative/label`.

Global Tokens são a fundação dos aliases e só devem ser usados diretamente quando não houver alias que expresse a intenção. Aurora e Floqui são modos do mesmo sistema, não sistemas independentes. Os grupos semânticos cobrem superfícies, texto, bordas, ícones, ações, seleção, desabilitado e feedback.

## Typography

Os estilos são semânticos e seus aliases definem tamanho, line-height, peso e cor. Aplique o estilo publicado; não replique nem sobrescreva manualmente seus atributos.

### Heading XL

Título principal de página ou contexto de maior destaque. Use uma vez por área principal; não use em seções, cards ou rótulos.

### Heading LG

Título de primeiro nível dentro de uma página. Organiza blocos principais sob um `Heading XL`.

### Heading MD

Título de seção, card, painel ou etapa dentro de uma área já identificada por heading maior. Não é texto de apoio ou metadado.

### Heading SM

Título curto de agrupamentos locais que aumenta a escaneabilidade sem criar nova camada dominante.

### Heading XS

Título de menor escala para subgrupos compactos, itens complexos e áreas internas. Não use como label, metadado ou destaque decorativo.

### Paragraph

Texto corrido de explicação, orientação, introdução ou conteúdo principal. Não é para rótulos curtos ou metadados.

### Description

Texto secundário para contexto, metadados, instrução auxiliar e suporte. Não use para informação crítica, erro ou instrução obrigatória.

## Layout

Use a variável publicada correspondente em gaps, paddings, raios, fundos e bordas. Para cores, prefira Alias Tokens; para medidas, use Global Tokens somente se não houver alias. Um valor manual, ainda que visualmente idêntico, não é aplicação do token.

Todo texto autoral fora de um componente publicado deve receber um estilo semântico Core Web (`Heading`, `Paragraph` ou `Description`). Não sobrescreva família, tamanho, peso ou line-height; textos de instâncias públicas seguem o componente.

Assets publicados incluem ícones, símbolos, logos e marcas de pagamento. Ícones em ações usam `Button Icon` e, quando ambíguos, `Tooltip`. Use `Brand` para logo — nunca arquivo solto quando o componente existir.

Para área logada desktop, use [Home área logada](https://www.figma.com/design/7R9SXfp0vhVqh8hSBtpQRr/SB-Mural?node-id=52-2273) como precedente: navegação global superior, painel de abertura, indicadores e seções de acompanhamento. Uma arquitetura diferente exige justificativa na especificação da tela.

## Components

### Ações

#### Button

Executa ação no contexto atual, como enviar, confirmar ou avançar. Não use para navegação; use `Link Icon` ou navegação nativa. Use `Toast` após conclusão e `Alert` quando a consequência precisa persistir.

#### Button Icon

Executa ação por ícone em espaços reduzidos, como fechar, editar, excluir ou expandir. Não use em ação primária/crítica ou quando o ícone não for autoexplicativo; nesses casos use `Button` com rótulo e, quando necessário, `Tooltip`.

#### Link Icon

Navega a outro destino ou representa ação textual de baixa hierarquia com ícone direcional. Não use para ação primária ou operação local.

### Conteúdo, identidade e dados

#### Accordion

Revela conteúdo complementar em FAQ, detalhes, configurações ou filtros avançados. Não oculte conteúdo essencial nem use como navegação.

#### Brand

Exibe logo ou símbolo em cabeçalhos, rodapés, autenticação e carregamento. Não é ornamento ou avatar; use o `.svg` do tema na biblioteca DS Assets.

#### Avatar

Representa pessoa, entidade ou perfil por imagem, iniciais ou ícone. Não use para logo ou ação. `Badge` indica status, `Tooltip` pode mostrar nome e `Skeleton` circular cobre carregamento.

#### Currency e Sale Currency

`Currency` exibe preço, saldo ou transação; `Sale Currency` compara promoção a preço original tachado. Não use para números não monetários nem captura de valor.

#### Icon

Representa conceito, categoria ou ação visualmente. Ícone isolado não é botão; use `Button Icon` para interação e `Brand` para identidade.

#### Image

Reserva mídia com proporção previsível para cards, galerias e listas. Não use para avatar ou logo; use `Skeleton` quadrado no carregamento.

#### Badge

Indica contador, notificação ou status numérico sobre outro elemento. Não classifica conteúdo por texto nem é ação.

#### Tag

Classifica categoria ou status por texto curto e cor semântica. É informativa, não interativa; não substitui `Button`, `Badge` ou `Toast`.

### Containers e overlays

#### Card

Agrupa conteúdo relacionado. Use `Clickable Card` quando toda a superfície navegar e `Selectable Card` para escolha; pode conter `Image`, `Button` e slots.

#### Clickable Card

Torna o card uma única zona de toque para navegação ou ação contextual. Não use se houver ações internas independentes nem para seleção.

#### Selectable Card

Escolhe opções visualmente ricas, como planos, pagamento ou configurações. Prefira `Radio Button` ou `Checkbox` quando um controle compacto atender.

#### Popover

Conteúdo complementar flutuante e ancorado, para formulários curtos, configurações rápidas e interação contextual. Não use para ações em lista, feedback ou texto curto.

#### Popover Menu

Lista flutuante de ações ou opções contextuais. Não use para conteúdo genérico ou seleção de formulário. `.Popover Menu-Items` e `.Popover Menu-List` são internos.

#### Tooltip

Explicação breve ao hover, especialmente para ícones e botões sem rótulo. Não use para conteúdo longo, formulário, feedback ou informação essencial.

### Formulários e seleção

#### Input Text

Captura informação curta em uma linha, como nome, e-mail e endereço. Para texto longo use `Input Text Area`; para opções, `Input Select`.

#### Input Password

Captura senha, PIN ou dado oculto, com alternância de visibilidade, label, apoio e erro. Não use para dado não sensível.

#### Input Select

Captura uma escolha predefinida em formulário. Não use para texto livre, múltipla seleção ou navegação; com duas a cinco opções, prefira `Radio Button`.

#### Input Date e Date Picker

`Input Date` captura data ou intervalo e integra `Date Picker`, que não aparece isolado. Não use para data somente leitura ou horário isolado; componentes `.Date Picker` são internos.

#### Input Text Area

Captura conteúdo em múltiplas linhas, como comentários e mensagens. Não use para entrada curta ou formato estruturado interno.

#### Checkbox

Seleciona múltiplas opções independentes, inclusive estado indeterminado. Não use para escolha exclusiva ou alternância imediata.

#### Radio Button

Seleciona exatamente uma opção em grupo pequeno. Não use para múltipla seleção, alternância binária ou lista extensa.

#### Switch

Ativa ou desativa configuração binária de efeito imediato. Não use quando a escolha exige confirmação ou submissão de formulário.

### Navegação e progresso

#### Dropdown

Agrupa links ou ações sob rótulo. Não use para valor de formulário (`Input Select`) ou conteúdo livre (`Popover`).

#### Progress Stepper

Mostra etapa de fluxo sequencial, como onboarding, cadastro ou checkout. Não use para progresso contínuo ou navegação livre; `.Progress Stepper-Settings` é interno.

### Feedback

#### Alert

Comunica situação persistente que pede atenção ou ação, como instabilidade, manutenção ou erro. Não substitui `Toast`, `Tooltip` ou `Tag`.

#### Toast

Confirma ou informa resultado breve e temporário de uma ação. Para mensagem que deve persistir, use `Alert`.

#### Skeleton

Preserva estrutura visual no carregamento: circular para avatar e quadrado para imagem. Não use como estado permanente.

## Do's and Don'ts

### Semântica

- **Ação local:** `Button`; **navegação/destino:** `Link Icon`, `Clickable Card` ou `Dropdown`; **ação contextual em lista:** `Popover Menu`.
- **Múltipla seleção:** `Checkbox`; **escolha única pequena:** `Radio Button`; **efeito binário imediato:** `Switch`; **escolha de formulário:** `Input Select`; **escolha rica:** `Selectable Card`.
- **Confirmação temporária:** `Toast`; **situação persistente:** `Alert`; **explicação de controle:** `Tooltip`; **carregamento estruturado:** `Skeleton`.

### Acessibilidade e conteúdo

- Todo controle interativo precisa de nome acessível; ícone sozinho não basta.
- `Tooltip` complementa, não substitui, nome visível ou acessível.
- Label explica o dado; placeholder não substitui label.
- Labels de ação devem conter verbo, ser sucintos e ter no máximo três palavras.
- Erros explicam como corrigir o problema.
- Estados dependentes de cor exigem texto, ícone ou outro sinal adicional.
- Foco e teclado seguem a ordem lógica do conteúdo.

### Gate de entrega

Uma tela só está concluída após conferir vínculos no Figma:

1. No frame raiz, `Global Tokens` e `Alias Tokens` devem estar no modo correto — para Floqui, ambos em `Floqui`.
2. Na tela de login, o frame externo usa `surface/bg brand bold`; no dashboard, o banner `Painel geral` usa `elements/bg brand subtle`.
3. Todo gap, padding e raio autoral deve estar vinculado à variável; número digitado manualmente reprova.
4. Todo texto autoral deve usar estilo semântico; vínculo apenas de cor não atende.
5. Registre frames verificados, exceções e motivo na entrega.

### Manutenção

Ao criar ou revisar componente no Figma, atualize sua description:

```md
**O que é:**

**Categoria:**

**Quando usar:**

**Quando não usar:**

**Componentes periféricos:**
```

Atualize este arquivo para mudança semântica, nova categoria, componente público, depreciação ou relação entre componentes. Mudanças exclusivamente visuais, de token ou propriedade permanecem no Figma; registre-as no histórico quando afetarem uso ou implementação.
