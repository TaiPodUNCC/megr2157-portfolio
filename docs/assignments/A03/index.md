# A3: Parametric and FEA
The purpose of this project was to design a beam within certain specifications to support a tension load. The beam must have a circular cross sectional area, be made from Aluminum with a Young's Modulus between 8.5x10^6 and 11.5x10^6 psi, have a maximum axial deflection of .009 in, and be exposed to a tension load between 300 and 500 lbf.

<img width="534" height="154" alt="Screenshot 2026-09-08 at 12 46 51 AM" src="https://github.com/user-attachments/assets/a779936c-1351-40d2-978f-3a470fce1109" />

# Part 1:
After listing all known values I began by intuitively choosing values for outside wall diameter and wall thickness per instructions. I initial chose arbitrary values of 3in and .25in knowing they could be changed at any time. With these values I calculated cross sectional area using formula A=(pi/4)(Do^2-Di^2) resulting in a value of 2.1598in^2. I then used cross sectional area to find the required length using the direct tension elongation equation found in the Machinery's Handbook. In this equation I used the minimum Young's Modulus within the range resulting in a value of 413.0703in or 34.4225ft. Initially I considered changing my chosen cross sectional area as this length was greater than expected, however, considering the application of this beam was never specified in the problem, I saw no reason to concluded that a length of 34 feet was not reasonable. Finally I found the specific weight of Aluminum from an online source and calculated weight using formula W=y*A*L resulting in a value of approximately 87 pounds.

<img width="587" height="727" alt="Screenshot 2026-09-08 at 1 00 27 AM" src="https://github.com/user-attachments/assets/053280c2-50a9-495c-8fe6-d6c0026c570f" />

At this point I was ready to model my beam using solid works. I began by changing the unit system to IPS and inputing all of my variables into solid works for later reference. Units such as psi and lbf were not available causing me to leave some entries without defined units.

<img width="924" height="449" alt="Screenshot 2026-09-08 at 1 08 23 AM" src="https://github.com/user-attachments/assets/d9943c77-0e59-4513-b0c1-e9b86edfd954" />


