# Compartilhando seu app

Vimos já o suficiente para que desenvolva os seus próprios aplicativos Shiny. É claro, que há muitas mais funções e possibilidades. Mas com as noções das ideias já vistas você consegue aprofundar, com segurança, em futuros projetos. E a complexidade dos seus apps dependem de sua lógica em R, e complementos na programação Shiny.

Mas para quê construímos projetos se não compartilhar-mos?!?!

Compartilhar é a parte central dos aplicativos. Para publicar seu app Shiny, basta trocar seu computador por um servidor na nuvem, e o RStudio pode tornar isso bem fácil. Inicialmente, recomendo que coloque todos os arquivos de seu app em uma pasta. E se você está utilizando o padrão de arquivo único para seu app, o nome do arquivo deve ser `app.R`.

Caso esteja utilizando a modalidade de dois arquivos separados, seus dois arquivos devem ter os nomes de `ui.R` e `server.R` com as respectivas funções em cada um `ui` e `server`. E não é necessário a chamada de `shinyApp(ui = ui, server = server)`.

Agora que seu app está em uma pasta exclusiva para ele, abra-o novamente com RStudio e 