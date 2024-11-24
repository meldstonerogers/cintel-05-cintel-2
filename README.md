# cintel-04-local
Cintel Project 4
Melissa Stone Rogers, [GitHub](https://github.com/meldstonerogers/cintel-04-local)

## Introduction
Professional project using git, python, and shiny to publish reactive shiny app. 
Commands were used on a Mac machine running zsh. Project was guided by Dr. Denise Case's GitHub repository, [pyshiny-penguine-dashboard-express](https://github.com/denisecase/pyshiny-penguins-dashboard-express).


## How to Install and Run the Project
Create project repository in Github and clone to your machine.

```
git clone project.url
```
Verify Python version of Python 3
```
python3 --version

```
```
python3 -m venv venv
source venv/bin/activate
```
Create requirements.txt in the root project folder if you have note already done so in your GitHub repository. 
```
touch requirements.txt
```

Install packages into virtual enviornment
```
python3 -m pip install --upgrade pip setuptools
python3 -m pip install --upgrade -r requirements.txt
pip install shinylive

```
Install VS Code Extension for Shiny.

## Freeze Dependencies 
```
python3 -m pip freeze > requirements.txt
```

## Initial Project Save
```
git add .
git commit -m "initial"                         
git push origin main
```
### Start and Complete Project 
Follow instructions within Dr. Case's GitHub repository, [pyshiny-penguine-dashboard-express](https://github.com/denisecase/pyshiny-penguins-dashboard-express) and other course content provided. 

#### Troubleshooting
Using the following code, I attempted to run my Shiny app within a web browser. 
```
shiny run --reload --launch-browser penguins/app.py
```

I got numerous errors and my app would not run and launch. Thanks to dilligent colleagues within the NWSU's Continuous Intelligence course, the following troubleshooting was noted. To successfully launch my Shiny app, I downgraded websockets to version 10.4 from 14.0 using the following code.
```
pip install websockets==10.4
```

Once completed, I was able to successfully run my Shiny app within a web browser with the initial code provided above.

## Complete Your Project
Save your project and push back to your repository. 
```
git add .
git commit -m "final"                         
git push origin main
```

## Resources 
This section was copied and pasted from Dr. Case's GitHub repository, [pyshiny-penguine-dashboard-express](https://github.com/denisecase/pyshiny-penguins-dashboard-express). Please note the following resources below. 

Example csv data from [penguins.csv](https://github.com/mwaskom/seaborn-data/blob/master/penguins.csv).
Used for review only. In the app, we import the data from the palmerpenguins package.

Palmer Penguins published in:

- Horst AM, Hill AP, Gorman KB (2020). palmerpenguins: Palmer
Archipelago (Antarctica) penguin data. R package version 0.1.0.
 <https://allisonhorst.github.io/palmerpenguins/>. doi:
10.5281/zenodo.3960218.

Data originally published in:

- Gorman KB, Williams TD, Fraser WR (2014). Ecological sexual dimorphism and environmental variability within a community of Antarctic penguins (genus Pygoscelis). PLoS ONE 9(3):e90081. <https://doi.org/10.1371/journal.pone.0090081>

The Shiny development team. Shiny for Python [Computer software]. <https://github.com/posit-dev/py-shiny>