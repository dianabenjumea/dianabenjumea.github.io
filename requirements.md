---
layout: page
title: "Requirements Identification and Allocation"
permalink: /RE/requirements/
---
<html lang="en">
   <head>
	 <script src="https://cdnjs.cloudflare.com/ajax/libs/mermaid/8.0.0/mermaid.min.js"></script>
    </head>
	 
<body>

<div class="mermaid">graph TD

Description["<b>AN AUTONOMOUS ROBOT IS TASKED WITH PERFORMING REGULAR INSPECTIONS OF A NUCLEAR ROOM, WITH THE PRIMARY OBJECTIVE BEING THE CAPTURE OF HIGH-QUALITY IMAGES OF FIVE SPECIFIC LOCATIONS FOR SUBSEQUENT ANALYSIS AND ASSESSMENT. </b>"];

H1(("<b>H1</b> Collisions with physical obstacles<br/> damaging the robot, equipment, and<br/> dispersing radioactive material."));
SF1{"<b>SF1</b> PREVENT COLLISION."};
R1("<b>R1</b> The robot shall avoid<br/> physical obstacles.");
R1.1("<b>R1.1</b> The robot shall maintain<br/> a safe distance from obstacles.");
R1.1.1("<b>R1.1.1</b> The robot shall have an<br/> emergency stop mechanism that<br/> activates when an obstacle is<br/> detected within a critical range<br/> of distance.");
R1.1.2("<b>R1.1.2</b> The robot shall return<br/> to the initial position when an<br/> obstacle is detected within a <br/> defined range of distance.");
R1.2("<b>R1.2</b> Initial robot position<br/> shall be obstacle-free.");
R1.3("<b>R1.3</b> Current robot position<br/> shall be accurate.");
R1.4("<b>R1.4</b> The vision subsystem shall confirm<br/> that the robot's initial recognised<br/> position matches the predefined<br/> starting position.");
R1.5("<b>R1.5</b> The vision subsystem shall report<br/> that the current position is not a<br/> position with an obstacle.");
R1.6("<b>R1.6</b> The path to the next destination<br/> shall be calculated from the current<br/> robot position that the robot believes<br/> its location to be.");
R1.7("<b>R1.7</b> All obstacles shall be correctly<br/> identified.");
R1.8("<b>R1.8</b> An obstacle shall not be in the same<br/> location as an inspection point.");
R1.9("<b>R1.9</b> The calculated path to the destination<br/> shall not include a location with an<br/> obstacle.");
R1.10("<b>R1.10</b> The robot shall not go faster than X<br/> kmph.");


H2(("<b>H2</b> Running out of battery could<br/> leave the robot stranded in<br/> a hazardous area, posing risks<br/> to retrieval personnel and<br/> causing environmental radiation<br/> exposure."));
H3(("<b>H3</b> Power supply issues may<br/> result in reduced operational<br/> time, potentially stranding the<br/> robot in hazardous areas."));
SF2{"<b>SF2</b> PREVENT RUNING<br/> OUT OF POWER."};
R2("<b>R2</b> The robot shall maintain<br/> a sufficient power level<br/> throughout the mission.");
R2.1("<b>R2.1</b> The robot shall monitor<br/> its battery level and<br/> activate a recharge process<br/> when it falls below a<br/> predefined threshold.");
R2.2("<b>R2.2</b> The robot shall update<br/> its estimated battery<br/> charge every m minutes<br/> based on both the<br/> current battery sensor<br/> and the robot's history<br/> of activity.");
R2.3("<b>R2.3</b> The robot shall return to<br/> the initial position if<br/> battery levels become<br/> critically low.");
R2.4("<b>R2.4</b> The charging station shall<br/> be selected as the next<br/> destination whenever the recharge<br/> flag is set to true.");
R2.5("<b>R2.5</b> The battery monitor shall<br/> show the battery charge 5%<br/> lower than currently estimated.");
R2.6("<b>R2.6</b> The interface recharge output<br/> shall be set to true<br/> when the current battery<br/> charge is lower than the<br/> battery needed to reach the<br/> charging station from the<br/> current position plus 5%<br/> battery charge.");
R2.7("<b>R2.7</b> Once at the charging station,<br/> the robot shall remain<br/> there until the battery reaches<br/> full charge.");
R2.8("<b>R2.8</b> Each step in the plan<br/> shall not use more than<br/> 1/n amounts of battery.");


H4(("<b>H4</b> Radioactive contamination from<br/> particles adhering to surfaces,<br/> equipment,and personnel, leading to<br/>contamination spread and an increased<br/>risk of radiation exposure."));
H5(("<b>H5</b> Contaminated equipment and<br/> personnel due to robot manual<br/> retrieval in hazardous environments."));
SF3{"<b>SF3</b> PREVENT THE ROBOT FROM<br/>BEING EXPOSED TO EXCESSIVELY<br/>HIGH LEVELS OF RADIATION."};
R3("<b>R3</b> The robot and personnel<br/>shall be protected from<br/>harmful radiation exposure.");
R3.1("<b>R3.1</b> The robot shall continually<br/>monitor radiation levels<br/>in its environment.");
R3.2("<b>R3.2</b> Initial robot position shall<br/>not be a location with<br/>out-of-range radiation levels.");
R3.3("<b>R3.3</b> The radiation monitor subsystem<br/>shall ensure that the initial<br/>robot measurement is equal<br/>to the manual set level.");
R3.4("<b>R3.4</b> The radiation monitor subsystem<br/>shall ensure that the current<br/>position is not a position<br/>with out-of-range radiation<br/>levels.");
R3.4.1("<b>R3.4.1</b> If radiation levels have<br/> exceeded, the robot shall<br/> go tothe exit immediately.");
R3.5("<b>R3.5</b> Room radiation levels shall<br/>be correctly identified.");
R3.6("<b>R3.6</b> The radiation level at<br/>the inspection points<br/>shall be within acceptable<br/>ranges.");
R3.7("<b>R3.7</b> The calculated path to<br/>the destination shall not<br/>include a location with<br/>out-of-range radiation<br/>levels.");
R3.8("<b>R3.8</b> Radiation levels<br/>shall be under R.");
R3.9("<b>R3.9</b> The robot shall perform<br/>regular checks on its<br/>equipment's performance and<br/>return to the initial<br/>position if anomalies<br/>are detected.");
R3.10("<b>R3.10</b> The robot shall undergo<br/>thorough decontamination<br/>procedures before and<br/>after each mission.");



Description --> H1;
H1 --> SF1;
SF1 --> R1;
R1 --> R1.1;
R1.1 --> R1.1.1;
R1.1 --> R1.1.2;
R1 --> R1.2;
R1 --> R1.3;
R1 --> R1.4;
R1 --> R1.5;
R1 --> R1.6;
R1 --> R1.7;
R1 --> R1.8;
R1 --> R1.9;
R1 --> R1.10;

Description --> H2;
Description --> H3;
H2 --> SF2;
H3 --> SF2;
SF2 --> R2;
R2 --> R2.1;
R2 --> R2.2;
R2 --> R2.3;
R2 --> R2.4;
R2 --> R2.5;
R2 --> R2.6;
R2 --> R2.7;
R2 --> R2.8;


Description --> H4;
Description --> H5; 
H4 --> SF3;
H5 --> SF3;
SF3 --> R3;
R3 --> R3.1;
R3 --> R3.2;
R3 --> R3.3;
R3 --> R3.4;
R3.4 --> R3.4.1;
R3 --> R3.5;
R3 --> R3.6;
R3 --> R3.7;
R3 --> R3.8;
R3 --> R3.9;
R3 --> R3.10;

</div>

	
</body>
<script>
var config = {
    startOnLoad:true,
    theme: 'forest',
    flowchart:{
            useMaxWidth:false,
            htmlLabels:true
        }
};
mermaid.initialize(config);
window.mermaid.init(undefined, document.querySelectorAll('.language-mermaid'));
</script>

</html>
