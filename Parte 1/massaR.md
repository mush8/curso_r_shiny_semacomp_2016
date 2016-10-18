# Primeiros passos com R

##### O R tem uma sintaxe muito simples! Porém, alguns cuidados sempre devem ser tomados

* Como em muitas linguagens, letras maiúsculas e minúsculas são diferenciadas. Ou seja, "A" e "a" são considerados símbolos diferentes e devem referir a variáveis diferentes.
* Geralmente, todos os símbolos [alfanuméricos](https://pt.wikipedia.org/wiki/Alfanum%C3%A9rico) são permitidos.
* Para comentar uma linha, basta utilizar o símbolo Hash ('#') no começo que até o final da mesma será considerada comentário.
* Quando for atribuir valor a alguma variável, utilize '<-'
* Para interpretar uma linha de código escrita fora do Console, pressione "Ctrl+Enter". Caso tenha mais de uma linha, selecione as linhas desejadas e pressione os mesmos botões.


```r
# Comentários    Minicurso R/Shiny    SEMaComp 2016    20/10/2016

semacomp <- 2016
SEMACOMP <- 6102
```

## Obtendo ajuda com funções e recursos



R possui embutido um sistema de ajuda. Para obter mais informação sobre uma função específica, por exemplo `solve`, o comando é:

```r
help(solve)
```
Outra alternativa é:

```r
?solve
```
Digite estes comandos no console do RStudio e veja os resultados.

Para um recurso especificado por caractéres especiais, o argumento deve ser envolto em aspas duplas ou simples, tornado-o um caracter. Isto também é necessário ára algumas palavras reservadas do R com algum significado sintático, exemplo: `if`, `for` e `function`.

```r
help("[[")
# ou
help("if")
# ou 
help("function")
```

Na marioria das instalações de R um sistema geral de ajuda está disponível, e pode acessa-lo com:

```r
help.start()
```

o que irá abrir seu navegador de internet, e permitirá navegar pelas páginas de ajuda com tutoriais e informações técnicas da linguagem. Na página de ajuda há também um "Motor de Busca" muito útil, pois contém acesso à todo o sistema CRAN, podendo ser usado para obter conhecimento amplo sobre a linguagem R e seus pacotes. Pode acessar o motor de busca diretamente do R com o seguinte comando:

```r
??solve
```

Que trará um resultado diferente ao do comando anterior `?solve`, teste em sua máquina e veja a diferença. Para avançar em seus estudos do R irá precisar usar, e bastante, o `help`. :)

## Executando comandos de arquivos

No RStudio temos a opção de abrir um editor de texto e escrever nosso código. Abrimos um arquivo novo para códigos R no menu `File -> New File -> R script`. Este arquivo nos permite escrever, editar e organizar nosso código (*script*), porém, diferente do console, os comandos não são executados ao apertar `Enter`. Para executar os comandos em um arquivo de texto há várias formas, a mais simples é colocar seu cursor na linha do comando que deseja executar e apertar `Ctrl + Enter`.

Uma outra forma é clicar no botão `Source` disponibilizado no canto superior direito do seu painel do editor de texto. Esta opção irá executar todos os comandos do seu arquivo, não só uma linha.

Uma outra forma utilizada, normalmente para programas mais complexos, é a função `source`. Esta função recebe como parâmetro o nome de um arquivo (incluso seu caminho referencial à partir de seu diretório de trabalho - veremos isto mais adiante). Considerando um exemplo, em que teriamos um arquivo chamado `comandos.R` em nosso diretório de trabalho, podemos executa-lo com o seguinte comando:

```r
source("comandos.R")
```

O comando `source` executa seu arquivo de forma silenciosa, ou seja, não mostra resultado algum da compilação do arquivo. Caso queira ver o resultado da execução, basta acrescentar a opção `echo= TRUE`, conforme abaixo::

```r
source("comandos.R", echo=TRUE)
```

Vamos agora para o próximo capítulo e começar a criar nossos primeiros *scripts*!