---
layout: page
title: Control-Barrier for Multi-robot systems
description:
img: assets/img/CBF.gif
importance: 2
category: work
giscus_comments:
---

Implemented Control Barrier Function (CBFs) layer for easy safe testing of different types of swarm/multi-agent algorithms using the motion capture.

<center>
<img src="/assets/img/projects/project_2/cbf_diagram.jpg" width="400"/>
</center>

We implement control barrier as a central controller which encodes local collision avoidance between each pair of robots deployed in the multi-robot system.

To guarantees collision avoidance between all the robots, we modify the control input using a Quadratic Program if and only if we sense the robots are closer than the distance we specify. 

Link Repo: https://github.com/FocasLab/Control_Barrier_MoCap.git

Demo Video : 
<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/g4LAO0o5jiE?si=oTtSRDE0aoffSPqd&amp;start=2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</center>

#### References
1) Sean Wilson, et al., "The Robotarium: Globally Impactful Opportunities, Challenges, and Lessons Learned in Remote-Access, Distributed Control of Multirobot Systems," in IEEE Control Systems Magazine, vol. 40, no. 1, pp. 26-44, Feb. 2020.<br>
2) Daniel Pickem, et al., "The Robotarium: A remotely accessible swarm robotics research testbed" 2017 IEEE International Conference on Robotics and Automation (ICRA). IEEE, 2017.<br>
3) Matthias Rungger and Majid Zamani. 2016. SCOTS: A Tool for the Synthesis of Symbolic Controllers. In Proceedings of the 19th International Conference on Hybrid Systems: Computation and Control (HSCC '16).