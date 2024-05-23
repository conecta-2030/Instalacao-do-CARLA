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
- [Segundo Passo: Construção do CARLA](#segundo-passo-constru%C3%A7%C3%A3o-do-carla)
- [Clonar o repositório](#clonar-o-reposit%C3%B3rio)
-  [Obter os ativos](#obter-os-ativos)

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
Antes de começar o processo de baixar a Unreal, **é preciso ter uma conta vinculada ao GitHub da Unreal Engine**, caso tenha uma dúvida siga [esse guia](https://www.unrealengine.com/en-US/ue-on-github) antes de iniciar a instalação. E se precisar saber mais de tutorial, siga esse [vídeo tutorial](https://youtu.be/lLkFA0fPrgs?si=AOt2KZXg1B2QskRL).

Para compilar a versão da Unreal Engine, utilize esse comando:

1. Entre no **Prompt de Comando** e acesse o caminho do sistema **C:\\>**, e clone a Unreal neste caminho:

       git clone https://github.com/EpicGames/UnrealEngine.git

Ou se precisar, utilize a versão da documentação, caso ocorra algum erro, entre no GitHub e pegue o link da versão da Unreal 4.26.2 e faça o mesmo precesso acima dando o **git clone**.

2. Dentro do caminho da Unreal Engine você vai precisar executar os scripts de configuração, então utilize esses comando no '**Prompt de Comando**' dentro da pasta *Unreal Engine*:

       Setup.bat
       GenerateProjectFiles.bat
   
3. Despois desses passos terem sido concluido, na pasta raiz da Unreal abra no Visual Studio 2019 o arquivo <code>UE4.sln</code></li>
 ![Arquivo UE4.sln](https://cdn.discordapp.com/attachments/1135539100468924457/1242459395959296081/image.png?ex=664de9fb&is=664c987b&hm=77d1caa2311a73ea261d0ae0f6afd3f264d260040e9d89b12d846281c79d8e2c&)

  1. Assim que abrir o Visual Studio, vai na aba de compilação e selecione as opções, '***Editor de Desenvolvimento***', '***Win64***' e '***UnrealBiuldTool***', tem que estar igual a imagem abaixo, se precisar de mais informações use esse [guia](https://dev.epicgames.com/documentation/en-us/unreal-engine/building-unreal-engine-from-source?application_version=5.4). <br/>
   
  ![Compilação](https://cdn.discordapp.com/attachments/1135539100468924457/1242462898962436096/Captura_de_tela_2024-05-21_100241.png?ex=664ded3e&is=664c9bbe&hm=2d992cb8dd2fa6bfedea6da2ad00d235a36c4a6200a3605ecf958ecbca2df446&) 

  2. No ***gerenciador de soluções*** clique com o botão direito em *UE4* e selecione *Build*, a imagem abaixo vai te mostrar caso tenha dúvidas.<br/>
  ![Biuld](https://media.discordapp.net/attachments/1135539100468924457/1242462898597527623/image.png?ex=664ded3e&is=664c9bbe&hm=ba29420b90e825e5a04d06e874a6ebcedfa9f961c9397f8559f3e5161a71cd59&=&format=webp&quality=lossless&width=385&height=607)

  3. Assim que for compilado pela primeira vez, acesse a pasta **Unreal Engine** e procure pelo '*UE4Editor.exe*'. Caso não encontre siga esse caminho. <code>Engine\Binaries\Win64\UE4Editor.exe</code></li>

<br/>

|Importante |
:-------|
Antes de dar inicio a segunda parte da instalção, é recomendado reiniciar o computador.

<br/>

# Segundo Passo: Construção do CARLA
## Clonar o repositório

| [Repositório CARLA](https://github.com/carla-simulator/carla)
:-------------------------------------------------------------: |

Caso queira escolher sua versão do CARLA, clique nesse repositório acima e terá acesso a todas as versões, no nosso caso utilizamos a versão 0.9.15.2 que acabou dando certo a instalação, e os erros que derem terá um tópico em específico.

![](https://cdn.discordapp.com/attachments/1135539100468924457/1243188609834553404/Captura_de_tela_2024-05-23_095207.png?ex=6650911d&is=664f3f9d&hm=2b2387641c870aea1c5543a593d7180196c53f6eb06847960ecc5909cb950412&)

Na imagem acima mostra aonde você pode estar pegando o link e clonando o repositório, e clone em um terminal seguindo o mesmo caminho **C:\\>** utilizando o seguinte comando:

    git clone https://github.com/carla-simulator/carla.git

# Obter os ativos

Para ter a versão mais recente é importante obter os ativos atualizados para que não ocorra nenhum conflito na execuções futuras e poder trabalhar com as versões atuais do **CARLA**. Execute o seguinte comando dentro da pasta raiz para adquirir os ativos

    Update.bat

Para poder enxergar comando para executar, a imagem mostra dea melhor forma para visualizar.<br/>
![](https://cdn.discordapp.com/attachments/1135539100468924457/1243199452408320140/Update.png?ex=66509b36&is=664f49b6&hm=ffec85c1ddde212bf70b9b35ce68db1347db0695b1ed3f66df49e897420df030&)

Esses ativos serão baixados e extraídos no local adequado se tiver o 7zip instalado corretamente








