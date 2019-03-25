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
