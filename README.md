# SUDOKU SOLVER
[![test](https://github.com/k310sto/Sudoku_Solver/actions/workflows/test.yml/badge.svg?branch=main)](https://github.com/k310sto/Sudoku_Solver/actions/workflows/test.yml)
[![](https://img.shields.io/github/license/k310sto/Sudoku_Solver)](https://github.com/k310sto/Sudoku_Solver/blob/main/LICENSE)
<br>
9×9の簡単な数独を解きます。

<img src="https://github.com/user-attachments/assets/28b5f273-fc42-456f-84eb-e8a6853c6eab" width="46.5%" > <img src="https://github.com/user-attachments/assets/f8f002cc-2289-4f0a-85ab-5b8e30d2e830" width="50%" >

## おことわり
現バージョンでは高度な手順を踏まないため、解けない問題があります。

## 目次
[使い方](./README.md#使い方)<br>
[追加機能&動作](https://github.com/k310sto/Sudoku_Solver/blob/main/README.md#%E8%BF%BD%E5%8A%A0%E6%A9%9F%E8%83%BD%E5%8B%95%E4%BD%9C)<br>
[その他](./README.md#その他)<br>
[ライセンス](./README.md#ライセンス)<br>

## 使い方
### インストール方法
ホームディレクトリに移動し、リポジトリをクローンします。
```
cd ~
git clone https://github.com/k310sto/Sudoku-Solver.git
```
ディレクトリ内に移動し、`install_bash.sh`を実行します。<br>
```
cd Sudoku_Solver
sh install_bash.sh
```
### アンインストール方法
ディレクトリ内に移動し、`uninstall_bash.sh`を実行します。<br>
```
cd ~/.Sudoku_Solver    #隠しファイルであることに注意
sh uninstall_bash.sh   
cd ~
rm -rf .Sudoku_Solver  #ディレクトリ削除
source ~/.bashrc
```
### 使用方法
コマンドは以下の通りです。
```
SDS     #Solverを起動
```
起動すると、次のようなメッセージが出ます。<br>
```
Let's play :
-------------------------


```
左上の数字から始まり、右に向かって入力、次段に移る際は改行します。<br>
また、空欄は0として下さい。<br>
9段目を入力し改行すると答えが計算されます。
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

<details><summary>問題例</summary>

```
0293
0080057
070084
802060374
960407802
45080209
69000008
000090035
0000006
```
※一度に入力すると表示が崩れますが、答えは正しく出力されます。<br>
参考：[数独無料問題集](http://数独無料問題集pdf.com/muryomondaishu.html)

</details>

## 追加機能&動作
- 右端まで空欄の場合、省略できます。
- `u`と打つことで前段の入力に戻ることができます。
- 先頭に`-`(ハイフン)を入れると、入力を逆から反映できます。
- 1段に入る文字数を超過した場合、その分は切り捨てられます。
- 数字以外が入力された場合、その段から打ち直しになります。

## その他
### 必須ソフトウェア
- C
### テスト環境
- Ubnutu 22.04.5 LTS
- Microsoft Windows Server 2022 10.0.20348 Datacenter
- macOS 14.7.1 23H222

## ライセンス
このスクリプトは、3条項BSDライセンスの下、再頒布および使用が許可されます。<br>
© 2024 Kensuke Sato
