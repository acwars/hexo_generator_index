# hexo-generator-index-berry

Index generator for [Hexo].

It generates an archive of posts on your homepage, according to the `index` or `archive` layout of your theme.

## Installation

``` bash
$ npm install @acwars/hexo-generator-index --save
```

## Options

Add or modify the following section to your root _config.yml file

``` yaml
index_generator:
  path: ''
  per_page: 10
  order_by: -date
  pagination_dir: page
```

- **path**: Root path for your blog's index page. 
  - default: ""
- **per_page**: Posts displayed per page.
  - default: 'config.per_page' as specified in the official Hexo docs (if present), otherwise '10'
  - `0` disables pagination
- **order_by**: Posts order. 
  - default: date descending
- **pagination_dir**: URL format.
  - default: 'page'
  - `awesome-page` makes the URL ends with 'awesome-page/<page number>' for second page and beyond.

## Usage

The `sticky` parameter in the post Front-matter will be used to pin the post to the top of the index page. Higher `sticky` means that it will be ranked first.

```yml
---
title: Hello World
date: 01/01/15 8:46:25 PM
sticky: 100
---
```

## License

MIT
