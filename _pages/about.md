---
permalink: /
title: "Ice Microstructure for Planetary Surfaces"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

  
Microstructure
======

Ices are widespread across the solar system, present on the surfaces of nearly all planets and moons. Icy moons, in particular, are of high interest due to their potential habitability, as they can harbor liquid water oceans beneath their icy crust. Among them, Europa, one of Jupiter’s moons, stands out as a prime candidate for studying habitability. Various space observations suggest that its surface is composed of granular ice material (Fig.1a), but its properties are still not well understood. Notably, the microstructure (referring to the microscopic arrangement and characteristics of ice grains, bonds (Fig.1b), crystallinity, etc.), plays a crucial role in determining the ice optical, thermal, and mechanical properties.


<p align="center">
<img src="/images/microstructure.png" alt="drawing" width="50%" class="center"/>
</p>

Icy Surfaces
======

Multiple surface processes, such as heat transfer, ice sintering (the formation of bonds between grains Fig.1c-d), space weathering, compaction, and irradiation, significantly alter the microstructure of the icy surface and subsurface (~ first few meters) (Fig.2). These processes are all interdependent and occur over large timescales, making it challenging for previous studies to estimate the current state of the ice. To address this, I have previously developed a multiphysics simulation model, **LunaIcy**, which integrates the main  physical phenomena affecting ice microstructure and simulates their interactions. This model has already shed light on Europa's surface, helping to estimate the cohesiveness and crystallinity, with findings published in research articles (see *Publications*).

<p align="center">
<img src="/images/europa_multisurf.png" alt="drawing" width="75%" class="center"/>
</p>

LunaIcy
======
The core concept of my research is to integrate the various physical phenomena that affect Europa’s ice microstructure and couple them within a 1D multiphysics simulation model named "LunaIcy" (see Figure 3). Just as scientists have developed General Circulation Models (GCMs) for climate studies, the study of planetary icy surfaces would benefit from the creation of multiphysics numerical models. This kind of simulation would be an analogous to snowpack models used for avalanche prediction, but here for solar system ices. 



<p align="center">
<img src="/images/lunaicy.png" alt="drawing" width="75%" class="center"/>
</p>


<script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
<div id="plot"></div>
<script>
  function updatePlot() {
    var a = document.getElementById('a').value;
    var b = document.getElementById('b').value;
    var x = [...Array(100).keys()].map(i => i / 10 - 5); // Range from -5 to 5
    var y = x.map(x => a * x * x + b);

    var trace = {
      x: x,
      y: y,
      mode: 'lines',
      type: 'scatter'
    };

    var layout = {
      title: 'Interactive Plot',
      xaxis: { title: 'x' },
      yaxis: { title: 'f(x)' }
    };

    Plotly.newPlot('plot', [trace], layout);
  }

  document.getElementById('updateButton').addEventListener('click', updatePlot);
</script>

<input type="number" id="a" placeholder="Enter value for a">
<input type="number" id="b" placeholder="Enter value for b">
<button id="updateButton">Update Plot</button>



