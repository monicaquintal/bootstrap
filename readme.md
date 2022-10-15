# Bootstrap - Introdução

Anotações e aplicação do conteúdo estudado na Seção 7: Boostrap 4 & Design responsivo do Curso Desenvolvimento Web Completo 2022.<br>

<hr>

## Aulas 01 e 02 - Configurando o Bootstrap

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

## Aula 03 - Formatação de textos

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
