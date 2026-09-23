---
version: alpha
name: Core App
description: Regras semânticas para componentes e composições de aplicativos móveis.
omitted:
  - Elevation & Depth
  - Shapes
---

# Core App

## Overview

Core App é a biblioteca de componentes para aplicativos móveis. Compartilha marca, tokens, assets e tipografia com Core Web; componentes, navegação e composição são específicos para contexto mobile.

### Fontes de verdade

- [Biblioteca Core App](https://www.figma.com/design/RXrjdZA9A3xqRGaUr2U3Ek/SB-Core-App?node-id=53-4420&p=f&t=DvbzE2OsMGjtGWvL-0)
- [Fundamentos compartilhados](../foundations/DESIGN.md)
- [Tokens](https://www.figma.com/design/ZPWfhmidgyfkok9RYa6QWE/Design-Tokens)
- [Assets](https://www.figma.com/design/fu1sRTGOuDJj2ZLkV8lSX1/Assets?node-id=209-36)
- Página App do [SB-Mural](https://www.figma.com/design/7R9SXfp0vhVqh8hSBtpQRr/SB-Mural?node-id=22-5108)

## Colors

Use os mesmos Global Tokens e Alias Tokens de Foundations. Prefira aliases semânticos e mantenha as duas coleções no modo da mesma marca.

## Typography

Use a escala compartilhada. Registre aqui apenas regras móveis de densidade, truncamento ou comportamento de texto.

## Layout

- Considere safe areas, teclado virtual e zonas de toque desde o início.
- Priorize uma tarefa principal por tela.
- Use a página App do Mural como precedente para hierarquia, densidade, estados e transições.
- Documente grid, margens, alvos mínimos de toque, bottom navigation, top bar, tabs, drawers, bottom sheets, orientação e teclado quando essas decisões forem publicadas.

## Components

Documente somente componentes públicos da Core App, sempre com: o que é, categoria, quando usar, quando não usar e componentes periféricos.

### Navegação

Adicione os componentes de navegação móveis publicados na biblioteca.

### Inputs e seleção

Adicione campos, seletores e controles específicos de App.

### Feedback e overlays

Adicione sheets, dialogs, alerts, carregamento e feedback específicos de App.

## Do's and Don'ts

- Use componentes Core App para interação móvel; não adapte componentes Web sem variante publicada.
- Não faça informação essencial depender de hover.
- Garanta rótulo acessível, ordem de foco lógica e erro acionável.
- Preserve tokens e propriedades publicadas; registre qualquer exceção na entrega.

