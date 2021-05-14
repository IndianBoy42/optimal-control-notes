論文情報
------------------

MISO ROBOTICSという会社が開発したFLIPPYというロボットシステムについての論文のようです.  
MISOは味噌？ ベンチャーの開発成果をRA-Lみたいな論文誌に通して技術力をアピールするのは海外では普通なんだろうか. すごい.

##### 論文リンク

[IEEE xploreのリンク](https://ieeexplore.ieee.org/abstract/document/8410040/:title)

##### Bibtex

    @ARTICLE{8410040, 
    author={S. Kolathaya and W. Guffey and R. W. Sinnet and A. D. Ames}, 
    journal={IEEE Robotics and Automation Letters}, 
    title={Direct Collocation for Dynamic Behaviors With Nonprehensile Contacts: Application to Flipping Burgers}, 
    year={2018}, 
    volume={3}, 
    number={4}, 
    pages={3677-3684}, 
    doi={10.1109/LRA.2018.2854910}, 
    month={Oct},}

##### 論文概要の動画

<iframe src="https://player.vimeo.com/video/234073915" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/234073915">FLIPPY | Miso Robotics</a> from <a href="https://vimeo.com/misorobotics">Miso Robotics</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

どんなもの？(概要)
------------------
nonprehensile contactとは, 把持を伴わない摩擦だけを介した接触のことを指す.  
本論文では, nonprehensile object manipulationの例としてハンバーガのパティをひっくり返すためのロボットマニピュレータの動作計画を提案している.  
パティをひっくり返すためには, パティの場所にエンドエフェクタ(ヘラ)を誘導する動作に始まり, パティをすくい上げる(ヘラの上に載せる)動作, 持ち上げる動作, ひっくり返す動作など, 一連の動作を計画する必要がある.  
本研究では, direct collocation法を用いて, これらの一連の動作に関する軌道最適化を行う方法を提案している.

先行研究と比べてどこがすごい？(新規性)
------------------
類似の研究事例として, パンケーキをひっくり返す動作の軌道計画を行う方法が提案されていた.  
従来研究では作業空間での軌道を計画し, 得られた軌道に対して逆運動学計算を行って関節動作へとマッピングする方法を提案していたが, この方法でグリル上の動作を計画してみると, 特異姿勢等の問題で解が得られないケースがあった.  
その問題点を解決することをモチベーションにして, 関節空間で軌道を計画するような問題設定とした点が従来研究との違いである. 

技術や手法の肝はどこ？(技術・手法の詳細)
------------------
direct collocation法を用いた軌道計画法を提案しており, パティひっくり返しの為の制約条件や初期・終端条件等を詳細に提示している点が学術的な貢献となっている.  
ひとたび一般的な最適化問題として定式化できれば, ソルバに投げるだけで解が得られるので, 汎用性が高いというメリットがある上, 評価関数や拘束条件の変更が容易なので, 有用性の面でも貢献度が高いと言える. また, 実応用の観点では計算が高速である必要があるため, 最適化計算が高速化されるような工夫を行っている(この部分がよくわからんかった).  

どうやって有効だと検証した？(実装・実験方法)
------------------
グリルの上の１０箇所をランダムに選択し, それぞれの場所でパティをひっくり返す実験を１０回ずつ実施した.  
特にヘラとパティの接触が伴う動作である, 1. すくい上げ, 2. 持ち上げ, 3. ひっくり返し, の３つの動作について評価したところ, 100%成功するケースとそうでないケースがあった. ワーストケースでは70%の成功率であった.

議論はある？(未解決課題)
------------------
実験的な観察に基づくと, パティの高さ(グリルの位置)の違いに非常に敏感で, 成功率が大きく変動することがわかった.  
他にも, 油が多いと滑りやすくて失敗したり, グリルの温度が低いとパティがネバネバして失敗したり, パティが部分的に崩れていると失敗しやすいらしい.  

コメントがあれば
------------------
失敗原因については, そりゃそうだという感じだけど, 論文にこういうことを書いてくれるのはいいことだと思う.

次に読むべき文献は？
------------------

- A. Cowley, B. Cohen, W. Marshall, C. J. Taylor, M. Likhachev, "Perception and motion planning for pick-and-place of dynamic objects", Proc. IEEE/RSJ Int. Conf. Intell. Robots Syst., pp. 816-823, 2013.
- K. M. Lynch, "Issues in nonprehensile manipulation", Proc. Robot. Algorithmic Perspective 3rd Workshop Algorithmic Found. Robot., pp. 237-250, 1998.
- T. Tsuji, J. Ohkuma, S. Sakaino, "Dynamic object manipulation considering contact condition of robot with tool", IEEE Trans. Ind. Electron., vol. 63, no. 3, pp. 1972-1980, Mar. 2016.
- A. Hereid, A. D. Ames, "FROST: Fast robot optimization and simulation toolkit", Proc. IEEE/RSJ Int. Conf. Intell. Robots Syst., pp. 719-726, Sep. 2017.
- A. Hereid, E. A. Cousineau, C. M. Hubicki, A. D. Ames, "3D dynamic walking with underactuated humanoid robots: A direct collocation framework for optimizing hybrid zero dynamics", Proc. IEEE Int. Conf. Robot. Automat., pp. 1447-1454, May 2016.
- C. R. Hargraves, S. W. Paris, "Direct trajectory optimization using nonlinear programming and collocation", J. Guid. Control Dyn., vol. 10, no. 4, pp. 338-342, 1987.
- M. Posa, C. Cantu, R. Tedrake, "A direct method for trajectory optimization of rigid bodies through contact", Int. J. Robot. Res., vol. 33, no. 1, pp. 69-81, 2014.
- J. Betts, Practical Methods for Optimal Control and Estimation Using Nonlinear Programming, Philadelphia, PA, USA:SIAM, 2010.
- H. Zhao, S. N. Yadukumar, A. D. Ames, "Bipedal robotic running with partial hybrid zero dynamics and human-inspired optimization", Proc. IEEE/RSJ Int. Conf. Intell. Robots Syst., pp. 1821-1827, Oct. 2012.


