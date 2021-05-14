論文情報
------------------

##### 論文リンク

[IEEE xploreのリンク](https://ieeexplore.ieee.org/document/8392756/)

##### Bibtex

    @ARTICLE{8392756, 
    author={D. Kaserer and H. Gattringer and A. Müller}, 
    journal={IEEE Robotics and Automation Letters}, 
    title={Online Robot-Object Synchronization With Geometric Constraints and Limits on Velocity, Acceleration, and Jerk}, 
    year={2018}, 
    volume={3}, 
    number={4}, 
    pages={3169-3176}, 
    doi={10.1109/LRA.2018.2849827}, 
    month={Oct},}

##### 論文概要の動画

https://ieeexplore.ieee.org/document/8392756/media

どんなもの？(概要)
------------------
移動物体とロボットマニピュレータの手先を同期させる軌道を計画するための研究.  
軌道計画の問題をGeometric Path Planning(GPP)の問題と, Time Optimal Path Parameterization (TOPP), Time Scalingの3つの問題に分離して, それぞれの問題を実時間で計算できるよう定式化した.  
結果的に, 全てのステップを100ms以内で計算できるようになった. 

先行研究と比べてどこがすごい？(新規性)
------------------
従来研究では, 速度, 加速度, ジャークの制約を考慮したものがあったが, 軌跡の幾何学的な制約を考慮していなかった.  
一方で, 著者らの過去の研究では, 軌跡の制約も考慮した手法を提案していた.  
本論文における違いは, 最適化問題の解き方が異なる点にある.  
リアルタイム性を意識して, それぞれのステップでいくつものテクニックを提案している.

技術や手法の肝はどこ？(技術・手法の詳細)
------------------
それぞれのステップで以下のような工夫を提案している.
- GPPの問題をB-スプラインの係数最適化問題(QP)に定式化して高速に解く
- TOPPを線形計画問題として定式化して高速に解く. ジャーク制約は非線形制約だが, 二回解くことで線形制約として扱う.
- Time Scalingの問題をQPとして定式化することで高速に解く

どうやって有効だと検証した？(実装・実験方法)
------------------
ロボットを二台用意して, 片方の手先を固定して定速で移動させる.  
それに対して, もう一方のロボットの手先を同期させるよう軌道計画した.
結果的に, 全ての試行で軌道計画に成功し, 100ms以下での計算が可能であった.

議論はある？(未解決課題)
------------------
特に記載なし.

コメントがあれば
------------------
過去の文献との比較が少ない気がする.

次に読むべき文献は？
------------------

 - R. Lampariello, D. Nguyen-Tuong, C. Castellini, G. Hirzinger, and J. Peters, “Trajectory planning for optimal robot catching in real-time,” in Proc. IEEE Int. Conf. Robot. Autom. , 2011, pp. 3719–3726. 
- B. B ̈auml,T.Wimb ̈ ock, and G. Hirzinger, “Kinematically optimal catching a flying ball with a hand-arm-system,” in Proc. IEEE Int. Conf. Intell. Robots Syst. , 2010, pp. 2592–2599. 
- T. Kr ̈oger,On-Line  Trajectory  Generation  in  Robotics  Systems ,B. Siciliano, O. Khatib, and F. Groen, Eds. Berlin, Germany: Springer, 2010. 
- A. Reiter, H. Gattringer, and A. M ̈ uller, “Real-time computation of inexact minimum-energy trajectories using parametric sensitivities,” in Advances in Service and Industrial Robotics , C. Ferraresi and G. Quaglia, Eds. New York, NY, USA: Springer, 2018, pp. 174–182. 
- H. Gattringer, M. Oberherber, and K. Springer, “Extending continuous path trajectories to point-to-point trajectories by varying intermediate points,”Int. J. Mech. Control , vol. 15, no. 01, pp. 35–43, 2014. 
