# python_playground

事情あって python 及び django を勉強している
参照している教科書は https://www.django-rest-framework.org/tutorial/1-serialization/

# Get started

**Nix OS 及び fish ユーザーを想定しているため他の環境は適宜調べて置き換えろ**

## 1. venv 環境を作る

`nix-shell -p venv .venv --copies` で `.venv` ディレクトリが出来てその中に python3 とか pip のバイナリ etc がインストールされる

実は python の実行環境構築は venv 使うのもいいが Nix 側としては `shell.nix` を作るほうが推奨されているぽい。そりゃそう。(ref https://wiki.nixos.org/wiki/Python)

## 2. venv の activate

`source .venv/bin/activate.fish` で仮想環境内部に入る。
これ入らないと `python3` とか `pip` が見つからんとか言われるので必須。

`// TODO: direnv でディレクトリ入ったときに自動で activate するようにしてもいいかも`

## 3. dependencies の導入

```sh
pip install django
pip install djangorestframework
pip install pygments  # We'll be using this for the code highlighting
```
これをする

`// TODO: requirements.txt なりに現状の依存を書き溜めて一括でインストールできるようにしたい`

`// TODO: そもそも requirements.txt がレガシーとの情報あり uv などのモダンなやつを使うといいカンジらしい`

## 4. がんばる

引数を参照するとき補完が効かなかったりとかでつらいががんばる

# General Improvements

全体的にわからんところとか、こういうの気になるっていうのを書き溜める場所

- [ ] 一部構文がわからん
  - snippets/models.py の `LEXERS` とかいうやつ特になにこれ
- [ ] linter とか formatter とか入れたい
  - そもそもあるん？
- [ ] uv をつかえるようにしたい
  - そもそも uv is なにってことについて package manager くらいしか現状知らない
- [ ] pydantic とかいうのが型をいいカンジにしてくれるらしいので
使ってみたい
