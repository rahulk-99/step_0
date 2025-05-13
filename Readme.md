# Isaac Lab Validation Demo – Two UR10 Bots

This repository demonstrates a validated setup on Ubuntu 22.04 with Isaac Sim 4.5.0 and Isaac Lab 2.1.0. The demo uses a modified version of the standard `arms.py` to run two UR10 robots.

**Requirements**  
Ensure the following packages/versions are installed in your environment:
- **Isaac Sim 4.5.0** 
- **Isaac Lab 2.1.0** (Follow the instructions provided in the [Isaac Lab pip installation guide](https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/isaaclab_pip_installation.html))


**Folder Structure**  
```bash
step_0/
├── modified_arms.py                # Modified demo script for two UR10 robots
├── README.md              # Project description and setup instructions
```

**Demo video drive link** 
This link contains 2 videos
```bash
├── modified.webm          # Video recording of environment setup and running problem statement
├── standard_demo.webm     # Video recording of standard arm.py available in IsaacLab environment
```
https://drive.google.com/drive/folders/1s8MGg_V-DxOfpNQoxJJdlL52F9vDUX6V?usp=drive_link


## Environment Setup

1. **Activate the Conda/Virtual Environment for IsaacLab**  
   Open a terminal and run:
   ```bash
   # If IsaacLab is installed using a conda environment
   conda activate env_isaaclab         # Replace 'env_isaaclab' with your custom environment name if different

   # If IsaacLab is installed using a Python virtual environment
   source env_isaaclab/bin/activate    # Replace 'env_isaaclab' with your custom environment name if different
   ```

   

## Running the Validation Example

The demo executable is located at `step_0/modified_arms.py` (modified to run two UR10 robots). To run the demo:

1. **Clone the repository**  
   ```bash
   git clone https://github.com/rahulk-99/step_0.git      # Clone to the desired directory
   cd step_0
   ```
   

2. **Run the modified script**  
   From the repository root, run:
   ```bash
   local_directory_of_IsaacLab/isaaclab.sh -p modified_arms.py   # Enter the local directory of Isaaclab
   ```

   The script will initialize the simulation, set up two UR10 manipulators on separate table mounts, and begin the simulation loop. 


3. **Run the standard script**  
   From the repository root, run:
   ```bash
   cd /local_directory_of_IsaacLab            # Enter the local directory of Isaaclab
   ./isaaclab.sh -p scripts/demos/arms.py  
   ```

   The script will initialize the simulation, set up two six different standard arms available with Isaaclab environment, and begin the simulation loop. 
