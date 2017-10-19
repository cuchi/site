title: Documentação
---
Seja bem-vindo(a) a documentação do Hexo. Case encontre algum problema, você pode consultar o [este guia](troubleshooting.html), abrir uma _issue_ no [GitHub](https://github.com/hexojs/hexo/issues) ou criar um tópico no [Grupo do Google](https://groups.google.com/group/hexo) do Hexo.

## O que é o Hexo?

O Hexo é um framework para criação de blogs rápido, simples e poderoso. Você escreve publicações em [Markdown](http://daringfireball.net/projects/markdown/) (ou outras linguagens) e o Hexo gera os arquivos estáticos com um lindo tema em poucos segundos.

## Instalação

A instalação do Hexo leva poucos minutos. Se você encontrar algum problema e não conseguir encontrar a solução aqui, por favor [abra uma _issue_ no GitHub](https://github.com/hexojs/hexo/issues) e eu tentarei resolver.

### Requisitos

Para instalar o Hexo é bem fácil. Porém, você precisa ja ter instalado o seguinte:

- [Node.js](http://nodejs.org/)
- [Git](http://git-scm.com/)

Se o seu computador já possui estes, parabéns! Apenas instale o Hexo com o npm:

``` bash
$ npm install -g hexo-cli
```

Caso contrário, siga as seguintes instruções para instalar todas as aplicações necessárias.

{% note warn Para usuários de Mac %}
Você pode encontrar alguns problemas para compilar. Primeiro instale o Xcode da App Store. Depois que o Xcode tiver instalado, abra-o e vá até **Preferences -> Download -> Command Line Tools -> Install** para instalar as ferramentas de linha de comando.
{% endnote %}

### Instale o Git

- Windows: Baixe e instale o [git](https://git-scm.com/download/win).
- Mac: Instale usando o [Homebrew](http://mxcl.github.com/homebrew/), [MacPorts](http://www.macports.org/) ou o [instalador](http://sourceforge.net/projects/git-osx-installer/).
- Linux (Ubuntu, Debian): `sudo apt-get install git-core`
- Linux (Fedora, Red Hat, CentOS): `sudo yum install git-core`

### Instale o Node.js

A melhor maneira de instalar o Node.js é com o [Node Version Manager](https://github.com/creationix/nvm).
Seus criadores fizeram um script que realiza a instalação automaticamente:

cURL:

``` bash
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
```

Wget:

``` bash
$ wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
```

Assim que o nvm tiver instalado, reinicie a sessão do terminal e execute o seguinte comando para instalar o Node.js:

``` bash
$ nvm install stable
```

Como alternativa, baixe e execute [o instalador oficial](http://nodejs.org/).

### Instale o Hexo

Assim que todos os requisitos forem instalados, você pode instalar o Hexo com o npm:

``` bash
$ npm install -g hexo-cli
```
