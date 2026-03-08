<script>
import { onMount } from "svelte";
import Chart from "chart.js/auto";
import ChartDataLabels from 'chartjs-plugin-datalabels';

Chart.register(ChartDataLabels);

let overallChart;
let milestoneChart;
let civilChart;

const centerTextPlugin = {
  id: 'centerText',
  beforeDraw: (chart) => {
    const { ctx, chartArea: { left, right, top, bottom, width, height } } = chart;
    ctx.save();
    ctx.font = 'bold 30px Arial';
    ctx.fillStyle = '#d62828';
    ctx.textAlign = 'center';
    ctx.textBaseline = 'middle';
    ctx.fillText('58%', width / 2 + left, height / 2 + top);
    ctx.restore();
  }
};

onMount(() => {

new Chart(overallChart, {
type: "doughnut",
data: {
labels: ["Completed", "Remaining"],
datasets: [{
data: [58, 42],
backgroundColor: ["#d62828","#e5e7eb"]
}]
},
plugins: [centerTextPlugin],
options:{
responsive: true,
maintainAspectRatio: false,
plugins:{
legend:{display:false},
datalabels: { display: false }
}
}
});


new Chart(milestoneChart,{
type:"bar",
data:{
labels:[
"Land Acquisition",
"Access Road",
"Camp Establishment",
"Construction Power",
"Crusher Plant"
],
datasets:[{
label:"Progress %",
data:[99,87,85,95,100],
backgroundColor:"#0b4b8a"
}]
},
options:{
responsive: true,
maintainAspectRatio: false,
plugins:{
datalabels: {
  color: 'white',
  font: { size: 14, weight: 'bold' },
  formatter: (value) => value + '%',
  anchor: 'end',
  align: 'top'
},
legend: { labels: { font: { size: 16 } } }
},
scales:{
y:{beginAtZero:true,max:100, ticks: { font: { size: 12 } }},
x:{ ticks: { font: { size: 12 } } }
}
}
});


new Chart(civilChart,{
type:"bar",
data:{
labels:[
"Headworks",
"Tunnel",
"Headrace Alignment",
"Powerhouse",
"Hydromechanical",
"Electromechanical"
],
datasets:[{
label:"Progress %",
data:[20,8,7,5,5,7],
backgroundColor:"#d62828"
}]
},
options:{
responsive: true,
maintainAspectRatio: false,
plugins:{
datalabels: {
  color: 'white',
  font: { size: 14, weight: 'bold' },
  formatter: (value) => value + '%',
  anchor: 'end',
  align: 'top'
},
legend: { labels: { font: { size: 16 } } }
},
scales:{
y:{beginAtZero:true,max:100, ticks: { font: { size: 12 } }},
x:{ ticks: { font: { size: 12 } } }
}
}
});

});
</script>


<section class="hero">
<h1>Project Status</h1>
<p>Construction progress of Phalakhu Khola Hydropower Project</p>
</section>


<section class="dashboard">

<div class="container">

<h2>Overall Project Progress</h2>

<div class="chart-center">
<canvas bind:this={overallChart}></canvas>
</div>

</div>

</section>



<section class="milestones">

<div class="container">

<h2>Major Development Milestones</h2>

<div class="chart-container">
<canvas bind:this={milestoneChart}></canvas>
</div>

</div>

</section>



<section class="civil">

<div class="container">

<h2>Civil Construction Progress</h2>

<div class="chart-container">
<canvas bind:this={civilChart}></canvas>
</div>

</div>

</section>



<section class="cards">

<div class="container">

<h2>Key Progress Indicators</h2>

<div class="grid">

<div class="card">
<h3>Land Acquisition</h3>
<p>99%</p>
</div>

<div class="card">
<h3>Access Road</h3>
<p>87%</p>
</div>

<div class="card">
<h3>Construction Power</h3>
<p>95%</p>
</div>

<div class="card">
<h3>Crusher Plant</h3>
<p>100%</p>
</div>

</div>

</div>

</section>


<style>

.hero{
padding:120px 20px;
background:#f5f7fa;
text-align:center;
}

.hero h1{
color:var(--primary-blue);
font-size:40px;
}

.hero p{
color:#555;
font-size:18px;
}


.container{
max-width:1100px;
margin:auto;
padding:0 20px;
}

section{
padding:60px 0;
}

h2{
text-align:center;
color:var(--primary-blue);
margin-bottom:40px;
font-size:28px;
}

.chart-center{
width:100%;
max-width:300px;
height:300px;
margin:auto;
}

.chart-container{
width:100%;
height:350px;
margin:auto;
}


.grid{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:25px;
margin-top:40px;
}

.card{
background:white;
padding:30px;
border-radius:12px;
text-align:center;
box-shadow:0 10px 25px rgba(0,0,0,0.08);
}

.card h3{
margin-bottom:10px;
color:var(--primary-blue);
font-size:18px;
}

.card p{
font-size:24px;
font-weight:600;
color:#333;
}


@media(max-width:900px){

.grid{
grid-template-columns:repeat(2,1fr);
}

.chart-container{
height:300px;
}

}

@media(max-width:600px){

.hero{
padding:80px 20px;
}

.hero h1{
font-size:32px;
}

.hero p{
font-size:16px;
}

h2{
font-size:24px;
margin-bottom:30px;
}

.chart-center{
max-width:250px;
height:250px;
}

.chart-container{
height:250px;
}

.grid{
grid-template-columns:1fr;
gap:20px;
}

.card{
padding:25px;
}

.card h3{
font-size:16px;
}

.card p{
font-size:22px;
}

}

</style>