# yokiKana-releases

yokiKana（Windows の日本語 IME。変換エンジン Shonagon、誤字指摘の Chunagon、縦書き推敲エディタ）を、ほかの PC に入れるための zip を置く場所です。
ソースは別の repo にあります。ここには配る zip（Releases）だけがあります。

## 入れる

1. Releases から `yokiKana-<版>.zip` を取り、右クリック →「すべて展開」
2. 展開した `yokiKana` フォルダの `install.cmd` をダブルクリック → UAC で「はい」
   - zip は小さく、変換の重み（約 1.3GB）は入っていません。`install.cmd` が Hugging Face の `AkadashiOmiso/yokiKana-weights` から取ってきます（ネットが要ります）
3. Chunagon（誤字指摘）を使うときは `yokiKana-chunagon-<版>.zip` も同じように（モデル約 5GB も Hugging Face から）

2 回目からは、設定のページ（タスクバーの yokiKana のアイコンを右クリック →「設定を開く」）の「更新」のタブから更新できます。

## 中身の確かめ

`SHA256SUMS.txt` に zip と重みの SHA256 があります（`Get-FileHash <ファイル>`）。`weights-*.json` は zip に入っていないファイルの一覧（置き場・SHA256・大きさ）です。
