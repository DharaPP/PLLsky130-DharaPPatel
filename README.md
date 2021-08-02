Attended 2 –Day silicon ready, tape out oriented workshop on “Phase Locked Loop (PLL) IC Design on Open Source Google Skywater 130nm”

![1](https://user-images.githubusercontent.com/52772201/127811679-ef04fc60-6666-49bb-b045-3f1b889d9391.png)

2 days - Workshop was planned for below tasks:

Day 1: PLL Theory and Lab setup
     1.	Introduction to PLL
     2.	Introduction to Phase Frequency Detector
     3.	Introduction to Charge Pump
     4.	Introduction to VCO and Frequency Divider
    5.	Tool Setup and design flow
    6.	Introduction to PDK, specifications and pre-layout circuits
    7.	Circuit design simulation tool-Ngspice setup
    8.	Layout design tool- Magic Setup
  
Day 2: PLL labs and post-layout simulations
      9.	PLL components circuit design
     10.	PLL components circuit simulations
     11.	Steps to combine PLL sub-circuits and PLL full design Simulations
     12.	Troubleshooting steps
     13.	Layout design
     14.	Layout Walkthrough
     15.	Parasitics extraction
     16.	Post Layout simulations
     17.	Steps to combine layouts
     18.	Tapeout theory
     19.	Tapeout labs

 
Generic block Diagram of PLL:
     ![bd](https://user-images.githubusercontent.com/52772201/127814948-fd84b187-64eb-4227-8f58-5f1917888f78.png)
     
Detailed Block Oriented block diagram of  PLL:

     ![bd1](https://user-images.githubusercontent.com/52772201/127815125-a84e22bf-4c78-4330-87b3-deba11e96ac6.png)

EDA Setup
          I. Install Ng-spice for Transistor level Schematic Design on Ubuntu platform
          II. Install Magic for layout design and parasitic extraction
Ref: https://www.udemy.com/course/vsd-a-complete-guide-to-install-open-source-eda-tools/
Step 2: Check the Ng-spice and Magic tool
       ![magic](https://user-images.githubusercontent.com/52772201/127812103-e9f4a66e-e6e2-4e65-b600-18ab5e7de31b.png)
       ![image](https://user-images.githubusercontent.com/52772201/127812015-97d12721-2462-447d-b44f-ac11931add04.png)
         
Model parameters are taken from google-skywater 130nm PDK

          ![3](https://user-images.githubusercontent.com/52772201/127812180-446bc87e-247a-4780-af35-23d13d6c3549.png)

Make spice_lib folder comprises of TT corner mosfet files and parametrs files for required transistor parametreres. Add in library file.
        ![6](https://user-images.githubusercontent.com/52772201/127812320-6861e308-d83a-4ee0-8076-e24c50a783a0.png)

Frequency Divider (FD) :

Frequency Divide by 2 circuit using inverter and transmission gates.
     ![fd](https://user-images.githubusercontent.com/52772201/127814557-751f48f0-09f7-4a1f-bf07-95180657e05d.png)

![fdcode](https://user-images.githubusercontent.com/52772201/127818956-3e61d792-d9f8-4d25-98cf-83efd90c8475.png)

![7](https://user-images.githubusercontent.com/52772201/127818937-f7db425a-c456-44ce-a3d5-ca9481ab6ee7.png)

Phase Frequency Divider (PFD) 
Finite state diagram tells that UP signal will go high when neg edge of REF is detected till the neg edge of OUT detects. 
DOWN signal sets to one when neg edge of OUT is detected till the neg edge of REF detects.



![Uploading fsm.png…]()
![pfd](https://user-images.githubusercontent.com/52772201/127819229-0ac7b1ee-c866-4971-bf1d-6479140da4cb.png)

![cp](https://user-images.githubusercontent.com/52772201/127814416-0b6bfc0e-30c9-4d52-a0d3-e6584bb8d621.png)


![cpinitial](https://user-images.githubusercontent.com/52772201/127818195-afda7330-c5c6-430f-b6ff-689881495ced.png)

![cpoperation](https://user-images.githubusercontent.com/52772201/127821363-6635b93e-18ad-4f99-9874-6aea19f1457c.png)

![cp](https://user-images.githubusercontent.com/52772201/127821207-06d8023e-25dc-4d52-bd06-56d9f7016ca0.png)



![cpcode](https://user-images.githubusercontent.com/52772201/127817867-5415a035-b73f-4a19-84f5-a727f8115621.png)


![7](https://user-images.githubusercontent.com/52772201/127813888-b56e1a1e-9d1c-4ea7-a871-4481da210fb9.png)

![8](https://user-images.githubusercontent.com/52772201/127813900-36dff8e6-8cdd-4ee5-bac5-d64b6c2869f7.png)

![vcoout](https://user-images.githubusercontent.com/52772201/127818096-29b5bc12-f5b9-4334-ab9a-b4aec7826a1d.png)
![pfdout](https://user-images.githubusercontent.com/52772201/127818309-683d106b-a815-48d9-9254-088631ae3e28.png)




