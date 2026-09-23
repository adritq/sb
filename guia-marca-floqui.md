# Guia de Marca — Floqui

> Documento de referência para pessoas e IAs que criam comunicações, conteúdos e peças visuais para a Floqui.

## 1. Essência da marca

### Categoria e descrição

A Floqui oferece soluções tecnológicas para restaurantes que operam exclusivamente por delivery. Ajuda equipes a receber, organizar e entregar pedidos com mais eficiência e previsibilidade.

### Plataforma de marca

- **Propósito:** fazer o delivery funcionar melhor para quem prepara, entrega e pede comida.
- **Visão:** ser a parceira tecnológica mais confiável para restaurantes que nascem e crescem no delivery.
- **Missão:** simplificar a operação de restaurantes delivery-first para que equipes possam focar em comida boa e clientes bem atendidos.
- **Promessa:** operação sob controle, pedidos no caminho certo.
- **Posicionamento:** para restaurantes que operam somente por delivery, a Floqui centraliza e simplifica a operação de pedidos, ajudando a reduzir ruídos e dar mais previsibilidade à rotina.

### Valores

- Eficiência que respeita pessoas
- Simplicidade
- Confiabilidade
- Transparência
- Melhoria contínua

## 2. Público

### Público principal

Donos, gestores e líderes operacionais de restaurantes delivery-first, dark kitchens e marcas de alimentação com alto volume de pedidos.

**Necessidades:** organizar pedidos de diferentes canais, reduzir erros e atrasos, acompanhar a operação em tempo real e melhorar a experiência do cliente sem sobrecarregar a equipe.

**Dores:** pedidos dispersos em múltiplos aplicativos, falhas de comunicação entre cozinha e entrega, atrasos difíceis de identificar e pouca visibilidade da operação.

### Público secundário

Equipes de atendimento, cozinha e expedição que precisam de processos claros em horários de pico.

## 3. Personalidade e voz

### Personalidade

**É:** ágil, objetiva, confiável, parceira e calma sob pressão.

**Não é:** fria, apressada, acusatória, excessivamente técnica ou informal demais.

### Tom de voz

Fale de forma direta, clara e serena. A Floqui entende que o ritmo do delivery é intenso; suas mensagens devem reduzir atrito, não criar mais.

- **Objetiva:** diga o que acontece, por que importa e qual é o próximo passo. Sim: “Centralize os pedidos para a equipe acompanhar tudo em um só lugar.” Não: “Maximize a orquestração omnicanal da sua operação.”
- **Confiável:** seja precisa, transparente e não esconda limitações. Sim: “Você acompanha cada etapa do pedido e identifica pontos de atenção.” Não: “Nunca mais tenha problemas com o delivery.”
- **Parceira:** reconheça a pressão da operação e ofereça apoio prático. Sim: “No pico do jantar, informação clara ajuda cada pessoa a agir mais rápido.” Não: “Se sua equipe errar, o problema será dela.”

### Linguagem verbal

**Prefira:** “pedido”, “cozinha”, “expedição”, “entrega”, “operação”, “tempo de preparo” e “acompanhar”.

**Evite:** “caos”, metáforas de guerra, “sem erro”, “garantido”, “disruptivo” e “solução 360”.

**Regras:**

- Use português do Brasil.
- Prefira instruções claras e em etapas para conteúdos operacionais.
- Não culpe equipe, entregadores ou clientes por problemas.
- Não use urgência artificial ou promessas absolutas.
- Explique siglas e termos técnicos na primeira menção.

### Mensagens-chave

- Delivery não precisa significar operação fragmentada.
- Quando o pedido flui, a equipe respira e o cliente percebe.
- Mais visibilidade para decidir rápido nos horários de pico.
- Tecnologia que acompanha o ritmo da sua cozinha.

## 4. Pilares de conteúdo

### Operação eficiente

Ajudar gestores a reduzir atritos entre pedido, cozinha e expedição.

Exemplos: “Como organizar a rotina antes do pico de pedidos” e “Cinco sinais de gargalo na expedição”.

### Experiência do cliente

Mostrar como uma operação organizada melhora cada entrega.

Exemplos: “O que torna a comunicação sobre atraso mais útil para o cliente” e “Como reduzir erros de pedido com processos simples”.

### Gestão com clareza

Apoiar decisões com dados e acompanhamento da rotina.

Exemplos: “Quais tempos acompanhar em uma operação delivery-first” e “Como usar os horários de pico para planejar sua equipe”.

## 5. Linguagem visual

### Conceito

Uma identidade essencialmente tipográfica, minimalista e elegante. Azul profundo sobre fundo creme cria reconhecimento com serenidade; a marca não depende de ícone, ilustração ou grafismo para comunicar confiança.

### Princípios

- **Tipográfica:** a palavra Floqui é o principal ativo visual, usada com presença e espaço.
- **Essencial:** poucos elementos, poucas cores e nenhuma decoração sem função.
- **Serena:** o contraste azul e creme transmite organização sem o aspecto frio de tecnologia.
- **Precisa:** alinhamento, ritmo e respiro tornam a informação fácil de ler.

### Paleta

- **Principais:** Azul, Creme e Branco
- **Secundárias:** Laranja, Verde e Vermelho

**Tema**
- As definições de hexadeciais, tipografia e demais variações para componentes deve respeitar o tema Floqui do design system. 
- Use as definições de hexadeciais dos global tokens (SB Design Tokens)
- Use as definições de alias tokens (SB Design Tokens)
- Quando for utilizar os componentes, aplique o Figma o Appareance: Alias Tokens = Floqui e Global Tokens = Floqui 

### Aplicação da Floqui em interfaces

Em cada tela Floqui, aplique `Global Tokens = Floqui` e `Alias Tokens = Floqui` no frame raiz.

#### Login

- Vincule o preenchimento do frame externo da tela a `surface/bg brand bold`.
- Use o componente `Brand` com o logotipo Floqui na área de autenticação.
- Aplique os estilos de texto publicados ao título (`Heading`) e ao texto explicativo (`Paragraph` ou `Description`, conforme a importância da mensagem).
- Vincule os gaps e paddings da composição às variáveis publicadas de espaçamento. Os espaçamentos internos dos componentes publicados seguem a própria biblioteca.

#### Área logada e dashboard

- Siga a composição [Home área logada do SB-Mural](https://www.figma.com/design/7R9SXfp0vhVqh8hSBtpQRr/SB-Mural?node-id=52-2273), com navegação global superior no desktop.
- Organize o dashboard com painel de abertura, indicadores e seções de acompanhamento da operação de delivery.
- Vincule o preenchimento do banner `Painel geral` a `elements/bg brand subtle`.
- Use componentes publicados para cards, ações, estados e identidade da marca. Vincule os gaps e paddings criados para a composição às variáveis publicadas.
- Identifique como ilustrativos os pedidos, números e demais dados usados apenas para apresentar a interface.

#### Assinatura da marca

O logotipo por extenso é a assinatura padrão da Floqui e deve aparecer sozinho, sem um símbolo ao lado. Use a variante `Logotype` do componente `Brand` em login, navegação global e demais assinaturas institucionais.

Reserve a variante `Symbol` para aplicações compactas em que o logotipo por extenso não caiba, como ícone de aplicativo ou favicon. Não combine `Symbol` e `Logotype` para formar uma nova assinatura.

### Fotografia e imagens

**Use:** apenas quando a narrativa pedir contexto humano, de comida ou de operação; prefira luz suave, materiais reais e fundos neutros. A fotografia deve viver ao lado da tipografia, nunca competir com ela.

**Evite:** fotos de banco de imagem genéricas, filtros saturados, colagens e qualquer visual que tente substituir a clareza da marca por decoração.

### Composição

O sistema visual é tipográfico: grandes palavras ou frases, muito espaço negativo e uma linha fina opcional como divisor. O wordmark deve aparecer sozinho, sem ícone acompanhante. Para interfaces, ícones funcionais podem existir, mas não fazem parte da assinatura da marca.

Organize informações em blocos escaneáveis e alinhamentos consistentes. Destaque uma ação principal por tela ou peça. Use aproximadamente 80% de respiro e clareza informacional, e 20% de expressão de marca.

## 6. Instruções para IA

### Objetivo

Criar comunicações de marketing, vendas, suporte e educação para a Floqui com foco em clareza operacional, eficiência e respeito por quem faz o delivery acontecer.

### Ao criar conteúdo

- Defina público, canal, objetivo e ação desejada antes de redigir.
- Priorize informações acionáveis e organizadas por ordem de importância.
- Em conteúdos de suporte, explique uma ação por vez.
- Mantenha tom sereno ao abordar atrasos, falhas ou picos de demanda.
- Quando houver dados, informe a fonte ou deixe clara a limitação.
- Se faltarem informações, declare a limitação em vez de inventar.

### Não faça

- Não invente integrações, preços, funcionalidades ou métricas.
- Não garanta redução de atrasos, aumento de pedidos ou melhoria de lucro.
- Não ofereça orientação sanitária, trabalhista ou jurídica como aconselhamento especializado.
- Não culpe funcionários, entregadores, plataformas ou clientes.

### Checklist final

- A informação pode ser compreendida rapidamente durante uma operação intensa?
- O tom é objetivo, sereno e respeitoso?
- A peça visual é funcional e tem uma ação principal clara?
- Há promessas ou dados não comprovados?
- Está claro qual é o próximo passo?


### Outras orientações

Sempre que for apresentar a logo, utilize o componente Brand do Design System, puxando o .svg da biblioteca DS Assets.
Quando o componente estiver na variante Logotype, use o arquivo de nome logotype com o nome Floqui.
Quando o componente estiver na variante Symbol, use o arquivo de nome symbol com o nome Floqui.
Se fizer sentido, aplique o svg com o token de cor da marca.


#### Aplicações obrigatórias nas interfaces Floqui

- Aplique `Alias Tokens = Floqui` e `Global Tokens = Floqui` no frame raiz de cada tela, para que os elementos internos herdem os modos corretos.
- Na tela de login, vincule o preenchimento do **frame externo da tela** ao alias `surface/bg brand bold`.
- No dashboard, vincule o preenchimento do banner **Painel geral** ao alias `elements/bg brand subtle`.
- Use variáveis publicadas em todos os gaps e paddings criados para a composição da tela. Confira o vínculo na propriedade do Figma; não basta reproduzir o valor numérico.
- Aplique os estilos de texto publicados do Core Web aos títulos, parágrafos e descrições criados para a tela. Confira o estilo de cada camada de texto autoral; um token de cor isolado não atende a essa regra.