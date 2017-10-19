title: Configuração
---
Você pode modificar as configurações do site no `_config.yml`, ou em algum outro [arquivo que você definir](#Using-an-Alternate-Config).

### Site

Definição | Descrição
--- | ---
`title` | O título do seu site
`subtitle` | O subtítulo do seu site
`description` | A descrição do seu site
`author` | Seu nome
`language` | O idioma do seu site. Utilize o código [ISO-639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) de duas letras. O padrão é `en`.
`timezone` | O fuso-horário do seu site. Por padrão, o Hexo se baseia na configuração do seu computador. Você pode encontrar mais informações à respeito de fuso-horários [aqui](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). Alguns exemplos são `America/Sao_Paulo`, `Japan`, e `UTC`.

### URL

Definição | Descrição | Padrão
--- | --- | ---
`url` | A URL do seu site |
`root` | O diretório raiz do seu site |
`permalink` | O formato dos [links permanentes](permalinks.html) dos artigos | `:year/:month/:day/:title/`
`permalink_defaults` | O valor padrão para cada segmento dos links permanentes |

{% note info Usando subdiretórios %}
Se o seu site estiver em um subdiretório, (como `http://exemplo.org/blog`), defina `url` como `http://exemplo.org/blog` e `root` como `/blog/`.
{% endnote %}

### Diretórios

Definição | Descrição | Padrão
--- | --- | ---
`source_dir` | A pasta dos códigos-fontes, onde ficará o conteúdo | `source`
`public_dir` | Onde o site estático será gerado | `public`
`tag_dir` | Diretório de _tags_ | `tags`
`archive_dir` | Onde o conteúdo ficará arquivado | `archives`
`category_dir` | Diretório cas categorias | `categories`
`code_dir` | Include code directory (subdiretório de `source_dir`) | `downloads/code`
`i18n_dir` | i18n directory | `:lang`
`skip_render` | Paths not to be rendered. You can use [glob expressions](https://github.com/isaacs/minimatch) for path matching |

### Writing

Setting | Description | Default
--- | --- | ---
`new_post_name` | The filename format for new posts | `:title.md`
`default_layout` | Default layout | `post`
`titlecase` | Transform titles into title case? | `false`
`external_link` | Open external links in new tab? | `true`
`filename_case` | Transform filenames to `1` lower case; `2` upper case | `0`
`render_drafts` | Display drafts? | `false`
`post_asset_folder` | Enable the [Asset Folder](asset-folders.html)? | `false`
`relative_link` | Make links relative to the root folder? | `false`
`future` | Display future posts? | `true`
`highlight` | Code block settings |

### Category & Tag

Setting | Description | Default
--- | --- | ---
`default_category` | Default category | `uncategorized`
`category_map` | Category slugs |
`tag_map` | Tag slugs |

### Date / Time format

Hexo uses [Moment.js](http://momentjs.com/) to process dates.

Setting | Description | Default
--- | --- | ---
`date_format` | Date format | `YYYY-MM-DD`
`time_format` | Time format | `HH:mm:ss`

### Pagination

Setting | Description | Default
--- | --- | ---
`per_page` | The amount of the posts displayed on a single page. `0` disables pagination | `10`
`pagination_dir` | Pagination directory | `page`

### Extensions

Setting | Description
--- | ---
`theme` | Theme name. `false` disables theming
`deploy` | Deployment setting


### Include/Exclude Files or Folders

In the config file, set the include/exlude key to make hexo explicitly process or ignore certain files/folders.

Setting | Description
--- | ---
`include` | Hexo defaultly ignore hidden files and folders, but set this field will make Hexo process them
`exclude` | Hexo process will ignore files list under this field

Sample:
```yaml
# Include/Exclude Files/Folders
include:
  - .nojekyll
exclude:
  - .DS_Store
```

### Using an Alternate Config

A custom config file path can be specified by adding the `--config` flag to your `hexo` commands with a path to an alternate YAML or JSON config file, or a comma-separated list (no spaces) of multiple YAML or JSON files.

``` bash
# use 'custom.yml' in place of '_config.yml'
$ hexo server --config custom.yml

# use 'custom.yml' & 'custom2.json', prioritizing 'custom2.json'
$ hexo server --config custom.yml,custom2.json
```

Using multiple files combines all the config files and saves the merged settings to `_multiconfig.yml`. The later values take precedence. It works with any number of JSON and YAML files with arbitrarily deep objects. Note that **no spaces are allowed in the list**.

For instance, in the above example if `foo: bar` is in `custom.yml`, but `"foo": "dinosaur"` is in `custom2.json`, `_multiconfig.yml` will contain `foo: dinosaur`.

