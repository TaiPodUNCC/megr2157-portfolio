# A3: Parametric and FEA
The purpose of this project was to design a beam within certain specifications to support a tension load. The beam must have a circular cross sectional area, be made from Aluminum with a Young's Modulus between 8.5x10^6 and 11.5x10^6 psi, have a maximum axial deflection of .009 in, and be exposed to a tension load between 300 and 500 lbf.

<img width="534" height="154" alt="Screenshot 2026-09-08 at 12 46 51 AM" src="https://github.com/user-attachments/assets/a779936c-1351-40d2-978f-3a470fce1109" />

# Part 1:
After listing all known values I began by intuitively choosing values for outside wall diameter and wall thickness per instructions. I initial chose arbitrary values of 3in and .25in knowing they could be changed at any time. With these values I calculated cross sectional area using formula A=(pi/4)(Do^2-Di^2) resulting in a value of 2.1598in^2. I then used cross sectional area to find the required length using the direct tension elongation equation found in the Machinery's Handbook. In this equation I used the minimum Young's Modulus within the range resulting in a value of 413.0703in or 34.4225ft. Initially I considered changing my chosen cross sectional area as this length was greater than expected, however, considering the application of this beam was never specified in the problem, I saw no reason to concluded that a length of 34 feet was not reasonable. Finally I found the specific weight of Aluminum from an online source and calculated weight using formula W=y*A*L resulting in a value of approximately 87 pounds.

<img width="587" height="727" alt="Screenshot 2026-09-08 at 1 00 27 AM" src="https://github.com/user-attachments/assets/053280c2-50a9-495c-8fe6-d6c0026c570f" />

At this point I was ready to model my beam using solid works. I began by changing the unit system to IPS and inputing all of my variables into solid works for later reference. Units such as psi and lbf were not available causing me to leave some entries without defined units. The equations implemented through solid works mirrored the work I completed on paper

<img width="924" height="449" alt="Screenshot 2026-09-08 at 1 08 23 AM" src="https://github.com/user-attachments/assets/d9943c77-0e59-4513-b0c1-e9b86edfd954" />

Next I created a new sketch, and drew two concentric circles about the origin. I then assigned their dimensions to reflect the inner and outer diameters of my beam's cross sectional area. I then extruded the sketch to the calculated beam length of 413.07in.

<img width="507" height="483" alt="Screenshot 2026-09-08 at 1 13 47 AM" src="https://github.com/user-attachments/assets/eb837172-0919-4b0e-8375-8b18d0e3aab1" />

<img width="838" height="597" alt="Screenshot 2026-09-08 at 1 14 46 AM" src="https://github.com/user-attachments/assets/3bd38649-9bd3-4aea-8d0e-5cb5754bf2a3" />

Solid works did not have an aluminum alloy preset that possessed the required young's modulus. To account for this I created a custom material with properties identical 1060 Aluminum except for the corrected young's modulus. English units were not available for the material properties so I converted psi to N/m^2 before submitting.

<img width="927" height="692" alt="Screenshot 2026-09-08 at 1 21 50 AM" src="https://github.com/user-attachments/assets/52feaa6c-b163-4381-8407-5a73b3052947" />



