---
layout: post
title: I presented at the 2024 AAAI Fall Symposium!
date: 2024-11-08
inline: false
related_posts: false
---

I presented my work on [Goals vs. Actions as User-Facing Representations for Robot Programming](https://drive.google.com/file/d/1E1xZMXu1w4NgvCXlS96RJAJaCFl7SP35/view?usp=drive_link) at the [2024 AAAI Fall Symposium on Unifying Representations for Robot Application Development](https://sites.google.com/view/aaai-ur-rad-symposium/home?authuser=0) (UR-RAD)!

<div style="text-align: center;">
    <img src="/assets/img/ur_rad/ur-rad-presentation.png" width="60%">
</div>

<p></p>

In my talk, I presented my research plan for investigating different representations for capturing human intent when specifying tasks for a robot by comparing goals (*i.e.,* the partial state of the world that the robot strives to achieve) versus actions (*i.e.,* what the robot does to change the state of the world). I emphasized the need for future robot application development research to investigate different representations for expressing tasks for a robot.

You can read more about this work below!

<div style="text-align: center;">
    <h2><strong>Goals vs. Actions as User-Facing Representations for Robot Programming</strong></h2>
</div>

<div style="flex: 1; text-align: center;">
    <p style="margin: 3px 0;"><strong><a href="https://nhitran04.github.io" target="_blank" rel="noopener noreferrer">Nhi Tran</a></strong></p>
    <p style="margin: 3px 0;">nhi.y.tran5.civ@us.navy.mil</p>
    <p style="margin: 3px 0;">Navy Center for Applied Research in Artificial Intelligence</p>
    <p style="margin: 3px 0;">U.S. Naval Research Laboratory, Washington, D.C. 20375</p>
</div>

<!-- Table of Contents Box (centered, narrower) -->
<div style="
  border: 2px solid #ccc; 
  border-radius: 10px; 
  padding: 15px; 
  margin: 1em auto; 
  max-width: 200px;
  text-align: center;
">
  <h3 style="margin-top: 0;">Table of Contents</h3>
  <ul style="list-style-type: none; padding-left: 0; margin-bottom: 0; text-align: left; display: inline-block;">
    <li><a href="#abstract"><strong>Abstract</strong></a></li>
    <li>
      <a href="#introduction"><strong>Introduction</strong></a>
    </li>
    <li>
      <a href="#related work"><strong>Related Work</strong></a>
    </li>
    <li>
      <a href="#research plan"><strong>Research Plan</strong></a>
      <ul style="list-style-type: none; margin: 0; padding-left: 1em;">
        <li><a href="#user interface"><em>User Interface</em></a></li>
        <li><a href="#planned evaluation"><em>Planned Evaluation</em></a></li>
        <ul style="list-style-type: none; margin: 0; padding-left: 1em;">
            <li><a href="#study design"><em>Study Design</em></a></li>
            <li><a href="#measures"><em>Measures</em></a></li>
        </ul>
      </ul>
    </li>
    <li><a href="#conclusion"><strong>Conclusion</strong></a></li>
    <li><a href="#acknowledgements"><strong>Acknowledgements</strong></a></li>
    <li><a href="#references"><strong>References</strong></a></li>
  </ul>
</div>

<div style="text-align: center;">
    <h2 id="abstract"><strong>Abstract</strong></h2>
</div>

<em>Robot application development (RAD)</em> tools provide novice developers with the ability to specify what tasks a robot needs to perform and how it should perform these tasks. Existing RAD tools often focus on how end-user developer intent should be captured and stored as a computational artifact, including but not limited to mixed-reality interfaces, natural language programming, and visual programming environments. However, these tools fail to incorporate robot intelligence in the development pipeline, making it cumbersome for end-user developers to specify a detailed sequence of steps for the robot to complete a task, as well as overconstraining the robot. We thereby suggest that <em>robot intelligence</em> needs to be incorporated into RAD tools. Our proposed work will focus on balancing the amount and nature of domain knowledge that the end-user developer must provide to the robot with the robot’s ability to plan and act autonomously, as well as how the end-user’s domain knowledge should be represented as a computational artifact. In particular, we will be comparing two different approaches – <em>goals</em> versus <em>actions</em> – as a user-facing representation for collecting developer task specifications and intent while leveraging the robot’s ability to plan and act autonomously through robot intelligence by extending the *Polaris* interface, developed by Porfirio, Roberts, and Hiatt (2024), through a user study.

<div style="text-align: center;">
    <h2 id="introduction"><strong>Introduction</strong></h2>
</div>

<em>Robot application development</em> (RAD) environments enable novice robot programmers and designers (<em>end-user developers</em>) to specify what tasks a robot needs to perform, and podsibly how it should perform these tasks. As the landscape of artificial intelligence (AI) changes, RAD environments must adapt to these changes. While current RAD tools focus primarily on novel ways to capture developer intent, these tools often require developers to overconstrain the robot, i.e., specify the exact steps for a robot to perform, similar to traditional computer programming, while neglecting to leverage robot autonomy. In short, future RAD environments must incorporate <em>robot intelligence</em> in the development pipeline, <em>i.e.,</em> the robot’s knowledge and ability to make decisions autonomously.

It is thereby critical that future RAD research investigates how to incorporate robot intelligence in RAD tools. Key questions to focus on are, broadly, (1) balancing the amount and nature of domain knowledge that end-user developers must provide to the robot with the robot’s ability to fill in
the gaps, including how end-user domain knowledge should be represented as a computational artifact, (2) what tasks are best suited for RAD (as opposed to alternative approaches such as pure machine learning or planning), and (3) the contexts that are best suited for RAD. As of yet, there has been
little research to answer these questions.

We propose to start investigating how robot intelligence should be incorporated in RAD tools with (1)—comparing different approaches for end-user developers providing a necessary and sufficient amount of domain knowledge to the robot using a RAD tool, including different approaches for
representing this knowledge within compuational artifacts.

In particular, we are interested in comparing <em>goals</em> versus <em>actions</em> as a user-facing representation for collecting developer task specifications and intent while leveraging the robot’s ability to plan and act autonomously through robot intelligence. We refer to goals as the desired partial states of the world that the robot strives to achieve. We refer to actions as the steps that the robot takes to achieve its goals, namely <em>what</em> the robot does to achieve them. For example, the goal for a robot might be to have a cup at a table. The actions that the robot might take to achieve this goal would be to move to the cup, pick up the cup, move to the table, and then put the cup on the table. Our proposed work will extend the <em>*Polaris*</em> system developed by Porfirio, Roberts, and Hiatt (2024), a system that enables the user to provide specifications to the robot in the form of goals.

Should end-user developers specify robot tasks in terms of goals, actions, or both goals and actions? There are many anticipated tradeoffs between using goals and actions in RAD tools. Goals can be more concise than actions and can leverage the robot’s ability to plan and act autonomously. If given a goal, the robot can then fill in the gaps of knowledge (<em>i.e.,</em> actions) that are necessary to achieve the goal. With goals, users thus have control over the robot’s behavior while allowing the robot to plan its actions autonomously. However, reasoning about a robot’s plan in terms of goals may increase their cognitive load. Users may spend more time thinking about the final solution for the robot’s plan and fixing errors when reasoning about the plan, whereas building
a sequence of steps to a desired end-result with actions may be more intuitive for users. However, reasoning with actions may cause users to provide redundant or unnecessary steps for the robot, leading to a longer plan length.

In unveiling the tradeoffs between goals and actions as user-facing representations for RAD, our proposed work will be closely related to Porfirio, Roberts, and Hiatt (2024), which shifts the action-oriented development paradigm that is traditional within end-user development to a goal-oriented paradigm, in which end users specify a robot’s task not in terms of actions, but instead in terms of goals. While the paper demonstrates how a goal-oriented programming system may be designed, it does not explicitly compare the tradeoffs between specifying a task in terms of goals versus actions.

<div style="text-align: center;">
    <h2 id="related work"><strong>Related Work</strong></h2>
</div>

Robot application development (RAD) has historically existed in many different forms. One common example is the *visual programming environment* (VPE), in which end-user developers express a robot’s task in terms of visual building blocks in a graphical user interface. Examples include flow-based interfaces such as *RoboFlow* (Alexandrova, Tatlock, and Cakmak 2015) and *Interaction Composer* (Glas, Kanda, and Ishiguro 2016), and block-based interfaces constructed using Google *Blockly* (*e.g.,* Gargioni and Fogli 2024). Recent research has begun to focus on less traditional ways to capture developer intent. Examples include mixed-reality interfaces such as *V.RA* (Cao et al. 2019b) and *GhostAR* (Cao et al. 2019a). Natural language programming, as another example, is rising in popularity, through both chat interfaces (*e.g.,* Beschi, Fogli, and Tampalini 2019) and spoken language (*e.g.,* Forbes et al. 2015). While natural language is an intuitive form of communication, it can be ambiguous (Piantadosi, Tily, and Gibson 2012). Furthermore, if communicating with robots through spoken language, errors can arise in speech-to-text translation (Porfirio et al. 2023) and in conveying context-specific phrases and expressions (*e.g.,* language associated with a particular culture as in Andrist et al. 2015). A common theme with all of these works, however, is the *representation* of developer intent, or how developer intent is captured and stored as a computational artifact. Overwhelmingly, existing RAD tools capture and store developer intent in an *action-oriented* fashion, expressing the exact steps that the robot must perform to achieve its task objectives.

Although the action-oriented paradigm is the most common way that RAD tools express developer intent, it can be tedious for the user to specify the exact steps that the robot needs to take in order to achieve an objective, as well as more error-prone. Recent work has been done to address this issue by incorporating robot intelligence into RAD tools, allowing robots to act more autonomously while giving the user control over the robots’ behavior. Thus, there is a growing need for RAD tools to capture and store developer intent in a *goal-oriented* fashion, expressing the task objectives that the robot needs to achieve. Some examples of recent work in goal-oriented programming for RAD tools include *RoboCat* (Aguinaldo et al. 2022), a framework that leverages a string diagram to automate the translation of functional specifications into procedural code, and a robot dialog agent (Amiri et al. 2019), a system that captures human intent and augments its knowledge as-needed.

Porfirio, Roberts, and Hiatt (2024) investigated the effectiveness of helping users reason about a plan using goals in their system *Polaris*. While the paper discusses how object-oriented programming interfaces for robots should be designed, it does not address the tradeoffs between designing robot programs in terms of goals and actions.

Prior work has shown that users exhibit a bias in the direction in which they naturally reason about problems. Trafton and Reiser (1991) investigated the benefits and difficulties between forward reasoning (*i.e.,* with imperative programming) and backward reasoning (*i.e.,* with declarative programming) for novice programmers. The results of the study showed that participants strongly preferred to work in the forward study condition more than the backward study condition since it was less costly to repair errors in the solutions that the participants created. Participants in the backward study condition had longer initial planning times than in the forward study condition. Overall, the results showed that it was more difficult for participants to construct and implement a plan in the backward study condition than in the forward study condition.

This work suggests that there are several different existing and potential RAD paradigms. The preference for reasoning about a problem using a sequence of steps until the end-result is achieved (*i.e.,* the forward reasoning study condition) rather than reasoning abstractly about a problem starting from the end-result (*i.e.,* the backward reasoning study condition) suggests that users in our study will prefer to reason with actions rather than goals.

The preference for forward reasoning may suggest that users will prefer to reason with actions rather than goals for our study. However, Porfirio, Roberts, and Hiatt (2024) suggest that there is a theoretical benefit to using goals due to its compactness and flexibility of allowing users to specify tasks for a robot at a high-level of detail or low-level of detail.

<div style="text-align: center;">
    <h2 id="research plan"><strong>Research Plan</strong></h2>
</div>

Our future research will involve (1) extending the *Polaris* interface and (2) conducting a user study.

<div style="text-align: center;">
    <h3 id="user interface"><strong>User Interface</strong></h3>
</div>

*Polaris* is an end-user programming (EUP) tool, developed by Porfirio, Roberts, and Hiatt (2024), that allows users to specify tasks to a robot either at a high-level of detail or low-level of detail using *goal predicates* and fills in the gaps of knowledge between goal predicates using a planner. Users can specify tasks for the robot in the form of *checkpoints*, which contain goals, on the *Drawing Board* interface. A checkpoint is satisfied when the robot is able to compute a plan and has reached the desired goal. The user can visualize the plan output at runtime using the *Plan Visualizer* interface to ensure that the robot will behave in the way that they expect it would.

For this research, we are extending *Polaris* in three ways. First, we will extend *Polaris* to allow users to specify tasks in terms of not only goals, but also actions. If configured to specify tasks in terms of goals, *Polaris* constructs a plan to achieve each goal in sequence, which is no different from Porfirio, Roberts, and Hiatt (2024). This configuration will enforce that users can provide specifications only in the form of goals and cannot configure the actions that *Polaris* generates to achieve the goals. If, on the other hand, *Polaris* is configured to specify tasks in terms of actions in sequence, a plan will be constructed to achieve the preconditions of each user-specified action in sequence. Second, in contrast to Porfirio, Roberts, and Hiatt (2024), users will not be able to specify branching conditions. That is, users will be restricted to specifying purely *linear* sequences of either goals and/or actions on the *Timeline*. Third, our approach to providing feedback to users will differ from Porfirio, Roberts, and Hiatt (2024). In particular, rather than hiding the plan (i.e., sequences of actions) that the robot will take to satisfy a checkpoint behind a separate interface (called the *Plan Visualizer* in Porfirio, Roberts, and Hiatt 2024), the plan will be visualized within the *Timeline* itself, as shown in <a href="#fig1">Figure 1</a>.

<div id="fig1" style="text-align: center;">
    <img src="/assets/img/ur_rad/fig1.png" width="60%">
</div>

<p></p>

<a href="#fig1">Figure 1</a> shows our vision for how the user will specify tasks for the robot in terms of *goal predicates* (left) and actions (right) on the *Timeline*. Users can specify a goal or action by selecting an option from the white dropdown box. To aid the user in their understanding of what their chosen goal or action means, a natural language translation will be placed below the white dropdown box. For example, in the goals condition, the natural language translation for *agent_has is “[agent] is carrying [item]*.” Users can change the parameters using the dropdown boxes in the container with the natural language translation. Users can then visualize how the robot fills in the plan between goal predicates and user-specified actions (*e.g., gandalf approaches plate and gandalf grabs plate* in <a href="#fig1">Figure 1</a>).

<div style="text-align: center;">
    <h3 id="planned evaluation"><strong>Planned Evaluation</strong></h3>
</div>

To evaluate the tradeoffs between using goals and actions for RAD, we are planning a human subjects study in which participants will interact with the extended version of *Polaris*.

<div style="text-align: center;">
    <h4 id="study design"><strong>Study Design</strong></h4>
</div>

We propose a within-subjects experiment where participants will specify tasks for the robot using three study conditions – *goals*, *actions*, and *both*. In the *both* condition, participants can choose to use goals and/or actions. Participants will be tasked with different scenarios when exposed to each study condition.

Participants in the study will initially be provided a tutorial to gain familiarity with the *Timeline*. Within the tutorial, there will be a map of the robot’s physical environment similar to <a href="#fig2">Figure 2</a>, which will help the participants when they are considering how they should be specifying tasks for the robot for a given scenario. For example, we might provide a scenario where we ask participants to imagine that they are in a house with a robot and expose them to a map similar to <a href="#fig2">Figure 2</a>. The objective is to have the *plate on the kitchen table first and then the *cup on the kitchen table* next. Participants will then begin interacting with the *Timeline* (<a href="#fig1">Figure 1</a>) to specify tasks for the robot in the form of *checkpoints*.

<div id="fig2" style="text-align: center;">
    <img src="/assets/img/ur_rad/fig2.png" width="60%">
</div>

<p></p>

<div style="text-align: center;">
    <h4 id="measures"><strong>Measures</strong></h4>
</div>

The criteria we are considering to use to measure the effectiveness and tradeoffs between using goals and actions for end-user programming will include both objective robot performance and subjective robot perceptions. 

For robot performance, we ask: how will the robot’s ability to achieve its task objectives be affected by whether end-user developers specify tasks in terms of goals, actions, or both? Objective measures may include task performance—namely reliability and efficiency in completing task objectives—and the time it takes for end-users to specify a program for a given scenario.

For subjective performance, we ask: how will end-user developers’ perceptions of the robot be affected by whether they specify tasks with goals, actions, or both? We aim to assess users’ subjective perceptions both before and after observing the robot executing the task as specified by the end-user. Examples of subjective measures that we wish to include are trust, expectations, perceived reliability, objective reliability, usability, cognitive load, and perceived agency.

We might assess which particular representation users strongly preferred when specifying tasks for the robot in the *both* scenario. We will measure how users perceive the robot’s intelligence before and after having them specify tasks for the robot in terms of goals, actions, or both. We will also compare the robot’s task performance (*i.e.,* its ability to successfully complete the task) that results from the user-specified tasks between each condition.

<div style="text-align: center;">
    <h4 id="user interface"><strong>User Interface</strong></h4>
</div>

The criteria we are considering to use to measure the effectiveness and tradeoffs between using goals and actions for end-user programming will include both objective robot performance and subjective robot perceptions. For robot performance, we ask, how will the robot’s ability to achieve its task objectives be affected by whether end-user developers specify tasks in terms of goals, actions, or both? Objective measures may include task performance, namely reliability and efficiency in completing task objectives, and time it takes for end-users to specify a program for a given scenario. For subjective performance, we ask, how will end-user developers’ perceptions of the robot be affected by whether they specify tasks with goals, actions, or both? We aim to assess users’ subjective perceptions both before and after observing the robot executing the task as specified by the end-user. Examples of subjective measures that we wish to include are trust, expectations, perceived reliability, objective reliability, usability, cognitive load, and perceived agency.

We might assess which particular representation users strongly preferred when specifying tasks to the robot in the both scenario. We will measure how users perceive the robot’s intelligence before and after having them specify tasks for the robot in terms of goals, actions, or both. We will also compare the robot’s task performance (i.e., its ability to successfully complete the task) that results from the user-specified tasks between each condition.

<div style="text-align: center;">
    <h2 id="conclusion"><strong>Conclusion</strong></h2>
</div>

By extending *Polaris* to include the *Timeline* interface, we will compare the benefits and pitfalls of having end-user developers provide task specifications to a robot with two different approaches – goals versus actions – while leveraging the robot’s ability to plan and act autonomously through robot intelligence. Our work aims to contribute to future improvements of RAD tools, emphasizing the need to balance task-specification intuitiveness with robot autonomy in the development pipeline and allow users to provide a sufficient amount of domain knowledge to the robot.

<div style="text-align: center;">
    <h2 id="acknowledgements"><strong>Acknowledgements</strong></h2>
</div>

The views and conclusions contained herein are those of the authors and should not be interpreted as necessarily representing the official policies, either expressed or implied, of the U.S. Navy.

<div style="text-align: center;">
    <h2 id="references"><strong>References</strong></h2>
</div>

Aguinaldo, A.; Bunker, J.; Pollard, B.; Shukla, A.; Canedo, A.; Quiros, G.; and Regli, W. 2022. RoboCat: A Category Theoretic Framework for Robotic Interoperability Using Goal-Oriented Programming. *IEEE Transactions on Automation Science and Engineering*, 19(3): 2637–2645.

Alexandrova, S.; Tatlock, Z.; and Cakmak, M. 2015. RoboFlow: A flow-based visual programming language for mobile manipulation tasks. In *2015 IEEE International Conference on Robotics and Automation (ICRA)*, 5537–5544.

Amiri, S.; Bajracharya, S.; Goktolgal, C.; Thomason, J.; and Zhang, S. 2019. Augmenting Knowledge through Statistical, Goal-oriented Human-Robot Dialog. In *2019 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)*, 744–750.

Andrist, S.; Ziadee, M.; Boukaram, H.; Mutlu, B.; and Sakr, M. 2015. Effects of Culture on the Credibility of Robot Speech: A Comparison between English and Arabic. In *Proceedings of the Tenth Annual ACM/IEEE International Conference on Human-Robot Interaction*, HRI ’15, 157–164. New York, NY, USA: Association for Computing Machinery.

Beschi, S.; Fogli, D.; and Tampalini, F. 2019. CAPIRCI: A Multi-modal System for Collaborative Robot Programming. In Malizia, A.; Valtolina, S.; Morch, A.; Serrano, A.; and Stratton, A. (Eds.), *End-User Development*, 51–66. Cham: Springer International Publishing.

Cao, Y.; Wang, T.; Qian, X.; Rao, P. S.; Wadhawan, M.; Huo, K.; and Ramani, K. 2019a. GhostAR: A Time-space Editor for Embodied Authoring of Human-Robot Collaborative Task with Augmented Reality. In *Proceedings of the 32nd Annual ACM Symposium on User Interface Software and Technology*, UIST ’19, 521–534. New York, NY, USA: Association for Computing Machinery.

Cao, Y.; Xu, Z.; Li, F.; Zhong, W.; Huo, K.; and Ramani, K. 2019b. V.RA: An In-Situ Visual Authoring System for Robot-IoT Task Planning with Augmented Reality. In *Proceedings of the 2019 on Designing Interactive Systems Conference*, DIS ’19, 1059–1070. New York, NY, USA: Association for Computing Machinery.

Forbes, M.; Rao, R. P. N.; Zettlemoyer, L.; and Cakmak, M. 2015. Robot Programming by Demonstration with situated spatial language understanding. In *2015 IEEE International Conference on Robotics and Automation (ICRA)*, 2014–2020.

Gargioni, L.; and Fogli, D. 2024. Integrating ChatGPT with Blockly for End-User Development of Robot Tasks. In *Companion of the 2024 ACM/IEEE International Conference on Human-Robot Interaction*, HRI ’24, 478–482. New York, NY, USA: Association for Computing Machinery.

Glas, D. F.; Kanda, T.; and Ishiguro, H. 2016. Human-robot interaction design using Interaction Composer eight years of lessons learned. In *2016 11th ACM/IEEE International Conference on Human-Robot Interaction (HRI)*, 303–310.

Piantadosi, S. T.; Tily, H.; and Gibson, E. 2012. The communicative function of ambiguity in language. *Cognition*, 122(3): 280–291.

Porfirio, D.; Roberts, M.; and Hiatt, L. M. 2024. Goal-Oriented End-User Programming of Robots. In *Proceedings of the 2024 ACM/IEEE International Conference on Human-Robot Interaction*, HRI ’24, 582–591. New York, NY, USA: Association for Computing Machinery.

Porfirio, D.; Stegner, L.; Cakmak, M.; Sauppé, A.; Albarghouthi, A.; and Mutlu, B. 2023. Sketching Robot Programs On the Fly. In *Proceedings of the 2023 ACM/IEEE International Conference on Human-Robot Interaction*, HRI ’23, 584–593. New York, NY, USA: Association for Computing Machinery.

Trafton, J. G.; and Reiser, B. J. 1991. Providing natural representations to facilitate novices’ understanding in a new domain: Forward and backward reasoning in programming. In *Proceedings of the 13th Annual Conference of the Cognitive Science Society*, 923–927. Lawrence Erlbaum Associates, Inc.

