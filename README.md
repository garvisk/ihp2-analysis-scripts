# ihp2-analysis-scripts
These are the scripts used for data analysis on the IHP2 project.  "analysis_ihp2_all-3-vehicle-analysis.py" creates all plots in verification testing besides mph tests. "analysis_ihp2_2-car_mph-analysis.py" creates all plots for mph tests in verification testing.

# Download required rosbags from google drive link below for IHP2 data
https://drive.google.com/drive/folders/1Wf2zP4De83JEKdajv1cFFmQ927InJs1J?usp=drive_link


# Reindexed rosbags (incase script can't read the bag files)
rosbag reindex *.bag


# HOW TO USE SCRIPT:
## Run the following in a terminal:
   ### sudo add-apt-repository ppa:deadsnakes/ppa
   ### sudo apt-get update
   ### sudo apt install python3.7
   ### python3.7 -m pip install --upgrade pip
   ### python3.7 -m pip install matplotlib
   ### python3.7 -m pip install --extra-index-url https://rospypi.github.io/simple/ rospy rosbag rospkg
   ### python3.7 -m pip install lz4
   ### python3.7 -m pip install roslz4 --extra-index-url https://rospypi.github.io/simple/

## In terminal, navigate to the directory that contains this python script and run the following:
python3.7 <name_of_analysis_script> <path to folder containing IHP2 .bag files> 


## To edit the scripts for different x-axis dimensions, search for the lines which contain the info below:
###    ax.set_ylabel("Vehicle Speed (m/s)") # Plot Y Title
###    ax.set_xlim([-5, 175]) 
###    ax.set_ylim([0, 20])

###Change the xlim or ylim values to change the dimensions of the plot.  This should show up multiple times throughout the script.
