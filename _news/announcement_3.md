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
  max-width: 500px;
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

Crowdsourcing data for Human-Robot Interaction (HRI) research remains a challenge, requiring scalable, flexible, and immersive methods to collect meaningful interaction data. This paper introduces <em>CrowdHRI</em>, a novel approach to gamify HRI data collection through a multiplayer mixed reality (MR) game. The proposed system integrates a web server and Unity-based client architecture, enabling users to schedule or join sessions dynamically. Through immersive MR, <em>CrowdHRI</em> offers realistic environments and supports customizable experimental setups, gathering high-fidelity data on human-robot interactions. The system includes automated metrics to capture interaction quality, alongside a robust data science framework for analysis. By addressing the limitations of existing platforms—such as restricted scalability and interaction fidelity—<em>CrowdHRI</em> enables a wide range of experimental conditions and advances the field of HRI research.

<em><strong>Index Terms</strong></em>—crowd sourcing, hri, vr, user study, gamification

<div style="text-align: center;">
    <h2 id="introduction"><strong>I. Introduction</strong></h2>
</div>

The advancement of Human-Robot Interaction (HRI) research heavily relies on the availability of robust, high-quality interaction datasets. While traditional data collection methods, such as Wizard-of-Oz studies [<a href="#ref23">23</a>], crowdsourcing platforms [<a href="#ref7">7</a>], and competitions [<a href="#ref11">11</a>], have made significant contributions, they often suffer from scalability, logistical, and environmental constraints. They fail to scale effectively or simulate the nuanced interplay of human and robot roles. To address these limitations, we present CrowdHRI, a multiplayer Mixed Reality (MR) environment for immersive and dynamic experimental setups designed to gamify HRI data collection by allowing participants to take on various HRI roles while adhering to realistic constraints inspired by robotic systems.

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
5) <strong>Mixed Reality Interfaces</strong>: VR, computer-based, smartphones, and tablet interfaces allow for greater diversity in input and constraints (e.g., a robot supervisor may only need a laptop, not full VR).

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

Communication repair remains an under-explored area in HRI. While the need for repair is well-documented in human-human interactions, the process by which humans and robots collaboratively resolve misunderstandings or non-understandings is less understood. This gap is partly due to methodological challenges. Existing studies often rely on small-scale, in-lab experiments that limit the scope of possible interaction conditions and repair strategies [<a href="#ref22">22</a>], [<a href="#ref23">23</a>].

<div style="text-align: center;">
    <h3 id="b-woz"><em><strong>B. Wizard-of-Oz (WoZ)</strong></em></h3>
</div>

WoZ experiments allow HRI researchers to evaluate how humans behave when robots interact with them in a certain way and in specific environments. In this experimental design, the “wizard” is the human operator who controls the robot from behind the scenes without the other participant(s) knowledge. With these evaluations, HRI researchers and developers can discover interaction paradigms before the underlying robotic systems are fully developed. This illusion provides valuable insights into user expectations, behaviors, and preferences in a controlled yet flexible environment.

However, traditional WoZ experiments require significant manual effort for the human operator to learn the system and task requirements [<a href="#ref3">3</a>]. HRI WoZ user studies are often done in person in the lab, so they are not easily scalable. These experiments require a human user to be available at all times, which limits large-scale studies. Variability or inconsistencies of responses across sessions can also affect validity. Finally, these experiments are constrained by the simulation’s fidelity.

<div style="text-align: center;">
    <h3 id="c-vr"><em><strong>C. VR vs. Real Environments</strong></em></h3>
</div>

HRI researchers have often used VR, along with other mixed-reality setups, to simulate collaborative tasks between humans and robots through immersive and interactive experiences [<a href="#ref10">10</a>]. VR setups present both potential for enhanced interactions and technical/usability challenges [<a href="#ref10">10</a>].

[<a href="#ref6">6</a>] compared human responses to drones in real vs. virtual environments, noting marginal differences in stress, discomfort, and threat. However, [<a href="#ref6">6</a>] cautions that VR may not capture the full complexity of real environments. [<a href="#ref17">17</a>] validated VR for teleoperating a social robot in conversational tasks, finding it more enjoyable and realistic, whereas a traditional WoZ setup was less engaging with response timing issues.

<div style="text-align: center;">
    <h3 id="d-hri-sim"><em><strong>D. HRI Simulators</strong></em></h3>
</div>

Gazebo [<a href="#ref12">12</a>] explored bridging virtual testing and real-world deployment via an open-source multi-robot simulator but faced performance constraints. AI2-THOR [<a href="#ref13">13</a>], CoppeliaSim (V-REP) [<a href="#ref20">20</a>], WeBots [<a href="#ref9">9</a>], and Isaac Gym [<a href="#ref16">16</a>], [<a href="#ref18">18</a>] each handle different accessibility/fidelity challenges. Habitat [<a href="#ref19">19</a>], [<a href="#ref21">21</a>], [<a href="#ref24">24</a>] can’t fully replicate real-world complexities. iGibson 2.0 [<a href="#ref14">14</a>] extends object states but remains limited by uniform assumptions.

<div style="text-align: center;">
    <h3 id="e-crowdsourcing"><em><strong>E. Crowdsourcing HRI Experiments</strong></em></h3>
</div>

There has been a growing need for outsourcing HRI experiments. Traditional methods are time-consuming [<a href="#ref7">7</a>], lack global diversity [<a href="#ref15">15</a>], and restrict accessibility [<a href="#ref11">11</a>], [<a href="#ref15">15</a>]. VR/multiplayer games [<a href="#ref11">11</a>] don’t always achieve realistic complexity or broad accessibility, limiting participation.

<div style="text-align: center;">
    <h3 id="f-bringing"><em><strong>F. Bringing it all together</strong></em></h3>
</div>

Prior work shows the need to standardize HRI data collection. WoZ, crowdsourcing, and simulators each solve parts of the puzzle but can’t replicate full real-world interaction. <em>CrowdHRI</em> aims to be flexible, scalable, and high-fidelity.

<div style="text-align: center;">
    <h2 id="implementation"><strong>III. Implementation</strong></h2>
</div>

As shown in Fig. 1, CrowdHRI integrates a Firebase database, ROS 2.0, and a Unity-based application to create an immersive, scalable environment. It supports Windows, macOS, Linux, plus Meta Quest 2 VR/Xbox controllers. The server is Dockerized for easy deployment on GCP, AWS, or local machines.

The architecture comprises three role-based components:
- <strong>Human Roles (Unity App)</strong>: VR/game controllers for immersive tasks  
- <strong>Robot Roles (Unity App with WoZ)</strong>: Remote robot control in constrained, role-specific scenarios  
- <strong>Researcher Tools</strong>: Web-based data preprocessing, annotation, visualization, analysis

WebSockets ensure real-time interaction. ROS 2.0 synchronizes robot actions with human inputs. A data API supports advanced processing, visualization, and annotation.

<div style="text-align: center;">
    <img src="/assets/img/crowdhri/fig1.png" width="70%">
</div>

<p></p>

<div style="text-align: center;">
    <h3 id="proof-of-concept"><strong><em>A. Proof of Concept and Validation</em></strong></h3>
</div>

A proof-of-concept experiment used a kitchen simulation (Fig. 2). A WoZ operator controlled a robot with a Meta Quest 2 VR controller, removing a pot lid via the robot’s first-person view (FPV). Multiple viewpoints (egocentric, third-person, static/dynamic cameras) recorded RGB, depth, segmentation, and semantics, all synced to a central server. The simulator logs dynamic object states and interactions, supporting speech, gesture, and controllers for a robust HRI dataset.

We track RTT, mean latency, percentile latency (P50, P90, P95, P99), and jitter (variance). Real-time requirements (RT-H, RT-F, RT-S) follow [<a href="#ref4">4</a>], [<a href="#ref1">1</a>]. We used RT-F for video/simulation, RT-H for controls, RT-S for instructions, and async for data recording. Geo-location metadata and NTP-sync align audio, video, and sensor data.

<div style="text-align: center;">
    <img src="/assets/img/crowdhri/fig2.png" width="70%">
</div>

<p></p>

<div style="text-align: center;">
    <h3 id="limitations"><strong><em>B. Limitations and Future Plans</em></strong></h3>
</div>

Early usability tests highlight the need for an improved GUI for HRI experiment design. CSV/JSON formats lack flexibility, and user-defined schemas or more compact data representations could reduce latency. Artificial lags might simulate remote telepresence. Currently, it’s limited to computers (no tablets/phones), which broadens pools but adds challenges (touch interfaces, sensor usage). Pilot walkthroughs revealed recruitment workflow gaps. Integrating real robots is a future goal due to safety and synchronization complexity.

<div style="text-align: center;">
    <h2 id="conclusion"><strong>IV. Conclusion</strong></h2>
</div>

<em>CrowdHRI</em> can bridge significant gaps in HRI research, offering a versatile, scalable, immersive platform for study design and data collection. Its architecture is cost-effective, readily deployable, and supports novel interaction paradigms. Ongoing improvements include usability, latency, and device compatibility. By open-sourcing, we aim to foster collaboration, iterative enhancements, and broader adoption, benefitting researchers worldwide with a unified, high-fidelity, scalable framework.

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
