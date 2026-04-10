# PMS Hackathon: guide for Tempo

Prerequisite: cmake is installed
1. Clone Tempo: `git clone https://gitlab.laas.fr/roc/emmanuel-hebrard/tempo.git`
2. create a build folder and move into it (`mkdir build; cd build`)
3. run `cmake -DCMAKE_CXX_COMPILER=g++-11 -DCMAKE_BUILD_TYPE=release ..`
4. run `make boxes`

This will compile an executable whose code is in `src/examples/boxes.cpp`.

This program implements helpers to read the instances, print the solutions, and provides skeletons of:
1. A object (`BoxVariable`) grouping all the variables relative to a box 
2. A model (`BoxPackingModel`) 
3. A user-defined heuristic (`MyHeuristic`)
4. A user-define LNS policy (`MyLNSPolicy`)

You can use this executable as basis for you solution.

Tempo's [Quickstart guide](#https://gitlab.laas.fr/roc/emmanuel-hebrard/tempo/-/edit/main/documentation/QUICKSTART.md?ref_type=heads) should help you.


