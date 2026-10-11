# Anthropomorphic-Robotic-Hand
Mechanical architecture for an anthropomorphic robotic hand built at Georgia Tech for prosthetic research. Packaged miniature DC actuators within an anatomical palm envelope, optimized multi-link finger kinematics, and integrated a 2-DOF opposable thumb. Validated fits via SLA/FDM prototyping for clinical amputee grasp evaluations.


##                        …  

<p align="center">
  <img src="./Images/updatesInProgress.svg" alt="Portfolio Updates in Progress" />
</p>


# Anthropomorphic Prosthetic Hand

<p align="center">
  <img src="Images/limbohand.png" width="70%"><br>
  <em>Figure 1: Fully Integrated Prosthetic Hand Assembly and Kinematic Model</em>
</p>

## GT Medical Robotics Club Team Limbo, Mechanical Lead

Team Limbo developed a low-cost biomechatronic prosthetic hand for trans-radial amputees. The goal was to build a functional, 5-digit underactuated terminal device that restores grasping capabilities without the high cost of commercial medical devices.

<p align="center">
  <img src="Images/fusion360_cad_digits.png" width="65%"><br>
  <em>Figure 2: Parametric Digit Kinematics and Internal Palm Routing in Autodesk Fusion 360</em>
</p>

As the Mechanical Lead, I owned the mechanical architecture, CAD modeling, physical prototyping, and sensor integration. I also worked with our controls team to validate the hardware for clinical testing with amputee participants. Key contributions include:

### Parametric Modeling and Modular Digits
I modeled the full hand assembly in Autodesk Fusion 360 with parametric clearance fits for smooth cable movement. The fingers were designed as modular units that pin directly into slots on the palm chassis. This setup lets us swap out a broken finger in under two minutes without taking apart the actuator carriage. I also added internal pockets in the fingertips to house custom slip and force-sensing boards flush with the grip pads.

<table align="center" width="100%">
  <tr>
    <td align="center" width="50%">
      <img src="Images/differential_wrist.png" width="100%"><br>
      <em>3D-Printed Differential Bevel Wrist</em>
    </td>
    <td align="center" width="50%">
      <img src="Images/machined_gearbox.png" width="100%"><br>
      <em>CNC-Milled Aluminum Worm Transmission</em>
    </td>
  </tr>
</table>
<p align="center"><em>Figure 3: Mechanism Exploration: 3D-Printed Differential Wrist (Left) and Machined Worm Transmission (Right)</em></p>

### Kinematic Synthesis and Transmission Exploration
I explored different transmission options to balance torque and packaging size. I designed a 3D-printed differential bevel-gear wrist unit that gives coupled 2-DOF pitch and roll articulation in a small footprint. To evaluate high-reduction holding torque, I also machined a test gearbox from 6061-T6 aluminum using a goBILDA planetary motor and a bronze worm gear set. This helped us evaluate non-backdrivable gear behavior and establish bearing fit tolerances.

<table align="center" width="100%">
  <tr>
    <td align="center" width="50%">
      <img src="Images/fdm_scale_hand.png" width="100%"><br>
      <em>FDM Anatomical Scale Model</em>
    </td>
    <td align="center" width="50%">
      <img src="Images/palm_actuator_layout.png" width="100%"><br>
      <em>Palm Actuator Assembly & Channeled Routing Layout</em>
    </td>
  </tr>
</table>
<p align="center"><em>Figure 4: Prototyping Evolution: FDM Scale Model (Left) and Palm Actuator Assembly Layout (Right)</em></p>

### Iterative Prototyping and Tendon Routing
I iterated through several desktop FDM prints to check scale against real hands and dial in joint clearances. The palm chassis packages five linear DC actuators in a compact staggered layout. I routed internal low-friction tendon channels with Delrin fairlead inserts. This kept the cables from fraying, cut down on line friction, and ensured smooth finger return.

<table align="center" width="100%">
  <tr>
    <td align="center" width="50%">
      <img src="Images/glove_teleoperation.gif" width="100%"><br>
      <em>Sensor Glove Teleoperation Test</em>
    </td>
    <td align="center" width="50%">
      <img src="Images/forearm_emg_testing.png" width="100%"><br>
      <em>Forearm Surface EMG Data Acquisition</em>
    </td>
  </tr>
</table>
<p align="center"><em>Figure 5: Control Verification: Animated Sensor Glove Teleoperation (Left) and Forearm Surface EMG Testing (Right)</em></p>

### Control Integration, Endurance Testing, and Clinical Trials
We validated the hand across multiple testing pipelines. First, I used a flex-sensor data glove to teleoperate the hand in real time and verify finger curling speeds. Next, we integrated the hardware with our forearm surface EMG setup. Our software team used an LSTM model to classify muscle signals into open and close states. I then ran an automated fatigue test on a microcontroller dyno rig, completing over 42,000 continuous grasp cycles without cable or joint failure. The finished device transitioned into trials with amputee participants to evaluate real-world grasping tasks.
