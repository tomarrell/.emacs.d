# Here be dragons

## What does it look like?

![magit-with-leaderkeys](https://raw.githubusercontent.com/d4ncer/.emacs.d/master/screenshots/magit-with-leaderkeys.png "It's Magi{t,c}!")

See more [here](SCREENSHOTS.md)

## Things you need

* Emacs 25+
* [Fira Code](https://github.com/tonsky/FiraCode)

## Quick install (recommended)

``` shell
wget -O - https://raw.githubusercontent.com/d4ncer/.emacs.d/master/setup.sh | bash
```

## Manual install

``` shell
mv ~/.emacs.d ~/.emacs.d.bak
git clone git@github.com:d4ncer/.emacs.d.git ~/.emacs.d
```

#### Go setup

Packages to install for Go config:

```bash
go get -u -v github.com/nsf/gocode
go get -u -v github.com/rogpeppe/godef
go get -u -v github.com/kardianos/govendor
go get -u -v golang.org/x/tools/cmd/guru
go get -u -v golang.org/x/tools/cmd/gorename
go get -u -v golang.org/x/tools/cmd/goimports
```

#### JS setup

Tern setup:

```bash
cd lisp/tern
npm install
```

Required binaries:

```bash
npm install -g stylefmt
```

Binaries for global fallback (this is optional, but highly recommended):

```bash
npm install -g eslint flow prettier eslint-config-airbnb eslint-config-prettier
```

If you do use a global `eslint`, you should add a fallback `.eslintrc.json` in
your root folder. A sample:

```js
{
  "extends": ["airbnb", "prettier", "prettier/flowtype", "prettier/react"],
  "env": {
    "browser": true,
    "jest": true,
    "node": true
  },
  "plugins": ["react", "flowtype"],
  "parser": "babel-eslint",
  "rules": {
    "flowtype/define-flow-type": 1,
    "import/no-extraneous-dependencies": ["error", {
      "devDependencies": true,
      "optionalDependencies": false,
      "peerDependencies": false
    }
    ]
  }
}

```

## Packages of note

Most of my work is on the frontend, which is reflected in my setup. Some
packages of note:

* Evil
* Ivy (with `ripgrep`)
* Spacemacs leader keys
* Projectile
* Flycheck
* Magit
* Org
* IBuffer
* Neotree
* Smartparens

## Language Modes

* Web
  * JS/JSX/HTML/CSS
  * Flow
  * Stylelint
  * Prettier
* Elisp
* Go
* Scala
* YAML
* Markdown
* CoffeeScript
* Dockerfile
* Groovy
* RNC
* Scala
* Haskell

## Planned Modes

**NB** In order of importance to me. If you're using my setup and want something
supported not on this list, feel free to issue a PR.

* OCaml
* TypeScript
* Java
* Racket

## Misc notes

* I use [Marked 2](http://marked2app.com/) to preview markdown files. If you don't have
  it, or you want to use something, set `markdown-open-command` to point to
  something else.
* If you want to tweak the font settings look in `config/rk-faces/rk-theme-base.el`.
* I put more effort into some modes than others, hence there are some modes
  with considered chordal bindings, and some with none. If you notice this,
  and you'd like to flesh these modes out, please send me a PR!

## Credits

* Heavily ~~copied~~ borrowed & adapted from [Chris Barrett](https://github.com/chrisbarrett)'s
wonderful [setup](https://github.com/chrisbarrett/.emacs.d).
* Thanks to [JH](https://github.com/jackhopner) for the setup script
