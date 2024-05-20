# Compilação no Windows
Esse repositório irá te ajudar a realizar a instalação de maneira correta direto no código fonte do Windows. Então possui duas parte diferentes, a primeira é a do requisitos do sistema e como instalar os softwares necessários, a segunda é a da compilação do CARLA no sistema. Antes de dar inicio siga essas etapas que sua instalação será bem sucedida.<br/>
<br/>
O processo de instalação leva em torno de (4 horas ou mais) por isso é interessante ler com atenção o guia, pois exige varios software important, então precisa analisisar cada processo da instalação.<br/>
<br/>
Caso precise de mais informação tem o [Documento do CARLA](https://carla.readthedocs.io/en/0.9.15/build_windows/) que pode ajudar, porém aqui será adicionado algumas informações que não possui na documentação, caso possua algum erro de instalação terá o tópico falando a respeito.

<br/>

- [Primeiro Passo: Pré-Requisitos](#primeiro-passo-pr%C3%A9-requisitos)
  - [Requisitos do Sistema](#requisitos-do-sistema)
  - [Requisitos do Software](#requisitos-do-software)
    - [Primeiras Instalações](#primeiras-instala%C3%A7%C3%B5es)

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

# Primeiro Passo: Pré-Requisitos
Nessa processo vai ser instalados pequenos softwares e essenciais para o sistema e as principais dependencias do Python, sendo necessárias antes de contruir o CARLA.<br/>

# Requisitos do Sistema

Aqui será mostrado quais os requisitos precisam ter em sua máquina:<br/>
<br/>
- **sistema x64:** O simulador precisa executar em qualquer Windows com 64 bits.<br/>
- **165 GB de disco livre:** Somente o CARLA levará 32 GB, e os outros principais softwares que estão relacionados (incluindo a Unreal Engine) utilizarão pelo menos 133 GB.<br/>
- **GPU adequada:** Nesse caso será necessário uma GPU dedicada para rodar as simulações realistas, ou de minimo 6 GB, porém o mais recomendado seria uma de 8 GB.<br/>
- **Conexão de Internet e 2 portas TCP:** Ter uma boa conexão com a internet para rodar melhor as simulações e não ter problemas de conexão.<br/>

# Requisitos do Software<br/>
Essa parte seria interessanter possuir os  softwares adequados instalados em seu computador para que não haja algúm problema de compilação, o caminho de ambiente devem estar dentro da variável de ambiente utilizando o diretório<code>bin</code></li>

## Primeiras Instalações

- [CMake:](https://cmake.org/download/) tem a finalidade de gerar arquivos de compilação a partir de arquivos de compilação simples.
- [Git:](https://git-scm.com/downloads) seria um controle de versões para gerenciar o repositório CARLA.
- [Make:](https://gnuwin32.sourceforge.net/packages/make.htm) ele gera os executáveis, sendo necessário utilizar a **versão 3.81**, ou a compilação pode ocorrer falhas. E se for preciso verificar a versão que você está utilizando em seu PATH, através desse comando. <code>make --version</code></li>
- [7Zip:](https://www.7-zip.org/) seria um software de compressão de arquivos, descompactando automaticamente arquivos de ativos evitando erros de compilação de arquivos grandes sendo extraídos incorretamentes.
- [Python3 x64:](https://www.python.org/downloads/) seria a principal linguagém de scripts do CARLA. Instale a versão x64, pois ter a versão x32 pode comflitar e ocorrer erros. 

# Requisitos

