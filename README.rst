######################
Ayame Labo ドキュメント
######################

これは時雨堂が提供予定の `Ayame Labo <https://ayame-labo.shiguredo.jp/>`_ のドキュメントです。

QA
==

- Ayame Labo は無料ですか？

  - 無料で利用可能です
- Ayame Labo は商用目的で利用可能ですか？

  - サインアップしていただき利用規約に同意いただく事で利用可能です
- Ayame Labo をサービスに利用可能ですか？

  - サービスで利用可能です
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
- Ayame Labo は映像ビットレートの制限はありますか？

  - TURN を利用している場合はビットレートが 800kbps に抑えられます
- Ayame Labo の接続時間制限はありますか？

  - ありません
- Ayame Labo は TURN-TCP や TURN-TLS を提供していますか？

  - 提供しています
  - TURN-TCP は 3478 ポート
  - TURN-TLS は 5349 ポート
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
  - 仕様は Go 版 Ayame と全く同じです
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

- Ayame の **HTTP API は利用できません**
- Ayame の **ウェブフック機能は利用できません**
- Ayame Labo は Ayame Web SDK 以外での利用を想定していません
- TURN のビットレート制限は 800kbps です

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

Ayame Labo はサインアップなしでも利用可能です。ただしサインアップなしでの利用は制限があります。
制限を確認してご利用ください。

サインアップなしでの制限
------------------------

- ルーム認証の利用不可
- STUN サーバの利用不可
- TURN サーバの利用不可
- 商用目的での利用不可
- サービスでの利用不可
- 法人や個人事業主の利用不可
- アカデミックの利用不可

利用方法
--------

Ayame Web SDK サンプルのデモ利用する
--------------------------------------

https://openayame.github.io/ayame-web-sdk-samples/

Ayame Web SDK を利用する
---------------------------

WebRTC Native Client Momo で Ayame Labo を利用する
----------------------------------------------------

`shiguredo/momo: WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_

Momo で Ayame が利用できます。

ルーム ID を ayame-labo に指定した場合::

    ./momo ayame wss://ayame-labo.shiguredo.jp/signaling ayame-labo


サインアップありでの利用方法
============================

サンプルを利用する
-------------------

ダッシュボードページにシグナリングキーを埋め込んであるサンプルを用意してありますので、気軽に確認できます。

Ayame Web SDK を利用する
---------------------------

WebRTC Native Client Momo で Ayame Labo を利用する
-------------------------------------------------------

`shiguredo/momo: WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_

Momo で Ayame が利用できます。

- ルーム ID を ``<自分の GitHub Username>@<好きな Room ID>`` のように指定してください

  - ここでは GitHub Username を ``shiguredo`` としています
- 自分のシグナリングキーを --metadata で指定してください

  - ここではシグナリグキーを ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` としています

GitHub Username が shiguredo で、 ルーム ID が ayame-labo の場合::

    ./momo ayame wss://ayame-labo.shiguredo.jp/signaling shiguredo@ayame-labo \
        --signaling-key jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa

認証方法
========

ルーム ID を決める
--------------------

シグナリングキーを利用してルームに認証をかけてみます。

まずルーム ID は GitHub アカウントの Username を先頭に指定する必要があります。

shiguredo という GitHub Username であれば。 その後 @ を間に挟んでルーム ID を指定してください。

以下は ayame-labo というルーム ID に shiguredo という Github Username を指定した例です

ルーム ID 例::

    shiguredo@ayame-labo

signaling_key を指定する
------------------------------------

Ayame の SDK は signaling_key をシグナリング時に指定できます。 ``signaling_key`` を指定して下さい。
これで利用可能になります。

シグナリングキーが ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` の場合

Ayame Labo のアカウントを削除する
--------------------------------

もし今後、 Ayame Labo を利用しないのであればアカウントを削除できます。

ダッシュボードの一番下にアカウントの削除があります。
