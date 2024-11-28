# SUDOKU-SOLVER
9×9の簡単な数独を解きます。

<img src="https://github.com/user-attachments/assets/28b5f273-fc42-456f-84eb-e8a6853c6eab" width="46.5%" > <img src="https://github.com/user-attachments/assets/f8f002cc-2289-4f0a-85ab-5b8e30d2e830" width="50%" >

## 注意
現バージョンでは高度な手順を踏まないため、解けない問題があります。

## 目次
[インストール方法](./README.md#インストール方法)<br>
[アンインストール方法](./README.md#アンインストール方法)<br>
[起動方法](./README.md#起動方法)<br>
[使い方](./README.md#使い方)<br>
[ライセンス](./README.md#ライセンス)<br>
[環境](./README.md#環境)<br>


## インストール方法
※現在bashのみ対応<br>
この方法を使用する場合、**ホームディレクトリ**直下に置いて下さい。<br>
```
cd ~
git clone https://github.com/k310sto/Sudoku-Solver.git
```
ディレクトリ内に移動し、`install_bash.sh`を実行<br>
```
cd Sudoku-Solver
sh install_bash.sh
```
## アンインストール方法
ディレクトリ内に移動し、`uninstall_bash.sh`を実行します。<br>
```
cd ~/.Sudoku-Solver    #隠しファイルであることに注意
sh uninstall_bash.sh   #ディレクトリごと消去されます
cd ~
bash
```
## 起動方法
コマンドは以下の通りです。
```
SdS     #Solverを起動
SdSf    #おまけ　question.txtから問題を読み取りますが、それ以外は同じです
```
## 使い方
起動すると、次のようなメッセージが出ます。<br>
```
Let's play :
-------------------------


```
左上の数字から始まり、右に向かって入力、次段に移る際は改行します。<br>
また、空欄は0として下さい。
```
Let's play :
-------------------------
| 1 2 3 |       |       |
|       | 4 5 6 |       |
|       |       | 7 8 9 |
|-------+-------+-------|
| 1 2 3 |       |       |

000456
```
### 追加機能・動作
- 右端まで空欄の場合、省略できます。
- `u`と打つことで前段の入力に戻ることができます。
- 先頭に`-`(ハイフン)を入れると、入力を逆から反映できます。
- 1段に入る文字数を超過した場合、その分は切り捨てられます。
- 数字以外が入力された場合、その段から打ち直しになります。
## ライセンス

## 環境
**開発環境：**
- Ubuntu 20.04 on Windows
- debian12 Bookworm (仮想環境)

**使用言語：**
- C
- Shell (インストール・アンインストール用のファイル)

## その他
### 未解決の問題と課題
- Undoやエラー処理(数字以外の入力)を沢山起こすと、意図しない場所まで書き換えられる問題
- 複数の手順を必要とする解法の実装
- 問題作成機能の実装
