<script lang="ts">
	import '../app.css';
	import { page } from '$app/state';

	let { children } = $props();

	import logoTransparent from '$lib/logo-transparent.png?enhanced'
	import artists from '$lib/artists.png?enhanced'
	import book from '$lib/book+buy.png?enhanced'
	import contact from '$lib/contact.png?enhanced'
	import faq from '$lib/faq.png?enhanced'

	let openMenu = $state(false);

	function displayMenu() {
		openMenu = !openMenu;
	}
</script>

<style>
	:global(body) {
		background-color: #f58447;
	}
</style>
<!-- Have buttons move on hover -->
{#if page.url.pathname != "/"}
<div class='flex flex-col z-30 absolute lg:flex-col lg:top-0 {openMenu ? "bg-orange-400" : "w-0"}'>
	<div class="lg:flex {openMenu ? "" : "hidden" } lg:flex-col lg:items-center transparent lg:w-[33vh] lg:mx-3">
		<div class="lg:absolute lg:top-[7vh] lg:h-[90vh] lg:w-[15vh] outline-5 outline-[#db5123] lg:rounded-full lg:-z-10"></div>
		<a href="/" class="lg:flex hidden w-[33vh]"><enhanced:img src={logoTransparent} alt="tatted ferret logo" class="select-none"/></a>
		<div class="mx-auto grid grid-cols-2 gap-y-2 align-middle z-10 lg:grid-cols-1 bg-orange-400 lg:bg-transparent">
			<a href="/artists/tatterjae" class="w-[47.6vw] {page.url.pathname.includes("/artists") ? "relative lg:left-10" : ""} lg:w-[17vh] "><enhanced:img src={artists} alt="artists" class="select-none"/></a>
			<a href="/bookings" class="{page.url.pathname == "/bookings" ? "relative lg:left-10" : ""} lg:w-[17vh] "><enhanced:img src={book} alt="bookings" class="select-none"/></a>
			<a href="/faq" class="w-[47.6vw] {page.url.pathname == "/faq" ? "relative lg:left-10" : ""} lg:w-[17vh] "><enhanced:img src={faq} alt="frequently asked questions" class="select-none"/></a>
			<a href="/contacts" class="relative bottom-[4.5vw] {page.url.pathname == "/contacts" ? "lg:left-10" : ""} lg:w-[17vh] lg:bottom-0"><enhanced:img src={contact} alt="contact" class="select-none"/></a>
		</div>
	</div>
</div>

{/if}

{@render children()}
