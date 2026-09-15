# A4: Motor Mount Project
# Description:
For this assignment we were tasked with designing a motor mount to support a motor with the provided dimensions. Were were given a choice of 3 materials (ABS, PETG, or PLA) and assigned a safety factor of 3. The general design of the mount and forces applied were also provided.

<img width="656" height="201" alt="Screenshot 2026-09-15 at 12 08 43 AM" src="https://github.com/user-attachments/assets/1d6fa03e-a57c-4429-bf46-9c0b3574ffbc" />
<img width="933" height="298" alt="Screenshot 2026-09-15 at 12 09 45 AM" src="https://github.com/user-attachments/assets/482894b8-f660-4841-949d-c40a0e51104c" />

# Initial Setup:
I began by drawing a rough sketch of the 2 features comprising the motor mount. I created this based on the provided initial diagram and the motor dimensions. I  decided that a square shape would be ideal for this project as it simplifies the design while still meeting design requirements. I intuitively decided on length of twice that of the motors diameter and arbitrarily selected ABS as my material.

<img width="792" height="577" alt="Screenshot 2026-09-15 at 12 17 04 AM" src="https://github.com/user-attachments/assets/73d402e3-5da3-4b8f-bec4-0b99d9835b23" />

# Feature 1:
 First I used the ABS property list to find yield strength and youngs modulus and listed my known and unknown values. I used the lower bound for these value to prepare for the worst case scenario. Next I derived the height from the bending stress formula symbolically, and plugged in my known values. I repeated the same process for the deflection formula and selected the greater height of the 2. I made sure to included my safety factor while completing these calculations
 
<img width="576" height="320" alt="Screenshot 2026-09-15 at 12 27 46 AM" src="https://github.com/user-attachments/assets/fa7b9a73-d62f-48b4-ab0a-04c1753f22b2" />
<img width="546" height="694" alt="Screenshot 2026-09-15 at 12 27 09 AM" src="https://github.com/user-attachments/assets/2e92106b-6b35-4616-92e9-671f944bd003" />
<img width="499" height="370" alt="Screenshot 2026-09-15 at 12 25 42 AM" src="https://github.com/user-attachments/assets/2e6350c3-7fc1-486f-bda7-186b773fd5a9" />

# Feature 2:

Since feature 2 is comprised of the same material and has the same outside dimensions as feature 1, the process to find the height was identical after calculating my new moment.

<img width="542" height="651" alt="Screenshot 2026-09-15 at 12 30 38 AM" src="https://github.com/user-attachments/assets/0cbd5936-c3a2-41f7-aaa3-930937b60cd5" />

# Sketch:
Using the final dimensions found in the previous step and the provided motor dimensions I drafted a 3d sketch of my design. 

<img width="412" height="724" alt="Screenshot 2026-09-15 at 12 34 02 AM" src="https://github.com/user-attachments/assets/89df0a19-fcff-46b8-be58-f7d29d278017" />

# CAD Design:
I decided to model my part in Creo Parametric due to my familiarity with the software. I began changing the unit system to meters.

<img width="555" height="655" alt="Screenshot 2026-09-15 at 12 37 42 AM" src="https://github.com/user-attachments/assets/7b1b7553-b058-4f59-8625-aa88667aef06" />

Next I created and extruded a sketch to create a cube with side length .056m.

<img width="528" height="518" alt="Screenshot 2026-09-15 at 12 39 14 AM" src="https://github.com/user-attachments/assets/e66ffce8-f295-41e6-adf8-6074a3e1eb4e" />
<img width="449" height="365" alt="Screenshot 2026-09-15 at 12 39 28 AM" src="https://github.com/user-attachments/assets/d1f67742-79c2-41f5-8f75-e54e33312c20" />

I then extruded again to reveal the faces of my features. I determine the extrude length by subtracting the height of the second feature from the overall side length.

<img width="469" height="447" alt="Screenshot 2026-09-15 at 12 42 27 AM" src="https://github.com/user-attachments/assets/ee3c4c9d-deae-47e8-9486-4ca41dbc8ac2" />

Next I created sketches for each hole on feature 1, and extruded them to their specified lengths.

<img width="487" height="527" alt="Screenshot 2026-09-15 at 12 46 24 AM" src="https://github.com/user-attachments/assets/114405c9-e7ea-4f78-98cf-a9a3331a9362" />
<img width="463" height="418" alt="Screenshot 2026-09-15 at 12 46 10 AM" src="https://github.com/user-attachments/assets/9b07f02d-377d-4c0a-8cb4-2d69798ea7ca" />
<img width="517" height="501" alt="Screenshot 2026-09-15 at 12 45 54 AM" src="https://github.com/user-attachments/assets/8f6f0704-6c7a-4458-812a-1425fd579946" />
<img width="365" height="461" alt="Screenshot 2026-09-15 at 12 45 23 AM" src="https://github.com/user-attachments/assets/8132c074-3d70-4645-8f33-7e187ed06797" />

Finally I repeated the process for feature 2's holes, finalizing my motor mount.

<img width="519" height="597" alt="Screenshot 2026-09-15 at 12 48 41 AM" src="https://github.com/user-attachments/assets/dc9aaa95-7825-4430-a65e-02fa86275088" />
<img width="421" height="460" alt="Screenshot 2026-09-15 at 12 48 55 AM" src="https://github.com/user-attachments/assets/42bc9832-c995-4bea-ad00-72c267a10c9b" />

# Lessons Learned:
This project took me approximately 4.5 hours to complete. In this time I was able to learn how to apply parametric equations within a design process. It also allowed me to reinforce concepts learned in previous classes.

[https://raw.githubusercontent.com/TaiPodUNCC/megr2157-portfolio/blob/main/a4_motor_mount.prt.1
](https://github.com/TaiPodUNCC/megr2157-portfolio/raw/refs/heads/main/a4_motor_mount.prt.1)


