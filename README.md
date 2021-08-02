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

Day : 1 

Step 1: 

EDA Setup
          I. Install Ng-spice for Transistor level Schematic Design on Ubuntu platform
          II. Install Magic for layout design and parasitic extraction
Ref: https://www.udemy.com/course/vsd-a-complete-guide-to-install-open-source-eda-tools/

Step 2: Check the Ng-spice and Magic tool

     ![magic](https://user-images.githubusercontent.com/52772201/127812103-e9f4a66e-e6e2-4e65-b600-18ab5e7de31b.png)

     ![image](https://user-images.githubusercontent.com/52772201/127812015-97d12721-2462-447d-b44f-ac11931add04.png)
     
    
Step 3: Model parameters are taken from google-skywater 130nm PDK

          ![3](https://user-images.githubusercontent.com/52772201/127812180-446bc87e-247a-4780-af35-23d13d6c3549.png)

Step 4: Make spice_lib folder comprises of TT corner mosfet files and parametrs files for required transistor parametreres.
        ![6](https://user-images.githubusercontent.com/52772201/127812320-6861e308-d83a-4ee0-8076-e24c50a783a0.png)

