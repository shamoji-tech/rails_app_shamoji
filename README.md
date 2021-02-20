# rails_app_shamoji
ポートフォリオ用リポジトリ

## 環境構築

### ruby編
```
brew install rbenv ruby-build rbenv-gemset
rbenv install 2.5.8
rbenv local 2.5.8
rbenv gemset create 2.5.8 venv
rbenv gemset init venv
gem install bundler:1.17.2
bundler install --path vendor/bundle
```

また、`/usr/local/bin`をrubyやbundlerがみてしまう場合は、
以下のことを`~/.bash_profile`や`~/.zshrc`へ書き込んでください

```
export PATH="~/.rbenv/shims:/usr/local/bin:$PATH"
eval "$(rbenv init -)"
```

### yarn編

まずyarnを入れるためにnpmを入れる必要があり、  
npmを入れるためにnode.jsを入れる必要があり、  
node.jsを入れるためにnodebrewが必要である。  

```
brew install nodebrew
```

`~/.zshrc`に以下を記載

```
export PATH=$HOME/.nodebrew/current/bin:$PATH
```

以下を実行

```
mkdir -p ~/.nodebrew/src
nodebrew install stable
nodebrew ls #→ここでinstallされたversionが出てくるので、useする
nodebrew use v14.15.5
npm install -g yarn
```


これでyarnがインストールされた。


