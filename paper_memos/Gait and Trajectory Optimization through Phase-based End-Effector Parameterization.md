論文情報
------------------

### 著者情報

ETHZの論文. Robotics and Automation lettersの論文.
[https://ieeexplore.ieee.org/document/8283570/:title]

### 論文概要の動画
<iframe width="560" height="315" frameborder="0" allowfullscreen="" src="//www.youtube.com/embed/0jE46GqzxMM"></iframe><br><a href="https://youtube.com/watch?v=0jE46GqzxMM">Gait and Trajectory Optimization through Phase-based End-Effector Parameterization</a>
  
なんと著者によるチュートリアル動画まである. すごい.  
[https://www.youtube.com/watch?v=KhWuLvb934g:embed:cite]

どんなもの？(概要)
------------------
歩行ロボットの歩容パターン, 一歩毎のタイミング, 着地地点, 遊脚動作や胴体(重心)の動作計画を決定する問題を, １つの最適化問題として定式化して解く方法を提案した研究. フラットでない地形における歩行パターンの生成も可能.  

先行研究と比べてどこがすごい？(関連研究との比較)
------------------
歩行ロボットの歩行パターンの生成は, 重心動作や遊脚動作についてそれぞれ独立に軌道計画が行われる場合が多い.  
本研究では, それらの処理を全て同時に, １つの最適化問題として定式化した点が最大の貢献となっている. 

技術や手法の肝はどこ？(新規性)
------------------
歩行パターンの生成問題は, タイミングなどの離散的な事象を含むので, 混合整数最適化問題となる.  
この時, 決定すべき変数が多くなると, 計算時間が問題となる. 本研究ではこの問題を避け, 連続非線形最適化問題として定式化する方法を提案した.  
これにより, 通常の非線形最適化ソルバを適用することができ, 数秒程度で全体の動作を計画することが可能となった.

どうやって有効だと検証した？(実験方法)
------------------
二足歩行ロボットモデルおよび４脚歩行ロボットモデル(ANYmal, HyQ)に対して動作計画を行なった. 詳細については上述の動画を参照.

議論はある？(未解決課題)
------------------
以下の課題が残っている.  
- 本手法では, 脚部の質量が胴体部と比較して無視できると仮定している (いわゆる単質点近似モデル). よって, 脚部が重いロボットに対してはダイナミクスの誤差が無視できなくなるので, 詳細なダイナミクスモデルを仮定する必要がある.  
- 床面の状態に関する拘束(床との衝突, 摩擦円錐など)は脚動作の軌道の交差点上でしか考慮されていないので, 制約を破ってしまう危険性がある (ここはよく分かってない).
- 床面が複雑すぎると局所最適解に陥る
  
今後の計画として, 最適化の計算時間をより短縮してモデル予測制御的な逐次最適化アプローチへと拡張する予定とのことである.

次に読むべき文献は？
------------------
著者, 論文めっちゃ書いてる.

[1] J. T. Betts, “Survey of numerical methods for trajectory optimization,” J. Guid., Control, Dyn., vol. 21, no. 2, pp. 193–207, 1998. [Online]. Available: http://arc.aiaa.org/doi/abs/10.2514/2.4231

[2] A. W. Winkler, “TOWR—An open-source trajecetory optimizer for legged robots in C++.” 2018. [Online]. Available: http://wiki.ros.org/towr

[9] A. W. Winkler, F. Farshidian, D. Pardo, M. Neunert, and J. Buchli, “Fast trajectory optimization for legged robots using vertex-based ZMP constraints,” IEEE Robot. Autom. Lett., vol. 2, no. 4, pp. 2201–2208, Oct. 2017.

[21] D. Pardo, M. Neunert, A. W. Winkler, R. Grandia, and J. Buchli, “Hybrid direct collocation and control in the constraint-consistent subspace for dynamic legged robot locomotion,” in Proc. Robot., Sci. Syst., 2017. [Online]. Available: http://www.roboticsproceedings.org/rss13/p42.html

[25] A. Herzog, S. Schaal, and L. Righetti, “Structured contact force optimization for kino-dynamic motion generation,” in Proc. IEEE Int. Conf. Intell. Robots Syst., 2016, pp. 2703–2710.

[27] A. Ibanez, P. Bidaud, and V. Padois, “Emergence of humanoid walking behaviors from mixed-integer model predictive control,” in Proc. IEEE Int. Conf. Intell. Robots Syst., 2014, pp. 4014–4021.

[28] R. Deits and R. Tedrake, “Footstep planning on uneven terrain with mixedinteger convex optimization,” in Proc. IEEE-RAS Int. Conf. Humanoid Robots, 2015, pp. 279–286.

[29] M. Neunert, F. Farshidian, A. W. Winkler, and J. Buchli, “Trajectory optimization through contacts and automatic gait discovery for quadrupeds,” IEEE Robot. Autom. Lett., vol. 2, no. 3, pp. 1502–1509, Jul. 2017.

[31] M. Posa, C. Cantu, and R. Tedrake, “A direct method for trajectory optimization of rigid bodies through contact,” Int. J. Robot. Res., vol. 33, no. 1, pp. 69–81, 2013. [Online]. Available: http://ijr.sagepub.com/content/33/1/69.short

[33] M. Diehl, H. G. Bock, H. Diedam, and P. B. Wieber, “Fast direct multiple shooting algorithms for optimal robot control,” in Fast Motions in Biomechanics and Robotics (Lecture Notes in Control and Information Sciences), vol. 340. Berlin, Germany: Springer, 2006, pp. 65–93.

[37] A. W. Winkler, “XPP—A collection of ROS packages for the visualization of legged robots.” 2017. [Online]. Available: http://wiki.ros.org/xpp

[39] C. Gehring et al., “Kindr library—Kinematics and dynamics for robotics,” 2016. [Online]. Available: https://docs.leggedrobotics.com/kindr/cheatsheet_latest.pdf. Accessed on: Nov. 25, 2017.
