<!--
@Author: Guan Gui <guiguan>
@Date:   2016-01-21T00:47:29+11:00
@Email:  root@guiguan.net
@Last modified by:   guiguan
@Last modified time: 2016-04-04T19:10:55+10:00
-->
# FileHeader for Atom
FileHeader allows you to customize, add, update and cooperate your authoring information in header comment like this:

![File Header Demo](https://raw.githubusercontent.com/guiguan/file-header/master/demo.gif)

This package is inspired by and could be considered equivalent to [FileHeader for Sublime](https://github.com/shiyanhui/FileHeader) by [shiyanhui](https://github.com/shiyanhui). It is compatible with headers generated by FileHeader for Sublime.

# Installation
Just search for `file-header` in Atom `Settings > Install`, and press `Install`.

# Usage
1. Configure your real name, username and email in FileHeader's settings.
2. Use <kbd>shift-cmd-H</kbd> to add new header for current editing file. You can also use menu item from menu bar `Packages > File Header` or context menu `Add File Header` to do so. Or, you can turn on `Enable Auto Adding Header` in the settings to add a header for a new file when you save your the file.
3. Just hit <kbd>cmd-s</kbd> to save and your header's last modified info will be automatically updated.

# Customise Template
FileHeader came with a pre-defiend language-to-template mappings (`lang-mapping.json`) and bunch of template files (`templates/*`). Check them out in the `lib` directory of FileHeader package. You are free to override or partially override them in your own config directory. Check out the option `Config Directory Path` from FileHeader settings for details.

# Language Specific Setting
You can also configure everything language specific directly in your `config.cson` file (`Atom > Open Your Config`):

```CoffeeScript
"*":
    "file-header":
        autoAddingHeaderEnabled: true
        email: "..."
        realname: "..."
        username: "paulloz"
".gfm.source":
    "file-header":
        username: "..."
        autoAddingHeaderEnabled: false
".plain.text":
    "file-header":
        autoAddingHeaderEnabled: true
```

## Supported Language
Here are a list of language-to-template mappings I came up with. Feel free to make a pull request to me if you want to contribute :).

| Language Scope | Template File |
| :------------- | :------------ |
|source.arm|Clojure.tmpl|
|source.c|C.tmpl|
|source.cake|C.tmpl|
|source.clojure|Clojure.tmpl|
|source.coffee|ShellScript.tmpl|
|source.coffee.jsx|ShellScript.tmpl|
|source.cpp|C.tmpl|
|source.cs|C.tmpl|
|source.css|C.tmpl|
|source.css.less|C.tmpl|
|source.css.scss|SASS.tmpl|
|source.csx|C.tmpl|
|source.erlang|Erlang.tmpl|
|source.gfm|HTML.tmpl|
|source.git-config|ShellScript.tmpl|
|source.go|C.tmpl|
|source.gotemplate|GoTemplate.tmpl|
|source.haskell|Haskell.tmpl|
|source.java|C.tmpl|
|source.java-properties|ShellScript.tmpl|
|source.js|C.tmpl|
|source.js.rails source.js.jquery|C.tmpl|
|source.js.jsx|C.tmpl|
|source.litcoffee|HTML.tmpl|
|source.makefile|ShellScript.tmpl|
|source.matlab|Erlang.tmpl|
|source.objc|C.tmpl|
|source.objcpp|C.tmpl|
|source.perl|ShellScript.tmpl|
|source.perl6|ShellScript.tmpl|
|source.plist|HTML.tmpl|
|source.python|ShellScript.tmpl|
|source.ruby|ShellScript.tmpl|
|source.ruby.rails|ShellScript.tmpl|
|source.ruby.rails.rjs|ShellScript.tmpl|
|source.rust|SASS.tmpl|
|source.sass|SASS.tmpl|
|source.shell|ShellScript.tmpl|
|source.sql|C.tmpl|
|source.sql.mustache|C.tmpl|
|source.sql.ruby|C.tmpl|
|source.strings|C.tmpl|
|source.swift|C.tmpl|
|source.toml|ShellScript.tmpl|
|source.yaml|ShellScript.tmpl|
|text.html.basic|HTML.tmpl|
|text.html.erb|HTML.tmpl|
|text.html.gohtml|HTML.tmpl|
|text.html.jsp|HTML.tmpl|
|text.html.mustache|HTML.tmpl|
|text.html.php|HTML.tmpl|
|text.html.ruby|HTML.tmpl|
|text.plain|Default.tmpl|
|text.xml|HTML.tmpl|
|text.xml.plist|HTML.tmpl|
|text.xml.xsl|HTML.tmpl|

You can find out the scope of current editing file using <kbd>alt-cmd-p</kbd>. For all supported language scopes, you can use following code in `Developer Tools`:

```js
console.log(Object.keys(atom.grammars.grammarsByScopeName).join('\n'))
```

`Developer Tools` can be opened using <kbd>alt-cmd-i</kbd>. You can use  [file-types](https://atom.io/packages/file-types) package by [execjosh](https://github.com/execjosh) to map more file types to language scopes.

<!-- Piwik Image Tracker-->
<img src="http://piwik.guiguan.net/piwik.php?idsite=4&rec=1" style="border:0" alt="" />
<!-- End Piwik -->
