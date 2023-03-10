---
title: "ダウンロード"
weight: 1
---

# <center>バージョン変更ログ</center>

<br>

***v1.4.3***:
### @GBotHQによる変更
* OpenGLのバージョンをバージョン3.1に引き下げました。
* SpinBox と DoubleSpinBox のライブアップデート、一度に 10 回ステップするためのキーバインド (値を変更するときにシフトを保持する)

### @p-yukusaiによる変更 
* オートセーブの追加
* キーバインド（Ctrl-C、Ctrl-V、Ctrl-X）によるキーのコピー、ペースト、削除を可能にする。
* 固定ネットワーク
* アニメエフェクトのダウンロードは、「アップデートを確認する」メニューから行うことができます。
* FFD選択時にメッシュを自動的に表示するオプションがあります。
* 書き出し前に FFmpeg のチェックを行うようにした。
* オプションメニューにFFmpegヘルパーを追加（トラブルシューティングとセットアップ）
* バグフィックス
* 文字列のマイナーチェンジ
* JPの翻訳を更新しました。
* キーバインドをデフォルトに戻すボタンを追加しました。
* 不足しているデフォルトのキーバインドを追加しました。
* Ubuntu BionicのビルドはEOLに達した。

**バージョンマージ**: https://github.com/AnimeEffectsDevs/AnimeEffects/pull/24 <br>
**完全なChangelog**: https://github.com/AnimeEffectsDevs/AnimeEffects/compare/v1.4.2...v1.4.3

{{< button "https://github.com/AnimeEffectsDevs/AnimeEffects/releases/v1.4.3" "ダウンロードはこちら">}}

<br><br>

***v1.4.2***:

- レイヤー ノードに新しいアニメーション キー (色相、彩度 & 値、または HSV) を追加しました。フォルダーのサポートは準備ができていませんが、オプトインできます。
   - シェーダーを作成し、他の OpenGL の問題を解決することで、この機能を可能にしてくれた Gambot に感謝します。
- 「アニメーション キー」と呼ばれる新しい設定タブを追加しました。ここで設定を変更できます。 現時点では、新しい HSV キーの動作を変更するための 3 つの設定があります。
- 新しい「最近使ったファイルのリストをリセット」ボタンを設定に追加しました。
- タイムラインは、ループしていない最終フレームに到達すると自動的に停止するようになりました。
- (できれば) 理解しやすいように、ほとんどのテキストを作り直しました。
- 前回の変更に合わせて日本語訳を調整しました。
- キーバインドの繰り返しを許可 (125ms の遅延あり)
- アソシエーション処理。これは、.anie プロジェクトをダブルクリックして、AnimeEffects をプログラムとして設定し、それらを開くことができることを意味します。
- 最適化されたパレットのエクスポートを修正
- 奇数の高さまたは幅の値でエクスポートすると、レンダリング パイプラインが壊れる可能性があるため、警告が追加されました。
- 「ヘルプ」メニューに「アップデートの確認」ボタンを追加しました。
- リソース ウィンドウにオプションの filewatcher を追加しました。画像ファイルの変更を監視し、変更が検出されたときにプロジェクト内でそれらを自動的に再読み込みできます。
- メニューの代わりに「リソースの追加」ボタンを使用することで、リソースの追加を簡素化
- 「プロジェクト」メニュー内で FPS 再生速度を変更するオプションが追加されました。これはプロジェクト自体に保存されます。
- ファイルの代わりに QSettings から読み取るように "Open Recents" を変更しました。
- .webp および .tiff 画像のインポートのサポートを追加
   - Tiff 画像は単一のレイヤーとしてインポートされます。レイヤー化されたサポートは現在利用できません。
- 「breeze_dark」テーマの既知のバグをすべて修正
- すべての GitHub アクションを修正
- すべてのアクションにナイトリー アーティファクトを追加しました。
- ##### 重大な変更: プロジェクトのバージョンを 0.5 から 0.6 に上げました。これにより、この新しいバージョンで作成されたプロジェクトを古いバージョンの AnimeEffects にロードすることができなくなります。

{{< button "https://github.com/AnimeEffectsDevs/AnimeEffects/releases/v1.4.2" "ダウンロードはこちら">}}

<br><br>

***v1.4.0***:

* 新しいダークテーマが追加されました (breeze_dark)
* ビルドおよびデプロイ用の新しいスクリプトが多数作成されました
* 1.3.5 から 1.4.0 へのバージョン バンプ
* のキーバインドを追加
* タイムラインの移動 (Ctrl + 左または右矢印キー)
* 最初または最後のフレームへのジャンプ (Ctrl + 上または下矢印キー)
* ループの切り替え (Ctrl + R)
* 再生の切り替え (Ctrl + スペースバー)
* ドックの切り替え (Ctrl + Q)
* 骨を引っ張る機能を修正しました (aoi さんに報告していただき、Larpon さんに診断を手伝っていただきました)
* FFMPEG エクスポートを修正し、利用可能なすべてのフォーマット ファイルにエクスポートできるようになりました。 (これが正しく機能するように、ファイル名に「%20」を含めないでください)
* 最小 OpenGL バージョンを 4.0 から 3.3 に引き下げ
* MathUtil を修正しました (これにより、プル ボーン機能が修正され、他の点に気付きませんでした)
* 最近使用したファイルを開いたときに、見つからない場合は自動的に記録から削除されます (変更は次回の再起動時に適用されます)。
* Linux CI を Ubuntu 20.04 Jammy にアップグレードします。古いディストリビューションの互換バージョンが利用可能になりました。
* MacOS CI を修正しました。AnimeEffects.app を含む zip が利用可能になりました。

**完全な変更ログ**: https://github.com/AnimeEffectsDevs/AnimeEffects/compare/v1.3.4...v1.4.0

{{< button "https://github.com/AnimeEffectsDevs/AnimeEffects/releases/v1.4.0" "ダウンロードはこちら">}}

<br><br>

***v1.3.5***:

* 最近のプロジェクトを開くオプションを追加
* 現在の開発状況をより反映するように「概要」セクションを変更
* 新しいキーフレームのデフォルトのイージングと範囲タイプを設定するオプション メニューの新しいセクション
* デバッグ版あり

**完全な変更ログ**: https://github.com/AnimeEffectsDevs/AnimeEffects/compare/v1.3.4...v1.3.5

{{< button "https://github.com/AnimeEffectsDevs/AnimeEffects/releases/v1.3.5" "ダウンロードはこちら">}}

<br><br>