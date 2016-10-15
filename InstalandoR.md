# Instalando R e RStudio e Shiny

Para iniciar com R você primeiro precisa adquirir uma cópia. R e RStudio são ambos gratuitos.

## Como baixar e instalar R

R é mantido por uma equipe internacional de desenvolvedores que fazem a linguagem disponível através da página web [**The Compehensive R Archive Network**](cran.r-project.org) (A rede compreensiva de arquivo R). No topo da página há três links que te direcionam às instalações em: Windows, Mac ou Linux.

### Binário ou da Fonte
O R pode ser instalado de arquivos binários pré-compilados (*precompiled binaries*) ou construído da fonte (*built from source*) para qualquer sistema operativo. Para Windows e Mac, instalar dos arquivos binários é bem fácil. O binário vem carregado com seu próprio instalador. Apesar de você poder contruir da fonte nestas plataformas, o processo é bem mais complicado e não irá oferecer muitos benefícios à maioria dos usuários. Para Linux, o oposto é verdade. Arquivos binários pré-compilados podem ser encontrados para alguns sistemas, mas é muito mais comum construir R de arquivos fontes. As páginas de download em [**CRAN**](https://cran.r-project.org/) fornece informações sobre contruir da fonte para Windows, Mac e Linux.

### 32-bit ou 64-bit

R vem em duas versões 32-bit e 64-dit. Ambas as versões utilizam inteiros de 32-bits, ou seja, sua precisão numérica é a mesma. A diferença ocorre em como cada versão gerencia a memória. 64-bit R usa 64-bit ponteiros de memória, e 32-bit R usa 32-bit ponteiros de memória. Isto significa que o R de 64-bits tem um espaço maior para usar (e procurar). Como regra, 32-bit R é mais rápido, mas nem sempre. Em ambas as versões, os vetores são limitados a algo em torno de 2 bilhões de elementos. Se o seu sistema não suporta programs de 64-bits, ou sua memória principal (RAM) for menor que 4 GB, então instale a versão de 32-bits. O instalador do Windows e Mac irão automaticamente instalar a versão de 64-bits caso o seu sistema suporte.

### Windows

Para instalar R no Windows clica no link *"Download R for Windows"*, à partir siga as instruções no site e do instalador. O instalador que baixar do site irá instalar R em seu sistema. Você precisará ter privilégios de administração para instalar novos programas em sua máquina.

### Mac

Para instalar R em um Mac, clique no link *"Download R for Mac"*. Um instalador irá te guiar durante a instalação, ele deixa você personalizar a instalação, mas o padrão irá atender a maioria dos usuários.

### Linux

R vem pré-instalado em várias distribuições Linux, mas se quiser a versão de R mais atualizada precisará instala-la. O [**site CRAN**](https://cran.r-project.org/) disponibiliza os arquivos para contruir R da fonte em Debian, Redhat, SUSE, e Ubuntu no link *"Download R for Linux"*. O procedimento exato de instalação varia dependendo da distribuição Linux em uso. CRAN oference os arquivos fontes com arquivos README que explicam como instala-los.

## Usando R

R não é um programa, é uma linguagem de programação, como C, C++, Python ou UNIX. Você usa R escrevendo comandos na linguagem R e pedindo para seu computador interpreta-los. Há pessoas que preferem utilizar R na janela terminal UNIX - como nos filmes de hackers de 1980... Mas na atualidade temos as IDEs (Interfaces de Desenvolvimento), as quais auxiliam muito

### Como baixar e instalar RStudio

## Instalando Shiny

## Outras referências
Em sistema Ubuntu, realizar até o passo 4 deste tutorial:
* https://www.digitalocean.com/community/tutorials/how-to-set-up-r-on-ubuntu-14-04
* e instalar o RStudio https://www.rstudio.com/

Em sistema Windows, seguir as instalações em:
* https://cran.r-project.org/
* https://www.rstudio.com/products/rstudio/download3/

Após instalar o R e RStudio, aplicar o comando abaixo para instalar o:
* install.packages("shiny")