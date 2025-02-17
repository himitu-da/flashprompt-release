# FlashPrompt

## 概要
**FlashPrompt** は、プロンプトテンプレートを活用してテキスト生成を効率化する Windows 向けのデスクトップアプリケーションです。ユーザーは、テンプレート内の変数を入力することでカスタマイズされたプロンプトを生成し、ワンクリックでクリップボードにコピーすることができます。シンプルで直感的な UI により、すぐに利用できるツールとなっています。

本アプリケーションは [Tkinter](https://docs.python.org/ja/3/library/tkinter.html) を用いて構築され、`ttk` スタイルを取り入れることでモダンな外観と使いやすさを実現しています。

## 主な機能
- **プロンプトテンプレート管理**  
  テンプレートの登録、編集、削除が可能です。テンプレート一覧からお気に入りのプロンプトを選択し、編集モードに切り替えることができます。

- **変数入力とプレビュー**  
  テンプレート内に記述された `{{変数名}}` の形式の変数に対して自動的に入力欄が生成され、ユーザーが値を入力すると右側のプレビューエリアに即座に反映されます。

- **クリップボード連携**  
  生成されたプロンプトは「コピー」ボタン一つでクリップボードに転送され、他のアプリケーションで簡単に利用できます。

- **シンプルな UI テーマ**  
  一貫性のある色彩およびフォント設定により、誰でもわかりやすい現代的なユーザーインターフェイスを提供します。

- **キーボードナビゲーション**  
  キーボードショートカットを利用してタブ切替やリスト操作が可能なため、効率的な作業が行えます。

## システム要件
- **OS:** Windows  
  （`LOCALAPPDATA` を利用しているため、他の OS での動作は保証されません）
- **実行ファイル:** 単一の exe ファイルとして配布されるため、Python のインストールは不要です。

## 使い方
1. **起動**  
   提供される exe ファイル（例: `FlasshPrompt_v1.0.0.exe`）をダブルクリックして起動します。

2. **テンプレート一覧タブ**  
   登録済みのプロンプトテンプレートが一覧表示されます。テンプレートを選択してダブルクリックまたは Enter キーで編集モードに入ることができます。

3. **テンプレート登録タブ**  
   テンプレート名と本文を入力すると、テンプレート内で使用されている変数が自動的に抽出され、一覧表示されます。必要に応じて変数の入力欄に値を入力し、完成したテンプレートを「保存」ボタンで登録します。

4. **設定タブ**  
   保存ディレクトリの指定やウィンドウの常時最前面表示など、アプリケーションの動作設定が変更できます。

5. **プロンプト作成/編集ウィンドウ**  
   テンプレートに基づいたプロンプト作成ウィンドウでは、動的に生成された変数入力欄に値を入力することで、右側のプレビューエリアがリアルタイムに更新されます。プレビュー内容は「コピー」ボタンからクリップボードへ転送されます。

## ビルドと配布について
- **ビルド方法**  
  本アプリケーションは `PyInstaller` を用いて単一の exe ファイルにパッケージ化されています。`build_exe.py` スクリプトを実行すると、エントリーポイントである `main.py` を基に `FlasshPrompt_v{バージョン番号}.exe` が生成されます。

- **配布形態**  
  リリース版は単一の exe ファイルのみとなります。ユーザーは exe ファイルをダウンロードし、直接実行するだけでアプリケーションを利用することができます。これにより、複雑な依存関係のインストールや Python のセットアップが不要です。

## ライセンス
本プロジェクトは [MIT License](LICENSE) の下で公開されています。詳細はライセンスファイルをご確認ください。

## Q&A
- **Q: プロンプトテンプレートで使用できる変数名に制限はありますか？**  
  A: 英数字とアンダースコア（_）のみが使用可能です。

- **Q: テンプレート一覧の表示順は変更可能ですか？**  
  A: 現在の実装では登録順に表示されますが、将来的にはソート機能の追加を検討しています。

- **Q: 設定タブでの変更は即時反映されますか？**  
  A: 一部の設定（例: 保存ディレクトリ）は、アプリケーション再起動後に反映されます。

---

FlashPrompt は、シンプルな操作性と直感的な UI を兼ね備えたプロンプト生成ツールです。ぜひご活用ください！
