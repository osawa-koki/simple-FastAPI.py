# simple-FastAPI.py

FastAPIの動作をテストするためのプログラム。  

## 実行方法

```shell
# デバグ用
uvicorn main:app --host localhost --port 80 --reload
```

```shell
# Dockerファイルをビルド
docker build -t fastapi-sample .

# Dockerコンテナを実行
docker run -it --name fastapi-sample -p 80:80 fastapi-sample
```

一行で書くなら、、、  

```shell
docker build -t fastapi-sample . && docker run -it --name fastapi-sample -p 80:80 fastapi-sample
```

<http://localhost:80>へアクセス。  

RESTfulAPIのテストは[postman](https://www.postman.com/)で♪  

---

以下のパスにアクセスして動作を確認。  

- /
- /pokemon/{name}
- / (POST | number,name,type1,type2をセットした状態で)
- /cookie
- /html
- /plain
- /redirect
- /stream/tako
- /file
- /error

## 環境構築手順

```shell
# Dockerなら不要
pip install -r requirements.txt
```

## 使用した画像ファイル

- [タコ](https://frame-illust.com/?p=13667)
- [スズメ](https://frame-illust.com/?p=13680)
- [キツネ](https://frame-illust.com/?p=9584)

## デプロイ設定(Render.com)

| キー | バリュー |
| ---- | ---- |
| Name | simple-fastapi-server |
| Region | Oregon(US West) |
| Branch | main |
| Root Directory |  |
| Environment | Docker |
| Dockerfile Path | ./Dockerfile |
| Docker Build Context Directory |  |
| Docker Command |  |

## 参考文献

- [公式ドキュメント](https://fastapi.tiangolo.com/ja/)
