## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
 エンドポイント：https://zipcloud.ibsnet.co.jp/api/search

  機能：日本の郵便番号（7桁）を入力すると、それに対応する住所（都道府県・市区町村・町名）を取得できる。
  
* リクエストとレスポンスのフォーマット
  リクエスト形式（GET）：https://zipcloud.ibsnet.co.jp/api/search?zipcode=1000001

  レスポンス形式（JSON）：
{
  "message": null,
  "results": [
    {
      "zipcode": "1000001",
      "address1": "東京都",
      "address2": "千代田区",
      "address3": "千代田",
      "kana1": "ﾄｳｷｮｳﾄ",
      "kana2": "ﾁﾖﾀﾞｸ",
      "kana3": "ﾁﾖﾀﾞ"
    }
  ],
  "status": 200
}
  
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
  名称：PokéAPI（ポケモンAPI）
　URL：https://pokeapi.co

* エンドポイントと機能
  エンドポイント例：https://pokeapi.co/api/v2/pokemon/{name}

　機能：入力されたポケモン名（英語）に対応する基本データを取得できる。返される情報には、ポケモンの画像、タイプなどが含まれる。
 
* リクエストとレスポンスのフォーマット
  リクエスト：https://pokeapi.co/api/v2/pokemon/pikachu

レスポンス：
{
  "name": "pikachu",
  "sprites": {
    "front_default": "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/25.png"
  },
  "types": [
    {
      "type": {
        "name": "electric"
      }
    }
  ]
}

### Q3-3. 感想
* 今回の課題で苦労したこと
  初めて使うAPIのレスポンス形式を理解し、解くのに時間がかかった。
  
* 演習を通して理解できたこと
  Web APIは、外部から情報を取得する手段として非常に便利であり、ページの様々な方向で活用できることがよくわかった。

　JSON形式のデータを扱うことで、APIの中身や構造を理解できた。
 
* Web APIの利便性や課題など
  APIを使えば、外部のデータ（天気、地図、翻訳、キャラクター情報など）を簡単に自分のWebアプリに組み込めるので、表現の幅が広がる。

　APIの仕様変更やサーバーエラーなどに備えたエラーハンドリングや、利用制限への対策も必要だと感じた。
