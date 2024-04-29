# ベースイメージを指定する
FROM ruby:3.2.3

# アプリケーションの作業ディレクトリを設定する
WORKDIR /app

# GemfileとGemfile.lockをコピーする
COPY Gemfile Gemfile.lock ./

# Gemをインストールする
RUN bundle install

# アプリケーションのソースコードをコピーする
COPY . .

# データベースの設定などを行う
# CMD ["rails", "db:migrate"]

# アプリケーションを起動する
CMD ["rails", "server", "-b", "0.0.0.0"]
