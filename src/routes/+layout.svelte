<script>
	import Navbar from '$lib/components/navbar.svelte'
	import Footer from '$lib/components/footer.svelte'
</script>
<Navbar />
<main>
    <slot />
</main>
<Footer />
<style>
	:global(body){
		margin: 0;
		padding: 0;
		font-family: 'Poppins', sans-serif;
		background-color: #F8F9FA;
	}
	:global(:root){
		--primary-blue: #0A2F5A;
		--primary-red:  #C62828;
		--light-bg: #F8F9FA;
		--white: #FFFFFF;
	}
</style>
