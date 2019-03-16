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
