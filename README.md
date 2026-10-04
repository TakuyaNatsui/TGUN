# TGUN — 軸対称熱電子銃シミュレーション（試用版）

TGUN は、軸対称の熱電子銃を設計するための Windows 用のシミュレーションソフトです。
有限要素法で電場・磁場を求め、空間電荷を含む電子ビームの軌道を自己無撞着に計算します。

- CAD 風の作図（拘束・寸法・パラメータ）で、電場と磁場の 2 つの形状を描けます
- 電極・カソード・コイル・鉄などの物理の指定、メッシュの生成（カソード近傍の細分化）、全計算、結果の表示
- Child-Langmuir 則によるエミッション、相対論的な軌道計算、空間電荷とビーム自身の磁場
- DGUN の入力の取り込みと比較（ビーム電流の差 -0.26%）

<!-- 下書きの元: TGUN_ver2/packaging/github/README.md（公開用のリポジトリにはこのまま README.md として置ける） -->

## ダウンロード

[Releases](../../releases) から `TGUN-<版>-trial-win64.zip` をダウンロードしてください。

- 必要な環境: Windows 10 / 11（64 ビット）。Python などのインストールは要りません。
- zip を展開して `TGUN.exe` をダブルクリックすると起動します。
- 初めての起動で「Windows によって PC が保護されました」と出たときは、「詳細情報」→「実行」を押してください
  （まだ電子署名を付けていないためです）。展開の前に zip のプロパティで「許可する」にチェックすると出にくくなります。
- 使い方は、zip の中の `manual\index.html`（TGUN の「ファイル」タブの「マニュアル」、F1 キー）を見てください。

## 試用版について

- すべての機能を使えます。使える期間は zip の中の `README.txt` と、TGUN の「このソフトについて」に書いてあります
  （その日を過ぎると起動しなくなります。新しい版を公開したときは、こちらの Releases でお知らせします）。
- 評価（試用）の目的で、無償で使えます。再配布・販売はできません。計算の結果は保証しません。
  条件は zip の中の `TERMS_OF_USE.txt`（利用条件）を読んでください。

## オープンソースのライセンスとソース

TGUN はオープンソースのソフトウェアを使っています（一覧とライセンスは zip の中の `THIRD_PARTY_NOTICES.txt` と
`licenses\`）。

- **mesher フォルダ**は、GNU General Public License（第 2 版以降）のもとで配布する別のプログラムです
  （メッシュ生成のヘルパ `tgun_mesh.py` と Gmsh）。`tgun_mesh.py` と Gmsh のソースは zip の中の `mesher\` にあります。
  Gmsh の DLL に組み込まれているライブラリ（OpenCASCADE、FLTK、PETSc、MED、CGNS、HDF5、Mmg、libjpeg、libpng、
  zlib など）のソースは、同じリリースのページに置いてあります（`SOURCES.txt` に一覧）。
- Qt（PySide6）は LGPL-3.0、planegcs は LGPL-2.1 のもとで使っています。`TGUN` のフォルダの DLL を差し替えて
  使うことができます。ソースの入手方法は `THIRD_PARTY_NOTICES.txt` にあります。

## 問い合わせ・不具合の報告

[Issues](../../issues) にお書きください。

---

Copyright (C) 2026 Takuya Natsui
