<script>
  import { onMount } from 'svelte';
  import * as d3 from 'd3';

  let data = [];

  onMount(async () => {
    const res = await fetch('pokemon.csv');
    const csv = await res.text();
    data = d3.csvParse(csv);
    console.log(data)
    drawPieChart(data);
  });

  function drawPieChart(data) {
    // D3 pie chart code here
    // Adapt the D3 code to use the 'data' variable
  }
</script>

<style>
  /* Add any necessary styles here */
</style>

<div id="pie-chart"></div>

