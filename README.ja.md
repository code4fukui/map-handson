# map-handson

このプロジェクトは、SPARQLクエリを使用してGoogleマップ上にオープンデータを表示するためのハンズオンチュートリアルを提供します。

## ライブデモとチュートリアルのステップ

これらのサンプルでは、基本的な地図の表示から複雑なデータクエリまで、段階的に概念を学べます。まずは `index.html` を開いて、すべてのデモを確認してください。

*   **[index.html](index.html)**: すべてのデモのメインインデックス。
*   **[map1.html](map1.html)**: 基本的なGoogleマップを表示。
*   **[map2.html](map2.html)**: マップに単一の静的なマーカーを追加。
*   **[map3.html](map3.html)**: 簡単なSPARQLクエリを実行し、複数のデータポイントを取得して表示。
*   **[map4.html](map4.html)**: データ内のキーワードでSPARQLの結果を絞り込み（フィルタリング）。
*   **[map5.html](map5.html)**: 緯度・経度による矩形領域（バウンディングボックス）を指定してSPARQLの結果を絞り込み。
*   **[map-school.html](map-school.html)**: 応用例：新宿・品川エリアの小学校マップ。
*   **[map-nursery.html](map-nursery.html)**: 応用例：品川エリアの保育園・幼稚園マップ。

## 特徴

*   SPARQLとマップの連携を学ぶためのステップバイステップのHTMLサンプル。
*   SPARQLクエリで取得したデータポイントを、インタラクティブなGoogleマップ上にマーカーとして描画。
*   キーワードや地理的座標によるデータの絞り込みのデモ。
*   マーカーのクリックイベントで各地点の詳細を表示。
*   再利用可能なJavaScriptユーティリティライブラリ（`fukuno.js`, `odp.js`）を同梱。

## はじめに

1.  このリポジトリをクローンまたはダウンロードします。
2.  プロジェクトのルートディレクトリでローカルWebサーバーを起動します。
3.  Webブラウザで `index.html` を開き、デモのリストを確認します。

**Google Maps APIキーに関する注意:** デモファイルには、利便性のためにGoogle Maps APIキーが事前に設定されています。マップが読み込まれない場合、キーの有効期限が切れている可能性があります。その場合は、HTMLファイル内の `<script>` タグを編集し、ご自身のキーに置き換えてください。

```html
<script src="https://maps.google.com/maps/api/js?key=YOUR_OWN_API_KEY"></script>
```

## コードの概要

*   **`.html` ファイル**: 各ファイルは独立したサンプルになっています。ソースコードを見て、マップの初期化方法やSPARQLクエリの構築・実行方法を確認してください。
*   **`fukuno.js`**: DOM操作やJSONPリクエストなどのヘルパー関数を提供する汎用ユーティリティライブラリ。
*   **`odp.js`**: オープンデータポータル（ODP）のSPARQLエンドポイントにクエリを実行するための専用ヘルパーライブラリ。なお、メインのHTMLデモでは、分かりやすさのために別のエンドポイントとインラインのクエリ関数を使用しています。

## データソース

各サンプルでは、公開されているSPARQLエンドポイントにクエリを実行し、公共施設のデータを取得しています。

*   **[https://sparql.opendata.cc/data/sparql](https://sparql.opendata.cc/data/sparql)**: メインのHTMLデモ（`map3.html`, `map-school.html` など）で使用しているエンドポイント。
*   **[http://sparql.odp.jig.jp/data/sparql](http://sparql.odp.jig.jp/data/sparql)**: `odp.js` ヘルパーライブラリが対象としているエンドポイント。

## ライセンスと帰属

このプロジェクトは [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) ライセンスの下で公開されています。

作成者: [福野泰介 / 一日一創](http://fukuno.jig.jp/2073)
