### Bootstrap - Introdução
Curso Desenvolvimento Web Completo 2022.<br><br>

Neste curso, é utilizado o Bootstrap-4 (atualmente, já foi lançada a versão 5).
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