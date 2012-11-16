Cluster Data Management Using Version Control
=============================================

Desired Outcomes
----------------
 * Reduce time spent managing the submission and collection of data
   off HPC infrastructure.

Requirements
------------
 * push from clusters but pull from local machines

Initialize
----------
 * install local python scripts
 * make project directory structure
 * construct VC exclude file
    * possibly different levels of exclude (local, cluster)
 * create repository (git,svn,etc) with detailed README.md

Ideas
-----
 * some kind of project database keeping track of running jobs



Directory Structure
-------------------
    Project/
        executable.e
         * record version of the code
        --> data/
            * not all under VC
            * torque submit scripts
            * input files
        --> results/
                data/*
                plots/
            * things we want to keep and upload to repo
            * under VC
        --> src/ 
            * scripts/programs belonging to this program, single use, etc.
            * under VC
