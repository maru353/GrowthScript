# ベースイメージを指定
FROM ruby:3.2.3

# 必要なパッケージをインストール
RUN apt-get update -qq && apt-get install -y \
    build-essential \
    nodejs \
    npm \
    postgresql-client

# 作業ディレクトリを設定
WORKDIR /app

# GemfileとGemfile.lockをコピー
COPY Gemfile Gemfile.lock ./

# Gemのインストール
RUN bundle install

# ソースコードをコピー
COPY . .

# ポートの公開
EXPOSE 3001

# コンテナ起動時のコマンド
CMD ["rails", "server", "-b", "0.0.0.0"]
