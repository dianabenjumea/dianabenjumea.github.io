---
layout: page
title: "Requirements Identification and Allocation"
permalink: /RE/requirementsTable/
---

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>REQUIREMENTS IDENTIFICATION AND ALLOCATION</title>
<style>
table {
  border-collapse: collapse;
  width: 100%;
}

th, td {
  border: 1px solid black;
  padding: 8px;
  text-align: left;
}

th {
  background-color: #f2f2f2;
}
</style>
</head>
<body>
<table>
<thead>
<tr>
<th>Source</th>
<th>Safety Function</th>
<th>Requirement</th>
<th>Group</th>
<th>System</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="20"><b>H1</b>. Collisions with physical obstacles damaging the robot, equipment, and dispersing radioactive material.</td>
<td rowspan="20"><b>SF 1</b> Prevent collision</td>
<td><b>R1</b> The robot shall avoid physical obstacles.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.1</b> The robot shall maintain a safe distance from obstacles.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.1.1</b> The robot shall have an emergency stop mechanism that activates when an obstacle is detected within a critical range of distance.</td>
<td>SR</td>
<td><b>SS</b></td>
<tr>
<td><b>R1.1.2</b> The robot shall return to the initial position when an obstacle is detected within a defined range of distance.</td>
<td>SR</td>
<td><b>SS</b></td>
</tr>
<tr>
<td><b>R1.3</b> Initial robot position shall be obstacle-free.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.4</b> Current robot position shall be accurate.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.5</b> The vision subsystem shall confirm that the robot's initial recognised position matches the predefined starting position.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.6</b> The vision subsystem shall report that the current position is not a position with an obstacle.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.7</b> The path to the next destination shall be calculated from the current robot position that the robot believes its location to be.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.8</b> All obstacles shall be correctly identified.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.9</b> An obstacle shall not be in the same location as an inspection point.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.10</b> The calculated path to the destination shall not include a location with an obstacle.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
<tr>
<td><b>R1.11</b> The robot shall not go faster than X kmph.</td>
<td>RGPR</td>
<td>SRAS</td>
</tr>
</tbody>
</table>
</body>
</html>
