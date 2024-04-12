---
layout: page
title: "Requirements Identification and Allocation"
permalink: /RE/requirementsTable/
---

# Formalising Safety Requirements for Robotic Autonomous Systems in Highly Regulated Domains

This document consolidates the identification and allocation of mitigation requirements for hazards associated with a hypothetical operation involving routine inspections in a nuclear facility — a critical scenario for the operational integrity of nuclear plants. The operation involves regular inspections in a space containing radioactive material, with the primary objective of capturing high-quality images for analysis and assessment. This document includes parent and child requirements, grouping associated requirements, and the allocation of these requirements to systems, the rules-based reasoning **Safety System** (SS) and the **Safety Related Autonomous System** (SRAS).

**Note.** The acronyms used for the requirement groups are:

- **SR:** Safety Requirements
- **PGPR:** Standards and Relevant Good Practice Requirements
- **OR:** Operational Requirements



<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<body>
<table>

<tr>
<th>Source</th>
<th>Safety Function</th>
<th>Requirement</th>
<th>Group</th>
<th>System</th>

</thead>
<tbody>
<tr>
<td rowspan="20"><b>H1</b>. Collisions with physical obstacles damaging the robot, equipment, and dispersing radioactive material.</td>
<td rowspan="20"><b>SF 1</b> Prevent collision</td>
<td><b>R1</b> The robot shall avoid physical obstacles.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.1</b> The robot shall maintain a safe distance from obstacles.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.1.1</b> The robot shall have an emergency stop mechanism that activates when an obstacle is detected within a critical range of distance.</td>
<td>SR</td>
<td><b>SS</b></td>
<tr>
<td><b>R1.1.2</b> The robot shall return to the initial position when an obstacle is detected within a defined range of distance.</td>
<td>SR</td>
<td><b>SS</b></td>

<tr>
<td><b>R1.2</b> Initial robot position shall be obstacle-free.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.3</b> Current robot position shall be accurate.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.4</b> The vision subsystem shall confirm that the robot's initial recognised position matches the predefined starting position.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.5</b> The vision subsystem shall report that the current position is not a position with an obstacle.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.6</b> The path to the next destination shall be calculated from the current robot position that the robot believes its location to be.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.7</b> All obstacles shall be correctly identified.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.8</b> An obstacle shall not be in the same location as an inspection point.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.9</b> The calculated path to the destination shall not include a location with an obstacle.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R1.10</b> The robot shall not go faster than X kmph.</td>
<td>RGPR</td>
<td>SRAS</td>

<tbody>
<td rowspan="15"><b>H2</b>. Running out of battery could leave the robot stranded in a hazardous area, posing risks to retrieval personnel and causing environmental radiation exposure.<br><br><b>H3</b>. Power supply issues may result in reduced operational time, potentially stranding the robot in hazardous areas.</td>
<td rowspan="15"><b>SF 2</b> Prevent running out of power</td>
<td><b>R2</b> The robot shall maintain a sufficient power level throughout the mission.</td>
<td>OR</td>
<td>SRAS</td>

<tr>
<td><b>R2.1</b> The robot shall monitor its battery level and activate a recharge process when it falls below a predefined threshold.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R2.3</b> The robot shall update its estimated battery charge every m minutes based on both the current battery sensor and the robot's history of activity.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R2.4</b> The robot shall return to the initial position if battery levels become critically low.</td>
<td>SR</td>
<td><b>SS</b></td>

<tr>
<td><b>R2.6</b> The charging station shall be selected as the next destination whenever the recharge flag is set to true.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R2.7</b> The battery monitor shall show the battery charge 5% lower than currently estimated.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R2.8</b> The interface recharge output shall be set to true when the current battery charge is lower than the battery needed to reach the charging station from the current position plus 5% battery charge.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R2.9</b> Once at the charging station, the robot shall remain there until the battery reaches full charge.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R2.10</b> Each step in the plan shall not use more than 1/n amounts of battery.</td>
<td>RGPR</td>
<td>SRAS</td>

<tbody>
<td rowspan="18"><b>H4</b>. Radioactive contamination from particles adhering to surfaces, equipment, and personnel, leading to contamination spread and an increased risk of radiation exposure.<br><br><b>H5</b>. Contaminated equipment and personnel due to robot manual retrieval in hazardous environments.</td>
<td rowspan="17"><b>SF 3</b> Prevent the robot from being exposed to excessively high levels of radiation</td>
<td><b>R3</b> The robot and personnel shall be protected from harmful radiation exposure.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.1</b> The robot shall continually monitor radiation levels in its environment.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.2</b> Initial robot position shall not be a location with out-of-range radiation levels.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.3</b> The radiation monitor subsystem shall ensure that the initial robot measurement is equal to the manual set level.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.4</b> The radiation monitor subsystem shall ensure that the current position is not a position with out-of-range radiation levels.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.4.1</b> If radiation levels have exceeded, the robot shall go to the exit immediately.</td>
<td>SR</td>
<td><b>SS</b></td>

<tr>
<td><b>R3.5</b> Room radiation levels shall be correctly identified.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.6</b> The radiation level at the inspection points shall be within acceptable ranges.</td>
<td>RGPR.</td>
<td>SRAS</td>

<tr>
<td><b>R3.7</b> The calculated path to the destination shall not include a location with out-of-range radiation levels.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.8</b> Radiation levels shall be under R.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.9</b> The robot shall perform regular checks on its equipment's performance and return to the initial position if anomalies are detected.</td>
<td>RGPR</td>
<td>SRAS</td>

<tr>
<td><b>R3.10</b> The robot shall undergo thorough decontamination procedures before and after each mission.</td>
<td>RGPR</td>
<td>SRAS</td>

<tbody>
<td rowspan="10"><b>H6</b>. Operational failure in the robot's navigation and inspection tasks could result in wrong navigation, and equipment damage.</td>
<td rowspan="10"><b>SF 4</b> Ensure all reachable inspection points are visited</td>
<td><b>R4</b> The robot shall visit all reachable inspection points.</td>
<td>OR</td>
<td>SRAS</td>

<tr>
<td><b>R4.1</b> All inspection points shall be correctly identified.</td>
<td>OR</td>
<td>SRAS</td>

<tr>
<td><b>R4.2</b> A valid inspection point shall not be at the same location as a valid obstacle.</td>
<td>OR</td>
<td>SRAS</td>

<tr>
<td><b>R4.3</b> Visited inspection points shall be removed from the list of destinations to visit.</td>
<td>OR</td>
<td>SRAS</td>

<tr>
<td><b>R4.4</b> The closest inspection point that was not visited before shall be the current goal when the recharge flag is false.</td>
<td>OR</td>
<td>SRAS</td>

<tr>
<td><b>R4.5</b> The shortest path to the current goal shall be selected.</td>
<td>OR</td>
<td>SRAS</td>

<tr>
<td><b>R4.6</b> The interface subsystem shall set the Goal flag to true only when the current robot position is equal to the current goal position.</td>
<td>OR</td>
<td>SRAS</td>


