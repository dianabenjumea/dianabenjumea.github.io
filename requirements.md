---
layout: page
title: "Requirements Identification and Allocation"
permalink: /RE/requirements/
---

<!DOCTYPE html>
<html lang="en">
   <head>
	 <script src="https://cdnjs.cloudflare.com/ajax/libs/mermaid/8.0.0/mermaid.min.js"></script>
    </head>
	 
<body>

<div class="mermaid">graph TD


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
