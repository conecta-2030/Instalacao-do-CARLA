# Compilação no Windows
Esse repositório irá te ajudar a realizar a instalação de maneira correta direto no código fonte do Windows. Então possui duas parte diferentes, a primeira é a do requisitos do sistema e como instalar os softwares necessários, a segunda é a da compilação do CARLA no sistema. Antes de dar inicio siga essas etapas que sua instalação será bem sucedida.<br/>
<br/>
O processo de instalação leva em torno de (4 horas ou mais) por isso é interessante ler com atenção o guia, pois exige varios software important, então precisa analisisar cada processo da instalação.<br/>
<br/>
Caso precise de mais informação tem o [Documento do CARLA](https://carla.readthedocs.io/en/0.9.15/build_windows/) que pode ajudar, porém aqui será adicionado algumas informações que não possui na documentação, caso possua algum erro de instalação terá o tópico falando a respeito.

<br/>

- [Primeiro Passo: Pré-Requisitos](#primeiro-passo-pr%C3%A9-requisitos)
  - [Requisitos do Sistema](#requisitos-do-sistema)
  - [Requisitos do Software](#requisitos-do-software-)
    - [Primeiras Instalações](#primeiras-instala%C3%A7%C3%B5es)
    - [Dependências do Python](#depend%C3%AAncias-do-python)
    - [Principais Instalações](#principais-instala%C3%A7%C3%B5es)
      - [Visual Studio 2019](#visual-studio-2019)
      - [Unreal Engine](#unreal-engine)

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

# Requisitos do Software <br/>
Essa parte seria interessanter possuir os  softwares adequados instalados em seu computador para que não haja algúm problema de compilação, o caminho de ambiente devem estar dentro da variável de ambiente utilizando o diretório<code>bin</code></li>

## Primeiras Instalações

- [CMake:](https://cmake.org/download/) tem a finalidade de gerar arquivos de compilação a partir de arquivos de compilação simples.
- [Git:](https://git-scm.com/downloads) seria um controle de versões para gerenciar o repositório CARLA.
- [Make:](https://gnuwin32.sourceforge.net/packages/make.htm) ele gera os executáveis, sendo necessário utilizar a **versão 3.81**, ou a compilação pode ocorrer falhas. E se for preciso verificar a versão que você está utilizando em seu PATH, através desse comando. <code>make --version</code></li>
- [7Zip:](https://www.7-zip.org/) seria um software de compressão de arquivos, descompactando automaticamente arquivos de ativos evitando erros de compilação de arquivos grandes sendo extraídos incorretamentes.
- [Python3 x64:](https://www.python.org/downloads/) seria a principal linguagém de scripts do CARLA. Instale a versão x64, pois ter a versão x32 pode dar conflito e ocorrer erros, então é aconselhável desinstalar. 

## Dependências do Python
Apartir de algumas versões, pode ser instalado o PythonAPI no CARLA, como as versões do CARLA 0.9.12 ou superior, é preciso ter atualização do *pip* tendo uma verção mais atualizado acima da 20.3. Para verificar se possui essa versão adequada, utilize o seguinte comando:

    pip3 -V

Se for preciso atualizar:

    pip3 install --upgrade pip

Sendo preciso intalar algumas dependências do Python:

    pip3 install --user setuptools
    pip3 install --user wheel

# Principais Instalações
## Visual Studio 2019

Será preciso ter a versão do Visual Studio 2019, pois as versões antigas podem conflitar com versões do CARLA 0.9.12 ou superior. Clique [aqui](https://developerinsider.co/download-visual-studio-2019-web-installer-iso-community-professional-enterprise/) para acessar o site oficial, e escolha a versão **Comunidade** que seria a gratuita. E utilize o instalador do Visual Studio para instalar 3 elementos importantes:

- **SDK Windows 8.1 ou Superior** Selecione essa opção na parte de *Detalhes da Instalação* ou até mesmo vá em *Componentes Individuais* e procure a opção de *SDKs, bibliotecas e estruturas*. No nosso caso utilizamos o **Windows 11**, e selecionamos todos os **SDKs Windows 10 e 11**, para não ocorrer algum erro na instalação.
- **X64 Conjunto de ferramentas do Visual C++**. Na sessão de *Cargas de Trabalho*, escolha **Desenvolvimento de área de trabalho com C++**. Com isso será habilitado um prompt comando x64 usado para a compilação. Veja com atenção se foi instalado o correto, tome cuidado para não abrir o **<code>x86_x64</code></li>**. <code>Windows</code></li><code>x64</code></li>
- **.NET Framework 4.6.2**. La na sesão *Cargas de trabalho*, selecione **.NET desktop development** e em *Painel de instalação*, esse processo será essencial para contruir o Unreal Engine.<code>.NET Framework 4.6.2 development tools</code></li>

# Unreal Engine

O CARLA apartir da versão 0.9.12 utiliza a versão da Unreal Engine 4.26, esse patch que seria uma forma de atualização melhorada, o CARLA ja possui esse sistema específico.
Antes de começar o processo de baixar a UInreal, **é preciso ter uma conta vinculada ao GitHub da Unreal Engine**, caso tenha uma dúvida siga [esse guia](https://www.unrealengine.com/en-US/ue-on-github) antes de iniciar a instalação.

Para compilar a versão da Unreal Engine, utilize esse comando:

1. Entre em um terminal e deixe no caminho sistema **C:\>**, e clone a Unreal no caminho desejado:

       git clone https://github.com/EpicGames/UnrealEngine.git

Ou se precisar, utilize a versão da documentação, caso ocorra algum erro, entre no GitHub e pegue o link da versão da Unreal 4.26.2 e faça o mesmo precesso acima dando o **git clone**.





