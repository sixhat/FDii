---
title: Apontamentos de Ferramentas Digitais II 18/19
author: David Sousa-Rodrigues\thanks{<david.s.rodrigues@ipleiria.pt> \\ <prof.david.esad@gmail.com>}
documentclass: tufte-handout
papersize: a4
colorlinks: true
lang: pt-PT
header-includes: |
  \usepackage{graphicx}
---

```{=latex}
\newcommand{\mfc}[2]{
\begin{marginfigure}
\includegraphics[width=\linewidth]{#1}
\caption{#2}
\end{marginfigure}
}
\newcommand{\mf}[1]{
\begin{marginfigure}
\includegraphics[width=\linewidth]{#1}
\end{marginfigure}
}
\newcommand{\fig}[1]{
\begin{figure}
\includegraphics[width=\linewidth]{#1}
\end{figure}
}
\newcommand{\figc}[2]{
\begin{figure}
\includegraphics[width=\linewidth]{#1}
\caption{#2}
\end{figure}
}
\newcommand{\figf}[1]{
\begin{figure*}
\includegraphics{#1}
\end{figure*}
}
\newcommand{\figfc}[2]{
\begin{figure*}
\includegraphics{#1}
\caption{#2}
\end{figure*}
}
```

\today

\tableofcontents

# Apontamentos de Ferramentas Digitais II

> Estes apontamentos seguem aproximadamente os tópicos do programa da cadeira de Ferramentas Digitais II, não sendo exaustivos na cobertura de todo o programa. Esta primeira versão encontra-se bastante incompleta e pretende apenas dar um pequeno enquadramento ao aluno. Os ficheiros fonte destes apontamentos encontram-se online no repositório <https://github.com/sixhat/FDii> sendo que serão continuamente melhorados. O repositório terá assim sempre a versão mais actual deste documento.

## Comunicação entre o docente e a turma

Para facilitar a comunicação entre todos, foi criado um grupo de discussão no google groups. O grupo é <https://groups.google.com/d/forum/ferramentas-digitais-ii> e o meu email de contacto utilizado será o <prof.david.esad@gmail.com>. 

\clearpage

# Conceitos básicos de algoritmia

No reino do mundo digital tudo o que utilizamos é executado por programas de computador. Como utilizadores destes programas muitas vezes não pensamos como é que eles são capazes de fazer certas coisas, como desenhar num ecrã ou verificar a ortografia de um texto. Por detrás destas tarefas está a noção de programa. Um programa é um conjunto de instruções agrupadas em tarefas específicas que ditam a forma de funcionar de um computador de forma a cumprir determinadas tarefas.

Um programa é como uma receita de culinária. Contém a lista de ingredientes e as instruções de como manipular esses ingredientes para obter o prato final. 

## B1. Conceito de Algoritmo

## B2. Partes de um Algoritmo

Um algoritmo é composto por diferentes tipos de unidades funcionais. De entras podemos assinalar:

* Instruções
* variáveis
* instruções condicionais
* ciclos (loops).

## B3. Representações de um Algoritmo - Fluxograma 

A visualização de um algoritmo facilita a compreensão dos passos que o algoritmo executa. Para isso foram desenvolvidos símbolos gráficos que ilustram o comportamento de um algoritmo. Estes diagramas / desenhos técnicos são conhecidos como fluxogramas de execução e foram adotados como um standard ISO (<https://www.iso.org/standard/11955.html>)  a partir de um standard americano ANSI prévio. 

__Exercício - Desenhar um Algoritmo com yEd.__

Para demonstrar como podemos visualizar um algoritmo vamos utilizar um software de diagramação chamado yEd. O yEd é um software de produção de diagramas gratuito que está disponível para as diversas plataformas de computação (Windows, Mac OS X e linux). Pode ser obtido em <https://www.yworks.com/products/yed>.

A utilização de fluxogramas é de importância crucial para a compreensão de um programa de computador e para comunicar o funcionamento desejado de um processo ou algoritmo. São de tal forma importante que algumas linguagens de programação tentaram inclusive utilizar uma representação de fluxograma como a própria linguagem de programação. Neste tipo de linguagem incluem-se __Flowgorithm__ e __Raptor__. 

A representação de um algoritmo computacional através de um fluxograma também não é a única forma de descrever um algoritmo. Outras representações existem, nomeadamente através da escrita do chamado pseudo-código, ou de utilização de outra linguagem visuais de modelação como __UML2__. No entanto os diagramas de fluxo de execução de um algoritmo, pela sua simplicidade e utilidade continuam a ser os diagramas mais utilizados.

\figc{img/fluxograma-todos-diagramas}{Lista dos diversos diagramas existentes no standard de Fluxogramas.}

__Principais elementos para o desenho de fluxograms__

Os principais elementos comuns a todos os fluxogramas são os que dizem respeito ao início e  fim de um algoritmo, os que indicam instruções e os que indicam locais onde conforme uma dada condição, e cuja resposta é verdadeiro/falso, levará o algoritmo por caminhos de execução diferentes.

_Princípio e fim do algoritmo_

O princípio e fim de um algoritmo tem sempre que ser indicados por símbolos apropriados. Tradicionalmente o símbolo a utilizar é o observado na figura à esquerda, no entanto outras linguagens derivadas dos fluxogramas adoptaram outros símbolos. À direita os símbolos de start e stop utilizados pela linguagem de modelação UML2. 

\mfc{img/fluxograma-start-stop}{Esq: início e fim de um fluxogram. Dir: os mesmos elementos em UML2}

*Condições*

Normalmente é comum pensar se uma condição desenhada por um losango pode dar respostas de uma escolha múltipla, eg: “Qual a sua cor favorita do arco-íris?” esta pergunta permite diversas respostas e seria plausível ter um losango com 7 setas de saída. No entanto convém notar que essas 7 opções podem ser substituídas por uma série de condições *verdadeiro*/*falso* do género: 

\mf{img/fluxograma-decision}

> A cor escolhida é azul? Se Verdadeiro seguir algoritmo, se Falso perguntar se a cor escolhida é amarelo? se Verdadeiro seguir algoritmo, se Falso perguntar se a core escolhida é …. e assim sucessivamente até se esgotarem as opções. 

Esta forma de colocar as questões em termos de serem Verdadeiras ou Falsas parece complicar a tarefa de definir um algoritmo, mas permite utilizar elementos de programação muito simples e genéricos em termos de computação. Uma condição apenas possui dois estados. Ou é verdadeira, ou é falsa e esta simplicidade binária é que permite aos computadores construirem estruturas complexas a partir de elementos muito simples.

*Instruções / Processos*

As instruções representam uma tarefa básica. São a unidade que executa algo e que após a sua conclusão retornam o controlo do algoritmo ao passo seguinte. As instruções são sempre executadas, não impõe condições para a sua execução e não terminam enquanto a tarefa nela indicada não estiver terminada. 

\mf{img/fluxograma-processo}

*Exemplo simples de um fluxograma:*

  Trocar uma lâmpada

1. Ligar o interruptor
2. Acendeu?
3. Se sim continuar, caso contrário Trocar a lâmpada.
4. Fim.

\includegraphics[width=6cm]{img/fluxograma-mudar-lampada}

__Exercício__: Desenhe um fluxograma para o algoritmo que executa todos os dias entre o momento que acorda e a saída de casa.

1. Acordar.
1. Sair da cama.
1. Se a luz estiver apagada, acendê-la. Se por algum motivo não houver luz, abrir persiana. 
1. Ir tomar banho.
1. Vestir
1. Preparar o pequeno almoço para a família.
1. Perguntar se querem torradas. Se a resposta for afirmativa fazer torradas.
1. Fazer sumo de laranja. Enquanto tiver laranjas na fruteira esprema-as.
1. Tomar o pequeno almoço.
1. Sair de casa

> Este exercício pode deve ser feito individualmente, e no final deve obter um diagrama de fluxo semelhante ao seguinte:

\mf{img/fluxograma-acordar-sair-casa}

\clearpage

# Introdução ao desenvolvimento de páginas Web

Nesta secção vamos aprender os fundamentos básicos do funcionamento da internet, e em particular de como são criadas as páginas Web que consultamos na WWW. 

A WWW ou Web foi criada por Sir Tim Berners-Lee\sidenote{Para mais informação em relação ao trabalho de Tim Berners-Lee consultar por exemplo \url{https://en.wikipedia.org/wiki/Tim_Berners-Lee} e \url{http://info.cern.ch/Proposal.html}} quanto trabalhava no CERN na Suíça. A Web foi imaginada em 1989 como um sistema de gestão e partilha de informação. Na altura a informação digital era basicamente texto simples (sem formatações nem imagens) e surgiu então a primeira versão do HyperText Transfer Protocol (HTTP). O HTTP é a fundação para a comunicação de dados na Internet. O **hipertexto** é uma forma de adicionar informação relevante a um texto por forma a estabelecer ligações relevantes entre diferentes documentos. Estas ligações são normalmente designadas por hiperligações.

\figc{img/hipertexto-geral}{Exemplo de vários documentos de hipertexto conectados entre si por hipeligações. Imagem de Andreariverac, utilizada sob licença CC BY-SA 3.0 \url{https://creativecommons.org/licenses/by-sa/3.0/deed.en}}





\clearpage

# Responsive Web Design

A programação de páginas Web em HTML5 é standard e são muito raros os casos em que se utiliza ainda HTML4 ou anteriores. O HTML5 veio simplificar tremendamente o trabalho de desenvolvimento com a introdução de novos elementos semânticos (novas tags estruturais), assim como suporte para audio e vídeo. E mesmo nos casos em que os browsers mais antigos não suportam todos os elementos do HTML5 (leia-se Microsoft Internet Explorer 9 e anteriores) é possível servir um *polyfill*\sidenote{\textbf{polyfill} é uma técnica que permite através de um programa de JavaScript simular o suporte para tags que browsers antigos não conseguem renderizar.} aos browsers que lhes permite renderizar correctamente os elementos. 


\clearpage

# Tipografia

A tipografia assume um papel primordial na comunicação visual e isto é naturalmente também importante nas páginas Web. Apesar de a programação de uma página conter o texto num formato agnóstico, é possível definir todos os aspectos de tipografia que o browser deve utilizar para renderizar esse bloco de texto. 

É no entanto possível não dar nenhuma indicação sobre as características tipográficas do texto da página web, sendo que nesses casos o browser irá assumir um conjunto de padrões e aplicá-los ao texto existente no HTML. 

Para evitar isso é importante que o web designer especifique claramente qual o tipo de fonte que quer utilizar. 

O standard define que qualquer fonte que esteja instalada no sistema operativo do utilizador possa ser utilizada, assim como qualquer fonte que possa ser descarregada em formato apropriado, aquando do carregamento da página web. 

```css
font-style 
font-family
font
```

Para utilizar uma determinada fonte é necessário definir a família da fonte que se quer utilizar. No CSS isso é conseguido definindo a propriedade **font-family** que pode receber uma lista de fontes separadas por vírgulas e.g.

```css
p {
  font-family: “Arial”, “Roboto”, sans-serif;
}
```

Neste exemplo os elementos do tipo `P` serão renderizados por uma de três fontes, “Arial”, “Roboto” ou a fonte sem serifa que o browser utilizar por defeito. A utilização será dada pela primeira fonte da lista que o browser conhecer, passando às opções seguintes sempre que as fontes mais à esquerda não estejam disponíveis.

No exemplo anterior é ainda possível ver que utilizamos um nome genérico para fontes sem serifa, o **sans-serif**. É possível definir famílias de fontes genéricas que os browsers interpretarão de acordo com os padrões definidos pelo programador. As famílias genéricas que todos os browsers suportam são o **sans-serif** anterior e ainda o **serif** para fontes serifadas, **cursive** para fontes cursivas que imitam a escrita humana, **fantasy** para fontes de fantasia e ilustração, e **monospace** para fontes monoespaçadas. 



Normalmente a especificação das fontes a utilizar não necessita as aspas quando o nome da fonte não tem espaços no nome. No exemplo anterior Arial e Roboto podiam ter sido escritas sem as aspas. No caso de utilizarmos fontes com espaços no nome então é necessário utilizar as aspas e.g. “Times New Roman”.



## Importar fontes não instaladas no computador do utilizador

Muitas vezes o designer pretende utilizar certos tipos de letra que não estão disponíveis nos computadores dos utilizadores. Para essas situações o designer pode importar tipos de letra a partir de recursos externos. Para isso utiliza-se a regra CSS **@font-face**\sidenote{\textbf{@font-face} devem ser declaradas imediatamente no topo do nosso ficheiro CSS de forma a poder utilizar a fonte no CSS. }.


```css
@font-face {
  font-family: MyHelvetica;
  src: local("Helvetica Neue Bold"),
       local("HelveticaNeue-Bold"),
       url(MgOpenModernaBold.ttf);
  font-weight: bold;
}
```

Neste exemplo o comando `@font-face` é utilizado para definir um tipo de letra chamado “MyHelvetica” que vai tentar encontrar o tipo de letra no computador do utilizador utilizando o comando **local**. Caso o browser não encontre nenhum dos dois ficheiros definidos com o comando local, então vai utilizar um ficheiro online definido pelo comando **url**. Para além do mais este exemplo define que este tipo de letra será utilizado a negrito.

A utilização de tipos de letra externos é de grande utilidade para se desenharem websites que não fiquem restritos a tipos de fonte padrão ou aos instalados nos dispositivos dos clientes. Tem no entanto o inconveniente de obrigar a um maior tráfego de dados para o cliente e naturalmente custos extra para o servidor.

Também é necessário ter em linha de conta que a distribuição de tipos de letra pode não estar enquadrado no licenciamento do tipo de letra aquando da sua compra. Muitas vezes a “compra” licencia apenas a produção de material impresso e não a distribuição online. É necessário portanto ter algum cuidado com o licenciamento destes componentes digitais para evitar violações das legislações de propriedade intelectual. 

## Utilizando uma fonte importada

Para utilizar um tipo de letra importado com comando **@font-face** basta utilizar a propriedade **font-family** como anteriormente.


```css
p {
  font-family: MyHelvetica;
}
```
Neste exemplo a fonte MyHelvetica carregada anteriormente é aplicada a todos os elementos do tipo parágrafo (`p`).

## Formatos suportados

As fontes a utilizar podem estar em diversos formatos (otf, ttf, woff, woff2) e nem todos são suportados pelos browsers actuais. Assim é conveniente oferecer mais do que um formato na definição de **@font-face,**  utilizando diversos elementos **url** (separados por vírgula). 

```css
src: url(ideal-sans-serif.woff) format("woff"),
     url(basic-sans-serif.ttf) format("opentype");
```

Para obter os ficheiros nos diversos formatos pode utilizar um serviço online como o Font Squirrel Generator\sidenote{Font Squirrel Generator - \url{https://www.fontsquirrel.com/tools/webfont-generator}}.

\clearpage

# Criar Listas Ordenadas e Desordenadas

Em HTML por vezes temos que criar listas *e.g.* lista de contactos numa aplicação de páginas brancas, ou a lista de hiperligações recomendadas para restaurantes num website de review de restaurantes, ou uma lista de outras notícias num website noticioso. 

A criação de listas é relativamente simples e o HTML incorpora dois tipos de listas fundamentais: Listas não ordenadas (unordered) e ordenadas (ordered). 

## Listas não ordenadas (UL)

Estas listas são as mais comuns são produzidas pela tag `UL` (unordered list). Dentro dessa tag ul cada elemento da lista é indicado pela tag `li`.

```html
<ul>
      <li>Elemento 1</li>
      <li>Elemento 2</li>
      <li>Elemento 3</li>
      <li>Elemento 4</li>
</ul>
```

Resulta em:

* Elemento 1
* Elemento 2
* Elemento 3
* Elemento 4

## Listas ordenadas (OL)

Estas listas são menos comuns mas também importantes. São utilizadas quando se pretende que os elementos possuam um número de ordenação. 

```html
<ol>
      <li>Elemento 1</li>
      <li>Elemento 2</li>
      <li>Elemento 3</li>
      <li>Elemento 4</li>
</ol>
```

Resulta em:

1. Elemento 1
2. Elemento 2
3. Elemento 3
4. Elemento 4

## Utilização de listas

As listas são muitas vezes utilizadas para criar sistemas de navegação com menus e submenus uma vez que podem ser colocadas listas dentro de listas (*nesting*) permitindo dessa forma criar hierarquias complexas.

## Personalização de listas

Utilizando CSS é possível alterar consideravelmente a forma como as listas são mostradas pelos browsers. 

Para isso é necessário definir a propriedade `list-style-type`

```html
ul {
 list-style-type: circle;
}
```

vai produzir uma lista em que os marcadores são círculos:


\begin{itemize}[$\circ$]
\item Elemento 1
\item Elemento 2
\item Elemento 3
\item Elemento 4
\end{itemize}


A propriedade `list-style-type` aceita diversos tipos de elementos: `disc, circle, square, decimal, lower-roman, upper-roman, lower-greek, lower-latin` são apenas alguns dos elementos suportados para os marcadores dos items das listas.	

\clearpage

# Projecto do semestre

## Web Portfólio Onepage

ESCOLA SUPERIOR DE ARTE E DESIGN  
CALDAS DA RAINHA  
**Unidade Curricular**: Ferramentas Digitais II  
**Ano letivo**: 2018/2019  
**Curso**: Design Gráfico e Multimédia  
**Ano**: 1º ano  
**Semestre**: 2º Semestre  
**Docentes**: David Sousa-Rodrigues, Miguel Carradas 

## ENQUADRAMENTO

Quando pensamos em internet, provavelmente pensamos imediatamente em websites, mas hoje em

dia a internet é muito mais do que isso: conteúdos; aplicações; ferramentas; experiência; velocidade;

acessibilidade; partilha; poder; etc. Se a estes conceitos juntarmos a diversidade de devices com capacidade de output — computadores, telefones, tablets, relógios, etc — estaremos então a falar de um complexo ecossistema centrado no indivíduo enquanto utilizador.

Esta multiplicidade de suportes e meios apresenta desafios distintos e requer abordagens particulares. O projecto que se propõe de seguida, é potenciado e ao mesmo tempo condicionado pelas especificidades e possibilidades da internet e dos diferentes devices onde esta está presente.

## PROJECTO

Desenvolver um portfólio baseado no conceito one page website, que deve ser visualizado em 3 versões (320px, 768px e 1200px), sendo assim ajustável a diferentes dimensões de ecrã. A programação deve ser compatível com as versões mais recentes dos seguintes browsers: Chrome, Firefox, Safari, Opera e IE.

O projecto deve ter pelo menos as seguintes secções de conteúdos: Sobre, Trabalho e Contactos.

## CRITÉRIOS DE AVALIAÇÃO

— Aplicação dos conhecimentos adquiridos na cadeira

— Construção semântica (só podem utilizar nomes em pt para designar ID’s e CLASSES)

— Capacidade de aplicação de novos conhecimentos

— Criatividade

— Tipografia

— Mockups dos layouts

## SUPORTES A ENTREGAR

— Maquetas em PDF ou JPG

— Pasta com os ficheiros de implementação (html, css, jpg, etc)

— Publicação online (em servidor a fornecer pelo docente)

## REFERÊNCIAS

http://www.semplicelabs.com/

https://onepagelove.com/

https://www.awwwards.com/websites/single-page/

## DATA DE ENTREGA

a definir pelo docente. 

Este projecto pode ser realizado individualmente ou em grupos de 2 alunos. Bom trabalho. 

