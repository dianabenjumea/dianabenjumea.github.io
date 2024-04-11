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

1(("<b>H1</b> Collisions with physical obstacles<br/>
damaging the robot, equipment, and<br/>
dispersing radioactive material.")) --> 2{"<b>SF1</b> PREVENT COLLISION."};
2 --> 3("<b>R1</b> The robot shall avoid<br/>
physical obstacles.");
3 --> 4("<b>R1.1</b> The robot shall maintain<br/>
a safe distance from obstacles.");
4 --> 5("<b>R1.1.1</b> The robot shall have<br/>
an emergency stop mechanism that<br/>
activates when an obstacle is<br/>
detected within a critical<br/>
range of distance.");
4 --> 7("<b>R1.1.2</b> The robot shall<br/>
return to the initial position<br/>
when an obstacle is detected<br/>
within a defined range of distance.")

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
