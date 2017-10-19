title: Primeiros passos
---

{% youtube 0m2HnATkHOk %}

Assim que o Hexo tiver instalado, execute os seguintes comandos para inicializar o Hexo no diretório `<site>`.

``` bash
$ hexo init <site>
$ cd <site>
$ npm install
```

Uma vez inicializado, o diretório se projeto ficará assim:

``` plain
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└── themes
```

### _config.yml

É o arquivo de [configuração](configuration.html) do site. Você pode configurar a maioria das definições aqui.

### package.json

Dados da aplicação, O [EJS](http://embeddedjs.com/), [Stylus](http://learnboost.github.io/stylus/) e o [Markdown](http://daringfireball.net/projects/markdown/) são renderizadores que já são instalados por padrão. Se quiser, pode desinstalá-los mais tarde.
``` json package.json
{
  "name": "hexo-site",
  "version": "0.0.0",
  "private": true,
  "hexo": {
    "version": ""
  },
  "dependencies": {
    "hexo": "^3.0.0",
    "hexo-generator-archive": "^0.1.0",
    "hexo-generator-category": "^0.1.0",
    "hexo-generator-index": "^0.1.0",
    "hexo-generator-tag": "^0.1.0",
    "hexo-renderer-ejs": "^0.1.0",
    "hexo-renderer-stylus": "^0.2.0",
    "hexo-renderer-marked": "^0.2.4",
    "hexo-server": "^0.1.2"
  }
}
```

### scaffolds

É o diretório onde ficarão os [_scaffolds_](writing.html#Scaffolds), que funcionarão como _esqueletos_. Quando você cria uma nova publicação, o Hexo se baseia no _scaffold_ para criar o novo arquivo.

### source

É a pasta do código-fonte. É aqui onde ficará todo o conteúdo do seu site. O Hexo ignora pastas e arquivos ocultos ou que estiverem prefixados com `_` (underline) - exceto a pasta de `_posts`.

Arquivos renderizáveis (por exemplo, Markdown, HTML) serão processados e colocados na pasta `public`, enquanto outros arquivos serão apenas copiados.

### themes

É o diretório onde ficará o [tema](themes.html). O Hexo gera o site estático combinando o conteúdo com o tema.
