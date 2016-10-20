# Compartilhando seu app

Vimos já o suficiente para que desenvolva os seus próprios aplicativos Shiny.

É claro, há muitas mais funções e possibilidades, mas com as ideias já vistas você consegue se aprofundar, com segurança, em futuros projetos.

A complexidade dos seus apps dependeram de sua lógica em R, e complementos na programação Shiny. Mas o importante é resolver problemas reais, atender alguma necessidade.E para isso é necessário disponibilizar seu app Shiny na web. 
Compartilhar é a parte central dos aplicativos Shiny. Para publicar seu app Shiny, basta trocar seu computador por um servidor na nuvem, e o RStudio pode tornar isso bem fácil.

Inicialmente, recomendo que coloque todos os arquivos de seu app em uma pasta. E se você está utilizando o padrão de arquivo único para seu app, o nome do arquivo deve ser `app.R`.

Caso esteja utilizando a modalidade de dois arquivos separados, seus dois arquivos devem ter os nomes de `ui.R` e `server.R` com as respectivas funções em cada um `ui` e `server`. E não é necessário a chamada de `shinyApp(ui = ui, server = server)`.

Com seus arquivos organizados, quero que conheça o [shinyapps.io](shinyapps.io).

Shinyapps.io é um servidor mantido pela empresa RStudio, onde você pode disponibilizar seus aplicativo online. O servidor é fácil de acessar e usar, e oferece uma opção gratuíta para seu uso. E serve para pequenos apps de teste ou aplicativos com os quais queira impressionar seu professor ou professora daquela disciplina bem difícil.

Como estamos utilizando os PCs da universidade, não recomendo conectar o RStudio agora.
Mas fica como tarefa de casa submeter seu primeiro aplicativo. Para publica-lo você precisa criar uma conta no site [shinyapps.io](shinyapps.io) e seguir as orientações de como conectar seu RStudio com a sua conta.

Por enquanto sugiro que siga para o desafio, boa sorte! :)
