# open-filemaker-url-scheme

---

#### FileMakerを起動するためのショートカットを生成するためのリンクです。
主にiPad、iPhoneでホーム画面にショートカットを生成する際に利用できます。
一度ホーム画面に追加すると、オフラインでも使用可能になります。

---

### 使い方
ベースのURLに各種パラメータをつけることで、ホーム画面用のショートカットを生成することができます。
```
https://sdw-inc.github.io/open-filemaker-url-scheme/
```

| パラメータ | 説明 | 必須/任意 | デフォルト値 | 例 |
| --- | --- | --- | ------- | --- |
| ```scheme``` | FileMaker Appの URLスキーマを指定してください。 | ◯ | ```-``` | fmp19、fmp20、fmp |
| ```address``` | FileMakerのソリューションがホスティングされている、サーバーのアドレスを指定してください。 | ◯ | ```-``` | fmsServer.com など スタンドアローンファイルの場合は ```~``` |
| ```filename``` | FileMakerのソリューション名を指定してください。 | ◯ | ```-``` | RECORERU.fmp12 |
| ```title``` | ホーム画面に生成されるタイトルが指定できます。 | × | 未設定の場合は、```fileName``` と同じ値 | RECORERU など |
| ```iconFileName``` | ```fullIconFilePath``` が設定済みの場合は、```fullIconFilePath```が優先されます。ホーム画面に生成されるアイコン名を指定できます。 ```images/``` の中にある画像に限り指定できます。 | × | 未設定の場合は、```images/filemaker-icon.png``` がセットされます。 | ```filemaker-icon.png``` |
| ```fullIconFilePath``` | ホーム画面に生成されるアイコンをフルパスファイルパスを指定できます。 | × | ```-``` | https://recoreru.com/app/imgs/logo.jpg |

---

### 例

```fmServer.com```にホスティングされた、```Sample.fmp12```のリンク
```
https://sdw-inc.github.io/open-filemaker-url-scheme/?scheme=fmp20&address=fmServer.com&filename=Sample.fmp12&title=Sample
```

スタンドアローンの```Sample.fmp12```のリンク
```
https://sdw-inc.github.io/open-filemaker-url-scheme/?scheme=fmp20&address=~&filename=Sample.fmp12&title=Sample&fullIconFilePath=https://cdn-icons-png.flaticon.com/512/9908/9908191.png
```
