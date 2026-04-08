# Hackathon PMS 2026 Game Packing

The goal is to pack boxes from various board games (data comes from https://www.espritjeu.com) in a rectangular container box with minimum sum of length, width and height. Boxes may be rotated but their axis must remain orthogonal to the axis of the container box.

The folder `dataset` contains 21 instance files. Each CSV file is a set of boxes, the name of the instance indicates the generation method (homogeneous, heterogeneous, random). There is one row per box and the fields are the name, length, width and height of that box. 

You can solve the problem in any way you want, as long as you follow the [solution submission procedure](#submitting-solutions).
There are helpers scripts for the following toolkits:
- [Tempo (recommended)](#solving-with-tempo) 
- [Python](#solving-with-cpmpy-(or-other-python-toolkits)) 
- [Minizinc](#solving-with-minizinc)

The solutions can be visualized using the Python library `blockviz`...


## Setting up your team repository and submitting solutions
First, fork this git repository, or create a new git repository with a copy of the file `team.json` and the entire folder `solutions`, and send the link to clone this repository at hebrard@laas.fr. For instance, you can follow these steps:

1. Clone this repo

> git clone https://gitlab.laas.fr/ROC/hackathon-pms-2026-game-packing

2. Create an empty repository on any git platform (say git@github.com/me/A-team)

3. push the team and solution files in your repo

>>>

cd hackathon-pms-2026-game-packing

git remote add team.json git@github.com/me/A-team

git remote add solutions git@github.com/me/A-team

>>>

4. Fill the file `team.json` with the relevant information

5. *When you find a new best solution*, copy it into the corresponding solution file and push into the corrsponding solution file, e.g., if this is a solution for `dataset/random_0005.csv`, copy it into `solutions/random_0005.json` and:

>>>

git commit -m "new solution" solutions/random_0005.json 

git push main

>>>


## Solving with Tempo

Prerequisites: cmake is installed
1. Clone Tempo: `git clone https://gitlab.laas.fr/roc/emmanuel-hebrard/tempo.git`
2. create a build folder and move into it (`mkdir build; cd build`)
3. run `cmake -DCMAKE_CXX_COMPILER=g++-11 -DCMAKE_BUILD_TYPE=release ..`
4. run `make boxes`

This will compile an executable whose code is in `src/examples/boxes.cpp`

This program implements helpers to read the instances, print the solutions, and provides skeletons of:
1. A object (`BoxVariable`) grouping all the variables relative to a box 
2. A model (`BoxPackingModel`) 
3. A user-defined heuristic (`MyHeuristic`)
4. A user-define LNS policy (`MyLNSPolicy`)





## Solving with CPMpy (or other Python toolkits)


## Solving with Minizinc


