#PID控制算法与ADRC算法角速率调试效果对比
首先我们先简单看下数据对比效果，使用数据均来自测试飞行，测试飞机为轴距300的四旋翼。
* 比较姿态模式横滚通道和俯仰通道的自稳效果。
![](/assets/Roll_Stablize.png)
![](/assets/Pitch_Stablize.png)
数据说明如下：
PIDR_r:表示悬停时使用PID控制器的 Rollrate的设定值；
PIDP_r:表示悬停时使用PID控制器的 Pitchrate的设定值；
PIDR_y:表示悬停时使用PID控制器的 Rollrate的测量值；
PIDP_y:表示悬停时使用PID控制器的 Pitchrate的测量值；
ADRCR_r:表示悬停时使用ADRC的 Rollrate的设定值；
ADRCP_r:表示悬停时使用ADRC的 Pitchrate的设定值；
ADRCR_y:表示悬停时使用ADRC的 Rollrate的测量值；
ADRCP_y:表示悬停时使用ADRC的 Pitchrate的测量值；
数据处理说明：
数据处理：将PID控制器的输入输出整体+0.2， 为了分离PID-ADRC两种控制器的输入输出，便于对比数据；
结论：
数据显示，在小设定值的情况下,ADRC跟踪性能明显优于PID控制器。

* 比较设定值变化比较大的情况下的横滚通道和俯仰通道的动态效果
![](/assets/Roll_Resp.png)
![](/assets/Pitch_Resp.png)
数据说明如下：
PID_Roll_r:表示悬停时使用PID控制器的 Rollrate的设定值；
PID_Pitch_r:表示悬停时使用PID控制器的 Pitchrate的设定值；
PID_Roll_y:表示悬停时使用PID控制器的 Rollrate的测量值；
PID_Pitch_y:表示悬停时使用PID控制器的 Pitchrate的测量值；
ADRC_Roll_r:表示悬停时使用ADRC的 Rollrate的设定值；
ADRC_Pitch_r:表示悬停时使用ADRC的 Pitchrate的设定值；
ADRC_Roll_y:表示悬停时使用ADRC的 Rollrate的测量值；
ADRC_Pitch_y:表示悬停时使用ADRC的 Pitchrate的测量值；

数据处理：将PID控制器的输入输出整体+5， 为了分离PID-ADRC两种控制器的输入输出，便于对比数据；

结论：
数据显示，在动态响应的快速性和超调上ADRC与PID控制器相当，基本都在60-80ms之间；但在恢复到稳态是，ADRC明显比PID控制器更平稳，无静态误差，如上图中红框所示；

最后再通过扫频得到了ADRC频域数据，扫频范围在2~35rad/s(0.3~5.5Hz),扫频结果如下图所示，
- 横滚通道扫频
![](/assets/ADRC_RollSP.jpg)
- 俯仰通道扫频

![](/assets/ADRC_PitchSP.jpg)

从横滚和俯仰内环的幅频特性图可以看出。扫频的频率范围为2-35rad/s（0.3-5.5Hz）。从图中可以看出，在2-30rad/s的频率范围内，几乎无超调，截止频率大约在25rad/s。相频特性曲线从0度逐渐下降到-180，说明延迟在逐渐增大。穿越频率大约在23rad/s。从截止频率和穿越频率两个指标来看，内环的响应速度很快，且无超调，但是稳定裕度偏低。





















