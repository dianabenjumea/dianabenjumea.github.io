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

H2(("<b>H2</b> Running out of battery could<br/> leave the robot stranded in<br/> a hazardous area, posing risks<br/> to retrieval personnel and<br/> causing environmental radiation<br/> exposure."));
H3(("<b>H3</b> Power supply issues may<br/> result in reduced operational<br/> time, potentially stranding the<br/> robot in hazardous areas."));
SF2{"<b>SF2</b> PREVENT RUNING<br/> OUT OF POWER."};

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

R2("<b>R2</b>The robot shall maintain<br/> a sufficient power level<br/> throughout the mission.");
R2.1("<b>R2.1</b>The robot shall monitor<br/> its battery level and<br/> activate a recharge process<br/> when it falls below a<br/> predefined threshold.");
R2.3("<b>R2.3</b>The robot shall update<br/> its estimated battery<br/> charge every m minutes<br/> based on both the<br/> current battery sensor<br/> and the robot's history<br/> of activity.");
R2.4("<b>R2.4</b>The robot shall return to<br/> the initial position if<br/> battery levels become<br/> critically low.");
R2.6("<b>R2.6</b>The charging station shall<br/> be selected as the next<br/> destination whenever the recharge<br/> flag is set to true.");
R2.7("<b>R2.7</b>The battery monitor shall<br/> show the battery charge 5%<br/> lower than currently estimated.");
R2.8("<b>R2.8</b>The interface recharge output<br/> shall be set to true<br/> when the current battery<br/> charge is lower than the<br/> battery needed to reach the<br/> charging station from the<br/> current position plus 5%<br/> battery charge.");
R2.9("<b>R2.9</b>Once at the charging station,<br/> the robot shall remain<br/> there until the battery reaches<br/> full charge.");
R2.10("<b>R2.10</b>Each step in the plan<br/> shall not use more than<br/> 1/n amounts of battery.");
        

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
R2 --> R2.3;
R2 --> R2.4;
R2 --> R2.6;
R2 --> R2.7;
R2 --> R2.8;
R2 --> R2.9;
R2 --> R2.10;

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
