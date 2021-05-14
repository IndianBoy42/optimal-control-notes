論文情報
------------------

##### 論文リンク

[IEEE xploreのリンク](https://ieeexplore.ieee.org/document/8338417/)

##### Bibtex

    @ARTICLE{8338417, 
    author={H. Pham and Q. Pham}, 
    journal={IEEE Transactions on Robotics}, 
    title={A New Approach to Time-Optimal Path Parameterization Based on Reachability Analysis}, 
    year={2018}, 
    volume={34}, 
    number={3}, 
    pages={645-659}, 
    doi={10.1109/TRO.2018.2819195},
    month={June},}

##### 論文概要の動画

なし

##### 実装

[TOPP-RA](https://github.com/hungpham2511/toppra)

どんなもの？(概要)
------------------
決められた軌跡に対してロボットを最短時間で移動させる動作を計画する, Time Optimal Path Parameterization (TOPP) 問題を高速に解くアルゴリズムを提案した.  
具体的には, 制御理論のreachability analysisを適用することで, 線形計画問題を解く問題へと帰着させることにより, 高速化を実現した.

先行研究と比べてどこがすごい？(新規性)
------------------
著者らが提案していた従来のTOPPアルゴリズムは数値積分を元に計算するアプローチであったが, 実装がトリッキーである上, 解を安定して求められない(failする可能性が高い)という欠点があった.  
対して, TOPP-RAでは, 線形計画問題を解く方式に帰着させるため, failすることなく解を求めることが可能になった.  
凸最適化に基づいてTOPP問題を解くアプローチは存在していたが, TOPP-RAによればさらに計算量を削減することが可能となる.

技術や手法の肝はどこ？(技術・手法の詳細)
------------------
reachability analysisに基づいて, 求めたい解(操作変数)をn点で離散化すると, 3n個の線形計画問題を解くことで求めたい解が求められることを示している. m個の不等式制約を考慮すると, O(mN)の計算量となる.  
前述の数値積分に基づいたTOPPはO(m^2N), 凸最適化に基づいたTOPPはO(mN^3)である.  
他にも, 既存の手法にはなかった, 以下の3つの利点が存在する.
- 冗長なケースが扱える
- 著者らの提案するAVP-RRTに自然に適用できる
- パラメータの不確かさを考慮した最適化が可能

どうやって有効だと検証した？(実装・実験方法)
------------------
以下の２つの数値実験を行なっている.
- 6軸のマニピュレータに対して, 速度/加速度の制約を与えた状態でTOPP問題を解く (外力なしのオイラー=ラグランジュシステムへの適用)
- ヒューマノイドロボットに対して, TOPP問題を解く (外力が加わったオイラー=ラグランジュシステムへの適用)  

詳細には, 成功率や計算時間の比較, グリッドサイズの変化による成功率への影響等を精査しているので, 論文を参照されたい.

議論はある？(未解決課題)
------------------
ジャークの制約や粘性摩擦を考慮した場合のトルクの制約が扱えない. 
それらの厳密に扱いたい場合は, 非線形な最適化問題として定式化する必要がある.
TOPP-RAでは線形計画問題を用いている性質上, 基本的には凸線形制約しか扱えないので, 非凸の制約を扱えるように拡張することが課題である.

コメントがあれば
------------------
この論文の著者らのAppendixがいつも超充実していて勉強になる. もっと読み込みたい.

次に読むべき文献は？
------------------
- S. V. Rakovic, E. C. Kerrigan, D. Q. Mayne, and J. Lygeros, “Reachability analysis of discrete-time systems with disturbances,” IEEE Trans. Automat. Control , vol. 51, no. 4, pp. 546–561, Apr. 2006. 
- M. Oberherber, H. Gattringer, and A. M ̈ uller, “Successive dynamic pro-gramming and subsequent spline optimization for smooth time optimal robot path tracking,”Mech. Sci. , vol. 6, no. 2, pp. 245–254, 2015. 
- K. Hauser, “Fast interpolation and time-optimization with contact,” Int. J. Robot. Res. , vol. 33, no. 9, pp. 1231–1250, Aug. 2014.
- Q. C. Pham, S. Caron, P. Lertkultanon, and Y. Nakamura, “Admissi-ble velocity propagation: Beyond quasi-static path planning for high-dimensional robots,”Int. J. Robot. Res. , vol. 36, no. 1, pp. 44–67, 2017.
