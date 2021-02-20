# rails_app_shamoji
ポートフォリオ用リポジトリ

## 環境構築

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

