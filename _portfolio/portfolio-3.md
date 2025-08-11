---
title: "Isothermal Sintering Simulation"
excerpt: "Results from LunaIcy simulations of isothermal sintering on Europ.<br/><img src='/images/bond_europa'>"
collection: Highlights
---

<div id="plotly-chart" style="width:600px;height:400px;"></div>
<script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
<script>
  const xVals = Array.from({length: 100}, (_, i) => i/10);
  const yVals = xVals.map(x => Math.sin(x)); // Example function
  const trace = {
    x: xVals,
    y: yVals,
    mode: 'lines',
    type: 'scatter'
  };
  Plotly.newPlot('plotly-chart', [trace], {
    title: 'y = sin(x)',
    xaxis: {title: 'x'},
    yaxis: {title: 'y'}
  });
</script>
