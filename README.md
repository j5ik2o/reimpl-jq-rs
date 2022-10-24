# Rustに入門して何か一つツールを作る会(reimpl-jq-rs)

Rustに(再)入門して何か一つツールを作りましょう。

お品書きは以下。

## Rust入門(15分ぐらい)

- 大まかな言語機能の解説。他の言語との違いを中心に
- 僕がどこに躓いたか・それをどう解消したか
- どういう用途に向いているか

## Rust入門を卒業するモブプロ(残り時間全部)

- モブプロ or ペアプロ
- お題はjqの再実装
- 主に以下を使ってjqっぽいものを作る
  - コマンドラインパーサ
  - JSONパーサ
  - JSONPATHパーサ
- 僕もメンバーに加わる

## 環境構築

Rustでのプログラミングを開始するにあたって、以下のツールのインストールとセットアップを行います。

- rustup(Rustのバージョンと関連ツールを管理するツール)
- IntelliJ IDEA Ultimate Edition
  - Rustプラグイン
  - Code With Me

本ハンズオンはエディタはIntelliJとし、リモートでのモブプロを[Code With Me](https://pleiades.io/help/idea/code-with-me.html)で行います。

### rustupのインストール

Rustのバージョンと関連ツールを管理するツールです。Javaに慣れた方であれば、SDKMANのようなものと説明すればわかりやすいかもしれません。
以下のコマンドでrustupをインストールします。

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

rustupのインストールと同時に、rustc(Rustコンパイラ)やCargo(ビルドツール)もインストールされます。
正しくインストールされているか確認するために以下のコマンドを打って確認してください。
(細かいバージョンの差異は気にする必要ありません。)

```shell
$ rustup help
rustup 1.24.3 (ce5817a94 2021-05-31)
The Rust toolchain installer

USAGE:
    rustup [FLAGS] [+toolchain] <SUBCOMMAND>
...

$ rustc --version
rustc 1.56.1 (59eed8a2a 2021-11-01)
$ cargo --version
cargo 1.56.0 (4ed5d137b 2021-10-04)
```

### IntelliJのセットアップ

おそらく社内ではIntelliJ Ultimate Editionが事実上標準IDEとなっているため、インストールは不要と思います。
万が一インストールが必要な場合は[こちら](https://www.jetbrains.com/ja-jp/idea/)から行ってください。

