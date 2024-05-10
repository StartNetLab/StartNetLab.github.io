---
permalink: /
title: "START Net Lab"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Tencent START Cloud Gaming

Achieving Ultra-Low Latency in Cloud Gaming
======
![Poster](./images/nsdi_poster_midsize.jpg)

Pudica: Toward Near-Zero Queuing Delay in Congestion Control for Cloud Gaming
------
Cloud gaming users have stringent requirements for both latency and bitrate, which further demands congestion control algorithms to satisfy the following three aspects. Firstly, it should achieve high link utilization without relying on overshootbased network probing. Secondly, it should avoid heavy queuing when multiple homogeneous flows coexist. Thirdly, in the presence of frequent bandwidth drops on the current internet, the congestion control algorithm must react promptly to sudden degradation of link conditions and empty bottleneck queues as soon as possible.

We has proposed a congestion control algorithm called Pudica, aiming for zero queuing and suitable for interactive streaming scenarios with strict requirements on latency and throughput. This algorithm ensures low latency by avoiding frame-level queuing and achieves accurate Bandwidth Utilization Ratio (BUR) estimation through an adaptive pace approach. Multiple rate control strategies are designed by utilizing long-term smoothed BUR estimation and short-term BUR estimation, which improve network bandwidth utilization and fairness while minimizing queuing delay.

Firstly, the algorithm does not intentionally trigger queuing during network probing. Instead, it estimates the link's bandwidth utilization ratio based solely on feedback from the endpoint. By adaptively controlling the pacing rate and introducing lightweight probing packets, the accuracy of link utilization estimation is effectively enhanced without triggering frame-level queuing. 

Based on the estimated link bandwidth utilization ratio, the algorithm employs multiple rate control strategies. When the link utilization is low, it adopts a multiplicative increase approach to boost the bitrate, quickly increasing the link utilization while ensuring it remains below 100%, thus achieving the goal of zero queuing and high link utilization. Additionally, by simultaneously applying adaptive AI and MD control methods, the algorithm can quickly converge to cross-flow fairness without causing severe queuing. Pudica algorithm also responds rapidly to any excessive adjustments of bitrate or sudden drops in link bandwidth, further consolidating its low-latency characteristics.

Pudica has been deployed on Tencent START cloud gaming platform, serving millions of players for several years. The results of the large-scale online deployment demonstrate that Pudica achieves "zero" queuing, high bandwidth utilization, and good fairness. Compared to state-of-the-art methods in the industry, Pudica reduces stall ratio by an order of magnitude while maintaining the same bitrate, and the average frame delay is reduced by 3.1 times.

Pudica has been deployed on the Tencent START cloud gaming platform, serving millions of players for several years. The large-scale online deployment of Pudica has effectively showcased Pudica's capabilities in achieving "zero" queuing, maximizing bandwidth utilization, and ensuring fairness. In comparison to state-of-the-art methods in the industry, Pudica significantly reduces the stall ratio by an order of magnitude while maintaining high bandwidth utilization. Additionally, the average frame delay is reduced by 3.1 times, further enhancing the overall gaming experience.

See more details in paper <https://www.usenix.org/conference/nsdi24/presentation/wang-shibo>.