# Mãos na massa!

Vamos iniciar montando um aplicativo de visualização dos dados `iris`, que vimos anteriormente. 

Bom, como começar? Lembre que falamos sobre dois arquivos `ui.R` e `server.R`? Para este projeto, como nosso código final não será muito grande, iremos criar um único arquivo. Pode então, criar um novo `R script` em seu RStudio (em `File -> New File -> R script`), e dê o nome de `app.R`.

Tendo o arquivo criado, vamos iniciar com a estrutura base para qualquer aplicativo Shiny:

  ```r
  library(shiny)

  ui <- fluidPage(

  )

  server <- function(input, output) {

  }

  shinyApp(ui = ui, server = server)
  ```

Veja que, como incluímos nosso *script* em um único arquivo temos uma nova função `shinyApp(ui = ui, server = server)`. A chamada dessa função recebe dois argumentos, que são os objetos criados `ui` e `server`. Essa função que fará