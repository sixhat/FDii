# Tipografia

\textsc{A tipografia assume um papel primordial} na comunicação visual e isto é naturalmente também importante nas páginas Web. Apesar de a programação de uma página conter o texto num formato agnóstico, é possível definir todos os aspectos de tipografia que o browser deve utilizar para renderizar esse bloco de texto.

É no entanto possível não dar nenhuma indicação sobre as características tipográficas do texto da página web, sendo que nesses casos o browser irá assumir um conjunto de padrões e aplicá-los ao texto existente no HTML.

Para evitar isso é importante que o web designer especifique claramente qual o tipo de fonte que quer utilizar.

O standard define que qualquer fonte que esteja instalada no sistema operativo do utilizador possa ser utilizada, assim como qualquer fonte que possa ser descarregada em formato apropriado, aquando do carregamento da página web.

A primeira propriedade que normalmente podemos personalizar numa fonte é a cor com que queremos que ela seja desenhada:

```css
.alerta {
  color: #FF0000;
}
```

O exemplo anterior define a cor do texto de todos os elementos que possuam a classe `alerta` para vermelho. 

Naturalmente muitas vezes é desejável alterar outras propriedades das fontes. 

```css
font-family
font-size
font-style
font-variant
font-weight
```

## font-family

Para utilizar uma determinada fonte é necessário definir a família da fonte que se quer utilizar. No CSS isso é conseguido definindo a propriedade **font-family** que pode receber uma lista de fontes separadas por vírgulas e.g.

```css
p {
  font-family: “Arial”, “Roboto”, sans-serif;
}
```

Neste exemplo os elementos do tipo `P` serão renderizados por uma de três fontes, “Arial”, “Roboto” ou a fonte sem serifa que o browser utilizar por defeito. A prioridade de utilização será dada pela primeira fonte da lista que o browser conhecer, passando às opções seguintes sempre que as fontes mais à esquerda não estejam disponíveis.

No exemplo anterior é ainda possível ver que utilizamos um nome genérico para fontes sem serifa, o **sans-serif**. É possível definir famílias de fontes genéricas que os browsers interpretarão de acordo com os padrões definidos pelo programador. As famílias genéricas que todos os browsers suportam são o **sans-serif** anterior e ainda o **serif** para fontes serifadas, **cursive** para fontes cursivas que imitam a escrita humana, **fantasy** para fontes de fantasia e ilustração, e **monospace** para fontes monoespaçadas. 

Normalmente na especificação das fontes a utilizar não é necessário incluir as aspas quando o nome da fonte não tem espaços. No exemplo anterior **Arial** e **Roboto** podiam ter sido escritas sem as aspas. No caso de utilizarmos fontes com espaços no nome então é necessário utilizar as aspas e.g. “Times New Roman”.

## font-size

A definição do tamanho da fonte é feito com **font-size** como por exemplo:

```css
div#margem {
  font-size: 22px;
}
```

Neste exemplo a `div` com o `id` **margem** vai utilizar uma font como tamanho de `22px`. 

## font-style

Esta propriedade define se a fonte deve ter um das quatro opções: **normal**, **italic**, **oblique** on **inherit**.

```css
header > p {
  font-style: italic;
}
```

\mfc{img/normal-italic-oblique}{Garamond, Garamond Itálico e Garamond Oblíquo}Fonte itálica e oblíqua não são a mesma coisa. Enquanto uma fonte oblíqua apresenta normalmente um eixo inclinado, a fonte itálica é normalmente uma variante mais complexa e inspirada num processo caligráfico. As diferenças não são óbvias em muitas fontes.\sidenote{Mais informação sobre estas diferenças pode ser encontrado em \url{https://en.wikipedia.org/wiki/Oblique_type}}

## font-variant

Algumas vezes é importante definir algumas propriedades especiais para alguns elementos das páginas como por exemplo títulos. Nestas alturas podemos desejar utilizar versaletes\sidenote{\textsc{Em tipografia versaletes são} caracteres maiúsculos com dimensões de caracteres minúsculos. São muito utilizados para chamar a atenção para uma palavra, ou para o início de uma frase.}

```css
.versalete {
  font-variant: small-caps;
  color: darkblue;
}
```

No exemplo anterior os elementos de HTML que possuirem a classe `versalete` serão desenhados a azul escuro e utilizarão versaletes.

## font-weight

O **peso** de uma fonte é definido pela propriedade **font-weigth**. 

```css
.titulo {
  font-weight: bold;
}
```

Os valores típicos possíveis para esta propriedade são um de **normal|bold|bolder|lighter|**número**|initial|inherit**.

Pode-se também definir esta propriedade com um número entre 100 e 900, sendo que uma fonte _normal_ corresponde ao valor de 400 e uma fonte **bold** corresponde a um valor de 700; Quando uma fonte não tem o valor escolhido vai utilizar o valor mais próximo. Por exemplo o Times New Roman possui os pesos 400 e 700 pelo que se especificarmos um peso de 900 o browser utilizará o 700.

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
