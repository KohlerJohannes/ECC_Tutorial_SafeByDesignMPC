# Safe-by-Design Control using Robust MPC
### Quantifying, Predicting & Optimizing over Uncertainty

**ECC 2026 Tutorial**  
Reykjavik, Iceland — July 2026

---

## Organizers

- **Johannes Köhler** – Imperial College London, UK  
  Email: j.kohler@imperial.ac.uk

- **Glen Chou** – Georgia Institute of Technology, USA  
  Email: chou@gatech.edu

---

## Speakers

- **Johannes Köhler** – Imperial College London, UK  
  Email: j.kohler@imperial.ac.uk

- **Glen Chou** – Georgia Institute of Technology, USA  
  Email: chou@gatech.edu

- **Lars Lindemann** – ETH Zurich, Switzerland  
  Email: llindemann@ethz.ch

- **Laura Ferranti** – TU Delft, Netherlands  
  Email: L.Ferranti@tudelft.nl

---

## Abstract
As autonomous systems move beyond controlled lab environments into the real world, *safe-by-design* control is becoming essential. 
Safe-by-design control methods aim to guarantee satisfaction of safety-critical constraints from the outset, eliminating reliance on trial-and-error tuning and systematically addressing the sim2real gap.  
This not only accelerates the deployment cycle but also makes these methods well-suited for safety-critical applications, especially those involving the risk of physical interaction with humans. 
This tutorial focuses on robust model predictive control (MPC) as a principled framework for designing reliable controllers despite uncertainty. Robust MPC integrates optimization algorithms with physical (or learned) models, and explicitly accounts for uncertainty arising from modeling errors, sensor noise, and external disturbances. 
We present a unified exposition of recently developed techniques to systematically handle *uncertainty*: (1) *quantifying* it from experimental data, (2) *predicting* the effect of uncertainty on the robot movement, and (3) *optimizing* safe motions. 
In addition, this tutorial will cover how *conformal predictions* provide a sound statistical tool for uncertainty quantification that can be integrated into robust MPC formulations. 
This tutorial will end with insights from applications in robotics, highlighting how (robust) MPC can be utilized to operate robots near humans, but also what challenges remain in practice. 
The goal of this tutorial is to provide researchers and practitioners with *systematic* tools to advance complex autonomous systems in safety-critical operations. 


## Program

### Talk 1

**Speaker:**  Johannes Köhler 

**Title:**  Safe-by-design control with robust MPC

**Abstract:**
This introductory talk presents how safe-by-design control is achieved through robust model predictive control (MPC). Designed to be accessible with minimal mathematical complexity, it focuses on the fundamental components of robust MPC, including robust predictions, optimization, and receding-horizon implementation.
The talk  covers basic theoretical results, highlighting how safety and stability are ensured with a proper design. 
Examples from diverse robotics applications illustrate the practical relevance and motivate the audience.  
The presentation concludes by highlighting the main challenges in the design. 
This sets the stage for the rest of the tutorial, explaining the structure and emphasizing the importance of each upcoming talk to achieve safe-by-design robot control. 

### Talk 2-3

**Speaker:**   Glen Chou & Johannes Köhler

**Title:**  Certified uncertainty propagation - I-II

**Abstract:**
This forms the core of the tutorial, providing a unified exposition on diverse techniques for uncertainty propagation of nonlinear robot dynamics. 
We cover trajectory-specific sum-of-squares approaches, contraction metrics, linearization-based techniques, system level synthesis (SLS), and sampling-based methods. 
We first provide intuition by explaining uncertainty propagation for linear dynamics and highlight the challenges arising due to nonlinear dynamics. 
he methods are contrasted based on which design decisions are made offline and which are optimized online during execution
Robotics examples demonstrate the effect of these differences in practice. 
For simplicity, we focus primarily on the robust case with bounded model error, but also briefly highlight how methods naturally extend to stochastic noise and probabilistic guarantees. 

### Talk 4

**Speaker:**  Glen Chou

**Title:**  Uncertainty quantification from data 

**Abstract:** This talk focuses on retrieving the model and the characterization of the model accuracy from data, which is a key step in the robust design. 
A variety of methods will be studied, highlighting their difference in setup (stochastic, robust, partial measurement), computational complexity, and theoretical guarantees (asymptotic vs. exact finite-sample). 
This includes set-membership estimation, maximum likelihood estimation and
Gaussian process models. 
The talks highlights how data-driven uncertainty quantification enables an automated and modular  design of safe-by-design controllers.
It will also highlight some of the specific challenges for uncertainty quantification that arise from perception-based control, i.e., when online processing of image data provides a critical measurement signal in the control loop.

### Talk 5

**Speaker:**  Lars Lindemann

**Title:**  When Control Changes the Data: Safety under Interaction-Driven Distribution Shifts

**Abstract:** Accelerated by rapid advances in machine learning and AI, there has been tremendous success in the design of learning-enabled autonomous systems in areas such as autonomous driving and robotics. These exciting developments are accompanied by new fundamental challenges that arise regarding the safety and reliability of these increasingly complex systems due to imperfect learning, system unknowns, and uncertain environments. Conformal prediction (CP) — a statistical tool for uncertainty quantification — has gained popularity due to its ability to deal with these challenges. However, CP-based safety guarantees assume i.i.d. data, an assumption that is violated when system changes induce shifts in the underlying data distribution. 
In this tutorial, I will provide new insight to design safe controllers under distribution shifts using robust CP. I will begin by advocating for the use of CP due to its simplicity, generality, and efficiency as opposed to existing optimization-based verification techniques. I will then provide an introduction to CP and summarize existing work that uses CP to design probabilistically safe controllers in dynamic environments. Subsequently, we will look into interactive settings where the system’s behavior may change the environment's behavior, and vice versa. This circular dependency creates an interaction-driven distribution shift that invalidates existing safety guarantees. To deal with this chicken-and-egg problem, we propose an iterative framework that episodically updates the controller while robustly maintaining safety guarantees by quantifying the potential impact of a controller update on the environment's behavior. We realize this via adversarially robust CP where we perform a regular CP step in each episode using observed data under the current controller, but then transfer safety guarantees across controller updates by analytically adjusting the CP result to account for distribution shifts. Lastly, we will discuss ways to deal with more general distribution shifts that go beyond this interactive setting using adaptive and distributionally robust CP. This talks is based on the references.

### Talk 6

**Speaker:**  Laura Ferranti

**Title:**  Model predictive control for robot motion planning near humans

**Abstract:**  This talk investigates the application of MPC for mobile robot motion planning in human-centric environments. As autonomous systems—such as self-driving cars, vessels, and drones—increasingly operate alongside people, they must effectively manage uncertainties arising from both external sources (e.g., human behavior) and internal constraints (e.g., hardware and software limitations).
We first present two approaches to handle human-induced uncertainties: a scenario-based design combined with MPC, and geometrical approaches to define the MPC navigation envelope. Finally, we demonstrate how robust MPC arguments can be used to overcome implementation constraints on resource-limited robots, such as drones. We will conclude with a discussion on the limitations of current methods and how to overcome them with tools taken from game theory and machine learning.
 


## Material

Slides and supplementary material will be uploaded here after the tutorial.
