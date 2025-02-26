---
layout: post
title: My Late-Breaking Report was accepted at HRI 2025!
date: 2025-01-06
inline: false
related_posts: false
---

# CrowdHRI: Gamifying HRI Data Collection as a Multiplayer Mixed Reality Game

## Abstract

Crowdsourcing data for Human-Robot Interaction (HRI) research remains a challenge, requiring scalable, flexible, and immersive methods to collect meaningful interaction data. This paper introduces *CrowdHRI*, a novel approach to gamify HRI data collection through a multiplayer mixed reality (MR) game. The proposed system integrates a web server and Unity-based client architecture, enabling users to schedule or join sessions dynamically. Through immersive MR, *CrowdHRI* offers realistic environments and supports customizable experimental setups, gathering high-fidelity data on human-robot interactions. The system includes automated metrics to capture interaction quality, alongside a robust data science framework for analysis. By addressing the limitations of existing platforms—such as restricted scalability and interaction fidelity *CrowdHRI* enables a wide range of experimental conditions and advances the field of HRI research.

***Index Terms*—crowd sourcing, hri, vr user study, gamification**

## I. Introduction

The advancement of Human-Robot Interaction (HRI) research heavily relies on the availability of robust, high-quality interaction datasets. While traditional data collection methods, such as Wizard-of-Oz studies [23], crowdsourcing platforms [7], and competitions [11], have made significant contributions, they often suffer from scalability, logistical, and environmental constraints. They fail to scale effectively or simulate the nuanced interplay of human and robot roles. To address these limitations, we present CrowdHRI, a multiplayer Mixed Reality (MR) environments for immersive and dynamic experimental setups designed to gamify HRI data collection by allowing participants to take on various HRI roles while adhering to realistic constraints inspired by robotic systems.

### *A. Expanding the Scope of Crowdsourcing*

A robust HRI simulator must:

1) **Support Diverse Roles**: Enable users to act as observers, peers, supervisors, operators, collaborators, and even robots themselves (Oz).

2) **Simulate Robotic Constraints**: Implement realistic robotic limitations on human participants, such as restricted fields of view, reduced or enhanced degrees of freedom, and isolated movement capabilities.

3) **Provide Immersive and Configurable Environments**: Offer customizable scenarios to address varying research objectives while providing appropriate immersion, constraints, and control through MR interfaces.

### *B. Lessons from Existing Systems*

Platforms such as SIGVerse [11] and crowdsourcing-based games [7] have captured large-scale HRI data but often fall short in replicating real-world constraints. These systems primarily focus on task performance and communication but lack role-specific configurations or the ability to simulate robotic constraints for human participants. Moreover, most existing solutions emphasize either scalability or fidelity, rarely achieving both [2], [5].

### *C. Bridging the Gap: Role-Driven HRI in MR*

Our proposed CrowdHRI platform bridges this gap by:

1) **Integrating Role Diversity**: Subjects can alternate between human and robot roles, taking on tasks as peers, supervisors, collaborators, or operators.

2) **Gamifying the Oz Role**: Subjects taking on the role of robot Oz would experience different sets of controls, constraints, and rewards from subjects taking on the role of the humans. Eg. robot Oz experience mimicking robotic limitations such as constrained fields of view, limited simultaneous movement etc.

3) **Enabling Experimental Flexibility**: Researchers can configure diverse HRI scenarios, including multi-role interactions, task delegation, and collaborative problem-solving.

4) **Ensuring Scalability and Immersion**: The Unity-based client and web server architecture supports both real-time multiplayer interactions and automated data logging, facilitating scalable experiments.

5) **Mixed Reality Interfaces**: Having VR, computer based, smartphones, and tablet interfaces and controllers allows for greater diversity in input and researchers' ability to define role based constraints in possible devices for each role Eg. robot supervisor might not need a full VR experience and a laptop might be sufficient.

### *D. Contribution*

By incorporating diverse roles and role-specific limitations into a gamified MR platform, *CrowdHRI* not only enhances the realism and fidelity of HRI data collection but also enables the exploration of novel interaction paradigms. This platform empowers researchers to investigate how constraints and roles affect human-robot collaboration, paving the way for deeper insights into adaptive and scalable HRI systems.

## II. Related Works

### *A. HRI Communication*

Human communication is inherently complex, going beyond simple turn-taking where one party expresses intent and the other either accepts or rejects the message. Instead, communication involves a dynamic process of interpretation, negotiation, interruption, and clarification. Achieving common ground often requires iterative exchanges, as individuals employ strategies to address non-understanding and misunderstanding. These strategies, known as communication repair mechanisms, are critical for maintaining effective dialogue in situations where intent is not immediately clear [8], [22].

Communication repair remains an under-explored area in HRI. While the need for repair is well-documented in human-human interactions, the process by which humans and robots collaboratively resolve misunderstandings or non-understandings is less understood. This gap is partly due to methodological challenges. Existing studies often rely on small-scale, in-lab experiments that limit the scope of possible interaction conditions and repair strategies that can be investigated [22], [23].

To overcome these limitations, what is needed is a scalable platform that enables researchers to design and test hundreds of conditions and permutations required to study repair mechanisms in HRI. By leveraging mixed reality (MR) environments and crowdsourcing, the system can simulate diverse scenarios and collect large-scale data on how repair strategies are employed in real-time, dynamic human-robot interactions. This approach facilitates the systematic investigation of repair processes, offering new insights into designing robots capable of more natural and effective communication.

### *B. Wizard-of-Oz (WoZ)*

WoZ experiments allow HRI researchers to evaluate how humans behave when robots interact with them in a certain way and in specific environments. In this experimental design, the ``wizard" is the human operator who controls the robot from behind the scenes without the other participant(s) knowledge. With these evaluations, HRI researchers and developers can discover interaction paradigms before the underlying robotic systems are fully developed. This illusion provides valuable insights into user expectations, behaviors, and preferences in a controlled yet flexible environment. 

However, traditional WoZ experiments require significant manual effort for the human operator to learn the system and task requirements [3]. HRI WoZ user studies are often done in person in the lab, so they are not easily scalable. These experiments require a human user to be available at all times, which limits the possibility of large-scale studies. Variability or inconsistencies of responses to behaviors and actions across sessions can also affect the validity of the user study. Finally, these experiments are constrained by the fidelity of the simulation: simplistic robot responses or environmental setups may fail to capture real-world interactions.

New approaches aim to overcome the constraints of WoZ experiments, such as Oz-of-Wizard (OoW) [2], an inverse of the WoZ experimental setup where robot behavior is evaluated by simulating human behavior, instead. However, since OoW relies heavily on simplified human models, the experimental setups may not capture the complexity and variability of real human interactions with robots. Additionally, simplistic or poorly tuned human models may lead to overgeneralization or inaccuracies of people globally, limiting the diversity of backgrounds and human behaviors. Finally, OoW requires pre-specified interaction scenarios and does not adapt easily to unanticipated behaviors since the human models are simplified.

In both WoZ and OoW, the experimental setups face challenges in scaling their experiments and struggle to achieve complexity in modeling human-robot interactions. 

### *C. VR vs. Real Environments*

HRI researchers have often used VR, along with other mixed-reality setups, to simulate collaborative tasks between humans and robots through immersive and interactive experiences [10]. VR setups in HRI present both the potential for enhanced interactions between humans and robots and the the technical and usability challenges [10].

[6] compared human responses to drones in real and virtual environments. In this user study, [6] found that there was marginal difference between participants' stress levels, level of discomfort, and a sense of threat when interacting with the drones between real and virtual environments, supporting the VR as a tool for studying human-robot interactions. However, [6] cautions that VR may not be able to capture the complexity of real physical environments, which may impact humans' perceptions and behavior when interacting with he robot. [17] also validated the use of VR as a tool for studying human-robot interactions after comparing VR and WoZ systems for teleoperating a social robot in conversational tasks. Participants of the user study conducted by [17] found that the VR setup offered a more enjoyable and realistic interaction, whereas the traditional WoZ setup was less engaging and had issues with response timing.

### *D. HRI Simulators*

Gazebo [12] explored how simulators could bridge the gap between virtual testing and real-world deployment via their open-source multi-robot simulator Gazebo. Though it can produce a high-fidelity simulation of physics and interaction dynamics and increases accessibility through its open-source nature, Gazebo faces performance constraints since it is computationally intensive. Additionally, Gazebo is limited in diverse applications and complex environments, since it does not support complex dynamics.

AI2-THOR [13], CoppeliaSim, formerly called V-REP [20] introduced interactive simulation platforms that provide support for diverse robot applications and are scalable and customizable. However, [20] contains features and simulation capabilities that require a large learning curve for users to master. Additionally, CoppeliaSim, faces challenges in latency and synchronization. This presents challenges in accessibility and the ability to conduct HRI experiments on a larger scale. Online simulators like WeBots [9] are open-source platforms, that address issues in accessibility and involve the wider robotics community. NVDIA's Isaac Gym [16], [18] addressed challenges in scalability and fidelity of robotic simulations by enabling the training of thousands of environments in parallel on a single GPU. In addition to improving the scalability and fidelity of simulations, [16], [18] was able to support complex environments and tools for customizing the environment. However, simulating the environment is costly and time-consuming, requiring users to purchase expensive and limited GPUs from NVDIA for optimal performance and familiarize themselves with the GPU-based pipelines, which also presents issues in accessibility.

Habitat v1.0 [19], v2.0 [21], v3.0 [24] investigated how simulation platforms can effectively model human-robot collaboration while balancing efficiency, scalability, and fidelity. These works developed an infrastructure for studying behaviors that emerge from human-robot collaborations from scalability and open-source nature. However, the simulated environments fail to replicate real-world complexity due to their predefined nature and inability to adapt to dynamic environmental changes. Their datasets are also limited in their cultural representation, limiting their study of diverse behaviors that could emerge from human-robot collaborations conducted on a global scale.

iGibson 2.0 [14] investigated how to support a more diverse set of tasks that robots can learn in a simulated household environment by extending object states (e.g., temperature, wetness level, cleanliness level, and toggled and sliced states), expanding tasks beyond motion and physical contact and bridging the gap between physical simulations and logical representations. However, [14] assumes that the extended object states are uniform across all objects, which does not reflect real-world scenarios involving heterogeneous objects.

### *E. Crowdsourcing HRI Experiments*

There has been a growing need for outsourcing HRI experiments in recent years, particularly highlighted by the COVID-19 pandemic. Traditional methods present several limitations, such as the time-consuming process of manually generating behaviors [7], the lack of global diversity in datasets [15], and the restricted accessibility of experimental setups [11], [15]. Current crowdsourcing approaches, including via VR-based platforms and multiplayer games [11], fall short of creating realistic, complex environments that effectively simulate real-life human-robot interactions. These systems often restrict the embodiment of user avatars, limit task complexity, and require technical knowledge, reducing accessibility to these systems, thereby lowering the participant pool for HRI experiments [11], [15].

### *F. Bringing it all together*

Prior work has demonstrated the need for standardizing how data is collected from HRI experiments. To study diverse and realistic human-robot dynamics and behaviors, there needs to be a standardized method for creating flexible, scalable, and high-fidelity platforms. WoZ studies, crowdsourcing HRI experiments, and HRI simulators have contributed to these efforts over the years but often fall short of replicating the complexity of real-world interactions and environments. *CrowdHRI* seeks to bridge this gap by addressing the limitations of existing systems and establish a framework that is flexible, scalable, and diverse. 

## III. Implementation

As shown in Fig. 1, the CrowdHRI platform integrates advanced tools, including a Firebase database, ROS 2.0, and a Unity-based application, to create an immersive, scalable environment for HRI research. The platform supports a wide range of devices, including Windows, macOS, and Linux systems, alongside Meta Quest 2 VR controllers and Xbox controllers, ensuring accessibility and flexibility for diverse experimental setups. The server is encapsulated in a Docker container, allowing seamless deployment on local machines or cloud services such as Google Cloud Platform (GCP) or Amazon Web Services (AWS).

The current architecture comprises three role-based key components and abilities:

- **Human Roles (Unity App)**: Participants interact with the environment using VR or game controllers to complete predefined tasks. This setup ensures an immersive experience and realistic interaction modeling.
- **Robot Roles (Unity App with WoZ)**: Participants adopt a Wizard-of-Oz (WoZ) role to control robot actions remotely, facilitating the exploration of human-robot dynamics in constrained, role-specific scenarios.
- **Researcher Tools**: Researchers access a web-based interface equipped with tools for data preprocessing, annotation, visualization, and analysis. This interface streamlines the process of extracting meaningful insights from interaction data.

Real-time interaction is facilitated through WebSockets, ensuring synchronized communication between devices. ROS 2.0 further enhances the platform by enabling precise synchronization of robot actions with human inputs. Additionally, the web server provides a data API for advanced data processing, visualization, annotation, and analysis.

![Fig1](/assets/img/crowdhri/fig1.png)

### *A. Proof of Concept and Validation*

To validate the platform, a proof-of-concept experiment was conducted using a kitchen simulation (Fig. 2). In this scenario, a WoZ operator controlled a robot via a Meta Quest 2 VR controller, performing a task that involved removing a pot lid using the robot’s first-person view (FPV). The simulator supports multiple viewpoints, including egocentric and third-person perspectives, as well as static and dynamic camera feeds. The data collected includes RGB images, depth maps, object segmentation, and semantic categorization, all synchronized with the central data server. This multi-view, multi-modal capability enables diverse task interpretation and autonomous behavior modeling. The simulation environment also records dynamic object states and interactions, providing researchers with a rich dataset for analysis. Participants can interact using various modalities, including speech, gesture, and controllers, allowing for a comprehensive exploration of HRI scenarios.

For latency we adopted round-trip time (RTT), mean latency, percentile latency (P50, P90, P95, P99), and jitter (variance.) Depending on the experiments and the specific data, there might be different types of real-time requirements hard (RT-H), firm (RT-F), and soft (RT-S) \cite{brandt_dynamic_2003, noauthor_real-time_2024}. We defined RT-H mean latency as under 8ms (SD 2ms, max 10ms), RT-F under 20ms (SD 10ms, max 30ms), and RT-S under 70ms (SD 30ms, max 100ms.) For our pilot, we used RT-F for video and simulation, RT-H for controls, RT-S for instructions, and async best effort for recording data with timestamps. The setup is considered valid if they meet the RT requirements. To ensure data are synchronized, we use geo-location metadata and NTP-sync which helps synchronize audio, video, and other sensor data. Speech and gestures are extracted from the audio and video data.

![fig2](/assets/img/crowdhri/fig2.png)

### *B. Limitations and Future Plans*

Our early internal usability testing and pilot studies highlighted the need for an improved graphical user interface (GUI) to facilitate experiment design for HRI researchers. While the current CSV and JSON formats are functional, they lack the flexibility required for researchers to easily make modifications \snehesh{and carry heavy payload. User defined schema with user friendly UI and better remote procedure call (RPC) protocols with more compact data representations will be helpful. Additionally, we observed lag in video and state updates based on the RT requirements} within the simulator caused by internet connection speeds. This issue revealed the importance of implementing priority-based queuing and quality-of-service (QoS) mechanisms to reduce latency. It also highlighted the need to introduce lags to simulate the realities of remote telepresence and teleportation. The current implementation is limited to computers and does not support tablets or smartphones yet. Expanding to these devices would increase the participant pool but would also introduce challenges, such as designing touch interfaces and leveraging on-device sensors like GPS and IMUs for enhanced interactions. Furthermore, pilot walkthroughs of the researchers' workflow, from recruitment to study participation, revealed gaps in the pipeline that need to be addressed, as crowdsourcing workflows for recruitment differ significantly from in-person lab HRI studies. Finally, the integration of real robots and synchronizing their states is currently absent from the design. While this feature would provide significant value, it also introduces complexities, particularly around safety, making it a longer-term goal in our roadmap.

## IV. Conclusion

CrowdHRI has the potential to bridge significant gaps in existing HRI research platforms by offering a versatile, scalable, and immersive solution for study design and data collection. The architecture, designed to be both cost-effective and easily deployable, enables researchers to explore novel interaction paradigms across diverse scenarios. Early prototypes and pilot studies have identified opportunities for improvement in usability, latency management, and device compatibility, which will guide future development efforts. By open-sourcing the platform, we aim to foster collaboration within the HRI research community, encouraging iterative enhancements and broader adoption. This initiative will enable researchers worldwide to contribute to and benefit from a unified framework for high-fidelity, scalable HRI experimentation.

## References

1. ["Real-time computing," Dec. 2024, page Version ID: 1263720334](https://en.wikipedia.org/w/index.php?title=Real-time-computing).

2. T. Abbas, V.-J. Khan, U. Gadiraju, E. Barakova, and P. Markopoulos, "Crowd of Oz: A Crowd-Powered Social Robotics System for Stress Management," *Sensors*, vol. 20, no. 2, p. 569, Jan. 2020.

3. A. Bejarano, S. Elbeleidy, T. Mott, S. Negrete-Alamillo, L. A. Armenta, and T. Williams, "Hardships in the Land of Oz: Robot Control Challenges Faced by HRI Researchers and Real-World Teleoperators," *2024 33rd IEEE International Conference on Robot and Human Interactive Communication (ROMAN)*, Pasadena, CA, USA: IEEE, Aug. 2024, pp. 1914–1921.

4. S. A. Brandt, S. Banachowski, C. Lin, and T. Bisson, "Dynamic integrated scheduling of hard real-time, soft real-time, and non-real-time processes," *RTSS 2003. 24th IEEE Real-Time Systems Symposium*, IEEE, 2003, pp. 396–407.

5. C. Breazeal, N. DePalma, J. Orkin, S. Chernova, and M. Jung, "Crowdsourcing Human-Robot Interaction: New Methods and System Evaluation in a Public Environment," *Journal of Human-Robot Interaction*, vol. 2, no. 1, pp. 82–111, Mar. 2013.

6. R. Bretin, M. Khamis, and E. Cross, "Do I Run Away?: Proximity, Stress and Discomfort in Human-Drone Interaction in Real and Virtual Environments," *Human-Computer Interaction – INTERACT 2023*, Cham: Springer Nature Switzerland, 2023, pp. 525–551.

7. S. Chernova, J. Orkin, and C. Breazeal, "Crowdsourcing HRI through online multiplayer games," *2010 AAAI Fall Symposium Series*, 2010.

8. H. H. Clark, "Grounding in communication," *Perspectives on socially shared cognition/American Psychological Association*, 1991.

9. Cyberbotics Ltd., ["Cyberbotics: Robotics simulation with Webots"](https://cyberbotics.com/), 1998.

10. M. Dianatfar, J. Latokartano, and M. Lanz, "Review on existing VR/AR solutions in human–robot collaboration," *Procedia CIRP*, vol. 97, pp. 407–411, Jan. 2021.

11. T. Inamura, Y. Mizuchi, and H. Yamada, "VR platform enabling crowdsourcing of embodied HRI experiments – case study of online robot competition," *Advanced Robotics*, vol. 35, no. 11, pp. 697–703, Jun. 2021.

12. N. Koenig and A. Howard, "Design and use paradigms for Gazebo, an open-source multi-robot simulator," *2004 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)*, IEEE, vol. 3, Sep. 2004, pp. 2149–2154.

13. E. Kolve, R. Mottaghi, W. Han, et al., "AI2-THOR: An Interactive 3D Environment for Visual AI," Aug. 2022, *arXiv:1712.05474*.

14. C. Li, F. Xia, R. Martín-Martín, et al., "iGibson 2.0: Object-Centric Simulation for Robot Learning of Everyday Household Tasks," Nov. 2021, *arXiv:2108.03272*.

15. C. Li, R. Zhang, J. Wong, et al., "BEHAVIOR-1K: A Human-Centered, Embodied AI Benchmark with 1,000 Everyday Activities and Realistic Simulation," 2024.

16. V. Makoviychuk, L. Wawrzyniak, Y. Guo, et al., "Isaac Gym: High Performance GPU-Based Physics Simulation For Robot Learning," Aug. 2021, *arXiv:2108.10470*.

17. J. Miniotaite, E. Torubarova, and A. Pereira, "Comparing Dashboard and Virtual Reality Wizard-of-Oz Setups In a Human-Robot Conversational Task," Mar. 2023.

18. NVIDIA Corporation, ["Isaac Sim: Robotics Simulation and Synthetic Data Generation"](https://developer.nvidia.com/isaac/sim), May 2021.

19. X. Puig, E. Undersander, A. Szot, et al., "Habitat 3.0: A Co-Habitat for Humans, Avatars and Robots," Oct. 2023, *arXiv:2310.13724*.

20. E. Rohmer, S. P. N. Singh, and M. Freese, "V-REP: A versatile and scalable robot simulation framework," *2013 IEEE/RSJ International Conference on Intelligent Robots and Systems*, Nov. 2013, pp. 1321–1326.

21. M. Savva, A. Kadian, O. Maksymets, et al., "Habitat: A Platform for Embodied AI Research," *Advances in Neural Information Processing Systems*, 2019, pp. 9339–9347.

22. E. A. Schegloff, G. Jefferson, and H. Sacks, "The preference for self-correction in the organization of repair in conversation," *Language*, vol. 53, no. 2, pp. 361–382, 1977.

23. A. Steinfeld, O. C. Jenkins, and B. Scassellati, "The oz of wizard: simulating the human for interaction research," *Proceedings of the 4th ACM/IEEE International Conference on Human-Robot Interaction*, La Jolla, CA, USA: ACM, Mar. 2009, pp. 101–108.

24. A. Szot, A. Clegg, E. Undersander, et al., "Habitat 2.0: Training home assistants to rearrange their habitat," *Advances in Neural Information Processing Systems*, vol. 34, pp. 251–266, 2021.
