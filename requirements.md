---
layout: page
title: "Requirements Identification and Allocation"
permalink: /RE/requirements/
---

<div class="mermaid">
  <pre><code>
    flowchart TD;
    1{H1 Collisions with physical obstacles
      damaging the robot, equipment, and
    dispersing radioactive material.} -->
    2[/SF1 PREVENT COLLISION./] --> 3(R1 The robot shall avoid
    physical obstacles.) -->
    4(R1.1 The robot shall maintain
     a safe distance from obstacles.) -->
    5(R1.1.1 The robot shall have
    an emergency stop mechanism that
    activates when an obstacle is
    detected within a critical
    range of distance.)
    4 --> 7(R1.1.2 The robot shall
    return to the initial position
    when an obstacle is detected
    within a defined range of distance.)
  </code></pre>
</div>



