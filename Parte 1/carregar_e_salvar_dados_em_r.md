# Carregar e Salvar Dados em R

Nesta seção você verá como carregar e salvar dados em R à partir de arquivos simples de texto. O R disponibiliza muitas mais possibilidades, como salvar e carregar dados em arquivos próprios do R e planilhas Excel. Há diversos pacotes que você pode usar para carregar e salvar dados de bancos de dados (MySQL, SQLite, Oracle, PostgreSQL, etc...) e outros programas comuns como SAS e MATLAB.

## Conjuntos de Dados em R

R já vem com diversos conjuntos de dados carregados no pacote `datasets`, o qual está no R base. Estes conjuntos de dados não são muito interessantes... mas te darão uma chance de testar código ou praticar algumas análises sem precisar obter dados de outras fontes. Você pode ver uma lista de conjuntos de dados e uma breve descrição de cada um rodando o seguinte comando:

  ```r
  help(package = "datasets")
  ```
Para usar um conjunto de dados, basta digitar seu nome. Cada conjunto já é pré-salvo em um objeto R. Por exemplo:

  ```r
  iris
  ```
Você deve obter uma resposta parecida com o abaixo: (observação: é um data frame) ;)
  ```
  ##     Sepal.Length Sepal.Width Petal.Length Petal.Width    Species
  ## 1            5.1         3.5          1.4         0.2     setosa
  ## 2            4.9         3.0          1.4         0.2     setosa
  ## 3            4.7         3.2          1.3         0.2     setosa
  ## 4            4.6         3.1          1.5         0.2     setosa
  ## 5            5.0         3.6          1.4         0.2     setosa
  ## 6            5.4         3.9          1.7         0.4     setosa
  ## 7            4.6         3.4          1.4         0.3     setosa
  ## 8            5.0         3.4          1.5         0.2     setosa
  ## 9            4.4         2.9          1.4         0.2     setosa
  ## 10           4.9         3.1          1.5         0.1     setosa
  ```
Contudo, os conjuntos do R não são substitutos para seus próprios dados, os quais você deve aprender como carregar no R. Mas antes de começar, precisamos aprender um pouco sobre o seu *working directory* (diretório de trabalho).

## Diretório de Trabalho

Cada vez que você abre o R, ele se conecta à um diretório em seu computador, o qual R chama de diretório de trabalho (*working directory*). É onde o R irá procurar pro arquivos quando você tentar carrega-los, e é onde o R irá salbar arquivos quando você mandar salva-los. O local de seu diretório de trabalho irá variar de computador para computador. Para determinar qual é o seu diretório do R, use:

  ```r
  getwd()
  ```

Você pode colocar arquivos de dados diretamente na pasta de seu diretório, ou você pode mover seu diretório de trabalho para onde seus arquivos de dados estão. Você pode mover seu diretório de trabalho para qualquer pasta em seu computador com a função `setwd`. Somente dê para a função `setwd` o caminho para seu novo diretório de trabalho. Eu prefiro definir meu diretório de trabalho em uma pasta dedicada ao projeto no qual estou trabalhando no momento. Dessa forma eu mantenho todos os meus dados, códigos, gráficos, e relatórios em um mesmo lugar. Por exemplo:

  ```r
  setwad("~/Users/ricardo/Documents/git_book_curso_semacomp2016")
  ```
No Linux, se o caminho que passar como argumento não iniciar em seu *root*, pasta raíz (é o `~` do endereço acima), o R irá assumir que o endereço dado inicia-se no seu atual diretório de trabalho.

Você pode mudar seu diretório de trabalho clicando em `Session > Set Working Directory > Choose Directory" no menu do RStudio.

Você pode ver quais arquivos estão em seu diretório de trabalho com a função `list.files()`. Se você ver aquele arquivo que quer abrir com este comando, pode abri-lo, pois está no seu diretório. Como abrir seus arquivos é o que veremos agora. :D

## Arquivos Simples de Texto

Arquivos de texto é um dos mais comuns meios de salvar dados. Eles são bem simples e podem ser lidos de diversas formas diferentes. Por esta razão, dados públicos (exceto no Brasil) são colocados neste formato... ou seja, nos Estados Unidos, Europa e grande maioria dos países faz isso. 0o'

Um arquivo de texto simples armazena uma tabela de dados em um documento de texto. Cada linha da tabela é salva em sua própria linha, e uma simples convenção é usada para separar as células em cada linha. Muitas vezes as células são separadas por vírgulas, mas podem também ser separadas por tabulações ("\t"), delimitador *pipe* ("|"), ou qualquer outro caracter. O importante é que cada arquivo utilize um método único para separar células, de forma a minimizar a confusão. Dentro de cada célula, os dados aparece como seria de esperar para vê-lo, como palavras e números.

Todos os arquivos de texto simples podem ser salvos com uma extensão *.txt* (de texto), mas há também alguns que recebem extensões especiais que avisam como suas células estão separadas. Como mencionamos antes, se os dados estão separados por vírgulas, a extensão normalmente é *.csv* (de *comma-separated-values*).

### read.table

Para carregar um arquivo de texto, use o comando `read.table`. O primeiro argumento da função deve ser o nome do arquivo (se estiver em seu diretório de trabalho), ou o caminho até o arquivo (se não estiver no seu diretório de trabalho). Se o caminho do arquivo não começa com seu diretório raíz (*root*), R irá anexa o caminho ao final do caminho que direciona para seu diretório de trabalho. Você pode dar à função read.table outros argumentos também. Os dois mais importantes são `sep` e `header`.

Algo que podemos fazer, para testar nosso potencial de carregar arquivos é, primeiro, salvar um arquivo. Portanto, vamos salvar, com a função `write.csv` o conjunto de dados `iris` visto anteriormente.

  ```r
  write.csv(iris, "iris.csv", row.names = FALSE)
  ```

Após processar este comando rode `list.files()` e confirme se o arquivo `iris.csv` foi criado. Se sim, podemos brincar agora de carrega-lo.
Perceba que o arquivo criado é um *.csv*, ou seja as células estão separadas por vírgulas, então o argumento **sep** de nossa função `read.table` irá receber `sep = ","`. E sabemos que o data frame `iris` possui cabeçalhos, e estes cabeçalhos foram escritos juntos no arquivo criado, logo o argumento **header** irá receber `header = TRUE`. Com isso teremos como carregar nossos dados para um novo data frame, por exemplo, de nome `semacomp_iris`:

  ```r
  semacomp_iris <- read.table("iris.csv", sep = ",", header = TRUE)
  semacomp_iris
  summary(semacomp_iris)
  ```

1) Agora, explique-se o que o argumento `sep` e `header` definem na função `read.table`?

2) Que outros argumentos a função `read.table` possui? e, basicamente, o que cada um faz?

3) Passamos rapidamente a função `write.csv` por praticidade, porém há também a função `write.table`, qual é a diferença entre as duas funções?
4) 
## Fim da Parte 1

Se chegou até aqui, parabéns! Você pode agora respirar um pouco, olhe ao seu redor, ajude algum companheiro. E enfrente o desafio se ainda tiver fôlego. ;D