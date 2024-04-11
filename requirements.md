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
 <pre><code class="language-mermaid">graph TD
	 **H1.** Collisions with physical obstacles damaging the robot, equipment, and dispersing radioactive material--&gt;
	 **SF 1** Prevent collision--&gt;
	 **R1** The robot shall avoid physical obstacles--&gt;
	 **R1.1** The robot shall maintain a safe distance from obstacles--&gt;
	 **R1.1.1** The robot shall have an emergency stop mechanism that activates when an obstacle is detected within a critical range of distance
	 **R1.1** The robot shall maintain a safe distance from obstacles--&gt;
	 **R1.1.2** The robot shall return to the initial position when an obstacle is detected within a defined range of distance
</code></pre>

	
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

