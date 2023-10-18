# HoogendoornSpliet2024_FullResults
Folder containing the full results regarding experiments for the paper "An evaluation of common modeling choices for the vehicle routing problem with stochastic demands" by Hoogendoorn, and Spliet. This readme explain all files contained in this folder

The .zip file "Jabalietal2014_Instances" contains the instance files of Jabali et al. (2014). We do not own these files and these are published with permission of the owner.

The .zip file "LSG18_Instances" contains the instance files used to reproduce the symmetric instances of Louveaux and Salazar-González (2018). The original CVRP instances E031-09h, E051-05e, E076-07s and E101-08e are contained in their own .dat files. Next to this, each file has four copies, mimicing the settings used in the experiments of Louveaux and Salazar-González (2018). Note that the only thing that changes between settings are the vehicle capacity, which is calculated using the number of vehicles (m) and average fill rate (f), shown in the file name itself. For these files, the demand section should be ignored, as Louveaux and Salazar-González (2018) set the demand distribution to a discrete triangular distribution with mean 5 and half-width 3 or 9.

Next to the .zip files, the repository contains one Excel sheet, in which the full results are detailed. The Excel sheet contains four tabs:
I) Jabali. Contains the results of the instances of Jabali et al. (2014). There are 27 classes of instances with 10 instances each. Each of them is named n_m_f_x, where n is the number of customers (including depot), m is the number of routes, f is the average fill rate (without the decimal point) and x is the instance number (ranging from 0 to 9).

Per instance 4 variants are run, named "VRPSD", "ECC-VRPSD", "FRC-VRPSD" and "Basic-VRPSD". We refer to our paper for the explanation of the variants. Per instance and per variant, we show 
1. Obj: the solution value (either optimal or best-known solution, if unavailable);
3. Time: the time needed to reach optimality, in seconds (or 3600 if the runtime exceeded 1 hour);
2. Gap: the optimality gap after 1 hour of solving (if 0, the found solution is optimal);
4. Nodes: the number of nodes explored in the branch-and-cut tree.

II) LSG18. Contains the results of the symmetric instances of Louveaux and Salazar-González (2018). There are 4 instances, each with 8 different settings, and are named n_m_f_K, where n is the name of the instance, m is the number of routes, f is the average fill rate (without the decimal point) and K is the half-width of the discrete triangular distribution. The table structure is identical as that of the tab "Jabali".

III) Florio. Contains the results of a solvalbe subset of instances of Florio et al. (2022). There are 4 instances, each based on a well-known CVRP benchmark instance of the A, E or P class. The table structure is identical as that of the tab "Jabali".

IV) NegDem. Contains the results regarding the negative demand simulations for the instances of Jabali et al. (2014). There are 27 classes of instances with 10 instances each. Each of them is named n_m_f_x, where n is the number of customers (including depot), m is the number of routes, f is the average fill rate (without the decimal point) and x is the instance number (ranging from 0 to 9).

Per instance 4 variants are considered, names "Norm", "Cens", "Trunc" and "Fold". These refer to the demand distribution assumed: the normal, the censored normal, the truncated normal and the folded normal distribution respectively. For the normal distribution, its optimal or best-known solution value is shown under "Obj" and its corresponding expected costs of recourse under "Rec". For the censored, truncated and folded normal, the we show the simulated objective value under "Obj" and its corresponding expected costs of recourse under "Rec". The solution used is from the normal distribution. An upper bound on the remaining optimality gap is shown under "Gap". We refer to our paper for details.
