# A9: Pulleys

# Introduction: 
For this assignment we were tasked with designing a simple pulley system with given specifications, to transfer power between two parallel axis.


Pulley Specifications:\
Pulley Diameter: 3in\
Rotational Speed: 1000 RPM\
Belt Tension (Static): 4 lbf\
Pulley Material: Steel\
Safety Factor: 3


Belt Specifications:\
Material: Polyurethane rubber\
Yield strength: 471 psi (20% strain)


# Belt Selection:
I began by creating a sketch of the system and listing all known and unknown variables. Next I drew my free body diagram and related the specified tension to the forces on the loose and tight ends of the pulley. Since the coefficient of friction was not specified I chose a value of .6 as online resources stated a value between .5 and .7 is commonly used in these situations. After calculating both forces I used the stress equation to find the cross sectional area and then the diameter of the belt. Finally I used the pulley diameter and distance between pulleys to calculate the optimal circumference and selected the corresponding belt from the McMaster website.

<img width="497" height="639" alt="Screenshot 2026-11-10 at 5 43 27 AM" src="https://github.com/user-attachments/assets/56c09bee-a948-4e75-81be-54b7075e37ec" />

# Shaft Diameter:
I began by listing all my known and unknown variables. I used online resources to determine my Sy value for the specified material (hardened 1060 steel). After drawing my free body diagram I used the power equation to find power using my calculated forces than related it to torque and rotation speed to find my torque. after incorporating my safety factor I used torque to solve for the required diameter and area.

<img width="479" height="506" alt="Screenshot 2026-11-10 at 6 11 34 AM" src="https://github.com/user-attachments/assets/84432ebd-2ae4-43ad-b99f-144f0218d4d8" />

# Journal Bearing Material Selection:
In order to select my bearing material, I needed to determine the max surface speed and PV limit. I began by listing my known and unknown variables, then drawing my free body diagram. I began by calculating the tangental force using the my determined shaft diameter and torque. I then used this value to find the radial force using the 20 percent strain angle from the specifications. Next, I began calculating pressure. I had some difficulties with this as I was not sure if I was meant to calculate length, choose it arbitrarily, or receive it from the specifications. After going over the directions I concluded that it could not be calculated with the information given so I settled on an arbitrary value of 3in. Using this length, shaft diameter, and radial force I found the pressure. Finally I used rotation speed and shaft diameter to find surface speed and combined it with my pressure to get my PV limit. After checking the material chart I realized I had to change my units and while doing so I applied my safety factor which I had forgotten. Using these values I chose Porous Iron as my material as it exceeded my minimum values.

<img width="667" height="434" alt="Screenshot 2026-11-10 at 6 47 55 AM" src="https://github.com/user-attachments/assets/c72ead24-e5e7-4582-8731-19c874ea1ade" />

<img width="555" height="689" alt="Screenshot 2026-11-10 at 6 47 26 AM" src="https://github.com/user-attachments/assets/9e357f55-6e27-482b-bf73-911cc616b4cf" />





