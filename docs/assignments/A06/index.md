# A6: Bracket Drawing Part 1

# Problem Overview:
This project was a continuation of the previous project (A5). We were tasked with taking the parametric calculations found through either stress or stiffness analysis and apply their respective values to a 3d model and drawing of our bracket design.

# Initial Set up:
The first step was to decide whether to use the dimensions found through stress analysis or stiffness analysis. I ultimately decided on my stress model due to it having generally slightly thicker dimensions giving my bracket a stronger constitution. After choosing, I took my sketch from the previous project and labeled the dimensions I intended on adding as global variables in Solid Works. At this point I felt ready to begin creating my 3d model

<img width="542" height="676" alt="Screenshot 2026-09-28 at 9 40 02 PM" src="https://github.com/user-attachments/assets/7cc06376-0b5b-490d-aebf-e67bdc3b1551" />

# Global Variables:
After opening Solid Works I changed the unit system to IPS, to ensure the units for my dimensions remained in inches. Next I opened the equations box and began creating my global variables. After referencing project A5, I added all known variables or constants used in the parametric equations as well as the formula for max stress which was rounded by Solid Works to a value about 4 psi greater than what was used in my hand calculations. Next, I added all the labeled dimensions from my A5 sketch by plugging in the equations used to initially calculate them. At this stage I realized I had made in error in the dimensions labeled "b" in my A5 calculations, causing me to correct this mistake getting a value half of its initial magnitude.

<img width="510" height="296" alt="Screenshot 2026-09-28 at 9 51 40 PM" src="https://github.com/user-attachments/assets/e50af2bc-3702-4a07-9bf0-c2c40bd9c8b9" />
