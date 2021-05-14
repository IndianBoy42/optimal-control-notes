論文情報
------------------

##### 論文リンク

[IEEE xploreのリンク](https://ieeexplore.ieee.org/abstract/document/8443115/)

##### Bibtex

    @ARTICLE{8443115, 
    author={A. Giusti and J. Malzahn and N. G. Tsagarakis and M. Althoff}, 
    journal={IEEE Transactions on Robotics}, 
    title={On the Combined Inverse-Dynamics/Passivity-Based Control of Elastic-Joint Robots},
    year={2018}, 
    volume={}, 
    number={}, 
    pages={1-11}, 
    doi={10.1109/TRO.2018.2861917}, 
    month={},}

##### 論文概要の動画
なし.

どんなもの？(概要)
------------------
弾性関節を有するロボットに対して, モデルの不確かさや外乱に対して頑健な制御方法を提案.  
具体的には, 弾性関節を考慮した逆動力学演算と受動性に基づいた制御法を組み合わせ, さらに従来のニュートン・オイラーアルゴリズムを活用することで高速に演算可能な方法を提案した.

先行研究と比べてどこがすごい？(新規性)
------------------
弾性関節を考慮した逆動力学演算と, 受動性に基づいた制御法を組み合わせた研究は本論文が初めて.
提案法によって制御系のロバスト性を向上することが可能.
著者らは過去に会議論文を発表しており, 差分として以下の三点を主張している.
1. モデルの不確かさと外乱に対するロバスト性の詳細な解析
2. フィードフォワード 逆動力学補償の演算において, 応答値でなく指令値に基づいて計算
3. 弾性関節を有する7軸ロボットで実験を実施

技術や手法の肝はどこ？(技術・手法の詳細)
------------------
弾性関節を有するロボットの逆動力学演算と, 受動性を用いた制御則を組み合わせる方法の設計法.
また, 提案法を単純に計算すると, 従来法と比較して著しく計算量が増加してしまうが, ニュートン・オイラー法を利用して効率化する方法を考案している.

どうやって有効だと検証した？(実装・実験方法)
------------------
弾性関節を有する7軸ロボットで手先位置決め制御の実験を実施.
実験に用いたロボットは, 弾性関節と非弾性関節の双方を有するロボットであるが, この点に関しても対応可能であることを示している.

議論はある？(未解決課題)
------------------
以下の課題が残っている.  
- 弾性がより低い場合の検討
- 制御系のパラメータはファインチューニングしているので, 調整法に関して課題が残っている

コメントがあれば
------------------
弾性関節を有している場合の逆動力学演算を参考にする.

次に読むべき文献は？
------------------

-  S. Avila-Becerril, A. Loria, and E. Panteley, “A separation principle for
underactuated lossless Lagrangian systems,” IEEE Trans. Autom. Control,
vol. 62, no. 10, pp. 5318–5323, Oct. 2017.
- G. Buondonno and A. De Luca, “A recursive Newton-Euler algorithm for
robots with elastic joints and its application to control,” in Proc. IEEE/RSJ
Int. Conf. Intell. Robots Syst., 2015, pp. 5526–5532.
- A. Muller, “Recursive second-order inverse dynamics for serial manipu- ¨
lators,” in Proc. IEEE Int. Conf. Robot. Automat., 2017, pp. 2483–2489.
-  R. Ortega, A. J. Van Der Schaft, I. Mareels, and B. Maschke, “Putting
energy back in control,” IEEE Control Syst., vol. 21, no. 2, pp. 18–33,
Apr. 2001.
- G. Buondonno and A. De Luca, “Efficient computation of inverse dynamics
and feedback linearization for VSA-based robots,” IEEE Robot.
Automat. Lett., vol. 1, no. 2, pp. 908–915, Jul. 2016.
