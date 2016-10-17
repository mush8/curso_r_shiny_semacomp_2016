# Shiny, como começo?

O pacote shiny disponibilizar onze exemplos já construídos que demonstram como shiny funciona. Cada exemplo é um aplicativo completo e independente.

![Exemplo *Hello Shiny*](01_hello.png)
O exemplo **Hello Shiny** traça o histograma da base `faithful` do R, com um número configurável de divisórias. O usuário pode mudar o número de divisórias com uma barra de deslizamento, e o app responde em tempo real. Vamos utilizar o **Hello Shiny** para explocar a estrutura de um aplicativo Shiny e criar nosso primeiro app.

Para rodar **Hello Shiny**, digite:
```r
library(shiny)
runExample("01_hello")
```

## Estrutura de um aplicativo Shiny

Aplicativos Shiny possuem dois componentes:
* um *script* para interface do usuário
* um *script* de servidor

O código da interface de usuário (**ui**) controla o aspecto visual (*layout*) de seu aplicativo. Ele é definido em um código fonte com nome `ui.R`. Aqui está o código `ui.R` de **Hello Shiny**.

#### ui.R
```r
library(shiny)

# Define um UI para aplicação que desenha um histograma
shinyUI(fluidPage(

  # Título do aplicativo
  titlePanel("Hello Shiny!"),

  # Barra lateral com uma entrada de barra deslizante (slider) para o número de divisórias
  sidebarLayout(
    sidebarPanel(
      sliderInput("divisorias",
                  "Número de divisórias:",
                  min = 1,
                  max = 50,
                  value = 30)
    ),

    # Show a plot of the generated distribution
    mainPanel(
      plotOutput("distPlot")
    )
  )
))
```

Já o código `server.R` contém as instruções que o computador precisa para construir o seu app. Aqui está o código `server.R` para **Hello Shiny**:

#### server.R

```r

```