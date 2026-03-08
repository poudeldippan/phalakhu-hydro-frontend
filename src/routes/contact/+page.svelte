<script>
let name = "";
let email = "";
let message = "";
let success = false;

async function submitForm() {

const res = await fetch('/api/contact', {
method: 'POST',
headers: { 'Content-Type': 'application/json' },
body: JSON.stringify({ name, email, message })
});

const data = await res.json();

if (data.success) {
success = true;
name = "";
email = "";
message = "";
}

}
</script>

<!--Hero section-->
<section class="page-hero">
<div class="hero-container">
<h1>Contact Us</h1>
<p>Have questions about the Rasuwa Hydropower Project? Reach out to our team and we will get back to you shortly.</p>
</div>
</section>

<div class="section-divider"></div>

<section class="contact-info">
<div class="container">
<h2>Contact Information</h2>
<div class="company-info-grid">

    <div class="info-card">
    <div class="info-icon">
    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.8" stroke="currentColor" width="24" height="24">
    <path stroke-linecap="round" stroke-linejoin="round" d="M3 21h18M4 21V7a1 1 0 011-1h4v15M9 21V4a1 1 0 011-1h4a1 1 0 011 1v17M14 21V10h4a1 1 0 011 1v10"/>
    </svg>
    </div>
    <h4>Office Address</h4>
    <p>Samakhusi, Kathmandu</p>
    </div>

     <div class="info-card">
     <div class="info-icon">
     <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.8" stroke="currentColor" width="24" height="24">
     <path stroke-linecap="round" stroke-linejoin="round" d="M8 7V3m8 4V3m-9 8h10m-13 9h16a2 2 0 002-2V7a2 2 0 00-2-2H4a2 2 0 00-2 2v10a2 2 0 002 2z"/>
     </svg>
     </div>
        <h4>Email</h4>
        <p>rasuwahydropower@yahoo.com</p>
      </div>

      <div class="info-card">
      <div class="info-icon">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.8" stroke="currentColor" width="24" height="24">
      <path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
      </svg>
      </div>
        <h4>Phone</h4>
        <p>01-4880041</p>
      </div>

</div>
</div>
</section>

<div class="section-divider"></div>

<section class="contact-form-section">

<div class="form-container">

<h2>Send us a Message</h2>

<form on:submit|preventDefault={submitForm}>

<input
type="text"
placeholder="Your Name"
bind:value={name}
required
/>

<input
type="email"
placeholder="Your Email"
bind:value={email}
required
/>

<textarea
rows="5"
placeholder="Your Message"
bind:value={message}
required
></textarea>

<button type="submit">
Send Message
</button>

</form>

{#if success}
<p class="success-message">
Message sent successfully.
</p>
{/if}

</div>

</section>


<div class="section-divider"></div>


<section class="map-section container">

<h2>Our Location</h2>

<iframe
src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d27306.986415527863!2d85.27897856228873!3d27.730058094110507!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x39eb190009501341%3A0x63fb435bb26d3f92!2sRasuwa%20Hydropower%20Ltd!5e0!3m2!1sen!2snp!4v1772294801149!5m2!1sen!2snp"
width="100%"
height="400"
style="border:0; border-radius:8px;"
allowfullscreen
loading="lazy"
referrerpolicy="no-referrer-when-downgrade"
title="Rasuwa Hydropower Limited Location">
</iframe>

</section>



<style>
.page-hero{
    padding: 40px 20px;
    text-align: center;
    background: linear-gradient(#fff, #f5f7fa);
}
.page-hero h1{
    font-size: 36px;
    color: var(--primary-blue);
    margin-bottom: 15px;
}
.page-hero p{
    max-width: 600px;
    margin: auto;
    color: #555;
    text-decoration: underline;
    font-size: 16px;
}

.section-divider{
    width:60px;
    height:2px;
    background:#e2e8f0;
    margin:50px auto;
}

.contact-info{
    padding: 20px;
}
.contact-info h2{
    color: var(--primary-blue);
    text-align: center;
    margin-bottom: 30px;
    font-size: 28px;
}
.container{
    max-width: 1100px;
    margin: auto;
    padding: 0;
}
.company-info-grid{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 25px;
    align-items: stretch;
}
.info-card{
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    background: rgba(255, 255, 255, 0.9);
    padding: 25px 20px;
    border-radius: 12px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.08);
    transition: transform 0.25s ease, box-shadow 0.25s ease;
    min-height: 160px;
    justify-content: center;
}
.info-card:hover{
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(0,0,0,0.12);
}
.info-card h4{
    color: var(--primary-blue);
    margin: 12px 0 8px 0;
    font-size: 18px;
    font-weight: 600;
}
.info-card p{
    color: #555;
    margin: 0;
    font-size: 15px;
    line-height: 1.4;
}
.info-icon{
    width: 48px;
    height: 48px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--primary-blue);
    background: rgba(10, 47, 90, 0.1);
    border-radius: 50%;
    margin-bottom: 5px;
}

.contact-form-section{
    padding: 60px 20px;
    background:#f8fafc;
    border-top:1px solid #e5e7eb;
    border-bottom:1px solid #e5e7eb;
}

.form-container{
    max-width:580px;
    margin:auto;
    background:white;
    padding:35px;
    border-radius:16px;
    box-shadow:0 10px 25px rgba(0,0,0,0.06);
}

.form-container h2{
    text-align:center;
    margin-bottom:8px;
    color: var(--primary-blue);
    font-size: 24px;
}

form{
    display:flex;
    flex-direction:column;
    gap:16px;
    margin-top:18px;
}

input, textarea{
    padding:12px 16px;
    border:1px solid #d1d5db;
    border-radius:8px;
    font-size:15px;
    font-family: 'Poppins', sans-serif;
    transition:border 0.2s;
}

input:focus,
textarea:focus{
    outline:none;
    border-color:#2563eb;
}

button{
    background:#2563eb;
    color:white;
    border:none;
    padding:12px 16px;
    border-radius:8px;
    font-weight:500;
    font-family: 'Poppins', sans-serif;
    cursor:pointer;
    transition:background 0.25s;
    font-size: 15px;
}

button:hover{
    background:#1d4ed8;
}

.success-message{
    margin-top:12px;
    color:green;
    text-align:center;
    font-family: 'Poppins', sans-serif;
}

.map-section{
    margin-bottom:60px;
    text-align: center;
    padding: 0 20px;
}

.map-section h2{
    color: var(--primary-blue);
    margin-bottom: 25px;
    font-size: 24px;
}

.map-section iframe{
    width:100%;
    height:350px;
    border-radius:12px;
    border:none;
    box-shadow:0 6px 20px rgba(0,0,0,0.08);
}

@media(max-width:800px){
    .company-info-grid{
        grid-template-columns: 1fr;
        gap: 20px;
    }
    .info-card{
        min-height: auto;
        padding: 20px;
    }
    .contact-info{
        padding: 15px 20px;
    }
    .contact-info h2{
        font-size: 24px;
        margin-bottom: 25px;
    }
}

@media (max-width:768px){
    .page-hero{
        padding: 50px 20px;
    }
    .page-hero h1{
        font-size: 28px;
    }
    .contact-form-section{
        padding: 50px 20px;
    }
    .form-container{
        padding: 25px;
    }
    .map-section iframe{
        height: 250px;
    }
}
</style>