# Data analysis and Manipulation
import plotly.graph_objs as go
import plotly.io as pio
import plotly.express as px
import pandas as pd

# Data Visualization
import matplotlib.pyplot as plt

# Importing Plotly
import plotly.offline as py
py.init_notebook_mode(connected=True)

# Data analysis and Manipulation
import plotly.graph_objs as go
import plotly.io as pio
import plotly.express as px
import pandas as pd

# Data Visualization
import matplotlib.pyplot as plt

# Importing Plotly
import plotly.offline as py
py.init_notebook_mode(connected=True)

# Initializing Plotly
pio.renderers.default = 'colab'
pd.read_csv('/content/covid.csv')
pd.read_csv('/content/covid_grouped.csv')
pd.read_csv('/content/coviddeath.csv')
print(dataset1.shape)
print(dataset1.size)
print(dataset2.shape)
print(dataset2.size)
print(dataset3.shape)
print(dataset3.size)
dataset1.drop(['Deaths/1M pop', 'TotalTests', 'Tests/1M pop',
       'WHO Region', 'iso_alpha'],
              axis=1, inplace=True)

# Select random set of values from dataset1
dataset1.sample(5)
dataset3.drop(['Data as of', 'Start Week', 'End Week', 'State', 'Condition Group',
       'Condition', 'ICD10_codes', 'Age Group', 'Number of COVID-19 Deaths'],
              axis=1, inplace=True)

# Select random set of values from dataset1
dataset3.sample(5)
from plotly.figure_factory import create_table

colorscale = [[0, '#4d004c'], [.5, '#f2e5ff'], [1, '#ffffff']]
table = create_table(dataset1.head(15), colorscale=colorscale)
py.iplot(table)
px.bar(dataset1.head(15), x = 'Country/Region',
       y = 'TotalCases',color = 'TotalCases',
       height = 500,hover_data = ['Country/Region', 'Continent'])
       px.scatter(dataset1, x='Continent',y='TotalCases',
           hover_data=['Country/Region', 'Continent'],
           color='TotalCases', size='TotalCases', size_max=80)
