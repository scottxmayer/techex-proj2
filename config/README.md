### To Export conda env

# best option for conda import 
`conda env export > environment.yml` 

# lists all packages installed by conda 
`conda list -e > evironment.txt`

# lists all packages installed by pip 
`pip freeze > requirements.txt`

# lists all pip packages required for project, not including other installs
`pipreqs /path/to/proj`

### to build environment 

`conda env create --name env_name -f environment.yml` 
