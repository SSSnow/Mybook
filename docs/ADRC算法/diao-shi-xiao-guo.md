#PID控制算法与ADRC算法调试效果对比
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





















