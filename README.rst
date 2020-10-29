###############################
Ayame Labo ドキュメント
###############################

:日時: 2020-10-29
:作: `時雨堂 <https://shiguredo.jp>`_ 
:資料 バージョン: 2020.1
:URL: https://ayame-labo.shiguredo.jp/

これは時雨堂が提供している `Ayame Labo <https://ayame-labo.shiguredo.jp/>`_ のドキュメントです。

.. contents:: :depth: 1
 
FAQ
===

- Ayame Labo は無料ですか？

  - 無料で利用可能です
- Ayame Labo は商用目的で利用可能ですか？

  - サインアップしていただき利用規約に同意いただく事で利用可能です
- Ayame Labo をサービスに利用可能ですか？

  - サインアップしていただき利用規約に同意いただく事で利用可能です
- Ayame Labo は法人や個人事業主で利用できますか？

  - サインアップしていただき利用規約に同意いただく事で利用可能です
- Ayame Labo はアカデミックで利用可能ですか？

  - サインアップしていただき利用規約に同意いただく事で利用可能です
- Ayame Labo は長期間利用しても問題ありませんか？

  - 問題ありません
- Ayame Labo は長時間接続しても問題ありませんか？

  - 問題ありません
- Ayame Labo は転送量制限がありますか？

  - 全体で月間 5T までです
- Ayame Labo は同時接続制限がありますか？

  - ありません
- Ayame Labo の接続時間制限はありますか？

  - ありません
- Ayame Labo は STUN を提供していますか？

  - サインアップ時のみ提供しています
- Ayame Labo は TURN-TCP や TURN-TLS を提供していますか？

  - サインアップ時のみ提供しています
  - TURN-TCP は 3478 ポート
  - TURN-TLS は 5349 ポート
- Ayame Labo は映像ビットレートの制限はありますか？

  - サインアップ時に TURN を利用している場合はビットレートが 800kbps に抑えられます
- Ayame Labo の SLA はいくつですか？

  - 保証はありません
- Ayame Labo はウェブフック機能を提供しますか？

  - 提供しません
- Ayame Labo は Ayame の HTTP API を提供しますか？

  - 提供しません
- Ayame Labo はサポートを提供しますか？

  - 提供しません
- Ayame Web SDK のサポートは提供しますか？

  - 提供しません
- メンテナンス告知は行いますか？

  - 時雨堂の営業時間である平日の 10:00-17:00 の間に行う場合のみ Discord にて通知します
  - それ以外はサイレントで行います
- Ayame Labo の Ayame のバージョンはいくつですか？

  - 公開している Go 版の Ayame ではなく、非公開の Erlang 版の Ayame を利用しています
  - 仕様は Go 版 Ayame と完全互換です
- 認証エラー理由に ``PLEASE-CONTACT-US`` が出ました

  - どれかの禁止事項に当てはまっている可能性がある場合に出ます、メールにてご連絡ください

Discord
=======

サポート
  しません

アドバイス
  します

フィードバック
  歓迎します

https://discord.gg/z6EJu3d

制限
====

- Ayame の **ウェブフック機能は利用できません**
- Ayame Labo は Ayame Web SDK 以外での利用を想定していません
- TURN のビットレート制限は 1 接続あたり 800kbps です

禁止
====

- サインアップ無しでの法人/個人事業主やアカデミックでの利用
- サインアップ無しでの商用目的での利用
- 負荷試験ツールの利用
- Ayame Labo のベンチマーク結果を第三者へ公開すること

商用利用について
=========================================

Ayame Labo はサインアップする事で商用利用を許可しています。

利用可能な SDK やクライアント、ライブラリ
=========================================

- `OpenAyame/ayame-web-sdk: Ayame Web SDK <https://github.com/OpenAyame/ayame-web-sdk>`_
- `react-native-webrtc-kit/react-native-webrtc-kit-samples <https://github.com/react-native-webrtc-kit/react-native-webrtc-kit-samples/tree/develop/HelloAyame>`_

サインアップなしでの利用方法
============================

Ayame Labo はサインアップせずに、シグナリングサーバだけを利用することが可能です。

ただし、その場合はルームの認証を行うことや、 STUN/TURN サーバの利用をすることができません。

以下の URL で利用することができます。 ルーム ID を利用する場合は「他の人が推測されにくい ID を利用するようにしてください」

::

    wss://ayame-labo.shiguredo.jp/signaling


サインアップなしでの制限
------------------------

Ayame Labo にサインアップせずにルーム認証を利用しない場合は以下の制限があります。

- ルーム認証の利用不可
- STUN サーバの利用不可
- TURN サーバの利用不可
- 商用目的での利用不可
- サービスでの利用不可
- 法人や個人事業主の利用不可
- アカデミックの利用不可

サインアップなしで Ayame Web SDK を利用する
--------------------------------------------------

SDK をそのまま利用可能です。

https://github.com/OpenAyame/ayame-web-sdk

サインアップなしで Ayame Web SDK サンプルのデモ利用する
---------------------------------------------------------------

**デフォルトで Ayame Labo のシグナリングサーバが設定されています**

https://openayame.github.io/ayame-web-sdk-samples/

サインアップ無しで WebRTC Native Client Momo で Ayame Labo を利用する
-----------------------------------------------------------------------------

`shiguredo/momo: WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_

Momo で Ayame が利用できます。

ルーム ID を ayame-labo に指定した場合::

    ./momo ayame wss://ayame-labo.shiguredo.jp/signaling ayame-labo


サインアップありでの利用方法
============================

シグナリングキー設定済みのサンプルを利用する
------------------------------------------------

ダッシュボードページにルーム認証用のルーム ID とシグナリングキーを埋め込んであるサンプルを用意してあります。

- 送信専用
- 受信専用
- 送受信
- 画面共有
- データチャネル

ルーム認証とは
-----------------------------------

サインアップありで利用する場合はシグナリングキーを利用してルームに認証をかける事が可能です。

ルーム認証を利用する場合はルーム ID の前に GitHub アカウントの Username を指定する必要があります。

``shiguredo`` という ``GitHub Username`` であれば。その後 @ を間に挟んでルーム ID を指定してください。

以下は ``ayame-labo`` というルーム ID に ``shiguredo`` という ``Github Username`` を指定した例です

ルーム認証を適用した ルーム ID 例::

    shiguredo@ayame-labo

Ayame Web SDK でルーム認証を利用する
----------------------------------------------

https://github.com/OpenAyame/ayame-web-sdk

Ayame Web SDK を利用する場合はオプションに signalingKey をシグナリング時に指定できます。 ``signalingKey`` を指定して下さい。
これで利用可能になります。

シグナリングキーが ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` の場合は

.. code-block::

    const signalingUrl = "wss://ayame-labo.shiguredo.jp/signaling"
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

WebRTC Native Client Momo でルーム認証を利用する
-------------------------------------------------------

`shiguredo/momo: WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_

Momo で Ayame Labo を利用する事ができます。

- ルーム ID を ``<自分の GitHub Username>@<好きな Room ID>`` のように指定してください

  - ここでは GitHub Username を ``shiguredo`` としています
- 自分のシグナリングキーを --metadata で指定してください

  - ここではシグナリグキーを ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` としています

GitHub Username が shiguredo で、 ルーム ID が ayame-labo の場合::

    ./momo ayame wss://ayame-labo.shiguredo.jp/signaling shiguredo@ayame-labo \
        --signaling-key jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa


Ayame Labo のアカウントを削除する
----------------------------------------

もし今後、 Ayame Labo を利用しないのであればアカウントを削除できます。

ダッシュボードの一番下にアカウントの削除があります。
