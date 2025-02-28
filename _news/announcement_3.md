---
layout: post
title: My Late-Breaking Report was accepted at HRI 2025!
date: 2025-01-06
inline: false
related_posts: false
---

<div style="text-align: center;">
    <h2><strong>CrowdHRI: Gamifying HRI Data Collection as a Multiplayer Mixed Reality Game</strong></h2>
</div>

<div style="display: flex; justify-content: center; text-align: center; gap: 40px;">

<div style="flex: 1;">
    <p style="margin: 3px 0;"><strong><sup>1</sup><a href="https://nhitran04.github.io" target="_blank" rel="noopener noreferrer">Nhi Tran</a></strong></p>
    <p style="margin: 3px 0;">Whiting School of Engineering</p>
    <p style="margin: 3px 0;">Johns Hopkins University</p>
    <p style="margin: 3px 0;">Baltimore, Maryland, USA</p>
    <p style="margin: 3px 0;">ntran29@jh.edu</p>
</div>

<div style="flex: 1;">
    <p style="margin: 3px 0;"><strong><sup>1</sup><a href="https://www.snehesh.com/" 
    target="_blank" rel="noopener noreferrer">Snehesh Shrestha</a></strong></p>
    <p style="margin: 3px 0;">University of Maryland</p>
    <p style="margin: 3px 0;">College Park, Maryland, USA</p>
    <p style="margin: 3px 0;">snehesh@umd.edu</p>
</div>

</div>

<!-- Table of Contents Box (centered, narrower) -->
<div style="
  border: 2px solid #ccc; 
  border-radius: 10px; 
  padding: 15px; 
  margin: 1em auto; 
  max-width: 400px;
  text-align: center;
">
  <h3 style="margin-top: 0;">Table of Contents</h3>
  <ul style="list-style-type: none; padding-left: 0; margin-bottom: 0; text-align: left; display: inline-block;">
    <li><a href="#abstract"><strong>Abstract</strong></a></li>
    <li>
      <a href="#introduction"><strong>I. Introduction</strong></a>
      <ul style="list-style-type: none; margin: 0; padding-left: 1em;">
        <li><a href="#a-expanding"><em>A. Expanding the Scope of Crowdsourcing</em></a></li>
        <li><a href="#b-lessons"><em>B. Lessons from Existing Systems</em></a></li>
        <li><a href="#c-bridging"><em>C. Bridging the Gap: Role-Driven HRI in MR</em></a></li>
        <li><a href="#d-contribution"><em>D. Contribution</em></a></li>
      </ul>
    </li>
    <li>
      <a href="#related-works"><strong>II. Related Works</strong></a>
      <ul style="list-style-type: none; margin: 0; padding-left: 1em;">
        <li><a href="#a-hri-comm"><em>A. HRI Communication</em></a></li>
        <li><a href="#b-woz"><em>B. Wizard-of-Oz (WoZ)</em></a></li>
        <li><a href="#c-vr"><em>C. VR vs. Real Environments</em></a></li>
        <li><a href="#d-hri-sim"><em>D. HRI Simulators</em></a></li>
        <li><a href="#e-crowdsourcing"><em>E. Crowdsourcing HRI Experiments</em></a></li>
        <li><a href="#f-bringing"><em>F. Bringing it all together</em></a></li>
      </ul>
    </li>
    <li>
      <a href="#implementation"><strong>III. Implementation</strong></a>
      <ul style="list-style-type: none; margin: 0; padding-left: 1em;">
        <li><a href="#proof-of-concept"><em>A. Proof of Concept and Validation</em></a></li>
        <li><a href="#limitations"><em>B. Limitations and Future Plans</em></a></li>
      </ul>
    </li>
    <li><a href="#conclusion"><strong>IV. Conclusion</strong></a></li>
    <li><a href="#references"><strong>References</strong></a></li>
  </ul>
</div>

<div style="text-align: center;">
    <h2 id="abstract"><strong>Abstract</strong></h2>
</div>

Crowdsourcing data for Human-Robot Interaction (HRI) research remains a challenge, requiring scalable, flexible, and immersive methods to collect meaningful interaction data. This paper introduces <em>CrowdHRI</em>, a novel approach to gamify HRI data collection through a multiplayer mixed reality (MR) game. The proposed system integrates a web server and Unity-based client architecture, enabling users to schedule or join sessions dynamically. Through immersive MR, <em>CrowdHRI</em> offers realistic environments and supports customizable experimental setups, gathering high-fidelity data on human-robot interactions. The system includes automated metrics to capture interaction quality, alongside a robust data science framework for analysis. By addressing the limitations of existing platforms—such as restricted scalability and interaction fidelity <em>CrowdHRI</em>enables a wide range of experimental conditions and advances the field of HRI research.

<em><strong>Index Terms</strong></em>—crowd sourcing, hri, vr, user study, gamification

<div style="text-align: center;">
    <h2 id="introduction"><strong>I. Introduction</strong></h2>
</div>

The advancement of Human-Robot Interaction (HRI) research heavily relies on the availability of robust, high-quality interaction datasets. While traditional data collection methods, such as Wizard-of-Oz studies [<a href="#ref23">23</a>], crowdsourcing platforms [<a href="#ref7">7</a>], and competitions [<a href="#ref11">11</a>], have made significant contributions, they often suffer from scalability, logistical, and environmental constraints. They fail to scale effectively or simulate the nuanced interplay of human and robot roles. To address these limitations, we present CrowdHRI, a multiplayer Mixed Reality (MR) environments for immersive and dynamic experimental setups designed to gamify HRI data collection by allowing participants to take on various HRI roles while adhering to realistic constraints inspired by robotic systems.

<div style="text-align: center;">
    <h3 id="a-expanding"><em><strong>A. Expanding the Scope of Crowdsourcing</strong></em></h3>
</div>

A robust HRI simulator must:

1) <strong>Support Diverse Roles</strong>: Enable users to act as observers, peers, supervisors, operators, collaborators, and even robots themselves (Oz).  
2) <strong>Simulate Robotic Constraints</strong>: Implement realistic robotic limitations on human participants, such as restricted fields of view, reduced or enhanced degrees of freedom, and isolated movement capabilities.  
3) <strong>Provide Immersive and Configurable Environments</strong>: Offer customizable scenarios to address varying research objectives while providing appropriate immersion, constraints, and control through MR interfaces.

<div style="text-align: center;">
    <h3 id="b-lessons"><em><strong>B. Lessons from Existing Systems</strong></em></h3>
</div>

Platforms such as SIGVerse [<a href="#ref11">11</a>] and crowdsourcing-based games [<a href="#ref7">7</a>] have captured large-scale HRI data but often fall short in replicating real-world constraints. These systems primarily focus on task performance and communication but lack role-specific configurations or the ability to simulate robotic constraints for human participants. Moreover, most existing solutions emphasize either scalability or fidelity, rarely achieving both [<a href="#ref2">2</a>], [<a href="#ref5">5</a>].

<div style="text-align: center;">
    <h3 id="c-bridging"><em><strong>C. Bridging the Gap: Role-Driven HRI in MR</strong></em></h3>
</div>

Our proposed CrowdHRI platform bridges this gap by:

1) <strong>Integrating Role Diversity</strong>: Subjects can alternate between human and robot roles, taking on tasks as peers, supervisors, collaborators, or operators.  
2) <strong>Gamifying the Oz Role</strong>: Subjects taking on the role of robot Oz would experience different sets of controls, constraints, and rewards from subjects taking on the role of the humans (e.g., constrained fields of view, limited simultaneous movement, etc.).  
3) <strong>Enabling Experimental Flexibility</strong>: Researchers can configure diverse HRI scenarios, including multi-role interactions, task delegation, and collaborative problem-solving.  
4) <strong>Ensuring Scalability and Immersion</strong>: The Unity-based client and web server architecture supports both real-time multiplayer interactions and automated data logging, facilitating scalable experiments.  
5) <strong>Mixed Reality Interfaces</strong>: Having VR, computer based, smartphones, and tablet interfaces and controllers allows for greater diversity in input and researchers' ability to define role based constraints in possible devices for each role (e.g., a robot supervisor may only need a laptop, not full VR).

<div style="text-align: center;">
    <h3 id="d-contribution"><em><strong>D. Contribution</strong></em></h3>
</div>

By incorporating diverse roles and role-specific limitations into a gamified MR platform, <em>CrowdHRI</em> not only enhances the realism and fidelity of HRI data collection but also enables the exploration of novel interaction paradigms. This platform empowers researchers to investigate how constraints and roles affect human-robot collaboration, paving the way for deeper insights into adaptive and scalable HRI systems.

<div style="text-align: center;">
    <h2 id="related-works"><strong>II. Related Works</strong></h2>
</div>

<div style="text-align: center;">
    <h3 id="a-hri-comm"><em><strong>A. HRI Communication</strong></em></h3>
</div>

Human communication is inherently complex, going beyond simple turn-taking where one party expresses intent and the other either accepts or rejects the message. Instead, communication involves a dynamic process of interpretation, negotiation, interruption, and clarification. Achieving common ground often requires iterative exchanges, as individuals employ strategies to address non-understanding and misunderstanding. These strategies, known as communication repair mechanisms, are critical for maintaining effective dialogue in situations where intent is not immediately clear [<a href="#ref8">8</a>], [<a href="#ref22">22</a>].

Communication repair remains an under-explored area in HRI. While the need for repair is well-documented in human-human interactions, the process by which humans and robots collaboratively resolve misunderstandings or non-understandings is less understood. This gap is partly due to methodological challenges. Existing studies often rely on small-scale, in-lab experiments that limit the scope of possible interaction conditions and repair strategies that can be investigated [<a href="#ref22">22</a>], [<a href="#ref23">23</a>].

To overcome these limitations, what is needed is a scalable platform that enables researchers to design and test hundreds of conditions and permutations required to study repair mechanisms in HRI. By leveraging mixed reality (MR) environments and crowdsourcing, the system can simulate diverse scenarios and collect large-scale data on how repair strategies are employed in real-time, dynamic human-robot interactions. This approach facilitates the systematic investigation of repair processes, offering new insights into designing robots capable of more natural and effective communication.

<div style="text-align: center;">
    <h3 id="b-woz"><em><strong>B. Wizard-of-Oz (WoZ)</strong></em></h3>
</div>

WoZ experiments allow HRI researchers to evaluate how humans behave when robots interact with them in a certain way and in specific environments. In this experimental design, the "wizard" is the human operator who controls the robot from behind the scenes without the other participant(s) knowledge. With these evaluations, HRI researchers and developers can discover interaction paradigms before the underlying robotic systems are fully developed. This illusion provides valuable insights into user expectations, behaviors, and preferences in a controlled yet flexible environment. 

However, traditional WoZ experiments require significant manual effort for the human operator to learn the system and task requirements [<a href="#ref3">3</a>]. HRI WoZ user studies are often done in person in the lab, so they are not easily scalable. These experiments require a human user to be available at all times, which limits the possibility of large-scale studies. Variability or inconsistencies of responses to behaviors and actions across sessions can also affect the validity of the user study. Finally, these experiments are constrained by the fidelity of the simulation: simplistic robot responses or environmental setups may fail to capture real-world interactions.

New approaches aim to overcome the constraints of WoZ experiments, such as Oz-of-Wizard (OoW) [<a href="#ref2">2</a>], an inverse of the WoZ experimental setup where robot behavior is evaluated by simulating human behavior, instead. However, since OoW relies heavily on simplified human models, the experimental setups may not capture the complexity and variability of real human interactions with robots. Additionally, simplistic or poorly tuned human models may lead to overgeneralization or inaccuracies of people globally, limiting the diversity of backgrounds and human behaviors. Finally, OoW requires pre-specified interaction scenarios and does not adapt easily to unanticipated behaviors since the human models are simplified.

In both WoZ and OoW, the experimental setups face challenges in scaling their experiments and struggle to achieve complexity in modeling human-robot interactions. 

<div style="text-align: center;">
    <h3 id="c-vr"><em><strong>C. VR vs. Real Environments</strong></em></h3>
</div>

HRI researchers have often used VR, along with other mixed-reality setups, to simulate collaborative tasks between humans and robots through immersive and interactive experiences [<a href="#ref10">10</a>]. VR setups in HRI present both the potential for enhanced interactions between humans and robots and the technical and usability challenges  [<a href="#ref10">10</a>].

[<a href="#ref6">6</a>] compared human responses to drones in real and virtual environments. In this user study, [<a href="#ref6">6</a>] found that there was marginal difference between participants' stress levels, level of discomfort, and a sense of threat when interacting with the drones between real and virtual environments, supporting the VR as a tool for studying human-robot interactions. However, [<a href="#ref6">6</a>] cautions that VR may not be able to capture the complexity of real physical environments, which may impact humans' perceptions and behavior when interacting with he robot. [<a href="#ref17">17</a>] also validated the use of VR as a tool for studying human-robot interactions after comparing VR and WoZ systems for teleoperating a social robot in conversational tasks. Participants of the user study conducted by [<a href="#ref17">17</a>] found that the VR setup offered a more enjoyable and realistic interaction, whereas the traditional WoZ setup was less engaging and had issues with response timing.

<div style="text-align: center;">
    <h3 id="d-hri-sim"><em><strong>D. HRI Simulators</strong></em></h3>
</div>

Gazebo [<a href="#ref12">12</a>] explored how simulators could bridge the gap between virtual testing and real-world deployment via their open-source multi-robot simulator Gazebo. Though it can produce a high-fidelity simulation of physics and interaction dynamics and increases accessibility through its open-source nature, Gazebo faces performance constraints since it is computationally intensive. Additionally, Gazebo is limited in diverse applications and complex environments, since it does not support complex dynamics.

AI2-THOR [<a href="#ref13">13</a>], CoppeliaSim, formerly called V-REP [<a href="#ref20">20</a>] introduced interactive simulation platforms that provide support for diverse robot applications and are scalable and customizable. However, [<a href="#ref20">20</a>] contains features and simulation capabilities that require a large learning curve for users to master. Additionally, CoppeliaSim, faces challenges in latency and synchronization. This presents challenges in accessibility and the ability to conduct HRI experiments on a larger scale. Online simulators like WeBots [<a href="#ref9">9</a>] are open-source platforms, that address issues in accessibility and involve the wider robotics community. NVDIA's Isaac Gym [<a href="#ref16">16</a>], [<a href="#ref18">18</a>] addressed challenges in scalability and fidelity of robotic simulations by enabling the training of thousands of environments in parallel on a single GPU. In addition to improving the scalability and fidelity of simulations, [<a href="#ref16">16</a>], [<a href="#ref18">18</a>]  was able to support complex environments and tools for customizing the environment. However, simulating the environment is costly and time-consuming, requiring users to purchase expensive and limited GPUs from NVDIA for optimal performance and familiarize themselves with the GPU-based pipelines, which also presents issues in accessibility.

Habitat v1.0 [<a href="#ref19">19</a>], v2.0 [<a href="#ref20">20</a>], v3.0 [<a href="#ref24">24</a>] investigated how simulation platforms can effectively model human-robot collaboration while balancing efficiency, scalability, and fidelity. These works developed an infrastructure for studying behaviors that emerge from human-robot collaborations from scalability and open-source nature. However, the simulated environments fail to replicate real-world complexity due to their predefined nature and inability to adapt to dynamic environmental changes. Their datasets are also limited in their cultural representation, limiting their study of diverse behaviors that could emerge from human-robot collaborations conducted on a global scale.

iGibson 2.0 [<a href="#ref14">14</a>] investigated how to support a more diverse set of tasks that robots can learn in a simulated household environment by extending object states (e.g., temperature, wetness level, cleanliness level, and toggled and sliced states), expanding tasks beyond motion and physical contact and bridging the gap between physical simulations and logical representations. However, [<a href="#ref14">14</a>] assumes that the extended object states are uniform across all objects, which does not reflect real-world scenarios involving heterogeneous objects.

<div style="text-align: center;">
    <h3 id="e-crowdsourcing"><em><strong>E. Crowdsourcing HRI Experiments</strong></em></h3>
</div>

There has been a growing need for outsourcing HRI experiments in recent years, particularly highlighted by the COVID-19 pandemic. Traditional methods present several limitations, such as the time-consuming process of manually generating behaviors [<a href="#ref7">7</a>], the lack of global diversity in datasets [<a href="#ref15">15</a>], and the restricted accessibility of experimental setups [<a href="#ref11">11</a>], [<a href="#ref15">15</a>]. Current crowdsourcing approaches, including via VR-based platforms and multiplayer games [<a href="#ref11">11</a>], fall short of creating realistic, complex environments that effectively simulate real-life human-robot interactions. These systems often restrict the embodiment of user avatars, limit task complexity, and require technical knowledge, reducing accessibility to these systems, thereby lowering the participant pool for HRI experiments [<a href="#ref11">11</a>], [<a href="#ref15">15</a>]

<div style="text-align: center;">
    <h3 id="f-bringing"><em><strong>F. Bringing it all together</strong></em></h3>
</div>

Prior work has demonstrated the need for standardizing how data is collected from HRI experiments. To study diverse and realistic human-robot dynamics and behaviors, there needs to be a standardized method for creating flexible, scalable, and high-fidelity platforms. WoZ studies, crowdsourcing HRI experiments, and HRI simulators have contributed to these efforts over the years but often fall short of replicating the complexity of real-world interactions and environments. <em>CrowdHRI</em> seeks to bridge this gap by addressing the limitations of existing systems and establish a framework that is flexible, scalable, and diverse. 

<div style="text-align: center;">
    <h2 id="implementation"><strong>III. Implementation</strong></h2>
</div>

As shown in <a href="#fig1">Fig. 1</a>, the CrowdHRI platform integrates advanced tools, including a Firebase database, ROS 2.0, and a Unity-based application, to create an immersive, scalable environment for HRI research. The platform supports a wide range of devices, including Windows, macOS, and Linux systems, alongside Meta Quest 2 VR controllers and Xbox controllers, ensuring accessibility and flexibility for diverse experimental setups. The server is encapsulated in a Docker container, allowing seamless deployment on local machines or cloud services such as Google Cloud Platform (GCP) or Amazon Web Services (AWS).

The architecture comprises three role-based components:
- <strong>Human Roles (Unity App)</strong>: Participants interact with the environment using VR or game controllers to complete predefined tasks. This setup ensures an immersive experience and realistic interaction modeling.
- <strong>Robot Roles (Unity App with WoZ)</strong>: Participants adopt a Wizard-of-Oz (WoZ) role to control robot actions remotely, facilitating the exploration of human-robot dynamics in constrained, role-specific scenarios.
- <strong>Researcher Tools</strong>: esearchers access a web-based interface equipped with tools for data preprocessing, annotation, visualization, and analysis. This interface streamlines the process of extracting meaningful insights from interaction data.

Real-time interaction is facilitated through WebSockets, ensuring synchronized communication between devices. ROS 2.0 further enhances the platform by enabling precise synchronization of robot actions with human inputs. Additionally, the web server provides a data API for advanced data processing, visualization, annotation, and analysis.

<div id="fig1" style="text-align: center;">
    <img src="/assets/img/crowdhri/fig1.png" width="70%">
</div>

<p></p>

<div style="text-align: center;">
    <h3 id="proof-of-concept"><strong><em>A. Proof of Concept and Validation</em></strong></h3>
</div>

To validate the platform, a proof-of-concept experiment was conducted using a kitchen simulation (<a href="#fig2">Fig. 2</a>). In this scenario, a WoZ operator controlled a robot via a Meta Quest 2 VR controller, performing a task that involved removing a pot lid using the robot’s first-person view (FPV). The simulator supports multiple viewpoints, including egocentric and third-person perspectives, as well as static and dynamic camera feeds. The data collected includes RGB images, depth maps, object segmentation, and semantic categorization, all synchronized with the central data server. This multi-view, multi-modal capability enables diverse task interpretation and autonomous behavior modeling. The simulation environment also records dynamic object states and interactions, providing researchers with a rich dataset for analysis. Participants can interact using various modalities, including speech, gesture, and controllers, allowing for a comprehensive exploration of HRI scenarios.

For latency we adopted round-trip time (RTT), mean latency, percentile latency (P50, P90, P95, P99), and jitter (variance.) Depending on the experiments and the specific data, there might be different types of real-time requirements hard (RT-H), firm (RT-F), and soft (RT-S) [<a href="#ref1">1</a>], [<a href="#ref4">4</a>]. We defined RT-H mean latency as under 8ms (SD 2ms, max 10ms), RT-F under 20ms (SD 10ms, max 30ms), and RT-S under 70ms (SD 30ms, max 100ms.) For our pilot, we used RT-F for video and simulation, RT-H for controls, RT-S for instructions, and async best effort for recording data with timestamps. The setup is considered valid if they meet the RT requirements. To ensure data are synchronized, we use geo-location metadata and NTP-sync which helps synchronize audio, video, and other sensor data. Speech and gestures are extracted from the audio and video data.

<div id="fig2" style="text-align: center;">
    <img src="/assets/img/crowdhri/fig2.png" width="70%">
</div>

<p></p>

<div style="text-align: center;">
    <h3 id="limitations"><strong><em>B. Limitations and Future Plans</em></strong></h3>
</div>

Our early internal usability testing and pilot studies highlighted the need for an improved graphical user interface (GUI) to facilitate experiment design for HRI researchers. While the current CSV and JSON formats are functional, they lack the flexibility required for researchers to easily make modifications and carry heavy payload. User defined schema with user friendly UI and better remote procedure call (RPC) protocols with more compact data representations will be helpful. Additionally, we observed lag in video and state updates based on the RT requirements within the simulator caused by internet connection speeds. This issue revealed the importance of implementing priority-based queuing and quality-of-service (QoS) mechanisms to reduce latency. It also highlighted the need to introduce lags to simulate the realities of remote telepresence and teleportation. The current implementation is limited to computers and does not support tablets or smartphones yet. Expanding to these devices would increase the participant pool but would also introduce challenges, such as designing touch interfaces and leveraging on-device sensors like GPS and IMUs for enhanced interactions. Furthermore, pilot walkthroughs of the researchers' workflow, from recruitment to study participation, revealed gaps in the pipeline that need to be addressed, as crowdsourcing workflows for recruitment differ significantly from in-person lab HRI studies. Finally, the integration of real robots and synchronizing their states is currently absent from the design. While this feature would provide significant value, it also introduces complexities, particularly around safety, making it a longer-term goal in our roadmap.

<div style="text-align: center;">
    <h2 id="conclusion"><strong>IV. Conclusion</strong></h2>
</div>

CrowdHRI has the potential to bridge significant gaps in existing HRI research platforms by offering a versatile, scalable, and immersive solution for study design and data collection. The architecture, designed to be both cost-effective and easily deployable, enables researchers to explore novel interaction paradigms across diverse scenarios. Early prototypes and pilot studies have identified opportunities for improvement in usability, latency management, and device compatibility, which will guide future development efforts. By open-sourcing the platform, we aim to foster collaboration within the HRI research community, encouraging iterative enhancements and broader adoption. This initiative will enable researchers worldwide to contribute to and benefit from a unified framework for high-fidelity, scalable HRI experimentation.

<div style="text-align: center;">
    <h2 id="references"><strong>References</strong></h2>
</div>

<!-- Wrap each reference in a div with an ID corresponding to its citation number -->

<div id="ref1">
1. "Real-time computing," Dec. 2024, page Version ID: 1263720334.
</div>

<div id="ref2">
2. T. Abbas, V.-J. Khan, U. Gadiraju, E. Barakova, and P. Markopoulos, 
   "Crowd of Oz: A Crowd-Powered Social Robotics System for Stress Management," 
   <em>Sensors</em>, vol. 20, no. 2, p. 569, Jan. 2020.
</div>

<div id="ref3">
3. A. Bejarano, S. Elbeleidy, T. Mott, S. Negrete-Alamillo, 
   L. A. Armenta, and T. Williams, 
   "Hardships in the Land of Oz: Robot Control Challenges Faced by HRI Researchers and Real-World Teleoperators," 
   <em>2024 33rd IEEE International Conference on Robot and Human Interactive Communication (ROMAN)</em>, 
   Pasadena, CA, USA: IEEE, Aug. 2024, pp. 1914–1921.
</div>

<div id="ref4">
4. S. A. Brandt, S. Banachowski, C. Lin, and T. Bisson, 
   "Dynamic integrated scheduling of hard real-time, soft real-time, and non-real-time processes," 
   <em>RTSS 2003. 24th IEEE Real-Time Systems Symposium</em>, IEEE, 2003, pp. 396–407.
</div>

<div id="ref5">
5. C. Breazeal, N. DePalma, J. Orkin, S. Chernova, and M. Jung, 
   "Crowdsourcing Human-Robot Interaction: New Methods and System Evaluation in a Public Environment," 
   <em>Journal of Human-Robot Interaction</em>, vol. 2, no. 1, pp. 82–111, Mar. 2013.
</div>

<div id="ref6">
6. R. Bretin, M. Khamis, and E. Cross, 
   "Do I Run Away?: Proximity, Stress and Discomfort in Human-Drone Interaction in Real and Virtual Environments," 
   <em>Human-Computer Interaction – INTERACT 2023</em>, Cham: Springer Nature Switzerland, 2023, pp. 525–551.
</div>

<div id="ref7">
7. S. Chernova, J. Orkin, and C. Breazeal, 
   "Crowdsourcing HRI through online multiplayer games," 
   <em>2010 AAAI Fall Symposium Series</em>, 2010.
</div>

<div id="ref8">
8. H. H. Clark, 
   "Grounding in communication," 
   <em>Perspectives on socially shared cognition/American Psychological Association</em>, 1991.
</div>

<div id="ref9">
9. Cyberbotics Ltd., "Cyberbotics: Robotics simulation with Webots", 1998.
</div>

<div id="ref10">
10. M. Dianatfar, J. Latokartano, and M. Lanz, 
    "Review on existing VR/AR solutions in human–robot collaboration," 
    <em>Procedia CIRP</em>, vol. 97, pp. 407–411, Jan. 2021.
</div>

<div id="ref11">
11. T. Inamura, Y. Mizuchi, and H. Yamada, 
    "VR platform enabling crowdsourcing of embodied HRI experiments – case study of online robot competition," 
    <em>Advanced Robotics</em>, vol. 35, no. 11, pp. 697–703, Jun. 2021.
</div>

<div id="ref12">
12. N. Koenig and A. Howard, 
    "Design and use paradigms for Gazebo, an open-source multi-robot simulator," 
    <em>2004 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)</em>, 
    IEEE, vol. 3, Sep. 2004, pp. 2149–2154.
</div>

<div id="ref13">
13. E. Kolve, R. Mottaghi, W. Han, et al., 
    "AI2-THOR: An Interactive 3D Environment for Visual AI," 
    Aug. 2022, <em>arXiv:1712.05474</em>.
</div>

<div id="ref14">
14. C. Li, F. Xia, R. Martín-Martín, et al., 
    "iGibson 2.0: Object-Centric Simulation for Robot Learning of Everyday Household Tasks," 
    Nov. 2021, <em>arXiv:2108.03272</em>.
</div>

<div id="ref15">
15. C. Li, R. Zhang, J. Wong, et al., 
    "BEHAVIOR-1K: A Human-Centered, Embodied AI Benchmark with 1,000 Everyday Activities and Realistic Simulation," 
    2024.
</div>

<div id="ref16">
16. V. Makoviychuk, L. Wawrzyniak, Y. Guo, et al., 
    "Isaac Gym: High Performance GPU-Based Physics Simulation For Robot Learning," 
    Aug. 2021, <em>arXiv:2108.10470</em>.
</div>

<div id="ref17">
17. J. Miniotaite, E. Torubarova, and A. Pereira, 
    "Comparing Dashboard and Virtual Reality Wizard-of-Oz Setups In a Human-Robot Conversational Task," 
    Mar. 2023.
</div>

<div id="ref18">
18. NVIDIA Corporation, 
    "Isaac Sim: Robotics Simulation and Synthetic Data Generation", 
    May 2021.
</div>

<div id="ref19">
19. X. Puig, E. Undersander, A. Szot, et al., 
    "Habitat 3.0: A Co-Habitat for Humans, Avatars and Robots," 
    Oct. 2023, <em>arXiv:2310.13724</em>.
</div>

<div id="ref20">
20. E. Rohmer, S. P. N. Singh, and M. Freese, 
    "V-REP: A versatile and scalable robot simulation framework," 
    <em>2013 IEEE/RSJ International Conference on Intelligent Robots and Systems</em>, 
    Nov. 2013, pp. 1321–1326.
</div>

<div id="ref21">
21. M. Savva, A. Kadian, O. Maksymets, et al., 
    "Habitat: A Platform for Embodied AI Research," 
    <em>Advances in Neural Information Processing Systems</em>, 2019, pp. 9339–9347.
</div>

<div id="ref22">
22. E. A. Schegloff, G. Jefferson, and H. Sacks, 
    "The preference for self-correction in the organization of repair in conversation," 
    <em>Language</em>, vol. 53, no. 2, pp. 361–382, 1977.
</div>

<div id="ref23">
23. A. Steinfeld, O. C. Jenkins, and B. Scassellati, 
    "The oz of wizard: simulating the human for interaction research," 
    <em>Proceedings of the 4th ACM/IEEE International Conference on Human-Robot Interaction</em>, 
    La Jolla, CA, USA: ACM, Mar. 2009, pp. 101–108.
</div>

<div id="ref24">
24. A. Szot, A. Clegg, E. Undersander, et al., 
    "Habitat 2.0: Training home assistants to rearrange their habitat," 
    <em>Advances in Neural Information Processing Systems</em>, vol. 34, pp. 251–266, 2021.
</div>
