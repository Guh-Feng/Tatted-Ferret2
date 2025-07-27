<script lang="ts">
	import logo from '$lib/logo-transparent.png?enhanced';
	import artists from '$lib/artists.png?enhanced';
	import bookBuy from '$lib/book+buy.png?enhanced';
	import contact from '$lib/contact.png?enhanced';
	import faq from '$lib/faq.png?enhanced';
</script>

<svelte:head>
	<title>Tatted Ferret | Home</title>
</svelte:head>

<div class="flex items-center justify-center min-h-screen p-4">
	<nav
		class="grid grid-cols-2 lg:grid-cols-4 lg:grid-rows-2 gap-4 w-full max-w-md lg:max-w-[95vw] items-center"
	>
		<div
			class="col-span-2 lg:col-start-2 lg:col-span-2 lg:row-start-1 lg:row-span-2 flex items-center justify-center"
		>
			<enhanced:img src={logo} alt="Tatted Ferret Logo" />
		</div>

		<a
			href="/artists"
			class="lg:col-start-1 lg:row-start-1 lg:self-center lg:justify-self-center"
		>
			<enhanced:img src={artists} alt="Artists" />
		</a>
		<a
			href="/booking"
			class="lg:col-start-4 lg:row-start-1 lg:self-center lg:justify-self-center"
		>
			<enhanced:img src={bookBuy} alt="Book & Buy" />
		</a>
		<a
			href="/contact"
			class="lg:col-start-1 lg:row-start-2 lg:self-center lg:justify-self-center"
		>
			<enhanced:img src={contact} alt="Contact" />
		</a>
		<a href="/faq" class="lg:col-start-4 lg:row-start-2 lg:self-center lg:justify-self-center">
			<enhanced:img src={faq} alt="FAQ" />
		</a>
	</nav>
</div>
