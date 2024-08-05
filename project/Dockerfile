# ベースイメージとしてPython 3.8を使用
FROM python:3.8

# 作業ディレクトリを設定
WORKDIR /app

# requirements.txtをコンテナの作業ディレクトリにコピー
COPY techtrends/requirements.txt requirements.txt

# 必要なパッケージをインストール
RUN pip install --no-cache-dir -r requirements.txt

# アプリケーションのソースコードをコンテナにコピー
COPY techtrends /app

# アプリケーションのポートを公開
EXPOSE 3111

# データベースを初期化し、アプリケーションを起動するコマンドを設定
CMD ["sh", "-c", "python init_db.py && python app.py"]

