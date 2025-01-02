# Ayame Labo ドキュメント

- 日時: 2024-08-29
- 作: [時雨堂](https://shiguredo.jp)
- 資料: バージョン: 2024.1
- URL:  <https://ayame-labo.shiguredo.app/>

これは時雨堂が提供している [Ayame Labo](https://ayame-labo.shiguredo.app/) のドキュメントです。

## ステータスページ

<https://shiguredo.onlineornot.com/>

## お知らせ

### 2024-08-29

- STUN のポートを 3478/UDP に変更しました
- TURN-UDP のポートを 3478/UDP に変更しました
- TURN-TCP のポートを 3478/TCP に変更しました
- TURN-TLS のポートを 5349/TCP に変更しました
- TURN 最大利用帯域を 500 kbps に変更しました
- TURN 転送量の制限を撤廃しました

## FAQ

- Ayame Labo とはなんですか？
  - [WebRTC Signaling Server Ayame 仕様](https://github.com/OpenAyame/ayame-spec) の仕様に準拠したシグナリングサーバを提供しているサービスです
- Ayame Labo は無料ですか？
  - 無料で利用可能です
- Ayame Labo は日本国外から利用できますか？
  - 利用できません
- Ayame Labo は商用目的で利用できますか？
  - できますが、ルーム認証の利用が必須になります
- Ayame Labo をサービスに利用できますか？
  - できますが、ルーム認証の利用が必須になります
- Ayame Labo は法人や個人事業主で利用できますか？
  - できますが、ルーム認証の利用が必須になります
- Ayame Labo はアカデミックで利用できますか？
  - できますが、ルーム認証の利用が必須になります  
- Ayame Labo は長期間利用しても問題ありませんか？
  - 問題ありません
- Ayame Labo は長時間接続しても問題ありませんか？
  - 問題ありません
- Ayame Labo は転送量制限がありますか？
  - ありません
- Ayame Labo は同時接続制限がありますか？
  - ありません
  - ただし Ayame の仕様上 1 ルーム 2 人までしか接続できません
- Ayame Labo の接続時間制限はありますか？
  - ありません
- Ayame Labo は STUN を提供していますか？
  - サインアップ時のみ提供しています
  - STUN は 3478/UDP ポート
- Ayame Labo は TURN-UDP を提供していますか？
  - サインアップ時のみ提供しています
  - TURN-UDP は 3478/UDP ポート
- Ayame Labo は TURN 転送量制限がありますか？
  - ありません
- Ayame Labo は TURN-TCP や TURN-TLS を提供していますか？
  - サインアップ時のみ提供しています
  - TURN-TCP は 3478/TCP ポート
  - TURN-TLS は 5349/TCP ポート
- Ayame Labo は IPv6 に対応していますか？
  - 対応していません
- Ayame Labo は映像ビットレートの制限はありますか？
  - TURN を利用している場合はビットレートが 500 kbps に抑えられます
- Ayame Labo の SLA はいくつですか？
  - 保証はありません
- Ayame Labo はウェブフック機能を提供していますか？
  - 提供していません
- Ayame Labo は Ayame の HTTP API を提供していますか？
  - 提供していません
- Ayame Labo はサポートを提供していますか？
  - 提供していません
- Ayame Web SDK のサポートは提供していますか？
  - 提供していません
- WebRTC Native Client Momo の Ayame モードのサポートは提供していますか？
  - 提供していません
- メンテナンス告知は行いますか？
  - 行いません
- Ayame Labo の Ayame のバージョンはいくつですか？
  - 公開している Go 版の Ayame ではなく、非公開の Erlang 版の Ayame を利用しています
  - 仕様は Go 版 Ayame と完全互換です
- 認証エラー理由に ``PLEASE-CONTACT-US`` が出ました
  - どれかの禁止事項に当てはまっている可能性がある場合に出ます、メールにてご連絡ください

## Discord

- サポート
  - しません
- アドバイス
  - します
- フィードバック
  - 歓迎します

<https://discord.gg/shiguredo>

## 制限

- Ayame の **ウェブフック機能は利用できません**
- Ayame Labo は Ayame Web SDK と WebRTC Native Client Momo 以外での利用を想定していません
- TURN のビットレート制限は 1 接続あたり 500 kbps です

## 禁止

- サインアップ無しでの法人/個人事業主やアカデミックでの利用
- サインアップ無しでの商用目的での利用
- 負荷試験ツールの利用
- Ayame Labo のベンチマーク結果を第三者へ公開すること
- 日本国外からの利用

## 不特定向けのサービスでの利用について

Ayame Labo のシグナリングキーの仕組みは不特定多数向けのサービスでの利用を想定していません。
シグナリングキーは簡単に悪用することが可能なためです。

もし不特定多数向けのサービスに Ayame を利用したい場合は、
Ayame Labo を利用せず、自前で Ayame の運用をすることをお勧めします。

## 法人や商用利用について

Ayame Labo はサインアップし、ルーム認証を利用する事で法人や商用利用を許可しています。

## 利用可能な SDK やクライアント、ライブラリ

### 公式 SDK

[OpenAyame/ayame-web-sdk: Ayame Web SDK](https://github.com/OpenAyame/ayame-web-sdk)

### サードパーティ

動作確認などは取っていません。

- [tarukosu/MixedReality-WebRTC-ayame: MixedReality-WebRTC にて、シグナリングサーバとして Ayame を利用するためのコード](https://github.com/tarukosu/MixedReality-WebRTC-ayame)
- [hakobera/go-ayame: go-ayame is go client library for WebRTC Signaling Server Ayame](https://github.com/hakobera/go-ayame)
- [tarakoKutibiru/UnityRenderStreaming-Ayame-Sample](https://github.com/tarakoKutibiru/UnityRenderStreaming-Ayame-Sample)

### サインアップなしでの利用方法

Ayame Labo はサインアップせずに、シグナリングサーバだけを利用することが可能です。

ただし、その場合はルームの認証を行うことや、 STUN/TURN サーバの利用をすることができません。

以下の URL で利用することができます。 ルーム ID を利用する場合は「他の人が推測されにくい ID を利用するようにしてください」

`wss://ayame-labo.shiguredo.app/signaling`

### サインアップなしでの制限

Ayame Labo にサインアップせずにルーム認証を利用しない場合は以下の制限があります。

- ルーム認証の利用不可
- STUN サーバの利用不可
- TURN サーバの利用不可
- 商用目的での利用不可
- サービスでの利用不可
- 法人や個人事業主の利用不可
- アカデミックの利用不可

### サインアップなしで Ayame Web SDK を利用する

SDK をそのまま利用可能です。

<https://github.com/OpenAyame/ayame-web-sdk>

### サインアップなしで Ayame Web SDK サンプルを利用する

<https://github.com/OpenAyame/ayame-web-sdk-examples>

### サインアップなしで WebRTC Native Client Momo で Ayame Labo を利用する

[shiguredo/momo: WebRTC Native Client Momo](https://github.com/shiguredo/momo)

Momo で Ayame が利用できます。

#### ルーム ID を ayame-labo に指定した場合

```bash
./momo ayame --signaling-url wss://ayame-labo.shiguredo.app/signaling --room-id ayame-labo
```

## サインアップありでの利用方法

### シグナリングキー設定済みのサンプルを利用する

ダッシュボードページにルーム認証用のルーム ID とシグナリングキーを埋め込んであるサンプルを用意してあります。

- 送信専用
- 受信専用
- 送受信
- 画面共有
- データチャネル

### ルーム認証とは

サインアップありで利用する場合はシグナリングキーを利用してルームに認証をかける事が可能です。

ルーム認証を利用する場合はルーム ID の前に GitHub アカウントの Username を指定する必要があります。

`shiguredo` という `GitHub Username` であれば。その後 @ を間に挟んでルーム ID を指定してください。

以下は `ayame-labo` というルーム ID に `shiguredo` という `Github Username` を指定した例です

ルーム認証を適用したルーム ID 例は `shiguredo@ayame-labo` になります。

### Ayame Web SDK でルーム認証を利用する

<https://github.com/OpenAyame/ayame-web-sdk>

Ayame Web SDK を利用する場合はオプションに signalingKey をシグナリング時に指定できます。 `signalingKey` を指定して下さい。
これで利用可能になります。

シグナリングキーが `jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa` の場合は

```javascript
const signalingUrl = "wss://ayame-labo.shiguredo.app/signaling"
const roomId = "shiguredo@ayame-labo";
const options = Ayame.defaultOptions;
options.signalingKey = "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa";
const conn = Ayame.connection(signalingUrl, roomId, options, true);
conn.on('disconnect', (e) => console.log(e));
const startConn = async () => {
  const mediaStream = await navigator.mediaDevices.getUserMedia({audio: true, video: true});
  await conn.connect(mediaStream);
  // あとは色々かいていく
};
```

### WebRTC Native Client Momo でルーム認証を利用する

[shiguredo/momo: WebRTC Native Client Momo](https://github.com/shiguredo/momo)

Momo で Ayame Labo を利用する事ができます。

- ルーム ID を `<自分の GitHub Username>@<好きな Room ID>` のように指定してください
  - ここでは GitHub Username を `shiguredo` としています
- 自分のシグナリングキーを --metadata で指定してください
  - ここではシグナリングキーを `jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa` としています

#### GitHub Username が shiguredo で、 ルーム ID が ayame-labo の場合

```bash
./momo ayame --signaling-url wss://ayame-labo.shiguredo.app/signaling --room-id shiguredo@ayame-labo \
    --signaling-key jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa
```

### Ayame Labo のアカウントを削除する

もし今後、 Ayame Labo を利用しないのであればアカウントを削除できます。

ダッシュボードの一番下にアカウントの削除があります。
