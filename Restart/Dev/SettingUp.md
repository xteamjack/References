Setting up the whole environment is slightly an involved activity. Please follow this document carefully

Application are developed using various technologies [node, python]. This list is expected to increase

Application follow a monorepo strategy. Setting the folder structure is important

Set environment variable by running [repo:utils]/scripts/sans-env.bat. Make sure all the base paths for the environment variables is set

## Cloning
For better management pick a "base" path and set everything relative to that
SANS_CODE_BASE should have all the code repos clone with respective technologies

eg., 
set SANS_CODE_BASE=D:/wspc3/repo/

1. clone all node repos to D:/wspc3/repo/node
2. clone all python repos to D:/wspc3/repo/python
3. Clone config.info into  SANS_CONFIG_BASE
4. Clone Utils into other folder and add Utils/script to path

**Special precautions for python repos**
- As python modules are directory path sensitive. Follow this mechanism
  - clone python.tech.libs tech
  - clone each of the module into respective directories under python


After cloning the repo and environment setting perform these steps
1. Node
   1. run npm i on each of the directories
2. Python
   1. Each of the repos contains version.cnf which indicates the python version 
   2. py-cnf on each of the application folders
   3. copy c_i.py as common_imports.py into python folder
   4. run pip install -r requirements.txt

## Setting up
Application may throw system exception (in certain cases) if these base folders are not found. Please create them before starting
1. List of folders to be created logs, store, 
2. Make sure they are assigned to env folder (preferably update utils/scripts/sans-env)


