# GitHub Pagesへの公開方法

## 1. GitHubに新しいリポジトリを作成

例: `wingsearch-ja`

公開URLは通常、次の形式になります。

`https://あなたのGitHubユーザー名.github.io/wingsearch-ja/`

## 2. このフォルダー内のファイルをリポジトリへアップロード

ZIPファイルそのものではなく、展開後の中身をアップロードしてください。
`.github/workflows/deploy-pages.yml` も含めます。

## 3. GitHub PagesをGitHub Actionsに設定

リポジトリで以下を開きます。

`Settings` → `Pages` → `Build and deployment` → `Source`

Sourceを **GitHub Actions** に変更します。

## 4. Actionsの実行を確認

`Actions` タブを開き、
`Deploy Japanese Wingsearch to GitHub Pages` が成功することを確認します。

初回公開後は、ソースを更新してmasterまたはmainブランチへ反映すると自動的に再公開されます。

## 補足

- 通常のプロジェクトリポジトリと、`ユーザー名.github.io` リポジトリの両方に対応しています。
- Angularの画面を直接再読み込みした場合に備え、`404.html` を自動生成します。
- GitHub PagesでJekyll処理されないよう、`.nojekyll` も自動生成します。
