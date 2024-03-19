# Glosensor Luciferase Assay: Project proposal
[Noa Nairner](https://noanai.github.io/) and [Ori Berman](https://ori1992.github.io/)

We plan to write a script that will interactively interpret data from an experiment via a GUI. 

Our raw data is an excel spreadsheet containing results from a 96-well plate, each row is a measurement of one well over time. The same conditions are repeated three times in consecutive rows. 

The script will plot each row data over time and display the graphs as a matrix in the GUI. The user is requested to select any graphs that seem unusual to be marked as outliers and the data to be removed from further analysis. 

The script will analyze the data based on user range inputs (subtract the corresponding baseline, normalize each data point by dividing by the row max value, calculate the average values for repetitions of the same conditions) and output a results spreadsheet, as well as another graphs matrix that plot the analyzed data. 

# Script Description
This script is run via jupyter notebook. Please make sure you install jupyter notebook:
```python
pip install jupyter notebook
```
The script requires the following modules to be installed: numpy, matplotlib, pandas, ipywidgets, pickleshare.
```python
pip install numpy matplotlib pandas ipympl ipywidgets pickleshare
```
