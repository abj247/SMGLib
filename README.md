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


#Installation

To run the experiments first clone the repository for installation

``` git clone https://github.com/abj247/MASDA.git ```

# Supporterd Scenarios
Our repository covers a wide spectrum of social navigation scenarios, including but not limited to:

* Doorway Navigation: Efficient passage through doorways, especially in crowded settings, is a common challenge. We offer strategies to prevent congestion and deadlocks at entrances and exits.

* Hallway Navigation: Managing traffic flow in narrow hallways is critical for safe and efficient movement. Our algorithms focus on optimizing hallway traversal.

* Intersection Management: Intersections, whether for pedestrians, vehicles, or mixed traffic, demand sophisticated deadlock avoidance strategies. We provide solutions to coordinate and prioritize agent movement at intersections
