#Chega de conversa, mão na massa!

#Operações Básicas e Vetores

## Expressões e Atribuições
Os comandos do R são feitos de **Expressões** e **Atribuições**. **Expressão** é quando os valores são computados, executados no prompt e perdidos. Em **Atribuições** temos os valores computados e atribuidos a uma variável.

Veja dois exemplos abaixo:

```r
#Expressão
2016 + 2016 ^ 20 - 10 / 2016
#Atribuição
SEMaComp <- 20 + 10 * 2016
```
Ah! Os comando de texto podem ser escritos tanto no console do RStudio ou no editor de texto. Quem estiver utilizando o editor de texto, terá acesso à todos seus comandos já compilados anteriormente, basta mover o cursor até a linha e clicar `Ctrl + Enter` para rodar novamente.

Caso esteja utilizando o console, fica uma dica, os comandos compilados anteriormente podem ser acessados com as setas do teclado. Utilizando as setas para cima e para baixo você navega nos comandos anteriores, e pode edita-los e/ou roda-los novamente.


---


## Atribuindo valores e operações básicas
* **Atribuir valor:** Para atribuir um valor a uma variável: nomeie-a e utilize '<-' antes do valor.
```r
minhaVariavel <- 10
```
* **Adição:** valor1 + valor2
```r
soma <- 10 + 20
```
* **Subtração:** valor1 - valor2
```r
sub <- 10 - 20
```
* **Multiplicação:** valor1 * valor2
```r
mult <- 10 * 20
```
* **Divisão:** valor1 / valor2
```r
divis <- 10 / 20
```
* **Potenciação:** valor1 ^ valor2
```r
pot <- 10 ^ 20
# ou
pot <- 10 ** 20
```

*Lembre-se da ordem de prioridade das operações: 1º Potenciação, 2º Multiplicação ou Divisão, 3º Adição ou Subtração.*


---


## Operações Lógicas
* **> ou >= :** *Maior* ou *Maior ou Igual*
* **< ou <= :** *Menor* ou *Menor ou Igual*
* **== ou != :** *Igual* ou *Diferente*
* **& ou | ou ! :** *And* ou *Or* ou *Not*
* **T ou F :** *True* ou *False


---


## Vetores

O R opera em [estruturas de dados](https://pt.wikipedia.org/wiki/Estrutura_de_dados). Um **vetor numérico** é a mais simples delas, que é uma **"coleção ordenada de números"**. Vejamos como funciona a atribuição de um vetor e operações com o mesmo.
* Para "criar" um vetor utilize: nome_Vetor <- c(a1, a2, a3...)

```r
meuVetor <- c(20.0, 15.65, 15.0, 235.0, 70.1)
```

Perceba que utilizamos a função c(), que coloca seus argumentos em uma coleção, ou seja, **c**oncantena-os.

Para vetores temos algumas operações iniciais importantes, que são as seguintes:

* **nome_do_vetor[indice]:** Retorna o valor da posição 'indice' do vetor.
```r
meuVetor[2]
> 15.65 # resposta prevista
```
*Observação: Diferente da linguagem C, na liguagem R o vetor começa no índice 1 e não em 0.*

* **nome_do_vetor <- c(nome_do_vetor, novo_valor):** Forma de adicionar um novo valor ao vetor.
```r
meuVetor <- c(meuVetor, 2016.0)
meuVetor[6]
> 2016.0 # resposta prevista
```
* **nome_do_vetor <- nome_do_vetor[-indice]:** Forma de eliminar o valor da posição 'indice' do vetor ou
* **nome_do_vetor <- nome_do_vetor[-c(indices)]:** Forma de eliminar os valores das posições 'indices' do vetor.
```r
meuVetor <- meuVetor[-c(1, 2)]
```
* **length(nome_do_vetor):** Retorna a quantidade de valores que seu vetor possui.
```r
length(meuVetor)
> 4 # resposta prevista
```

### Também podemos atribuir um Vetor de Caracteres

```r
vetorChar <- c("Ricardo", "Bruno", "Alexandre", "Camila")
```

### Vetores mistos

```r
vetorMix <- c("Ricardo", 12.5, 10, "Bruno")
```

## Exercícios


Bom, está muito fácil né! Só ler, talvez copiar os códigos e testar. rs

Agora que já está entendendo um pouco mais posso começar a cobrar, um pouco mais. ;D

Por favor, experimente com os códigos abaixo e responda as perguntas, para você mesmo(a) por enquanto.

```r
x <- c(20.0, 15.65, 15.0, 235.0, 70.1)
1/x
```
**1) Qual é o resultado de `1/x`?**

```r
x <- c(x, 0, x)
```
**2) Quantos elementos o novo vetor `x` terá? Qual função utilizar para obter o tamanho?**

**3) Caso esteja acostumado com programação, temos em R o laço de repetição com o `for` também. O que acontece se utilizarmos o seguinte código?**

```r
for (i in x){
  print(i)
}
```
**4) É igual à linguagem C? (caso esteja familiarizado com ela)**

**5) Como fariamos para realizar um `for` ao estilo de C?**

**dica:** uma forma rápida de criar um vetor no R é:

```r
a <- 1:10
> [1] 1 2 3 4 5 6 7 8 9 10 # resposta obtida
```

### Filtros em vetores

Vamos supor que queremos filtrar os elementos do nosso vetor original `x` conforme abaixo:

```r
x <- c(20.0, 15.65, 15.0, 235.0, 70.1)
```

A chamada de posição do vetor aceita muito mais do que somente índices como ensinado nesta seção. Podemos realizar filtros inteiro em sua chamada. Por exemplo:

```r
x [ x > 20]
```

**6) O que você obtém com o código acima?**

**7) E o que obtemos no código abaixo?**

```r
x > 20
```

**8) Consegue entender então o que ocorre para obtermos a resposta do exercício 6?**