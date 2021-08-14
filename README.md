# optimization_workspace
CasADiを使って非線形の最適化問題と最適制御問題を数値的に解く．

## 環境
Docker containerとしてPython3系の環境を構築．

- Image
    - [3.8.11-buster](https://github.com/docker-library/python/blob/670a51bde142663856c29c3ef85efcebde0aec6d/3.8/buster/Dockerfile)
- Packages
    - `.devcontainer/requirement.txt`

## 準備
1. Dockerのインストール (`docker`コマンドを使えるようにする)
    - Ubuntu
        - [シェルスクリプト](https://github.com/tcbn-ai/TIL/blob/main/Study_Docker/shellscript/install_docker.sh)を作成した
    - Windows
        - [Windows 10 Home で WSL 2 + Docker を使う](https://qiita.com/KoKeCross/items/a6365af2594a102a817b)
    - Mac
        - [Mac に Docker Desktop をインストール](https://docs.docker.jp/docker-for-mac/install.html)
        - [DockerをMacにインストールする（更新: 2019/7/13）](https://qiita.com/kurkuru/items/127fa99ef5b2f0288b81)
1. VSCodeのインストール
    - [Visual Studio Code](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)
    - 以下のExtentionsをインストール (その他好きなものをインストール)
        - Docker
        - Remote - Containers
        - Python
        - Jupyter

## ディレクトリ構成
```
|- .devcontainer/
    |- devcontainer.json        # VSCodeのRemote機能を使うときの設定
    |- docker-compose.yml       # containerに対する処理
    |- dockerfile               # containerを作るときの処理
    |- requirements.txt         # pip installするパッケージ
|- sample/
```

## 環境を構築する (Containerを開く) 方法
- 左下の"Open a Remote Window"をクリック．"Reopen in Container"を選択．
    - Containerの中身がVSCode上で開かれる．
    - あとはContainer内でコードを編集したり，実行したりする．