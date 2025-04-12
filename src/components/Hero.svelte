<script>
	import { onMount } from 'svelte';
	import { fade, fly } from 'svelte/transition';
	import { goto } from '$app/navigation';

	const stats = [
		{ label: 'Industry Partners', value: '50+', prefix: '' },
		{ label: 'Patents Filed', value: '3000+', prefix: '' },
	];

	const news = [
		'Student Startups Raised $5M+ This Quarter',
		'Cambridge Institute named Top Innovation Hub 2024',
		'New Industry Partnership Program Launched',
		'Student Startups Raised $5M+ This Quarter',
		'Join Our Next Innovation Workshop',
		'Cambridge Institute named Top Innovation Hub 2024',
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

	let currentNewsIndex = 0;
	let isVisible = false;

	onMount(() => {
		isVisible = true;
		const interval = setInterval(() => {
			currentNewsIndex = (currentNewsIndex + 1) % news.length;
		}, 4000);

		return () => clearInterval(interval);
	});

	const opportunities = [
		{
			title: 'Industry Innovation',
			description: 'Transform your business challenges into opportunities',
			cta: 'Submit Challenge',
			icon: '🎯',
			link: "/innovation"
		},
		{
			title: 'Research Partnership',
			description: 'Access cutting-edge research and development facilities',
			cta: 'Partner With Us',
			icon: '🔬',
			link: "/research"
		}
	];
</script>


<!-- Horizontal Quick Links Banner -->
<section class="bg-white pt-16 p-5">
	<div class="container mx-auto flex flex-wrap justify-center items-center gap-20 text-black text-sm font-medium">
	  <a href="/about" class="cursor-pointer hover:underline hover:text-blue-700 transition">About</a>
	  <a href="/programs" class="cursor-pointer hover:underline hover:text-blue-700 transition">Programs</a>
	  <a href="/facilities" class="cursor-pointer hover:underline hover:text-blue-700 transition">Facilities</a>
	  <a href="/login" class="cursor-pointer hover:underline hover:text-blue-700 transition">Login</a>
	  <a href="/contact" class="cursor-pointer hover:underline hover:text-blue-700 transition">Contact Us</a>
  
	  <!-- Courses Dropdown -->
	  <div class="relative group">
		<span class="cursor-pointer hover:underline hover:text-blue-700">Courses</span>
		<div class="absolute hidden group-hover:block mt-2 bg-white shadow-md border rounded-lg text-sm z-10">
		  <a href="www.google.com" class="block px-4 py-2 hover:bg-gray-100 text-[#000A30] cursor-pointer">UG</a>
		  <a href="/programs/pg" class="block px-4 py-2 hover:bg-gray-100 text-[#000A30] cursor-pointer">PG</a>
		</div>
	  </div>
	</div>
  </section>
  
  
<div class="top-banner flash-loop">
	<img class="flash-image image1" style="animation-delay: 0s" src="/lib/logos/Artboard 1.jpg" alt="Banner 1" />
	<img class="flash-image image2" style="animation-delay: 0s" src="/lib/logos/Artboard 1 copy.jpg" alt="Banner 2" />
	
</div>



<!-- ✅ Wrapper div with flex add your code here for the -->
<div class="relative w-full h-[100px] bg-white">

	<div class='relative top-4'>
	<!-- Center Line -->
	<div class="absolute top-5 left-42 w-236 h-[2px] bg-gray-300"></div>
  
	<!-- Circles Container -->
	<div class="absolute top-[2px] left-0 w-full flex justify-around items-start px-8">
	  
	  <!-- Circle A -->
	  <div class="flex flex-col items-center space-y-1">
		<div class="w-10 h-10 flex items-center justify-center rounded-full bg-yellow-400 text-white font-bold text-sm shadow-[0_0_10px_#facc15]">
		  A
		</div>
		<span class="text-[#000a30] text-xs font-medium">Shaping the Future </span>
	  </div>
  
	  <!-- Circle B -->
	  <div class="flex flex-col items-center space-y-1">
		<div class="w-10 h-10 flex items-center justify-center rounded-full bg-green-500 text-white font-bold text-sm shadow-[0_0_10px_#22c55e]">
		  B
		</div>
		<span class="text-[#000a30] text-xs font-medium">Student Startups</span>
	  </div>
  
	  <!-- Circle C -->
	  <div class="flex flex-col items-center space-y-1">
		<div class="w-10 h-10 flex items-center justify-center rounded-full bg-blue-500 text-white font-bold text-sm shadow-[0_0_10px_#3b82f6]">
		  C
		</div>
		<span class="text-[#000a30] text-xs font-medium">Industry Experts</span>
	  </div>
  
	  <!-- Circle D -->
	  <div class="flex flex-col items-center space-y-1">
		<div class="w-10 h-10 flex items-center justify-center rounded-full bg-[#800000] text-white font-bold text-sm shadow-[0_0_10px_#800000]">
		  D
		</div>
		<span class="text-[#000a30] text-xs font-medium">Transform Your Ideas</span>
	  </div>
  
	</div>
  </div>
  
</div>
<!-- Fixed News Ticker -->



<!-- Animated Down Arrow Centered -->
<div class="absolute left-1/2 top-[550px] transform -translate-x-1/2">
	<div class="w-16 h-16 animate-bounce text-gray-800">
	  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
		<path stroke-linecap="round" stroke-linejoin="round" stroke-width="10" d="M19 9l-7 7-7-7" />
	  </svg>
	</div>
  </div>
  
<style>

.flash-image {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	object-fit: cover;
	/* opacity: 0; */
	/* animation rules removed for testing */
}


.flash-loop {
	position: relative;
	width: 100%;
	height: 380px;
	overflow: hidden;
}

.flash-image {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	object-fit: cover;
	opacity: 0;
	animation-duration: 6s;
	animation-timing-function: ease-in-out;
	animation-iteration-count: infinite;
}

.image1 {
	animation-name: flashInOut1;
}

.image2 {
	animation-name: flashInOut2;
}

@keyframes flashInOut1 {
	0%, 49.9% {
		opacity: 1;
	}
	50%, 100% {
		opacity: 0;
	}
}

@keyframes flashInOut2 {
	0%, 49.9% {
		opacity: 0;
	}
	50%, 100% {
		opacity: 1;
	}
}


.glow-yellow {
	background-color: #abc0c3;
	box-shadow: 
		0 0 12px 4px rgba(35, 16, 202, 0.6),  /* soft yellow glow */
		0 0 20px 6px rgba(255, 255, 100, 0.8); /* brighter outer glow */
	animation: yellowPulse 2s ease-in-out infinite;
}

.glow-orange {
	background-color: #ddff00;
	box-shadow: 
		0 0 12px 4px rgba(35, 16, 202, 0.6),  /* soft yellow glow */
		0 0 20px 6px rgba(255, 255, 100, 0.8); /* brighter outer glow */
	animation: yellowPulse 2s ease-in-out infinite;
}

.glow-blue {
	background-color: #6622db;
	box-shadow: 
		0 0 12px 4px rgba(35, 16, 202, 0.6),  /* soft yellow glow */
		0 0 20px 6px rgba(255, 255, 100, 0.8); /* brighter outer glow */
	animation: yellowPulse 2s ease-in-out infinite;
}

.glow-green {
	background-color: #f44004;
	box-shadow: 
		0 0 12px 4px rgba(35, 16, 202, 0.6),  /* soft yellow glow */
		0 0 20px 6px rgba(255, 255, 100, 0.8); /* brighter outer glow */
	animation: yellowPulse 2s ease-in-out infinite;
}
	
	
	
@keyframes scrollX {
	0% {
		transform: translateX(0%);
	}
	100% {
		transform: translateX(-50%);
	}
}

.animate-scrollX {
	animation: scrollX 10s linear infinite;
}


@keyframes yellowPulse {
	0% {
		box-shadow: 0 0 6px 2px rgba(238, 241, 241, 0.4), 0 0 14px 5px rgba(242, 244, 242, 0.5);
	}
	50% {
		box-shadow: 0 0 6px 2px rgba(235, 246, 233, 0.9), 0 0 28px 10px rgb(179, 169, 197);
	}
	100% {
		box-shadow: 0 0 6px 2px rgba(223, 216, 225, 0.4), 0 0 14px 5px rgba(42, 10, 77, 0.5);
	}
}



.fixed-band {
	position: fixed;
	bottom: 0;
	left: 0;
	width: 100%;
	height: 50px;
	background-color: black;
	color: white;
	display: flex;
	align-items: center;
	justify-content: center;
	z-index: 50;
}

.band-text {
	font-size: 14px;
	font-weight: 500;
	letter-spacing: 0.5px;
}

	:global(html) {
		scroll-behavior: smooth;
		background: white;
		
	}





	.image-scroll-wrapper {
	width: 100%;
	height: 300px;
	overflow: hidden;
	position: relative;
}

.image-list {
	display: flex;
	flex-direction: row;
	gap: 20px;
	animation: scrollLeft 20s linear infinite;
	width: max-content;
}

.image-list img {
	width: 300px;
	height: 300px;
	object-fit: cover;
	border-radius: 12px;
	box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* DELETE THIS to stop vertical auto scroll */
@keyframes scrollLeft {
	0% {
		transform: translateX(0%);
	}
	100% {
		transform: translateX(-50%);
	}
}


h1 {
    font-size: 2rem; /* Big font */
    font-weight: 400; /* Extra bold */
    color: #000A30; /* Deep blue */
    text-align: left;
 
    text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  @media (max-width: 768px) {
    h1 {
      font-size: 4.5rem; /* Responsive scaling */
    }

}
	p {
		position: relative;
		top: 23px;
		left: 15px;
		font-size: 14px;
		word-spacing: 6px;
		line-height: 28px;
	}
	button {
		all: unset; /* This resets everything so we can style from scratch */
		cursor: pointer;
		font-size: 12px;
		color: white;
		background-color: #000A30; /* Tailwind's blue-800 */
		padding: 12px 13px;
		border-radius: 8px;
		display: inline-flex;
		align-items: center;
		height: 18px;
		width: 77px;
		position: relative;
		left:14px;	
		bottom: 10PX;
		
		transition: background-color 0.5s ease;
	}

	button:hover {
		background-color: #1c3faa; /* slightly darker on hover */
	}

	svg {
		width: 12px;
		height: 12px;
		margin-left: 4px;
	}

	/* Optional: override notification dot positioning */
	button .absolute {
		display: none; /* Or adjust position as needed */
	}


	.group {
		padding: 0rem;
		transition: all 0.2s ease;
		margin-right: 20px;
	
	}
	.group .text-3xl {
		font-size: 1px;
	}
	.group .text-2xl {
		font-size: 15px;
	}
	.group .text-lg {
		font-size: 15px;
	}
	.grid {
		max-height: 800px;
	}
	main {
		height: 500px;
	}
	@keyframes bounce {
		0%, 100% {
			transform: translateY(0);
		}
		50% {
			transform: translateY(8px);
		}
	}
	.animate-bounce {
		animation: bounce 0.8s infinite;
	}
</style>
