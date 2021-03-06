# マルウェア感染ネットワークの遮断最適化問題について

マルウェア感染ネットワークの遮断最適化問題とは、企業内ネットワークにマルウェアが感染した際、
ネットワークの遮断範囲によって生じるさらなる感染リスクとビジネス損失のトレードオフにおいて、
リスク＋損失を最小にするようなネットワークの遮断方法を計算する問題のことです。
詳細は[CSS2020](https://www.iwsec.org/css/2020/)の予稿集「2C2-1: アニーリング計算を用いたマルウェア感染ネットワークの遮断最適化」をご確認ください。



## サンプル問題のダウンロード

サンプル問題は[こちら](https://github.com/FujitsuLaboratories/NetworkDisconnectivityOptimization/archive/master.zip)からダウンロードできます。

### 公開している問題一覧

| フォルダ名 | 詳細                                                         |
| ---------- | ------------------------------------------------------------ |
| 10_10_10   | 各クラスタに端末が10個ずつ、計30個からなる3-クラスタ型ネットワークのサンプル問題 |
| 73_73_73   | 各クラスタに端末が73個ずつ、計219個からなる3-クラスタ型ネットワークのサンプル問題 |



### 問題ごとのファイル一覧

* ネットワークの遮断最適化問題のパラメータ設定を記述したファイル

| ファイル名          | 詳細                                                         |
| ------------------- | ------------------------------------------------------------ |
| params/cv.txt       | 辺の価値係数を保存するファイル。i行j列の数字は、機器iと機器jを結ぶ辺の価値係数cv_{i,j}を表します。 |
| params/incident.txt | マルウェアに感染した機器の番号を保存するファイル。           |
| params/num_v.txt    | ネットワークに属する機器の数を保存するファイル               |
| params/value_st.txt | 各機器の資産価値を保存するファイル。i番目の数字は機器iの資産価値v_iを表します。 |
| params/w.txt        | 各辺の通信量を保存するファイル。i行j列の数字は機器iと機器jを結ぶ辺の通信量w_{i,j}を表します。 |

* 上記の問題から生成されるハミルトニアンを保存するファイル
  * ハミルトニアンの計算方法は、[CSS2020](https://www.iwsec.org/css/2020/)の予稿集「2C2-1: アニーリング計算を用いたマルウェア感染ネットワークの遮断最適化」の第3章をご確認ください。

| ファイル名                  | 詳細                                                         |
| --------------------------- | ------------------------------------------------------------ |
| hamiltonian/hamiltonian.txt | ハミルトニアン（＝リスク関数＋損失関数）を記述したファイル   |
| hamiltonian/risk.txt        | リスク関数を記述したファイル                                 |
| hamiltonian/loss.txt        | 損失関数を記述したファイル                                   |
| hamiltonian/ans.txt         | DAが計算した解とその解のハミルトニアンの値を記述したファイル |









