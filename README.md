# 閲覧用サイト

推奨リポジトリ名：`sri-lanka-library`

GitHub Pages 公開手順（閲覧用・管理用）

1. リポジトリを2つ作る
閲覧用：sri-lanka-library
管理用：sri-lanka-admin
半角英小文字とハイフンをそのまま使ってください。
無料プランでGitHub Pagesを使う場合はPublicにしてください。
管理画面の操作はサーバー側のパスワード認証で保護しています。

2. ZIPを解凍する
閲覧用ZIP → sri-lanka-library リポジトリ
管理用ZIP → sri-lanka-admin リポジトリ
ZIPそのものはアップロードしません。
解凍して出てきた中身のファイル・フォルダをアップロードします。
index.html をリポジトリの一番上に置いてください。
assets フォルダ、config.js、.nojekyll も一緒にアップロードします。
閲覧用には art フォルダもあります。一緒にアップロードしてください。
外側に余計なフォルダを作ったり、index.html の名前を変えたりしないでください。
GitHub：Add file → Upload files → ファイルを選ぶ → Commit changes。
ファイルはビルド済みなので、npmなどの操作は必要ありません。

3. それぞれのリポジトリでPagesを有効にする
Settings → Pages → Build and deployment
Source：Deploy from a branch
Branch：main
Folder：/ (root)
Save を押します。
公開後は同じPages画面のVisit siteから開けます。

4. 公開URLの形
閲覧用：https://あなたのGitHubユーザー名.github.io/sri-lanka-library/
管理用：https://あなたのGitHubユーザー名.github.io/sri-lanka-admin/
「あなたのGitHubユーザー名」の部分は実際の名前に置き換えてください。
2つとも同じGitHubアカウントに作ると、相互リンクがそのまま動きます。

5. 管理画面で使う
今使っている管理パスワードでログインしてください。
動画・画像・写真・PDF・サイトリンクを追加、編集、削除、並び替えできます。
更新内容は共通の保存先に保存され、閲覧用サイトに反映されます。
閲覧用サイトを既に開いている場合は再読み込みしてください。
動画はサイト内で再生できます。MP4（H.264/AAC）が推奨です。
ログインはブラウザのタブ内に保持します。タブを閉じたらログインし直してください。
パスワードやログイントークンをGitHubに書かないでください。

6. 保存先について
GitHub Pagesは画面の公開先です。
資料の保存・管理・動画配信は現在の共通サーバーを利用します。
このサーバーが停止すると資料の表示・管理も利用できなくなります。
現在の接続先：https://tagiri-sri-lanka.mikutakane.chatgpt.site
GitHubのコードやZIPには動画本体・PDF本体・パスワードを入れていません。

7. 名前を変える場合だけ
リポジトリ名を上記以外にした場合、両方の config.js を編集します。
publicUrl に閲覧用の実際の公開URL、adminUrl に管理用の実際の公開URLを入れます。
apiBase は資料の保存サーバーなので、そのままにします。
例：
window.SRI_LIBRARY_CONFIG = {
  apiBase: "https://tagiri-sri-lanka.mikutakane.chatgpt.site",
  publicUrl: "https://YOUR-USERNAME.github.io/YOUR-PUBLIC-REPOSITORY/",
  adminUrl: "https://YOUR-USERNAME.github.io/YOUR-ADMIN-REPOSITORY/"
};
URL末尾は / を入れてください。
この版は github.io 上での公開に対応しています。独自ドメインへの変更にはサーバーの接続設定も必要です。

8. 教材・動画ファイルの名前
例：01_school-introduction.mp4、02_japanese-class.mp4、03_care-training.pdf
ファイル名は半角英数字＋ハイフンまたはアンダーバーにすると管理しやすくなります。
サイトに表示するタイトルや説明は日本語で自由に入力できます。
順番は管理画面から変更できるので、番号は必須ではありません。

公式手順：
https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
