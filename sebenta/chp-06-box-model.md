# O modelo da caixa.

Já vimos como é que diversos elementos HTML podem ser utilizados para definir diversos tipos de conteúdos—cabeçalhos, parágrafos. No entanto ainda não discutimos como é que estes conteúdos são desenhados pelos browsers. Este capítulo vai tentar responder à questão *como é que o browser desenha o conteúdo html?*

## Display

A propriedade **display**\sidenote{Mais informação sobre as diferentes propriedades do \textbf{display} pode ser obtida em \url{https://developer.mozilla.org/en-US/docs/Web/CSS/display}} do CSS permite controlar como os elementos HTML serão posicionados em relação aos seus pares e também definir como é que os elementos HTML seus descendentes se devem organizar. 

- a propriedade **display** define duas qualidades dos elementos quando estão a gerar a caixa onde são desenhados.
  - **tipo de display externo** - ou seja, como é que o elemento se vai inserir no fluxo da página juntamente com os outros elementos.
  - **tipo de display interno** - ou seja, como os elementos filhos se vão distribuir. 

## Block ou inline?

O primeiro aspecto importante a considerar é que os elementos tem que ser colocados no layout da página juntamente com outros elementos. Este fluxo de elementos HTML tem que se ajustar segundo alguma regra. As duas principais alternativas são **block** e **inline**. 

Os elementos em **block** vão ocupar a largura máxima possível do contentor onde estiverem inseridos. Os elementos **inline** pelo contrário vão ocupar apenas o espaço estritamente necessário para albergar o conteúdo. Exemplos de elementos **block** incluem o elemento html *DIV* que serve para criar um bloco estrutural de conteúdo. Por outro lado a tag *A* é um elemento cujo display é feito **inline** uma vez que a âncora estará por exemplo inserida num texto.

- **Block**: utilizados para conteúdos largos, como headings e elementos estruturais
- **Inline**: utilizados para pequenas quantidades de código, por exemplo para um enfatizar uma data ou um email.



Para definir esta propriedade em css basta modificar a propriedade **display**.\sidenote{Exemplo prático disponível em \url{https://codepen.io/sixhat/pen/NJLZRV}}

```css
p {
  display: block;
}
```

```css
p {
  display: inline;
}
```

Nestes exemplos o parágrafo *P* vais ser desenhado ocupando 100% do espaço disponível (**block**) ou utilizando o espaço estritamente necessário (**inline**).

De vez em quando pode-se também remover um elemento do ecrã. Isso também é possível de se fazer utilizando a propriedade **display** com o valor **none**.

```css
p.hidden {
  display: none;
}
```

Neste caso o parágrafo da class `hidden` não será desenhado pelo browser e será removido do fluxo de elementos a desenhados—isto implica que não vai afectar o posicionamento dos restantes elementos.

## Outros valores menos utilizados para o display

Para além dos valores **block**, **inline** e **none**, há também outros menos utilizados mas que convém ter presente na hora de programar uma página web\sidenote{A especificação dos valores para o display foi definida ao longo de diversas versões do CSS. Mais informação sobre o que cada versão do CSS adicionou pode ser encontrada em \url{https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Display\#Specifications}} :

- **inline-block** - elementos formatados com este valor tem um comportamento misto entre inline e block. Enquanto os conteúdos interiores são formatados como um bloco o elemento em si formata-se com sendo inline. 
  -Pode ser útil para fazer sistemas de navegação (menus).
- **list-item** - para fazer com que o elemento se comporte como uma lista com um sinal numa caixa de marca de lista.
- **table\*** - vários valores, fazem com que o elemento se comporte como uma tabela

