# Criar Listas Ordenadas e Desordenadas

Em HTML por vezes temos que criar listas *e.g.* lista de contactos numa aplicação de páginas brancas, ou a lista de hiperligações recomendadas para restaurantes num website de review de restaurantes, ou uma lista de outras notícias num website noticioso.

A criação de listas é relativamente simples e o HTML incorpora dois tipos de listas fundamentais: Listas não ordenadas (unordered lists `ul`) e ordenadas (ordered lists `ol`).

## Listas não ordenadas (UL)

Estas listas são as mais comuns são produzidas pela tag `ul` (unordered list). Dentro dessa tag `ul` cada elemento da lista é indicado pela tag `li`\sidenote{• Elemento 1\\
• Elemento 2\\
• Elemento 3\\
• Elemento 4}.

```html
<ul>
      <li>Elemento 1</li>
      <li>Elemento 2</li>
      <li>Elemento 3</li>
      <li>Elemento 4</li>
</ul>
```

## Listas ordenadas (OL)

Estas listas são menos comuns mas também importantes. São utilizadas quando se pretende que os elementos possuam um número de ordenação e são definidas pela tag `ol`\sidenote{1. Elemento 1\\
2. Elemento 2\\
3. Elemento 3\\
4. Elemento 4}.

```html
<ol>
      <li>Elemento 1</li>
      <li>Elemento 2</li>
      <li>Elemento 3</li>
      <li>Elemento 4</li>
</ol>
```

As listas ordenadas podem ser personalizadas para começar em valores diferentes do 1, bastando para isso adicionar a propriedade start à tag `OL`\sidenote{20. Elemento 1\\
21. Elemento 2\\
22. Elemento 3\\
23. Elemento 4}.

```html
<ol start=20>
      <li>Elemento 1</li>
      <li>Elemento 2</li>
      <li>Elemento 3</li>
      <li>Elemento 4</li>
</ol>
```

é também possível alterar a numeração a meio de uma lista bastando para tal indicá-lo com a propriedade `value`\sidenote{1. Elemento 1\\
10. Elemento 2\\
11. Elemento 3\\
12. Elemento 4}

```html
<ol>
      <li>Elemento 1</li>
      <li value=10>Elemento 2</li>
      <li>Elemento 3</li>
      <li>Elemento 4</li>
</ol>
```

## Utilização de listas

As listas são muitas vezes utilizadas para criar sistemas de navegação com menus e submenus uma vez que podem ser colocadas listas dentro de listas (*nesting*) permitindo dessa forma criar hierarquias complexas.

Por exemplo a criação de um sistema de navegação com submenu pode incluir algo semelhante ao seguinte código html.

```html
<ul>
  <li><a href="/">Home</a></li>
  <li><a href="/">Trabalhos</a>
    <ul>
      <li><a href="/ceramica.html">Cerámica</a></li>
      <li><a href="/ilustracao.html">Ilustração</a></li>
      <li><a href="/video.html">Vídeo</a></li>
    </ul>
  </li>
  <li><a href="/mapa.html">Localicação</a></li>
  <li><a href="/contactos.html">Contactos</a></li>
</ul>
```

É importante notar que a introdução de um submenu deve ser feito sempre dentro de um elemento `li`. O standard do HTML 5 exige que os únicos elementos hierarquicamente abaixo de um `ul` sejam `li`. Apesar de outras formas serem ainda assim renderizadas pelos browsers, tal é incorrecto.

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
