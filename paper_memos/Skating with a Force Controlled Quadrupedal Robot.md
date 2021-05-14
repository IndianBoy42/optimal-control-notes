読んだ論文
------------------

ETHZの論文. IROS2018で発表予定っぽい.

[https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/278902/3/iros-2018-bjelonic.pdf]


概要
------------------

ANYmalの足先に受動輪と爪をつけて, スケーティング動作ができるような動作計画と動作制御手法を提案した研究. ４脚ロボットや二足歩行ロボットにスケート動作をさせる研究は存在していたが, それらの多くが位置制御に基づいていた. この研究では, 全関節トルク制御が可能なANYmalを用いることで, 力制御ベースのスケート動作生成法および制御手法を提案したことが主な貢献となっている. 具体的には, ZMPをベースにして重心動作計画を行い, 脚の動作に関しては, 爪を使ったpushing phaseと, 車輪部を使ったgliding phaseに分けてそれぞれ動作計画を行なっている.  動作制御に関しては, J. PrattのVirtual Model Controlと, スケート動作に特有な非ホロノミック拘束を考慮した反力最適化問題を解くアプローチを採っている.

動画
------------------

<iframe width="560" height="315" frameborder="0" allowfullscreen="" src="//www.youtube.com/embed/fJfAWiylpxw"></iframe><br><a href="https://youtube.com/watch?v=fJfAWiylpxw">Planning and Control of Skating Motions for Quadrupedal Robots</a>

次に読む論文
------------------

久しぶりに4脚の論文を読んだので, 面白そうな論文がたくさん引用されている. 

[1] M. Hutter, C. Gehring, M. A. Hopflinger, M. Bl ¨ osch, and R. Siegwart,  “Toward combining speed, efficiency, versatility, and robustness in an autonomous quadruped,” IEEE Transactions on Robotics, 2014.

[2] M. Hutter, C. Gehring, D. Jud, A. Lauber, C. D. Bellicoso, V. Tsounis, J. Hwangbo, K. Bodie, P. Fankhauser, M. Bloesch, et al., “ANYmal - a highly mobile and dynamic quadrupedal robot,” in IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS),
2016.

[3] M. Hutter, C. Gehring, A. Lauber, F. Gunther, C. Bellicoso, V. Tsounis, P. Fankhauser, R. Diethelm, S. Bachmann, M. Bloesch, et al., “ANYmal - toward legged robots for harsh environments,” Advanced
Robotics, 2017.

[4] W. Reid, F. J. Perez-Grau, A. H. G ´ okto ¨ gan, and S. Sukkarieh, “Actively ˘ articulated suspension for a wheel-on-leg rover operating on a martian analog surface,” in IEEE International Conference on Robotics and
Automation (ICRA), 2016.

[10] C. D. Bellicoso, F. Jenelten, C. Gehring, and M. Hutter, “Dynamic locomotion through online nonlinear motion optimization for
quadrupedal robots,” IEEE Robotics and Automation Letters, 2018.

[12] C. Gehring, S. Coros, M. Hutler, C. D. Bellicoso, H. Heijnen, R. Diethelm, M. Bloesch, P. Fankhauser, J. Hwangbo, M. Hoepflinger, et al., “Practice makes perfect: An optimization-based approach to controlling agile motions for a quadruped robot,” IEEE Robotics & Automation Magazine, 2016

[13] G. Bellegarda, K. van Teeffelen, and K. Byl, “Design and evaluation of skating motions for a dexterous quadruped,” in IEEE International Conference on Robotics and Automation, 2018.

[22] C. D. Bellicoso, M. Bjelonic, L. Wellhausen, K. Holtmann, F. Gunther, M. Tranzatto, P. Fankhauser, and M. Hutter, “Advances in real-world applications for legged robots,” under review for Journal of Field Robotics, 2018.

[26] M. Bloesch, C. Gehring, P. Fankhauser, M. Hutter, M. A. Hoepflinger, and R. Siegwart, “State estimation for legged robots on unstable and slippery terrain,” in IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2013.

