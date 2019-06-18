#PID控制算法与ADRC算法调试效果对比
首先我们先简单看下数据对比效果，如下图所示，比较姿态模式横滚通道和俯仰通道的自稳效果。
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


