# A7: FEA on Bracket

# Introduction:
For this project we were tasked with using finite element analysis on the bracket part designed and modeled in assignments #5 and #6, to find areas in which we can improve our design. After completing FEA and confirming convergence with finer mesh values, we use the data found to improve our design. this process is to be repeated for two improved designs.

# Setting up:
I began by opening my part file from assignment #6 in Solidworks. I noticed that the material was not already defined so I set it to 6061 t6 aluminum in accordance with previous assignments. Next I started a new FEA study using default settings. After, I created a plane through feature A to be used as a reference when implementing the known forces for the simulation. To acomplish this I created a point at the center of feature A's face and added a plane coincident to it and parallel to the features length.

<img width="427" height="473" alt="Screenshot 2026-10-20 at 3 39 17 PM" src="https://github.com/user-attachments/assets/b8e81855-b4e4-4c2f-8f20-3032af1f821c" />

<img width="530" height="393" alt="Screenshot 2026-10-20 at 3 38 58 PM" src="https://github.com/user-attachments/assets/56339fc6-c16e-4b85-9ae7-07436167021b" />

Next I added fixed geometry to the two surfaces in contact with the bar. This allows Solidworks to incorporate the reaction forces into its analysis. Finally, I created a split line using my new plane and added a 1000 lbf force along the split area.

<img width="473" height="467" alt="Screenshot 2026-10-20 at 4 11 24 PM" src="https://github.com/user-attachments/assets/672fccdc-2074-4062-b45a-0bd7abbd7477" />

<img width="548" height="543" alt="Screenshot 2026-10-20 at 4 11 06 PM" src="https://github.com/user-attachments/assets/a772e4c5-6b0b-4970-b2e5-7af58340e14c" />

# Design 1
I set mesh to default and ran the first iteration. After running I recorded values for max stress, max deflection, factor of safety (with automatic failure criterion), mass, and number of mesh elements. 

<img width="944" height="518" alt="Screenshot 2026-10-20 at 4 47 00 PM" src="https://github.com/user-attachments/assets/ecb80b39-20ba-4455-97f6-9953b6d3c801" />

Next I increased the mesh density to be 75 percent of fine and ran the study again. After running I recorded values for max stress, max deflection, factor of safety (with automatic failure criterion), mass, and number of mesh elements. When checking for convergence using formula 2((xf-xi)/(xi+xf))*100 I found both FOS and ma stress to be greater than 7 percent causing me to try again with iteration 3.


<img width="955" height="494" alt="Screenshot 2026-10-20 at 4 52 23 PM" src="https://github.com/user-attachments/assets/567fb746-7d2e-406e-9eb0-734191182187" />

I increased mesh density to fine and ran the simulation. After running I recorded values for max stress, max deflection, factor of safety (with automatic failure criterion), mass, and number of mesh elements. When checking for convergence using formula 2((xf-xi)/(xi+xf))*100 I found once again convergence was not achieved. Despite this I had enough information to begin my redesign.

<img width="951" height="517" alt="Screenshot 2026-10-20 at 5 09 51 PM" src="https://github.com/user-attachments/assets/7b51a83a-e34a-477f-ab64-06e7fa9bf35c" />

<img width="526" height="160" alt="Screenshot 2026-10-20 at 5 10 38 PM" src="https://github.com/user-attachments/assets/78aa857a-2bdc-42da-908e-83a1e9988947" />

# Design 2:
As the main mode of failure in design 1 was the stress in feature B, I updated my design with a triangular support reinforcing feature B. Also, upon reassessing I determined that I should add fixed geometry to all of the inner surfaces as my design 

<img width="457" height="490" alt="Screenshot 2026-10-20 at 5 55 55 PM" src="https://github.com/user-attachments/assets/cb3ea90d-7f23-49f8-ba77-f2bbf65fdb20" />


