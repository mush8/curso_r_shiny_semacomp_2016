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

Uma alternativa é:

```r
?solve
```

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

o que irá abrir seu navegador de internet, e permitirá navegar pelas páginas de ajuda com tutoriais e informações técnicas da linguagem. Na página de ajuda há também um "Motor de Busca" muito útil, pois contém acesso à todo o sistema CRAN, podendo ser usado para obter conhecimento amplo sobre a linguagem R e seus pacotes.