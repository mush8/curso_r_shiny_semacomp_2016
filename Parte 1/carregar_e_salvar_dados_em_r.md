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

## Arquivos Simples de Texto

### read.table

#### sep

#### header

#### na.strings

#### skip and nrow

#### stringAsFactors

### A Família *read*

#### Links HTML

### Salvando Arquivos Simples de Texto