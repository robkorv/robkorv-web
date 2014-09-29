robkorv-web
===========

Build with [jekyll](https://github.com/jekyll/jekyll)

## needs

* [ruby](https://github.com/ruby/ruby)
* [bundler](https://github.com/bundler/bundler/)
* [node](https://github.com/joyent/node)
* [gulp](https://github.com/gulpjs/gulp/)

## build

```bash
git clone https://github.com/robkorv/robkorv-web.git
cd robkorv-web
bundle install
npm install
gulp build
```

Compiled site is in `_site`.


## develop

I recommend you use [rbenv](https://github.com/sstephenson/rbenv) to setup a
ruby environment. The following rbenv plugins are highly recommended:  
[rbenv-binstubs](https://github.com/ianheggie/rbenv-binstubs)  
[rbenv-gem-rehash](https://github.com/sstephenson/rbenv-gem-rehash)  
[rbenv-update](https://github.com/rkh/rbenv-update)  
[ruby-build](https://github.com/sstephenson/ruby-build)

Use an editor that has support for [editorconfig](http://editorconfig.org/). I
use [atom](https://github.com/atom/atom).

```bash
git clone https://github.com/robkorv/robkorv-web.git
cd robkorv-web
bundle install --binstubs .bundle/bin
npm install
gulp watch
```

Open [localhost:4000](http://localhost:4000). When you edit source files you
need to refresh your browser to see the changes. Use `ctrl+c` to stop Gulp.

The [markdown-writer](https://github.com/zhuochun/md-writer) for Atom is
supported, use a config like the following to mimic my markdown-writer behaviour.

```cson
'markdown-writer':
  'newPostFileName': '{year}-{month}-{day}-{title}{extension}'
  'sitePostsDir': '_posts'
  'fileExtension': '.md'
  'siteLocalDir': '/path/to/robkorv-web'
  'siteEngine': 'jekyll'
  'urlForCategories': 'http://localhost:3000/.md-writer/categories.json'
  'urlForPosts': 'http://localhost:3000/.md-writer/posts.json'
  'urlForTags': 'http://localhost:3000/.md-writer/tags.json'
```
