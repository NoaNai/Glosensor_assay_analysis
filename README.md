# Glosensor Luciferase Assay
## Project proposal
[Noa Nairner](https://noanai.github.io/) and [Ori Berman](https://ori1992.github.io/)

We plan to write a script that will interactively interpret data from an experiment via a GUI. 

Our raw data is an excel spreadsheet containing results from a 96-well plate, each row is a measurement of one well over time. The same conditions are repeated three times in consecutive rows. 

The script will plot each row data over time and display the graphs as a matrix in the GUI. The user is requested to select any graphs that seem unusual to be marked as outliers and the data to be removed from further analysis. 

The script will analyze the data based on user range inputs (subtract the corresponding baseline, normalize each data point by dividing by the row max value, calculate the average values for repetitions of the same conditions) and output a results spreadsheet, as well as another graphs matrix that plot the analyzed data. 

# Script Requirements
This script is run via jupyter notebook. Please make sure you install jupyter notebook:
```python
pip install jupyter notebook
```
In the project folder containing the data file, open jupyter notebook.

The script requires the following modules to be installed: numpy, matplotlib, pandas, ipywidgets, pickleshare.
```python
pip install numpy matplotlib pandas ipympl ipywidgets pickleshare
```

# Description
The repository contains 2 scripts: 1-Glosensor_plot_raw_data.ipynb and 2-Glosensor_assay_analyze_data.ipynb,hich should be run consecutively.

The first script allows the user to input an excel raw data file, and visualize each raw data row graphically in order to decide which rows to exclude from further analysis. This graph matrix opens automatically as a pdf file in the active folder. Please input the file with the extension, i.e. "DMEM_PLATE2_WORKFLOW.xlsx".
The user can choose an examplary row to plot interactively in the notebook and zoom in and out. 
At the end of script 1 are input widgets for the user to choose which rows to exclude, what the repitition value is (i.e. duplicates or triplicates) and what ranges of time should the program regard as baseline and max value. Example values are given as defaults. Once you have changed the the values, please re-run the final cell in order to save the changed values.

The second script takes the chosen values from the first script and analyzes the data accordingly. The outputs are:
- pdf file of normalized graphs matrix
- pdf file of graphs matrix of **averages** over repititions
- Excel file containing the normalized and averaged data