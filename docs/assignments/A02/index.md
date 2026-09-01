# A2 – Truss Stress Analysis
For this assignment we were tasked with designing a lightweight truss within specifications to support a given load.
<img width="573" height="307" alt="Screenshot 2026-09-01 at 2 22 55 AM" src="https://github.com/user-attachments/assets/5ced1904-4a3f-437f-9a7a-3405e29a122f" />

In addition to these dimensions the truss was to be constructed out of A500 structural steel, with all beams having the same cross sectional area and all pins being identical.

  
After arbitrarily deciding on a P value of 20kN, I began designing my truss. My initial design ultimately became my final design as its triangular structure is optimal for supporting vertical loads. After completing my sketch, I created a free body diagram to determine the external forces. I removed the internal beams, leaving only the outside structure, and added the two loads and reaction forces at connections. I made an error at this step, as I modeled a force in the x direction instead of the y for the roller support. I noticed this mistake later on in project causing me to have to redo much of my work. After completing the free body diagram I applied static equilibrium and determined the direction and magnitude of forces Ax, Ay, and By.

<img width="439" height="690" alt="Screenshot 2026-09-01 at 4 38 56 AM" src="https://github.com/user-attachments/assets/36fb6366-a39a-49d1-a15c-d4a75b195543" />

Before calculating the internal forces, I found the lengths of all beams involved in the truss. They were found by applying pythagoream theorem to the already defined dimensions. This helped with finding the angle phi for later calculations

<img width="676" height="721" alt="Screenshot 2026-09-01 at 4 40 21 AM" src="https://github.com/user-attachments/assets/67646919-f425-4bd0-81f9-10a4b28d26a7" />

I found the internal forces by applying the joint method. For each joint I created a free body diagram, and utilized component vectors to applicable forces allowing me to apply static equilibrium in the x and y directions to find the magnitude of each force. I had some trouble with this part due to using the wrong sign conventions leading to me mislabelling tension and compression forces. I resolved this by checking each equation multiple times.After finding all internal forces, I determined the force of highest magnitude to use in determining the minimum cross sectional area for my beams.

<img width="506" height="692" alt="Screenshot 2026-09-01 at 4 42 21 AM" src="https://github.com/user-attachments/assets/4dec781a-31a6-4e4c-bbc5-7746e462182f" />

<img width="557" height="718" alt="Screenshot 2026-09-01 at 4 42 59 AM" src="https://github.com/user-attachments/assets/c4089910-b721-4cda-9cd5-6a1a49e18ea1" />

Next I used the internet to find the yield strength of our assigned material and, along with a safety factor of 4 and the greatest internal force reaction found in the last part, applied the formula Amin=N|Fmax|/σᵧ to find the minimum area. I then found the volume of the truss by multiplying the cross section aria by each beams length and multiplied it by the density of steel to find the mass of the truss. Multiplying this value by the acceleration due to gravity gave the truss's weight.

<img width="830" height="674" alt="Screenshot 2026-09-01 at 4 46 50 AM" src="https://github.com/user-attachments/assets/7a11ba88-780b-441e-811b-1cc0d95aaab0" />

After determining the joint under the greatest stress was joint D in the previous step, I then found pin shear by combining the forces acting on joint D. I then used this figure to determine the minimum cross sectional area required by the pin.

<img width="606" height="702" alt="Screenshot 2026-09-01 at 4 48 38 AM" src="https://github.com/user-attachments/assets/95487b6c-ee9e-4e63-acab-246fef1a7b2d" />


