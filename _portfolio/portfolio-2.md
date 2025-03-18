---
title: "2. AR application for Pick and Place operations"
excerpt: "Learning to control a semi-autonomus simulated robotic arm <img src='/images/pickandplace_main.png'>"
collection: portfolio
---

The aim of this work was to learn how to utilize a Virtual Reality (VR) Head Mounted Display (HMD) for robotic applications. As a starting point, I decided to utilize one of the <a href="https://github.com/Unity-Technologies/Unity-Robotics-Hub/blob/main/tutorials/pick_and_place/README.md">unity's robotic hub tutorials</a>. Specifically, the pick and place tutorial.

The <a href="https://github.com/Unity-Technologies/Unity-Robotics-Hub/blob/main/tutorials/pick_and_place/README.md">niryo one</a> robotic arm was simulated in Unity. The robot communicated with <a href="https://moveit.ai">moveit</a> running in an external PC using <a href="https://www.ros.org">ROS</a> to increase the level of autonomy. The communication was stablished by a <a href="https://github.com/Unity-Technologies/ROS-TCP-Connector">ROS-TCP-Connector</a>. Through the VR HMD the user could command the autonomous stack to initiate a pick and place operation. To ease the way the commands were transmitted to the autonomous stack a custom graphical interface was created using the <a href="https://learn.microsoft.com/en-us/windows/mixed-reality/mrtk-unity/mrtk3-overview/">Mixed Reality Toolkit</a>.

To increase and ease interaction, the following design conisderations were taken:
1. Spatial information was incorporated by providing a label describing each simulated object within the application.
![](/images/pickandplace_info.gif)
2. The user could position the object anywhere within the vicinity of the environment to do the pick and place operation. Additionally, the position of the object could be moved back into its original position by selecting a button within the custom graphical interface.
![](/images/pickandplace_object.gif)
3. Visual feedback was given to the user after communicating with the autonomous stack. For example, when the user commanded to start the pick and place operation through the custom graphical interface the phrase "Pick and place has started" appeared to let the user know that the command was sent.
![](/images/pickandplace_demo.gif)
