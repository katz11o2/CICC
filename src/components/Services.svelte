<script>
	import { fly, fade } from 'svelte/transition';
	import { onMount } from 'svelte';

	let isVisible = false;

	onMount(() => {
		isVisible = true;
	});

	const services = [
		{
			title: 'Industry Problem Solving',
			description:
				'Transform complex business challenges into opportunities with our cutting-edge technological solutions and expert guidance.',
			icon: '🎯',
		
		
		},
		{
			title: 'R&D Partnership',
			description:
				'Access world-class research facilities and collaborate with leading experts to drive innovation in your field.',
			icon: '🔬'
			
		},
		{
			title: 'Innovation Support',
			description:
				'Get comprehensive support throughout your innovation journey, from initial concept to market success.',
			icon: '💡',
			
		}
	];
</script>

<section class="bg-white py-16 px-6 text-center">
  <div class="max-w-6xl mx-auto">
    <h2 class="text-4xl md:text-5xl font-bold">
      Transform Your Ideas Into <span class="text-blue-500">Innovation Reality</span>
    </h2>
    <p class="mt-4 text-gray-600 max-w-2xl mx-auto">
      Partner with us to access world-class resources, expert guidance, and comprehensive support to bring your innovations to life.
    </p>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-12">
      {#each services as service}
        <div class="border rounded-lg p-6 shadow-md hover:shadow-xl transition-all">
          <div class="text-4xl mb-4">{service.icon}</div>
          <h3 class="text-xl font-semibold mb-2">{service.title}</h3>
          <p class="text-sm text-gray-600 mb-4">{service.description}</p>
          <ul class="text-sm text-gray-800 space-y-1 mb-6">
            {#each service.points as point}
              <li>{point}</li>
            {/each}
          </ul>
         
        </div>
      {/each}
    </div>
  </div>
</section>




<style>
	section {
		min-height: 100vh;
		perspective: 800px;
	}

	h1,h2,p,h3 {
		color: #000A30;
	}
</style>
