# A6: Bracket Drawing Part 1

# Problem Overview:
This project was a continuation of the previous project (A5). We were tasked with taking the parametric calculations found through either stress or stiffness analysis and apply their respective values to a 3d model and drawing of our bracket design.

# Initial Set up:
The first step was to decide whether to use the dimensions found through stress analysis or stiffness analysis. I ultimately decided on my stress model due to it having generally slightly thicker dimensions giving my bracket a stronger constitution. After choosing, I took my sketch from the previous project and labeled the dimensions I intended on adding as global variables in Solid Works. At this point I felt ready to begin creating my 3d model

<img width="542" height="676" alt="Screenshot 2026-09-28 at 9 40 02 PM" src="https://github.com/user-attachments/assets/7cc06376-0b5b-490d-aebf-e67bdc3b1551" />

# Global Variables:
After opening Solid Works I changed the unit system to IPS, to ensure the units for my dimensions remained in inches. Next I opened the equations box and began creating my global variables. After referencing project A5, I added all known variables or constants used in the parametric equations as well as the formula for max stress which was rounded by Solid Works to a value about 4 psi greater than what was used in my hand calculations. Next, I added all the labeled dimensions from my A5 sketch by plugging in the equations used to initially calculate them. At this stage I realized I had made in error in the dimensions labeled "b" in my A5 calculations, causing me to correct this mistake getting a value half of its initial magnitude.

<img width="510" height="296" alt="Screenshot 2026-09-28 at 9 51 40 PM" src="https://github.com/user-attachments/assets/e50af2bc-3702-4a07-9bf0-c2c40bd9c8b9" />

# Solid Works Model:
I began creating my model by deciding whether or not I wanted to make each feature its own part. I decided on making the entire bracket as a single part and making each feature its own sketch to avoid having to create an assembly. I started with feature B, then continued on with A, C, D, and E respectively. Despite the sketches requiring a greater number of dimensions to be defined compared to the global variables I entered, I did not manually enter a single one. I accomplished this by manipulating the defined global variables by adding or subtracting from each other. During this stage I made the mistake of accidentally using the wrong variable without realizing causing me to waste nearly an hour searching for my error. Once my part was finished I surprised to see how differently my part looked compared to my initial sketch due to its dimensions not being drawn to scale.


<img width="538" height="485" alt="Screenshot 2026-09-28 at 10 02 11 PM" src="https://github.com/user-attachments/assets/bd3355df-f86f-4e3e-8214-7f222bd680b7" />

<img width="497" height="496" alt="Screenshot 2026-09-28 at 10 02 33 PM" src="https://github.com/user-attachments/assets/7db18477-2d67-432e-832c-cafddd240889" />

<img width="540" height="586" alt="Screenshot 2026-09-28 at 10 02 51 PM" src="https://github.com/user-attachments/assets/46c11b2c-4b3a-4e4f-b216-46f73deaae5e" />

<img width="536" height="570" alt="Screenshot 2026-09-28 at 10 03 07 PM" src="https://github.com/user-attachments/assets/e02851af-71f7-49f9-b0fd-7dcc7a0cd17f" />

<img width="554" height="562" alt="Screenshot 2026-09-28 at 10 03 24 PM" src="https://github.com/user-attachments/assets/f6d4b2d0-651c-4002-af1a-7c2ea707d6d2" />

<img width="446" height="536" alt="Screenshot 2026-09-28 at 10 03 41 PM" src="https://github.com/user-attachments/assets/50ecc715-e15c-4dd2-a8df-cb446ab848d3" />

# Solid Works Drawing
Finally I created my multi view drawing and added front, right, top, and parametric views. I added all necessary dimensions, selected hidden lines to be shown, and added necessary labels, concluding with a copy of the tolerance box specified in the project instructions.

<img width="689" height="533" alt="Screenshot 2026-09-28 at 10 11 08 PM" src="https://github.com/user-attachments/assets/409a6537-49d5-4911-a6ff-7e125e23e5fe" />


