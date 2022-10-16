# Bootstrap - Introdução

Anotações e aplicação do conteúdo estudado na Seção 7: Boostrap 4 & Design responsivo do Curso Desenvolvimento Web Completo 2022.<br>

<hr>

## Aulas 01 e 02 - Configurando o Bootstrap.

Neste curso, é utilizado o Bootstrap-4 (atualmente, já foi lançada a versão 5).<br>
Inicialmente, criar um arquivo index.html e colar o conteúdo do <a href="https://getbootstrap.com/docs/4.1/getting-started/download/" target="_blank">link</a> disponível no conteúdo da aula (na aba Introdução). <br><br>

Atributos no &lt;head&gt;:

- Required meta tags: são tags necessárias para o funcionamento do Bootstrap;
- &lt;meta&gt;: fornecem metadados estruturados sobre uma página da Web; fazem parte da seção principal de uma página da web.
- Atributo "name = viewport": é a área disponível e visualizável na interface;
- Content:
  - devide-width: determina que o viewport ocupará a largura do dispositivo (a width será de acordo com o dispositivo - celular, tablet, pc, etc);
  - initial-scale: define a escala (zoom) padrão. Quando gira a tela, por exemplo, o bootstrap se adapta, baseado nessa escala;
  - shrink-to-fit: "encolher para caber", na aula configuramos como "no". Caso utilize esse atributo, ele encolherá o conteúdo para que caiba na visualização do site.<br><br>

Configurando o bootstrap.css:

- O <strong>bootstrap.mim.css</strong> é um arquivo minified: é o mesmo arquivo de bootstrap.css, mas sem espaçamento, fazendo com que a execução seja a mesma, mas o arquivo torna-se menor. Geralmente essa versão é a mais utilizada, considerando que o carregamento é mais rápido;
- ao baixar o framework, é colocado um &lt;link rel=&gt; com um link que encaminha ao bootstrap cdn (uma fonte da internet para carregar o css); o professor orienta a trocar o href para o próprio bootsstrap que há dentro do arquivo - href="css/bootstrap.min.css. O problema é que, em caso de atualização, precisa baixar todos os arquivos novamente para atualizar.
- o atributo integrity são medidas de segurança para garantir que não houve alterações no arquivo CSS. Ele gera uma chave criptográfica, que é lida pelo browser. Caso tente recarregar o arquivo de outro lugar sem essa chave, não funcionará. Portanto, utiliza-se o "crossorigin", para que o browser saiba de onde está sendo carregado o arquivo. Na aula, como é carregado diretamente de dentro do site, o prof. remove esses atributos (integrity e crossover).<br><br>

Optional JavaScript:

- são códigos Javascript que não são obrigatórios, podem ser removidos sem alterar o funcionamento do BS;
- o professor mantém, pois alguns dos recursos que ele ensina utilizam JS.

<hr>

## Aula 03 - Formatação de textos.

As classes podem ser aplicadas em diversos outros elementos e tags, como span, div, etc.<br>
É possível também utilizar mais de uma classe por vez.<br><br>

A) Display classes:

- dão maior destaque aos título;
- &lt;h1 class="display-1"&gt; - o texto recebe outra formatação, dando maior destaque;
- há classes de display de 1 a 4.<br>

B) Parágrafo:

- &lt;p class="lead"&gt; - garante destaque ao parágrafo, mudando sua formatação.<br>

C) Parágrafo Monospace:

- tem o mesmo espaçamento e largura para todas as letras (caracteres com mesma largura);
- aplicação: &lt;p class="text-monospace"&gt;.<br>

D) Classes de estilo:

- texto em negrito: &lt;p class="font-weight-bold"&gt;;
- texto normal: &lt;p class="font-weight-normal"&gt;;
- texto em itálico: &lt;p class="font-italic"&gt;.<br>

E) Transformação de textos:

- letras maiúsculas: &lt;p class="text-uppercase"&gt;&lt;/p&gt;;
- letras minúsculas: &lt;p class="text-lowercase"&gt;&lt;/p&gt;;
- primeira maiúscula: &lt;p class="text-captalize"&gt;&lt;/p&gt;.

F) Alinhamentos:

- à direita: &lt;p class="text-right"&gt;&lt;/p&gt;;
- à esquerda: &lt;p class="text-left"&gt;&lt;/p&gt;;
- centralizado: &lt;p class="text-center"&gt;&lt;/p&gt;.<br>

G) Bloco de Citação:

- tag &lt;blockquote&gt; cria o bloco de citação, podendo também aplicar a class de mesmo nome;
- pode utilizar ainda a classe "blockquote-footer", que dá uma formatação especial ao bloco no rodapé;
- tag &lt;cite&gt; citação, para indicar um autor, por exemplo (deixa em itálico).<br>

H) Truncate:

- classe utilizada para truncar ou cortar partes do texto;
- aplicar no &lt;p&gt;, por exemplo (&lt;p class="text-truncate&gt;) - ao expandir a tela, o texto vai aparecendo mais e, ao passar o mouse em cima, aparece o texto todo (apenas no safari).<br>

I) Listas sem título:

- class="list-unstyled": remove o estilo da lista, sem marcadores;
- class="list-inline" (na lista) e "list-inline-item" (em cada um dos elementos dentro da lista).

<hr>

## Aula 04 - Alinhamento de textos.

A) A class="text-justify" justifica o texto.<br>

B) Sufixos utilizados no Bootstrap:

- com o bootstrap, criamos layouts responsivos, que podem mudar muito de acordo com o dispositivo - torna os sites mais adaptivos, criando exibições independente do tamanho da tela;
- há <strong>sufixos</strong> que podemos utilizar para criar exibições diferentes de acordo com o dispositivo:
  - SM: small (>= 576px);
  - MD: medium (>= 768px);
  - LG: large (>= 992px);
  - XG: extra large (>= 1200px).
- ou seja: é possível definir alinhamentos específicos para diferentes telas;
- para aplicar os sufixos acima, utilizar class="text-sufixoDaTela-alinhamento".<br>

C) Convertendo elementos de Block para Inline:

- class="bg-success": aplica uma cor de fundo (usado na aula apenas para mostrar o comportamento dos elementos block e inline), assim como a class="bg-warning";
- class="d-inline": transforma o elemento block em inline.<br>

D) Convertendo elemento Inline em Block:

- class="d-block": transforma em Block.<br>

E) Elemento Inline-Block:

- class="d-inline-block": converte o elemento para esse tipo híbrido;
- elemento inline não permite aplicar margem e padding superior, nem definir largura (já o block, permite a aplicação desses atributos);
- o inline-block, por sua vez, permite margem superior, padding e largura (como block), e mantém os elementos na mesma linha (como inline). Por isso [e chamado de híbrido.<br>

<hr>

## Aula 05 - Elementos flutuantes.

A) Elementos flutuantes:

- class="float-left" ou "float-right";
- a div com elementos flutuantes não tem altura. Para corrigir, podemos utilizar o "clear:both" - já no bootstrap, aplicar no elemento pai (parent, que abriga a div flutuante) a class="clearfix".<br>

B) Posicionamento fixo:

- class="fixed-top" ou "fixed-bottom".<br>

C) Floats responsivos:

- class="float-tamanhoTela-direcao";
- apenas direções "left" e "right".<br>

D) Colar no topo (sticky):

- class="sticky-top": "gruda" a lista no topo quando a mesma o atinge (quando o menu chega lá em cima da página).<br>

<hr>

## Aula 06 - Cores & Backgrounds.

A) Classes para formatação de textos:
- class="text-primary";
- class="text-secondary";
- class="text-success" - pode ser utilizado para exibição de mensagens de sucesso ao usuário;
- class="text-info";
- class="text-warning";
- class="text-danger";
- class="text-light"; 
- class="text-dark" - é a cor de texto padrão;
- class="text-white";
- class="text-black-50" - aplicada opacidade de 50% sobre a cor padrão;
- class="text-white-50" - também recebe opacidade sobre a cor branca, se tornando mais claro. Pode ser usado, por exemplo, para formatar textos que ficam sobre imagens. <br>

B) Formatações de links:
- exatamente as mesmas classes acima.<br>

C) Backgrounds:
- ao invés de "text", colocar "bg" nas mesmas classes acima.
- class="bg-primary";
- class="bg-secondary";
- class="bg-success";
- class="bg-info";
- class="bg-warning";
- class="bg-danger";
- class="bg-light";
- class="bg-dark";
- class="bg-white";
- class="bg-transparent".<br>

<hr>

## Aula 07 - Margin & Padding.

A) Margin:
- Valor a definir, que vão de 0 até 5, sendo uma unidade de medida do CSS (REM);
- Abreviações:
  - mt -> Margin Top
  - mb -> Margin Bottom
  - ml -> Margin Left
  - mr -> Margin Right
  - mx -> Margin no eixo x (horizontal) esquerda/direita
  - my -> Margin no eixo y (vertical) top/bottom
  - m  -> Margin em todos os lados <br>

B) Padding:
- aplicado da mesma maneira, apenas trocando o m por p;
- valor a definir (0 até 5)
- abreviações:
  - pt -> Padding Top
  - pb -> Padding Bottom
  - pl -> Padding Left
  - pr -> Padding Right
  - px -> Padding no eixo x (horizontal) esquerda/direita
  - py -> Padding no eixo y (vertical) top/bottom
  - p  -> Padding em todos os lados<br>

<hr>

## Aula 08 - Tamanhos & Bordas.

A) Classes de largura:
- é possível usar classes do bootstrap para definir larguras por porcentagem;
- utilizar "w-%".<br>

B) Classes de altura:
- também é definida em %;
- utilizar "h-%".<br>

C) Bordas:
- há os atributos:
  - border: todas as bordas
  - border-top: borda superior
  - border-bottom: borda inferior
  - border-right: bordar direita
  - border-left: borda esquerda
- possibilidades de cores de bordas:
  - primary, secondary, success, info, warning, danger, light, dark, white;
  - utilizar "border-cor". <br>

D) Border radius:
- rounded - arredonda todos os lados;
- rounded-top - arredonda o topo;
- rounded-right - arredonda a direita;
- rounded-left - arredonda a esquerda;
- rounded-circle - converte em um círculo.<br>

<hr>

## Aula 09 - Media queries (parte 01).

(Arquivo ../media-queries/index.html)<br>

- utilizadas para fazer exibições diferentes baseado no tamanho do dispositivo = conceio de layout responsivo. <br>

A) Tipos de mídias (Media types):
- all – todos os dispositivos;
- aural – sintetizadores de voz;
- braille – leitores de Braille;
- embossed – impressoras de Braille;
- handheld – dispositivos de mão (como celulares com telas pequenas);
- print – impressoras convencionais;
- projection – apresentações de slides;
- screen – monitores coloridas;
- tty – teleimpressores e terminais;
- tv – televisores. <br>

B) Exemplos:
- de utilização: &lt;link rel="stylesheet" media="print" href="print.css" /&gt;;
- de resoluções de telas:
  - 320 pixels – Smartphones no modo retrato;
  - 480 pixels – Smartphones no modo paisagem;
  - 600 pixels – Tablets pequenos. Ex: Amazon Kindle (600×800);
  - 768 pixels – Tablets maiores em modo retrato. Ex: iPad (768×1024);
  - 1024 pixels – Tablets maiores em modo paisagem, monitores antigos;
  - 1200 pixels – Monitores wide.<br>

C)<a href="https://getbootstrap.com/docs/4.1/layout/overview/"> Links de media queries no Bootstrap</a>.<br>

D) Exemplos de utilização media queries: @media (min-width: tamanho da tela) {formatação a ser aplicada pra essa categoria}.<br>


<hr>

## Aula 10 - Media queries (parte 02).

(Arquivo ../media-queries/index.html)<br>

As definições de larguras mínimas para exibição do site são chamadas de breakpoint (pontos de quebra ou pontos de interrupção). Ou seja, nesses pontos são feitas as mudanças de layout (define formatações específicas para cada tipo de dispositivo).<br>

No <a href="https://getbootstrap.com/docs/4.0/layout/overview/">site do bootstrap</a> há os valores padrão de width. São combinados valores de max e min width para definir intervalos de tamanhos de dispositivos.<br>


<hr>

## Aula 11 - Botões.

A) Botões:
- a formatação padrão é: class="btn";
- formatação específicas: btn-primary, btn-secondary, btn-success, btn-info, btn-warning, btn-danger, btn-light, btn-dark, btn-link;
- utilizar a classe "btn" junto com a classe de formatação, ex: "btn btn-dark";
- é possível aplicar a formatação de botões em diferentes tags, como link, button, input (submit, reset, etc);
- para inserir contorno, utilizar class="btn btn-outline-formatação";
- há também diferentes opções de tamanho de botão: btn-lg, btn-sm, btn-block (botão bloco ocupa todo o espaçamento disponível);
- podemos controlar os estados do botão: active, disabled, alternar entre estados (incluir o atributo data-toggle="button").<br>

B) Grupos de botões:
- horizontal: class="btn-group" na &lt;div&gt;;
- vertical: class="btn-group-vertical" na &lt;div&gt;;
- toolbar: class="btn-toolbar" na &lt;div&gt;;
- botões dropdown: na &lt;div&gt; externa, incluir class="dropdown-toggle" e data-toggle="dropdown". Em seguida, adicionar à &lt;div&gt; que agrupa os links class="dropdown-menu", e em cada um dos links, class="dropdown-item".
  - obs: "dropdown-divider", quando aplicado em uma div entre os links, cria um divisor entre eles. 
<br>
<hr>

## Aula 12 - Introdução: barra de navegação.

Disponibilizada a <a href="https://getbootstrap.com/docs/4.1/components/navs/">documentação oficial sobre Navs (Navegação)</a> para consulta.<br>

A) Navegação simples/abas:
- &lt;ul class="nav"&gt; -> os itens passam a ser exibidos inline;
- &lt;li class="nav-item"&gt; -> define que trata-se de um item da navegação;
- &lt;a href="" class="nav-link"&gt; -> insere o link na navegação;
- devem ser definidos os 3 parâmetros listados;
- as classes nav-item e nav-link determinam o espaçamento entre os itens;
- há também diferentes tipos de navegação:
  - nav-pills -> no exemplo: &lt;ul class="nav nav-pills"&gt; e &lt;a href="" class="nav-link active"&gt; - usar para indicar qual a página ativa no momento;
  - nav-tabs: navegação por abas -> no exemplo: &lt;ul class="nav nav-tabs"&gt; e &lt;a href="" class="nav-link active"&gt;.
- podemos também alinhar a navegação: (por padrão, fica à esquerda)
  - justify-content-center: &lt;ul class="nav nav-tabs justify-content-center"&gt; -> alinha o menu de navegação centralizado;
  - justify-content-end: alinha a navegação à direita; 
  - flex-column: deixa a estrutura em colunas.
- há também a classe disabled, que inativa um link, mudando dua cor, indicando que está inativo para o usuário.
  <br>

B) Barra de Navegação Simples:
- a class="navbar" cria uma barra de navegação; para isso, aplicar: 
  - &lt;nav class="nav-bar"&gt;
  - &lt;ul class="navbar-nav"&gt;;
  - &lt;li class="nav-item"&gt; e 
  - &lt;a href="" class="nav-link"&gt;. 
- entretando, inserindo apenas o descrito acima, a navegação ficará à direita e o logo, à esquerda. Portanto, inserir outra class: &lt;nav class="navbar navbar-expand-tamanhodatela"&gt;, para adequar esse "espaçamento" ao dispositivo específico;
- class="navbar-brand": indica que o item é o logo da barra de navegação;
- é possível também utilizar backgrounds, utilizando duas classes:
  - na &lt;nav&gt;, inserir: navbar-dark ou navbar-light;
  - podemos aplicar também o bg dentro desta class.
<br>
<hr>

## Aula 13 - Barra de navegação - parte 01.

A) Barra de navegação com menu responsivo:
- cria um menu hamburguer (estrutura que "esconde" o menu de navegação de um site e deixa a página mais “limpa”, usado especialmente em dispositivos com telas menores);
- criar um botão para o menu hamburguer, utilizando:
  - &lt;button class="navbar-toggler" data-toggle:"collapse" data-target="#nav-target"&gt;;
  - &lt;span class="navbar-toggler-icon"&gt;;
  - criar uma div que englobe toda a ul, e inserir a class="collapse navbar-collapse" e o id="nav-target";
- portanto, devemos definir o data-toggle="collapse" e em seguida o data-target (item que queremos exibir ou ocultar quando o botão for clicado).
<br>
<hr>

## Aula 14 - Barra de navegação - parte 02.

A) Barra de navegação com formulário:
- inserido dentro da &lt;nav&gt;, imediatamente antes do seu fechamento:
  - &lt;form class="form-inline"&gt;
  - &lt;input type="text" class="form-control" placeholder="pesquisar"&gt; e
  - &lt; button class="btn btn-outline-success"&gt;
- caso coloque o formulário dentro da div que controla o menu hamburguer, ele também ficará oculto em telas menores, assim como a barra de navegação, no exemplo da aula anterior. <br>

B) Barra de navegação com menu dropdown:
- são menus em que aparecem outras opções quando clicamos;
- definir:
  - class="dropdown" no &lt;li&gt;;
  - class="dropdown-toggled" e data-toggle="dropdown" no &lt;a&gt;;
  - class="dropdown-menu" na &lt;div&gt;;
  - class="dropdown-item" no &lt;a&gt; que fica dentro da div.<br>

C) Cores:
- podem ser aplicadas as mesmas cores para bg (bg-primary, bg-secondary, bg-success, bg-info, bg-warning, bg-danger, bg-light, bg-dark) e navbar (dark e light), já estudadas anteriormente. <br>

D) Alinhamentos:
- class="navbar fixed-top" -> fixa a barra de navegação no topo da página;
- class="navbar fixed-bottom" -> fixa a barra de navegação no fim da página;
- class="navbar sticky-top" -> após passar pela barra de navegação, ela é fixada.<br>

<hr>

## Aula 15 - Listas.

A) Listas:
- aplicar class="list-group" na &lt;ul&gt; e class="list-item" nas &lt;li&gt;;
- a classe "active" deixa o item selecionado como "ativo".<br>

B) Classe flush:
- &lt;ul class="list-group list-group-flush"&gt;;
- a lista terá apenas bordas superior e inferior (não possui borda lateral e arredondamento no canto);
- a classe "active" deixa o item selecionado como "ativo".<br>

C) Classes contextuais:
- inserir: class=list-group-item-opçãoescolhida;
- opções: primary, secondary, success, info, warning, danger, light, dark. <br>

D) Badges:    
- são muito comuns nos e-mails;   
- classe: badge-opçãoescolhida;
- opções: primary, secondary, success, info, warning, danger, light, dark.<br>

E) Breadcrumb:
- usadas para identificar o local em que o usuário encontra-se no site;
- aplicar:
  - &lt;ol class="breadcrumb"&gt;;
  - &lt;li class="breadcrumb-item"&gt; e selecionar o item ativo incluindo "active" na class escolhida.<br>

  <hr>

## Aula 16 - Formulários.

A) Elementos de texto (como label, input, email):
- &lt;div&gt; é utilizada para agrupar os elementos (como label e input), podendo ainda aplicar na div a class="form-group" para dar espaçamento.
- no &lt;input&gt; podemos usar a class="form-control", que da formatação na caixa de texto -> podemos usar essa classe tambem em selects e textareas;
  - há também as opções sm e lg, que alteram o tamanho da caixa de texto (exemplo: "form-control-lg");
- o atributo "readonly" deixa o campo cinza e impede que o usuário clique;
- a classe "form-text" é a formatação padrão para textos dentro de um formulário. <br>

B) Inputs tipo file: 
- podemos utilizar a class="form-control-file" para selecionar um arquivo;
- temos outra opção, que é aplicar a class="custom-file" na div, na label a class="custom-file-label", e no input class="custom-file-input".<br>

C) Range:
- no input, a class="custom-range" altera a formatação. <br>

D) Button:
- classes btn, conforme já estudado em aulas anteriores. <br>

E) Formulários inline:
- aplicasa a class="form-inline" na tar &lt;form&gt;.<br>

F) Validação de formulário:
- a validação é feira via JS, e as classes são aplicadas a partir dela;
- classes: is-valid, is-invalid, invalid-feedback, valid-feedback.<br>
<hr>

## Aula 17 - Input group.