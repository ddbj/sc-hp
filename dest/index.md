


# 遺伝研スーパーコンピュータシステム

 

国立遺伝学研究所は生命・医学系研究における情報処理のための大規模計算基盤として、大規模クラスタ型計算機・大規模メモリ共有型計算機・大容量高速ディスク装置を備えた最新鋭のスーパーコンピュータシステムサービスを提供しています。

![top\_image2.png](%E9%81%BA%E4%BC%9D%E7%A0%94%E3%82%B9%E3%83%BC%E3%83%91%E3%83%BC%E3%82%B3%E3%83%B3%E3%83%94%E3%83%A5%E3%83%BC%E3%82%BF%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0_files/top_image2.png "top_image2.png")

 

**![caution.png](%E9%81%BA%E4%BC%9D%E7%A0%94%E3%82%B9%E3%83%BC%E3%83%91%E3%83%BC%E3%82%B3%E3%83%B3%E3%83%94%E3%83%A5%E3%83%BC%E3%82%BF%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0_files/a4910b91-4299-4da0-aa28-80fd159914bc.png "caution.png"){.image-inline} ディスク容量が逼迫しているためユーザーホームディレクトリ内のデータについて当研究所ではバックアップを取っておりません。[免責事項](https://sc.ddbj.nig.ac.jp/ja/application/regulations/844bwb)の通り、利用者の責任においてバックアップを取っていただくようお願いいたします。** 

------------------------------------------------------------------------

## 新着情報

### Asperaの構成変更について {#asperaの構成変更について style="border-bottom: solid 0.5px #7db4e6; padding: 0.25em 0.5em; border-left: solid 8px #7db4e6;"}

2020.08.27

これまではAsperaを使用する場合には、遺伝研スパコンのサポートまでご連絡頂いてAspera用のユーザー登録を別途行って頂く運用になって
おりましたが、構成を変更し、一般解析環境のユーザーは特別な申請なしに大規模データのアップロード、ダウンロードを行えるようにしました。利用方法は「[システム利用案内
\>
一般解析環境におけるファイル転送の方法](https://sc.ddbj.nig.ac.jp/ja/guide/usage-for-general-analysis-environment/file-transfer)」をご参照ください。

 

個人ゲノム解析環境につきましてはさくらインターネット（株）社のHCPToolsを用いてAsperaと同様の機能を提供するよう準備しており、近日中に利用可能となります。

 

### 個人ゲノム解析環境のゲートウェイ構成変更について

2020.06.30

これまで個人ゲノム解析環境ではデータのアップロード、ダウンロード時に
一旦検疫ゲートウェイサーバーにデータをコピーし検疫を行うようお願いしておりましたが、
検疫ゲートウェイサーバーが混雑し処理速度が低下していたため、
今回これを廃止し、直接ユーザーディレクトリにデータ転送できるよう、構成を変更いたしました。


これに伴いSSL-VPNクライアントソフトウェアのポート番号の変更(10443 =\>
443)をお願いいたします。
これによりデータ転送が簡便になり速度も向上します。

VPN接続ポートの変更手順については、下記URLをご参照ください。

- [Mac版](https://sc.ddbj.nig.ac.jp/ja/guide/usage-for-analysis-environment-for-individual-genomes/longin-mac)
- [Linux版](https://sc.ddbj.nig.ac.jp/ja/guide/usage-for-analysis-environment-for-individual-genomes/login-linux)
- [Windows版](https://sc.ddbj.nig.ac.jp/ja/guide/usage-for-analysis-environment-for-individual-genomes/login-windows)

 

### 遺伝研スパコンの計算ノード増設について

 2020.04.01

遺伝研スパコンシステムは、2020年4月1よりシステムが増強され、計算ノードの総コア数が11,696コアから15,280コアへ増加しました。

追加されるサーバは、AMDの最新型CPU（AMD EPYC
Rome）を搭載しており、スパコンシステム一般解析区画のThin計算ノードほぼ全て（epyc.qノード全体並びにGPUノードを除くlogin.qノード）がこれに入れ替わります。

これによりコア当たりの浮動小数点演算性能が倍増します（16GFLOPS/core →
32GFLOPS/core）。

 

入れ替え前後におけるThin計算ノードの詳細情報は以下の通りです。

<table>
<th>
<td>計算ノード</td><td>変更前</td><td>変更後</td>
<th>
<th>
<td>プロセッサ名</td><td>変更前</td><td>変更後</td>
<th>

</table>
+-----------------------+-----------------------+-----------------------+
| **計算ノード**        | #### **変更前**       | #### **変更後**       |
|                       |                       |                       |
| **プロセッサ名**      | **Thin Type 1**       | **Thin Type 1\        |
|                       |                       | **                    |
|                       | **AMD EPYC7501**      |                       |
|                       |                       | **AMD EPYC7702\       |
|                       |                       | **                    |
+=======================+=======================+=======================+
| **コードネーム**      |  Naples               | Rome                  |
+-----------------------+-----------------------+-----------------------+
| **リリース時期**      | 2017年第2四半期　　　 | 2019年第2四半期　　　 |
+-----------------------+-----------------------+-----------------------+
| **コア数**            | 32（ノード当たり64コア） | 64（ノード当たり128コア） |
+-----------------------+-----------------------+-----------------------+
| **スレッド数**        | 64                    | 128                   |
+-----------------------+-----------------------+-----------------------+
| **クロックスピード**  | 2.0GHz                | 2.0GHz                |
+-----------------------+-----------------------+-----------------------+
| **理論演算性能(CPU当たり)** | 512GFLOPS       | 2048GFLOPS            |
+-----------------------+-----------------------+-----------------------+
| **boost最大周波数**   | 3GHz                  | 3.35GHz               |
+-----------------------+-----------------------+-----------------------+
| **Cache**             | 64MB                  | 256MB                 |
+-----------------------+-----------------------+-----------------------+
| **台数内訳**          | epyc.q 45台、login.q  | epyc.q 25台、login.q  |
|                       | 6台                   | 3台                   |
+-----------------------+-----------------------+-----------------------+

 

</div>

 

### ログインアカウントの年度末更新について {#ログインアカウントの年度末更新について style="border-bottom: solid 0.5px #7db4e6; padding: 0.25em 0.5em; border-left: solid 8px #7db4e6;"}

[ログインアカウント年度末更新・停止申請](https://sc2.ddbj.nig.ac.jp/index.php/ja-application-continue)

  

[ \>\> その他の新着情報](https://sc.ddbj.nig.ac.jp/ja/operation/news)

------------------------------------------------------------------------

メンテナンス情報 {#メンテナンス情報 style="position: relative; padding: 5px 5px 5px 42px; background: #77c3df; color: white; margin-left: -33px; line-height: 1.3; z-index: -1;"}
----------------

2020.07.01

今年度の定期メンテナンスは11月頃(遺伝研法廷停電の日程による）、3月末(ストレージ増設)の2回を予定しています。 

::: {#content-core .section style="box-sizing: border-box; color: #4d4d4d; display: block; font-family: &quot; roboto&quot;,&quot;helvetica neue&quot;,helvetica,arial,sans-serif; font-size: 14px; font-style: normal; font-variant: normal; font-weight: 500; letter-spacing: normal; orphans: 2; text-align: left; text-decoration: none; text-indent: 0px; text-transform: none; -webkit-text-stroke-width: 0px; white-space: normal; word-spacing: 0px;"}
::: {#parent-fieldname-text style="box-sizing: border-box;"}
 
:::
:::

::: {#content-core .section}
::: {#parent-fieldname-text}
 
:::
:::

 

[\>\>
その他のメンテナンス情報 ](https://sc.ddbj.nig.ac.jp/ja/operation/maintenance)

 

------------------------------------------------------------------------

謝辞について {#謝辞について style="position: relative; padding: 5px 5px 5px 42px; background: #77c3df; color: white; margin-left: -33px; line-height: 1.3; z-index: -1;"}
------------

遺伝研スーパーコンピュータシステムの活動は皆様の謝辞で評価されています。当スーパーコンピュータシステムを利用した論文が採択された際には以下の記載例を参考に謝辞への記載をお願いします。

記載例\
==============================================\
　　＜謝辞　英語＞\
　　Computations were partially performed on the NIG supercomputer\
　　at ROIS National Institute of Genetics.\
==============================================\
　　＜謝辞　日本語＞\
　　本研究は、情報・システム研究機構 国立遺伝学研究所が\
　　有する遺伝研スーパーコンピュータシステムを利用しました。\
================================================

その他 {#その他 style="position: relative; padding: 5px 5px 5px 42px; background: #77c3df; color: white; margin-left: -33px; line-height: 1.3; z-index: -1;"}
------

[サイトポリシーと個人情報の取り扱いについて](https://sc.ddbj.nig.ac.jp/ja/guide/site-policy)

 

 
:::
:::

::: {#viewlet-below-content-body .section}
::: {.visualClear}
:::

::: {.documentActions}
:::
:::
:::
:::

::: {.col-xs-12 .col-sm-12}
::: {#viewlet-below-content}
:::
:::
:::

::: {#column2-container}
:::
:::
:::
:::

::: {#portal-footer .container}
::: {.row}
::: {.col-xs-12}
<div>

Resarch Organization of Information and Systems\
National Institute of Genetics.\
This Home Page is licensed under a [Creative Commons 表示 2.1 日本
License.](http://creativecommons.org/licenses/by/2.1/jp/) © 2018

</div>
:::
:::
:::
