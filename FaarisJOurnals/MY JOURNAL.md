# MY COMMITMENTS TO THE SCDF TRACKED VEHICLE

### About vehicle
Basically as the head mechanical designer i am tasked to do everything about the chassis and moving parts. To begin, i first designed the main platform to mount the turret and the engine compartment.I split this platform into two, engine platform to hold the "engine compartment" which houses the electronics and turret platform to hold the turret. I ensures that they are in seperate compartments so that any water leakage from the nozzle on the turret wont spill into the electronics compartment. See the photo below

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform1.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform2.PNG" width ="300">

I used a partial V shaped slider to secure both platforms into one rigid object, and secured them to the chassis of the tank with M10 screw and nut

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform5.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform6.PNG" width ="300">

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform4.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform3.PNG" width ="300">

Next i move on the "engine compartment". I designed rather large compartment to easily store the electronics component, which is easily accesible with a sliding lid on top. See the photos below

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineCompartment1.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineCompartment2.PNG" width ="300">

Much like the engine platform, i also used a V shaped slider to secure my engine compartment and the platform, and with an additional 5.8 diameter bolt and nut to further secure it to ensure its rigidity

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineCompartment3.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineComaprtment4.PNG" width ="300">

As for the lid its tight fit

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineCompartment5.PNG" width ="300">

Next ill shall move on to the turret. A servo rest inside the turret platform, and the turret ring is secured to the servo with a screw which holds the turret ring between the head of the screw and the servo. Do note theres a thread inside the servo head which can be screwed into

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret1.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret2.PNG" width ="300">

Next the z axis servo holder is placed into one of the turret ring's pin slot. I added a small out facing pillar so that the servo holder does not fall right through the pin slot

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret3.PNG" width ="300"><img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret4.PNG" width ="300">

Next i we insert the servo, followed by the modular mount and screw to secure them together

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret5.PNG" width ="300"><img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret6.PNG" width ="300">

The modular mount has two V shaped slider to mount multiples types of accessories.That would be the fpv camera or the nozzle for the water spray. If there are any other mods we want to put we just need to design a V shaped mount on it. See the photos

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret7.PNG" width ="300"><img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret8.PNG" width ="300">

Notice the V shape slider

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret9.PNG" width ="300">


Having my own 3D printer at home, i needed to check for the dimensional tolerances of my prints.Therefore i printed sectioned parts of the actual print for testing. I found out that my printer would need an offset of 0.2mm for a nice fitting between a pair of sliders.Here are some of the test prints

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/TestPrint1.jfif" width ="300">

### Motor calculations
##### Find Total Weight
L298N motor driver=26g
FS5106B servo motor=40.0 g x 2 = 80g
3D printed base,engine cover and turret estimated weight:500g
Main chassis and motors combined:620g
Estimated total screws weight(M10,M5,and other screws):50g
Batteries:80g
ESP32:10g
pca9685:5.5g
water pump: 50g
Estimate wires:50g
TOTAL WEIGHT : 1471.5 grams (3.24LBs)

##### Determine Vmax and acceleration
V max = rpm x 2 x Pi x radius 
           = 30 x 2 x 3.1459 x 0.0255m
           =  4.807m/min
           =  0.0801m/s (0.263ft/s)
Acceleration = Vmax / 3s **Where does the 3 seconds come from??
                     = 1.05 / 3
                     = 0.35 m/s2 (1.15 ft/s2)

##### Step One: Determine Rolling Resistance
Rolling Resistance (RR) is the force necessary to propel a vehicle over a particular surface. The worst possible surface type to be encountered by the vehicle should be factored into the equation. 
RR [lb] = WGV [lb] x Crr [-] where:
 RR = rolling resistance [lb]
 WGV = gross vehicle weight [lb] 
Csf = surface friction coeff. (value from Table 1) 

RR = 3.24 x 0.015 (fair concrete) = 0.0486lbs (0.22N)

##### Step Two: Determine Grade Resistance 
Grade Resistance (GR) is the amount of force necessary to move a vehicle up a slope or grade. This calculation must be made using the maximum angle or grade the vehicle will be expected to climb in normal operation. To convert incline angle, α, to grade resistance: 
GR [lb] = WGV [lb] x sin(α) where: GR = grade resistance [lb] 
WGV = gross vehicle weight [lb] 
α = maximum incline angle [degrees]

GR = 3.24 lb x sin(45) = 2.29 lb (10.19N) 

##### Step Three: Determine Acceleration Force
Acceleration Force (Fa) is the force necessary to accelerate from a stop to maximum speed in a desired time. 
Fa [lb] = WGV [lb] x Vmax [ft/s] / (32.2 [ft/s2 ] x ta [s]) where:
 Fa = acceleration force [lb] 
WGV = gross vehicle weight [lb] 
Vmax = maximum speed [ft/s] 
ta = time required to achieve maximum speed [s]

Fa = 3.24 lbs x 0.263 ft/s / (32.2 ft/s2 x 1 s) = 0.0265lb (0.12N)

##### Step Four: Determine Total Tractive Effort 
The Total Tractive Effort (TTE) is the sum of the forces calculated in steps 1, 2, and 3. (On higher speed vehicles friction in drive components may warrant the addition of 10%-15% to the total tractive effort to ensure acceptable vehicle performance.) 
TTE [lb] = RR [lb] + GR [lb] + FA [lb] 
 TTE = 0.0486lbs (0.22N) + 2.29 lb (10.19N) + 0.0265lb (0.12N) = 2.365lb(10.53N)
 
 ##### Step Five: Determine Wheel Motor Torque 
 To verify the vehicle will perform as designed in regards to tractive effort and acceleration, it is necessary to calculate the required wheel torque (Tw) based on the tractive effort.  
Tw [lb-in] = TTE [lb] x Rw [in] x RF [-] where:
 Tw = wheel torque [lb-in] 
TTE = total tractive effort [lb] 
Rw = radius of the wheel/tire [in] 
RF = resistance factor [-] 

Tw = 2.365lb x 1 in(25.5mm) x 1.1 = 2.6015 lb-in (0.2939Nm)

##### CONCLUSION
As we can see , the cumulative max torque of our two motors:
10 kg.cm x 2 = 20 kg.cm(1.96Nm)
is sufficient for our tracked vehicle’s need of   0.2939Nm