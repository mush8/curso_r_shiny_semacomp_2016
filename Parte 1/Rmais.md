#Chega de conversa, mão na massa!

##Operações Básicas com Vetores

####Expressões e Atribuições
Os comandos do R são feitos de **Expressões** e **Atribuições**. **Expressão** é quando os valores são computados, executados no prompt e perdidos. Em **Atribuições** temos os valores computados e atribuidos a uma variável.

Veja dois exemplos abaixo:

```r
#Expressão
2016 + 2016 ^ 20 - 10 / 2016
#Atribuição
SEMaComp <- 20 + 10 * 2016
```



---


####Atribuindo valores e operações básicas
* **Atribuir valor:** Para atribuir um valor a uma variável: nomeie-a e utilize '<-' antes do valor.
```r
minhaVariavel <- 10 ```
* **Adição:** valor1 + valor2
```r
soma <- 10 + 20```
* **Subtração:** valor1 - valor2
```r
sub <- 10 - 20```
* **Multiplicação:** valor1 * valor2
```r
mult <- 10 * 20```
* **Divisão:** valor1 / valor2
```r
divis <- 10 / 20```
* **Potenciação:** valor1 ^ valor2
```r
pot <- 10 ^ 20```

*Lembre-se da ordem de prioridade das operações: 1º Potenciação, 2º Multiplicação ou Divisão, 3º Adição ou Subtração.*


---


####Operações Lógicas
* **> ou >= :** *Maior* ou *Maior ou Igual*
* **< ou <= :** *Menor* ou *Menor ou Igual*
* **== ou != :** *Igual* ou *Diferente*
* **& ou | ou ! :** *And* ou *Or* ou *Not*
* **T ou F :** *True* ou *False


---


####Vetores

O R opera em [estrutura de dados](https://pt.wikipedia.org/wiki/Estrutura_de_dados). Um **vetor numérico** é a mais simples delas, uma **"coleção ordenada de números"**. Vejamos como funciona a atribuição de um vetor e operações com o mesmo.
* Para "criar" um vetor utilize: nome_Vetor <- c(v1, v2, v3...) 

```r
meuVetor <- c(20.0, 15.65, 15.0, 235.0, 70.1)```

*Utiliza-se a função c() que coloca seus argumentos em uma coleção, ou seja, concantena-os.*
* **nome_do_vetor[indice]:** Retorna o valor da posição 'indice' do vetor.
```r
meuVetor[2]
> 15.65```
*Diferente da linguagem C, na liguagem R o vetor começa no índice 1 e não em 0.*
* **nome_do_vetor <- c(nome_do_vetor, novo_valor):** Forma de adicionar um novo valor ao vetor.
```r
meuVetor <- c(meuVetor, 2016.0)
meuVetor[6]
> 2016.0```
* **nome_do_vetor <- nome_do_vetor[-c(indice)]:** Forma de retirar o valor da posição 'indice' do vetor.
```r
meuVetor <- meuVetor[-c(1)]```
* **length(nome_do_vetor):** Retorna a quantidade de valores que seu vetor possui.
```r
length(meuVetor)
> 5
```

#####Também podemos atribuir um Vetor de Caracteres:
```r
vetorChar <- c("Ricardo", "Bruno", "Alexandre", "Camila")```



  


