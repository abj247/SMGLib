![GitHub last commit (by committer)](https://img.shields.io/github/last-commit/abj247/MASDA)
![Static Badge](https://img.shields.io/badge/Status-Incomplete-red)
![GitHub Repo stars](https://img.shields.io/github/stars/abj247/MASDA)
![GitHub repo file count (file type)](https://img.shields.io/github/directory-file-count/abj247/MASDA)
![GitHub language count](https://img.shields.io/github/languages/count/abj247/MASDA)
![GitHub top language](https://img.shields.io/github/languages/top/abj247/MASDA)

<div style="display: flex; flex-direction: row;">
    <img src="animations/CADRL_2agents_intersection.gif" width="200">
    <img src="animations/IMPC_doorway.gif" width="200" height="160">
    <img src="animations/CADRL_2agents_hallway.gif" width="200">
    <img src="animations/CADRL_2agents_doorway.gif" width="200">
</div>


# Multi Agent Social Deadlock Avodidance (MASDA)

<p class="justify">The Multi Agent Social Deadlock Avoidance (MASDA) repository represents a culmination of extensive efforts dedicated to addressing the intricate challenge of deadlock avoidance within multi-agent social navigation contexts. In bustling environments characterized by doorways, hallways, intersections, and other intricate settings, the seamless and efficient movement of both individuals and autonomous agents is not just a convenience but a critical necessity. It is in this dynamic and challenging backdrop that the MASDA project takes center stage. Our primary objective revolves around the meticulous compilation of a diverse array of algorithms and methodologies hailing from various domains, each meticulously curated to serve as a potential solution for the multifaceted deadlock challenges prevalent in social navigation scenarios. </p>

<p class="justify">These scenarios are marked by their inherent complexity, where agents need to navigate through spaces while intelligently avoiding bottlenecks, traffic congestion, and potential gridlocks. In the pursuit of deadlock avoidance excellence, the MASDA repository is meticulously designed to offer a plethora of innovative strategies tailored to address these real-world challenges. Whether it's guiding pedestrians through congested doorways, orchestrating the movements of autonomous vehicles within intricate intersections, or facilitating the seamless flow of agents in narrow hallways, MASDA houses a rich collection of algorithms catering to an extensive spectrum of scenarios.</p>

# About
* Multi Agent Navigation
* Deadlock Avoidance
* Social Navigation

# Table of Contents
- [**About**](#About)
- [**Dependcies**](#Dependcies)
- [**Installation**](#Installation)
- [**Supported Scenarios**](#Supported-Scenarios)
- [**CADRL**](#CADRL)
- [**ORCA-MAPF**](#ORCA-MAPF)
- [**IMPC-DR**](#IMPC-DR)



# Dependencies
* Matlab 2021
* Python         3.6
* gym            0.26.2
* PyQt5          5.15.1
* opencv-python  4.1.2.30
* numpy          1.19.2
* mosek          9.4.20
* cvxpy          1.1.6
* scipy          1.5.3
* matplotlib     3.4.3


# Installation

To run the experiments first clone the repository for installation

``` git clone https://github.com/abj247/MASDA.git ```

# Supporterd Scenarios
Our repository covers a wide spectrum of social navigation scenarios, including but not limited to:

* Doorway Navigation: Efficient passage through doorways, especially in crowded settings, is a common challenge. We offer strategies to prevent congestion and deadlocks at entrances and exits.

* Hallway Navigation: Managing traffic flow in narrow hallways is critical for safe and efficient movement. Our algorithms focus on optimizing hallway traversal.

* Intersection Management: Intersections, whether for pedestrians, vehicles, or mixed traffic, demand sophisticated deadlock avoidance strategies. We provide solutions to coordinate and prioritize agent movement at intersections.

# CADRL
Continuous Action-Value Distributional Reinforcement Learning (CADRL) stands as a pivotal component within our repository, specializing in the realm of social navigation. It is a cutting-edge framework that harnesses the power of reinforcement learning to enable autonomous agents to navigate complex social environments seamlessly. CADRL leverages continuous action-value distributional reinforcement learning techniques to imbue agents with the ability to make dynamic decisions while considering the presence and behaviors of other agents. 

To run CADRL experiments for Social mini games go to specified folder and choose the scenario to run. For example to simulate doorway scenario with CADRL use following command

``` cd ./Methods/Social-CADRL/experiments/src ```

``` python doorway.py ```

The animation file for the simulation will be saved at 
``` ./Methods/Social-CADRL/experiments/results/example/animations ```

With CADRL, our repository equips agents to make informed, real-time decisions in congested scenarios, such as doorways, hallways, and intersections, ensuring not only efficient movement but also social adherence. CADRL plays a crucial role in enhancing the overall safety and functionality of multi-agent systems in social navigation contexts, making it an indispensable tool within our collection of algorithms and methodologies.

# ORCA-MAPF
ORCA-MAPF (Optimal Reciprocal Collision Avoidance for Multi-Agent Path Finding): Within our repository, ORCA-MAPF takes center stage as a robust and efficient solution designed to address multi-agent pathfinding challenges in dynamic social environments. This state-of-the-art algorithm leverages the principles of optimal reciprocal collision avoidance to enable autonomous agents to navigate complex scenarios, such as crowded doorways, hallways, and intersections, with precision and safety. ORCA-MAPF excels in optimizing the trajectories of multiple agents simultaneously, considering not only their paths but also their velocities and intentions.

To run the ORCA-MAPF for social mini game scenario first build the project.

```bash
cd ./Methods/Social-ORCA/
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE={Release/Debug} -DFULL_OUTPUT_FLAG={ON/OFF} -DFULL_LOG_FLAG={ON/OFF} -DMAPF_LOG_FLAG={ON/OFF} ..
make
```

where optins:
- `CMAKE_BUILD_TYPE` — Standard CMake option that specifies the build type. For more information see [[CMake Documentation](https://cmake.org/cmake/help/latest/variable/CMAKE_BUILD_TYPE.html)]    
etc
  - `Release` uses to build with no debugging information. 
  - `Debug` usually uses to enable debugging information, disable optimization 
- `FULL_OUTPUT_FLAG` — Enables/disables full output to stdout about reading xml files.
- `FULL_LOG_FLAG` — Enables/disables logging to xml file agents state information
- `MAPF_LOG_FLAG` — Enables/disables logging to xml files information about MAPF instances in coordinated mode

After this launch the social navigation scenario to run using following command
```bash
./single_test {file_name num}
```
where 
- `file_name` — name of the XML file, which contain social; scenario;
- `num` — the number of agents with which tasks will run.

For example to simulate intersection scenario use following command

```bash
./single_test ../task_examples/intersection.xml 2
```
Summary will be displayed after execution using standard output, full log (if such option in in CMake was chosen) 
will be saved in same directory as task file and will be named according to the following pattern:
```
*taskfilename*_*number_of_agents*_log.xml
```
For example:
```
intersection_2_log.xml
```
By incorporating ORCA-MAPF into our collection, we enhance the capability of agents to make real-time decisions that promote both smooth movement and social compliance. It represents a key component in our endeavor to advance the science and technology of multi-agent systems for social navigation, contributing to safer and more efficient interactions between agents in shared spaces.

# IMPC-DR
IMPC-DR for Social Navigation: IMPC-DR, or Infinite-Horizon Model Predictive Control with Deadlock Resolution, holds immense promise in the context of social navigation scenarios. In bustling environments characterized by doorways, hallways, and intersections, where multiple agents, be they pedestrians or autonomous robots, coexist, IMPC-DR shines as a beacon of efficiency and safety. By providing rigorous guarantees on optimization feasibility, IMPC-DR ensures collision-free trajectory generation for agents within shared workspaces. It not only tackles the challenge of resolving deadlocks but also preemptively detects and resolves potential deadlocks through its adaptive resolution scheme. This proactive approach promotes smooth agent movements and prevents gridlocks, even in the most crowded and high-speed scenarios.

To simulate IMPC-DR for social mini games go to specified folder and launch the app to run specific social scenario

``` cd ./Methods/Social-IMPC-DR/ 
python app.py
```
After the simulation is completed the animation will be saved at 
``` ./Methods/Social-IMPC-DR/ ```

IMPC-DR is a key asset within our repository, contributing to the enhancement of multi-agent systems' performance in social navigation contexts. Its ability to combine theoretical rigor with practical effectiveness makes it an invaluable tool for creating safe and efficient interactions between agents navigating shared spaces.


