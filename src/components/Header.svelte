<script>
	import { CIT, CHOSS, CIC, IISC } from '$lib';
	import { onMount } from 'svelte';
	import { fade, slide } from 'svelte/transition';
	

	let isMenuOpen = false;
	let scrollY = 0;

	const logos = [
    { src: CIT, alt: 'CIT', class: 'h-8' },
	
    { src: CHOSS, alt: 'CHOSS', class: 'h-9' },
     
];

const navLinks = [
		{ href: '/about', text: 'About' },
		{ href: '/programs', text: 'Programs' },
		{ href: '/Facilities', text: 'Facilities' },
		{ 
			text: 'Courses', 
			dropdown: [
				{ href: '/programs/ug', text: 'UG' },
				{ href: '/programs/pg', text: 'PG' }
			]
		},
		{ href: '/login', text: 'Login' },
		{ href: 'https://engg.cambridge.edu.in/photo-gallery/', text: 'Gallery' },
		{ href: '/contact', text: 'Contact' }
	];


	$: isScrolled = scrollY > 50;
	$: isCompact = scrollY > 100;

	const toggleMenu = () => (isMenuOpen = !isMenuOpen);

	let currentNewsIndex = 0;
	const news = [
		'Cambridge Institute named Top Innovation Hub 2024',
		'New Industry Partnership Program Launched',
		'Student Startups Raised $5M+ This Quarter',
		'Join Our Next Innovation Workshop'
	];

	onMount(() => {
		const newsInterval = setInterval(() => {
			currentNewsIndex = (currentNewsIndex + 1) % news.length;
		}, 4000);

		return () => clearInterval(newsInterval);
	});

	onMount(() => {
		const handleResize = () => {
			if (window.innerWidth >= 768) isMenuOpen = false;
		};
		window.addEventListener('resize', handleResize);
		return () => window.removeEventListener('resize', handleResize);
	});

	// Adjust height based on scroll position
	$: headerHeight = isCompact ? 'h-2' : isScrolled ? 'h-2' : 'h-2';
	$: headerPadding = isCompact ? 'py-0' : isScrolled ? 'py-1' : 'py-2';
</script>

<svelte:window bind:scrollY />

<header class="fixed top-0 z-50 w-full bg-[#17194a] py-2">

	<div class="container mx-auto px-6">
		 
      

		
		
		<!-- Mobile Header -->
		<div class="flex items-center justify-between md:hidden bg-[#000A30] w-full">

			
			<img src={CIT} alt="CIT" class="h-12 w-auto" />
			<button
				on:click={toggleMenu}
				class="rounded-lg p-2.5 text-white transition-colors hover:bg-white/10"
				aria-label="Toggle menu"
			>
				<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					{#if isMenuOpen}
						<path stroke-linecap="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
					{:else}
						<path stroke-linecap="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
					{/if}
				</svg>
			</button>
		</div>

		
	

		<!-- Desktop Navigation -->
		<div class="hidden md:block">
			<div
				class="flex items-center justify-between transition-all duration-300 {isCompact
					? 'py-0'
					: 'py-1'}"
			>
			<div
			class="flex items-center space-x-6 transition-all duration-300"
		>
		<div class="flex items-center space-x-6 transition-all duration-300">
			<!-- First Logo -->
			<div class="flex flex-col items-center relative">
				<img
					src={logos[0].src}
					alt={logos[0].alt}
					class="{logos[0].class} w-auto transition-transform hover:scale-105"
				/>
			</div>
		
			<!-- Vertical Line -->
			<div class="w-px h-10 bg-white"></div>
		
			<!-- Second Logo -->
			<div class="flex flex-col items-center relative">
				<img
					src={logos[1].src}
					alt={logos[1].alt}
					class="{logos[1].class} w-auto transition-transform hover:scale-105"
				/>
			</div>
		</div>
		
			
				</div>


				
				<div
				
					class="text-center transition-all duration-300 {isCompact
						? '-translate-y-0.5 transform'
						: ''}"
				>
					
					
				</div>

				
				<div
					class="flex items-center space-x-6 transition-all duration-300"
					
				>
					{#each logos.slice(2) as logo}
						<img
							src={logo.src}
							alt={logo.alt}
							class="{logo.class} w-auto transition-transform hover:scale-105"
						/>
					{/each}

					<!-- Search Box -->
<div class="relative">
	<input
		type="text"
		placeholder="Search..."
		class="w-32 rounded-md bg-white px-3 py-1 text-sm text-black placeholder-gray-500 shadow focus:outline-none"
	/>
</div>
 
<!-- Social Media Icons -->
<div class="flex space-x-3 mt-0 ml-auto">
	<a href="#" aria-label="Twitter" class="text-white hover:text-blue-400">
		<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
			<path d="M8.29 20c7.547 0 11.675-6.155 11.675-11.495 0-.175 0-.349-.012-.522A8.18 8.18 0 0 0 22 5.92a8.19 8.19 0 0 1-2.357.637 4.077 4.077 0 0 0 1.804-2.23 8.19 8.19 0 0 1-2.605.981 4.097 4.097 0 0 0-6.993 3.73A11.623 11.623 0 0 1 3.149 4.81a4.066 4.066 0 0 0-.555 2.06 4.09 4.09 0 0 0 1.824 3.404A4.073 4.073 0 0 1 2.8 9.27v.052a4.098 4.098 0 0 0 3.292 4.01 4.1 4.1 0 0 1-1.08.141c-.264 0-.522-.025-.772-.073a4.11 4.11 0 0 0 3.834 2.82A8.233 8.233 0 0 1 2 18.407a11.615 11.615 0 0 0 6.29 1.84"/>
		</svg>
	</a>
	<a href="#" aria-label="Facebook" class="text-white hover:text-blue-600">
		<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
			<path d="M22 12a10 10 0 1 0-11.5 9.87V15.5h-2v-3h2v-2.28c0-2 1.2-3.12 3.03-3.12.88 0 1.8.16 1.8.16v2h-1.02c-1 0-1.31.63-1.31 1.27V12.5h2.23l-.36 3h-1.87v6.37A10 10 0 0 0 22 12Z"/>
		</svg>
	</a>
	<a href="#" aria-label="Instagram" class="text-white hover:text-pink-500">
		<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
			<path d="M7 2C4.243 2 2 4.243 2 7v10c0 2.757 2.243 5 5 5h10c2.757 0 5-2.243 5-5V7c0-2.757-2.243-5-5-5H7Zm10 2c1.654 0 3 1.346 3 3v10c0 1.654-1.346 3-3 3H7c-1.654 0-3-1.346-3-3V7c0-1.654 1.346-3 3-3h10Zm-5 3.5a4.5 4.5 0 1 0 0 9 4.5 4.5 0 0 0 0-9Zm0 2a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm4.25-2.25a.75.75 0 1 0 0 1.5.75.75 0 0 0 0-1.5Z"/>
		</svg>
	</a>
	<a href="#" aria-label="YouTube" class="text-white hover:text-red-500">
		<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
			<path d="M21.8 8s-.2-1.5-.8-2.2c-.7-.9-1.5-.9-1.9-1C16.6 4.5 12 4.5 12 4.5s-4.6 0-7.1.3c-.4.1-1.2.1-1.9 1C2.3 6.5 2.1 8 2.1 8S2 9.6 2 11.1v1.8c0 1.5.1 3.1.1 3.1s.2 1.5.8 2.2c.7.9 1.6.8 2 .9 1.5.1 6.9.3 6.9.3s4.6 0 7.1-.3c.4-.1 1.2-.1 1.9-1 .6-.7.8-2.2.8-2.2s.1-1.5.1-3.1v-1.8C22 9.6 21.8 8 21.8 8Zm-11 7.4V8.6l5.8 3.4-5.8 3.4Z"/>
		</svg>
	</a>
	<a href="#" aria-label="LinkedIn" class="text-white hover:text-blue-500">
		<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
			<path d="M19 0h-14C2.2 0 0 2.2 0 5v14c0 2.8 2.2 5 5 5h14c2.8 0 5-2.2 5-5V5c0-2.8-2.2-5-5-5Zm-9 19H7v-7h3v7Zm-1.5-8.1c-1 0-1.7-.7-1.7-1.6s.7-1.6 1.7-1.6 1.7.7 1.7 1.6-.8 1.6-1.7 1.6Zm11.5 8.1h-3v-3.4c0-.8 0-1.8-1.1-1.8s-1.3.9-1.3 1.8V19h-3v-7h2.9v1h.1c.4-.7 1.2-1.4 2.4-1.4 2.5 0 3 1.6 3 3.6V19Z"/>
		</svg>
	</a>
</div>

				</div>
			</div>

			
			

			
		</div>

		<!-- News Ticker -->
			

		<!-- Mobile Menu -->
		{#if isMenuOpen}
			<div
				class="absolute top-full right-0 left-0 border-t border-white/10 bg-slate-900/95 shadow-lg backdrop-blur-sm"
				transition:slide={{ duration: 300 }}
			>
				<nav class="divide-y divide-white/10">
					{#each navLinks as { href, text }}
						<a
							{href}
							class="block px-6 py-3 text-blue-100 transition-colors hover:bg-white/5 hover:text-white"
							on:click={toggleMenu}
						>
							{text}
						</a>
					{/each}
				</nav>
				<div class="grid grid-cols-2 gap-6 bg-slate-800/50 p-6">
					{#each logos as logo}
						<img src={logo.src} alt={logo.alt} class="mx-auto h-12 w-auto" />
					{/each}
				</div>
			</div>
		{/if}
	</div>
</header>

<div class="{headerHeight} transition-all duration-300"></div>



<style>
	header {
		box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
	}

	.nav-container {
    margin-top: 30px;  /* Adjust this value as needed */
}

	nav a {
		-webkit-tap-highlight-color: transparent;
	}

	p {
		min-width: 300px;
	}

	.invisible {
		visibility: hidden;
		pointer-events: none;
	}


	
</style>
