<script>
let openIndex = null;

function toggle(i){
  openIndex = openIndex === i ? null : i;
}
</script>

<section class="hero">
<h1>Salient Features</h1>
</section>

<section class="features-container">

<!-- 1 Project Location -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(1)}>
<span>Project Location</span>
<span class="icon">{openIndex===1 ? "−" : "+"}</span>
</div>

{#if openIndex===1}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Province</td><td>Bagmati</td></tr>
<tr><td>District</td><td>Rasuwa</td></tr>
<tr><td>Intake Site</td><td>Sangachaur</td></tr>
<tr><td>Powerhouse Site</td><td>Saramthali</td></tr>
<tr><td>Latitude</td><td>28°00'10" N to 27°58'40" N</td></tr>
<tr><td>Longitude</td><td>85°15'17" E to 85°16'14" E</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 2 General Consideration -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(2)}>
<span>General Consideration</span>
<span class="icon">{openIndex===2 ? "−" : "+"}</span>
</div>

{#if openIndex===2}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Name of River</td><td>Phalakhu and Gochyan</td></tr>
<tr><td>Nearest Town</td><td>Bhorle Bazaar</td></tr>
<tr><td>Type of Scheme</td><td>Run-of-River</td></tr>
<tr><td>Installed Capacity</td><td>7.29 MW</td></tr>
<tr><td>Gross Head</td><td>181.98 m</td></tr>
<tr><td>Net Head</td><td>171 m</td></tr>
<tr><td>Design Discharge</td><td>5.03 m³/s</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 3 Hydrology -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(3)}>
<span>Hydrology</span>
<span class="icon">{openIndex===3 ? "−" : "+"}</span>
</div>

{#if openIndex===3}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Catchment Area at Headworks</td><td>103.85 km²</td></tr>
<tr><td>Catchment Area at Powerhouse</td><td>112.70 km²</td></tr>
<tr><td>Design Discharge</td><td>5.03 m³/s</td></tr>
<tr><td>Design Flood (100 year)</td><td>249 m³/s</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 4 Diversion Weir -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(4)}>
<span>Diversion Weir</span>
<span class="icon">{openIndex===4 ? "−" : "+"}</span>
</div>

{#if openIndex===4}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Type</td><td>Free overflow weir</td></tr>
<tr><td>Crest Length</td><td>15 m</td></tr>
<tr><td>Crest Level</td><td>EL 1064.15 masl</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 5 Intake -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(5)}>
<span>Intake</span>
<span class="icon">{openIndex===5 ? "−" : "+"}</span>
</div>

{#if openIndex===5}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Type</td><td>Side Intake</td></tr>
<tr><td>No of Opening</td><td>2</td></tr>
<tr><td>Size</td><td>3.0m x 2.5m</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 6 Gravel Trap -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(6)}>
<span>Gravel Trap</span>
<span class="icon">{openIndex===6 ? "−" : "+"}</span>
</div>

{#if openIndex===6}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Type</td><td>Surface Rectangular</td></tr>
<tr><td>Particle Size</td><td>5 mm</td></tr>
<tr><td>Efficiency</td><td>90%</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 7 Desilting Basin -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(7)}>
<span>Desilting Basin</span>
<span class="icon">{openIndex===7 ? "−" : "+"}</span>
</div>

{#if openIndex===7}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Type</td><td>Dufour Two Chamber</td></tr>
<tr><td>Dimension</td><td>85m x 6.10m x 5.41m</td></tr>
<tr><td>Efficiency</td><td>90%</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 8 Water Conveyance -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(8)}>
<span>Water Conveyance System</span>
<span class="icon">{openIndex===8 ? "−" : "+"}</span>
</div>

{#if openIndex===8}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Head Race Pipe</td><td>Mild Steel</td></tr>
<tr><td>Length</td><td>530m + 1110m</td></tr>
<tr><td>Diameter</td><td>1.8m to 1.6m</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 9 Surge Tank -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(9)}>
<span>Surge Tank</span>
<span class="icon">{openIndex===9 ? "−" : "+"}</span>
</div>

{#if openIndex===9}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Type</td><td>Circular</td></tr>
<tr><td>Height</td><td>20.89 m</td></tr>
<tr><td>Diameter</td><td>8 m</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 10 Penstock -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(10)}>
<span>Steel Penstock Pipe</span>
<span class="icon">{openIndex===10 ? "−" : "+"}</span>
</div>

{#if openIndex===10}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Type</td><td>Mild Steel E350</td></tr>
<tr><td>Diameter</td><td>1.6m to 1.4m</td></tr>
<tr><td>Length</td><td>1450 m</td></tr>
<tr><td>Thickness</td><td>12-18 mm</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 11 Powerhouse -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(11)}>
<span>Powerhouse</span>
<span class="icon">{openIndex===11 ? "−" : "+"}</span>
</div>

{#if openIndex===11}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Type</td><td>Surface</td></tr>
<tr><td>Dimension</td><td>25.65m x 8.50m x 13.50m</td></tr>
<tr><td>Turbine Axis Level</td><td>883.45 masl</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 12 Turbine -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(12)}>
<span>Turbine</span>
<span class="icon">{openIndex===12 ? "−" : "+"}</span>
</div>

{#if openIndex===12}
<div class="accordion-body">
<table>
<tbody>
<tr><td>No of Units</td><td>2</td></tr>
<tr><td>Type</td><td>Horizontal Axis Francis</td></tr>
<tr><td>Rated Output</td><td>3645 kW</td></tr>
<tr><td>Efficiency</td><td>91%</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 13 Transformer -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(13)}>
<span>Transformer</span>
<span class="icon">{openIndex===13 ? "−" : "+"}</span>
</div>

{#if openIndex===13}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Type</td><td>Three Phase Outdoor</td></tr>
<tr><td>Capacity</td><td>9434 kVA</td></tr>
<tr><td>Voltage Ratio</td><td>6.6/33 kV</td></tr>
</tbody>
</table>
</div>
{/if}
</div>


<!-- 14 Power & Energy -->
<div class="accordion">
<div class="accordion-header" on:click={()=>toggle(14)}>
<span>Power and Energy</span>
<span class="icon">{openIndex===14 ? "−" : "+"}</span>
</div>

{#if openIndex===14}
<div class="accordion-body">
<table>
<tbody>
<tr><td>Deemed Energy</td><td>38.74 GWh</td></tr>
<tr><td>Dry Season Energy</td><td>6.53 GWh</td></tr>
<tr><td>Wet Season Energy</td><td>32.21 GWh</td></tr>
</tbody>
</table>
</div>
{/if}
</div>

</section>

<style>

.hero{
padding:60px 20px;
background:#f5f7fa;
text-align:center;
}

.hero h1{
font-size:40px;
color:var(--primary-blue);
}

.features-container{
max-width:900px;
margin:auto;
padding:40px 20px;
}

.accordion{
border-bottom:1px solid #e5e5e5;
}

.accordion-header{
display:flex;
justify-content:space-between;
align-items:center;
padding:10px 10px;
font-size:18px;
font-weight:500;
cursor:pointer;
transition:0.3s;
border: #e5e5e5 solid 1px;
border-radius: 8px;
}

.accordion-header:hover{
color: white;
background: var(--primary-blue);
}


.icon{
font-size:20px;
font-weight:700;
}

.accordion-body{
padding:10px 40px;
animation:fade 0.3s ease;
}

table{
width:100%;
border-collapse:collapse;
}

td{
padding:8px 0;
border-bottom:1px solid #eee;
}

@keyframes fade{
from{
opacity:0;
transform:translateY(-5px);
}
to{
opacity:1;
transform:translateY(0);
}
}

</style>