<script>
    // import images from the asset folder so Vite can bundle them correctly
    import pic1 from '$lib/assets/Images3/Picture1.png';
    import pic2 from '$lib/assets/Images3/Picture2.png';
    import pic3 from '$lib/assets/Images3/Picture3.png';
    import pic4 from '$lib/assets/Images3/Picture4.png';
    import pic5 from '$lib/assets/Images3/Picture5.png';

    const directors = [
        {
            name: 'Mr. Deepak Thapa',
            role: 'Executive Chairman',
            img: pic1,
            details: 'Mr. Deepak Thapa serves as the Executive Chairman of Rasuwa Hydropower Limited and has been actively involved in the business sector since 2001. He holds a Bachelor’s degree and has extensive experience in hydropower development, manpower services, and education management. In addition to leading Rasuwa Hydropower Limited, he has held key roles in several organizations including Sadhika Overseas Pvt. Ltd. as Managing Director, Liverpool International College as Director, and Asias Force Pvt. Ltd. as Director.'
        },
        {
            name: 'Mr. Bisham Rimal',
            role: 'Director',
            img: pic3,
            details: 'Mr. Bisham Rimal is a Director of Rasuwa Hydropower Limited with professional experience in construction, agriculture, and hydropower development. He holds a Bachelor’s degree and has been involved in business since 2005. He is also associated with Suryakunda Agricultural Firm Pvt. Ltd., Betrawati Hydroelectric Pvt. Ltd. (14.7 MW) as Chairman, and Raluka Devi Construction Pvt. Ltd., contributing valuable expertise in infrastructure and energy sector development.'
        },
        {
            name: 'Mr. Thakur Prasad Panta',
            role: 'Director',
            img: pic5,
            details: 'Mr. Thakur Prasad Panta serves as a Director of Rasuwa Hydropower Limited and has been engaged in business activities since 2008. Holding a Bachelor’s degree, he has experience primarily in the construction sector. Along with his role in Rasuwa Hydropower Limited, he is involved with Subas and Sons Company Pvt. Ltd. and Manaslu Higher Secondary School, contributing his experience in construction and organizational management.'
        },
        {
            name: 'Mr. Dipak Kumar Ray',
            role: 'Director(proposed)',
            img: pic2,
            details: 'Mr. Dipak Kumar Ray is a proposed Director of Rasuwa Hydropower Limited with business experience since 2005. He holds a Bachelor’s degree and has professional involvement in overseas services, consultancy, and education sectors. His business engagements include Brothers International Employment Pvt. Ltd., Praney Chanda Technical Services LLC (UAE), and Tower Info Foreign Employment Orientation Pvt. Ltd., bringing diverse managerial and international exposure to the company.'
        },
        {
            name: 'Mr. Sujan Poudel',
            role: 'Director(proposed)',
            img: pic4,
            details: 'Mr. Sujan Poudel is a proposed Director of Rasuwa Hydropower Limited and holds a Bachelor of Business Administration (BBA). He has been involved in business since 2019 and has experience in the transport and education sectors. In addition to his involvement with Rasuwa Hydropower Limited, he is associated with Basuki Transport Pvt. Ltd. as Chairman and Sochi International Academy as Director.'
        }
    ];

    let selected = null;
</script>
<section class="wrap">
    <h1>Our Team</h1>

    <hr class="line"/>

    <h3>Board Of Directors</h3>

    <div class="grid">
        {#each directors as p}
            <div class="card" on:click={() => selected = p}>
                <div class="photo">
                    <img src={p.img} alt={p.name}>
                </div>

                <strong>{p.name}</strong>
                <small>{p.role}</small>
            </div>
        {/each}
    </div>
</section>
{#if selected}
    <div class="modal">
	<div class="box">

		<button class="close" on:click={() => selected = null}>×</button>

		<div class="modal-top">
			<div class="photo big">
				<img src={selected.img} alt={selected.name}>
			</div>

			<div>
				<h3>{selected.name}</h3>
				<p><em>{selected.role}</em></p>
			</div>
		</div>

		<div class="details">
	{@html selected.details}
    </div>
    </div>
    </div>
{/if}
<style>
.wrap{
	max-width:1050px;
	margin:80px auto;
	text-align:center;
	padding:0 15px;
}

h1{
	color:var(--primary-blue);
}

.line{
	margin:20px auto 30px;
	width:70%;
	color:#ccc;
}

h3{
	margin-top:10px;
	color:var(--primary-blue);
}

/* GRID */
.grid{
	display:grid;
	grid-template-columns:repeat(4,1fr);
	gap:28px;
	margin-top:25px;
}

.card{
	background:white;
	border-radius:14px;
	padding:18px;
	box-shadow:0 10px 25px rgba(0,0,0,.12);
	cursor:pointer;
	transition:.2s;
}

.card:hover{
	transform:translateY(-4px);
}

/* PHOTO */
.photo{
	width:120px;
	height:120px;
	border-radius:50%;
	overflow:hidden;
	margin: auto;
}

.photo img{
	width:100%;
	height:100%;
	object-fit:cover;
}

/* TEXT */
strong{
	display:block;
	margin-top:10px;
}

small{
	color:#555;
}


/* ===== POPUP ===== */

.modal{
	position:fixed;
	inset:0;
	background:rgba(0,0,0,.6);
	display:flex;
	justify-content:center;
	align-items:flex-start;
	padding-top:180px; /* distance below header */
	z-index:100;
}

.box{
	background:white;
	border-radius:18px;
	padding:25px;
	max-width:520px;
	width:92%;
	position:relative;
}

.close{
	position:absolute;
	top:10px;
	right:12px;
	font-size:28px;
	background:none;
	border:none;
	cursor:pointer;
}

.modal-top{
	display:flex;
	gap:20px;
	align-items:center;
}

.big{
	width:140px;
	height:140px;
}

.details{
	margin-top:15px;
	color:#333;
}


/* RESPONSIVE */

@media(max-width:900px){
	.grid{
		grid-template-columns:repeat(2,1fr);
	}
}

@media(max-width:550px){
	.grid{
		grid-template-columns:1fr;
	}
}
</style>

