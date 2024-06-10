# 作業メモ

## 環境情報（2024/05/17 現在）

- node.js のバージョンは v20.11.1(lts)

## 作業手順

### 初回の雛形導入まで

- node.js バージョン切り替えツール nvm のインストール
- 'nvm use stable'コマンドで node.js の lts 版をインストール?
- 以下、作業記録（vite で雛形作成 + npm install + git init）

```sh
react_ts_boilerplate $ node -v
v20.11.1
react_ts_boilerplate $ npm create vite@latest
Need to install the following packages:
create-vite@5.2.3
Ok to proceed? (y) y
✔ Project name: … react-ts-boilerplate
✔ Select a framework: › React
✔ Select a variant: › TypeScript + SWC

Scaffolding project in /Users/t-yuya/Desktop/react_ts_boilerplate/react-ts-boilerplate...

Done. Now run:

  cd react-ts-boilerplate
  npm install
  npm run dev

npm notice
npm notice New minor version of npm available! 10.2.4 -> 10.8.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v10.8.0
npm notice Run npm install -g npm@10.8.0 to update!
npm notice
react_ts_boilerplate $
react_ts_boilerplate $ cd react-ts-boilerplate
react-ts-boilerplate $ npm install

added 159 packages, and audited 160 packages in 34s

38 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
react-ts-boilerplate $ git init
Initialized empty Git repository in /Users/t-yuya/Desktop/react_ts_boilerplate/react-ts-boilerplate/.git/
```

### prettier導入

- 下記コマンドを実行

```sh
$ npm install --save-dev --save-exact prettier

added 1 package, and audited 161 packages in 3s

39 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

- vscode設定ファイル等修正

```sh
# ファイルフォーマットコマンド
$ npx prettier . --write

# ファイルフォーマット済か判定するコマンド（CIで使えそう）
$ npx prettier . --check

```

## ToDo リスト

- node.js の適宜アップデート
- editorconfig がファイル保存時に動くことを確認
- pre-commit設定（https://prettier.io/docs/en/precommit）
- eslint を初期ルールから修正する。
- tsconfig ファイルの修正
- vite.config.ts の修正
