# Social ORCA-MAPF
ORCA-MAPF (Optimal Reciprocal Collision Avoidance for Multi-Agent Path Finding): Within our repository, ORCA-MAPF takes center stage as a robust and efficient solution designed to address multi-agent pathfinding challenges in dynamic social environments. This state-of-the-art algorithm leverages the principles of optimal reciprocal collision avoidance to enable autonomous agents to navigate complex scenarios, such as crowded doorways, hallways, and intersections, with precision and safety. ORCA-MAPF excels in optimizing the trajectories of multiple agents simultaneously, considering not only their paths but also their velocities and intentions.

To run the ORCA-MAPF for social mini game scenario first build the project.

```bash
cd ./Methods/Social-ORCA/
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE={Release/Debug} -DFULL_OUTPUT_FLAG={ON/OFF} -DFULL_LOG_FLAG={ON/OFF} -DMAPF_LOG_FLAG={ON/OFF} ..
make
```

where optons:
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
