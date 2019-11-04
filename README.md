# bds_api
A brief python wrapper designed to access the Census Business Dynamics Statistics API

BDS-API is a lightweight wrapper for the Census Business Dynamics Statistics API. From the census website:

>The Business Dynamics Statistics (BDS) includes measures of establishment openings and closings, firm startups, job creation and destruction by firm size, age, and industrial sector, and several other statistics on business dynamics.

# Installation:

install using pip:  `pip install bds-api`

# Usage and Examples:

bds-api takes two arguments: `variables` and `filters`, and returns a Pandas Dataframe object. For instance:

```
from bds_api import census_bds_api as api

vars = ['estabs', 'fage4', 'fsize',]
filters = {'state':'01','sic1':'0', 'time':'2014', 'key': 'Your API key here'}
# you are required to pass a location, time, and key filter.

content = api.get(variables=vars, filters=filt)

```

`variables` must be passed as a list, and `filters` must be passed as a dictionary. That is to say, `variables` are passed to give columns to your data, `filters` are passed to filter the returned data columns. Full documentation on possible parameters can be found [here](https://api.census.gov/data/timeseries/bds/firms/variables.html).

API Keys can be created [here](https://api.census.gov/data/key_signup.html).

License
----
© 2019 Ryan Cogburn
Licensed under MIT provision
