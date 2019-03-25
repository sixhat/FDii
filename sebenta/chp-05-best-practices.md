# Escrever código segundo as melhores práticas

Ao longo das semanas anteriores vimos que é importante que o código `html` e `css` que escrevemos esteja correctamente estruturado. Intuitivamente a sua organização permite uma leitura e compreensão mais rápida e eficaz.

No entanto é necessário ter em atenção que a industria utiliza normalmente convenções que nem sempre são representadas nos _standards_. Essas práticas levam a que se tenha desenvolvido um conjunto de boas práticas cujas regras muitas vezes não estão codificadas em nenhum documento.

Aqui seguem-se alguns conselhos que devem ter quando estiverem a escrever código para os vossos projectos.

## Escrever código que seja compatível com os standards

Muito embora os browsers modernos tenham alguma flexibilidade em interpretarem código que não esteja de acordo com o standards, tal não quer dizer que o venham a fazer no futuro. A escrita de código de acordo com os standards\sidenote{O último standard do HTML publicado é o 5.2 e pode ser encontrado online em \url{https://www.w3.org/TR/html/}} é de primordial importância. Por exemplo:

**Errado:**

```html
<p id="intro">Este texto que <strong>vos deixo</p></strong>
<p id="intro">Não será assim muito extenso.
```

**Correcto:**

```html
<p class="intro">Este texto que <strong>vos deixo<strong></p>
<p class="intro">Não será assim muito extenso.</p>
```

O primeiro caso tem diversos erros nomeadamente a utilização do `id` _intro_ por múltiplas vezes e o *nesting* errado do `p` e do `strong` no final da primeira linha. Na segunda linha o parágrafo não foi fechado com a *tag* correspondente pelo que também está errada. Com alta probabilidade os dois exemplos seriam renderizados pelo browser de forma semelhante. No entanto a primeira forma é claramente errada.

## Utilizar elementos semânticos

O HTML 5 possui mais de 100 elementos diferentes. Apesar de parecerem muitos elementos, eles ajudam a dar significado à página web permitindo aos browsers inferirem o objetivo e importância de cada bloco de conteúdo. O HTML 5 introduziu novos elementos semânticos que facilitam e clarificam o que cada conteúdo é.
