<script>

function goTo(page) {
        window.location.href = page;
    }
    const stats = [
        { icon: '⩇', value: '10+', label: 'Years Experience' },
        { icon: '𖣠 ', value: '50+', label: 'Industry Partners' },
        { icon: '✧', value: '100+', label: 'Success Stories' },
        { icon: ' ⌕', value: '25+', label: 'Expert Mentors' }
    ];

    const studentStartups = [
        { name: 'Miceter.Tech', description: 'AI Solutions',  status: 'Active' },
        { name: 'Gananiya', description: 'Eco-Friendly Products',  status: 'Active' },
        { name: 'Koko Shell', description: 'Decoratives',  status: 'Active'  },
        { name: 'Naticutz', description: 'Animal Husbandry',  status: 'Active'  }
    ];

    const achievements = [
        { year: '2024', title: 'Innovation Excellence Award' },
        { year: '2023', title: 'Best Incubator Program' },
        { year: '2023', title: 'Top Research Institution' }
    ];

    const facultyAchievements = [
        {
            name: 'Industry 1',
           /// title: 'Head of Innovation',
            achievements: [
                'Research Excellence Award 2024',
                'Published in Nature Technology',
                '5 Patents Filed'
            ],
           /// image: 'src/lib/logos/image-2[1].png'
        },

        {
            name: 'Industry 2',
           /// title: 'Head of Innovation',
            achievements: [
                'Research Excellence Award 2024',
                'Published in Nature Technology',
                '5 Patents Filed'
            ],
           /// image: 'src/lib/logos/image-2[1].png'
        },
        {
            name: 'Industry 3',
           /// title: 'Lead Research Mentor',
            achievements: [
                'Best Mentor Award 2023',
                'Industry Innovation Prize',
                '10+ Startups Mentored'
            ],
           /// image: 'src/lib/logos/WhatsApp Image 2025-04-02 at 08.45.11_4c753bca.jpg'
        },
        {
            name: 'Industry 4',
           /// title: 'Lead Scientist',
            achievements: [
                'Tech Innovation Award',
                'IEEE Fellow',
                '15+ Research Papers'
            ],
           /// image: 'https://media.licdn.com/dms/image/v2/D5603AQGPKisYexfYeA/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1696911278245?e=1749081600&v=beta&t=Bm9ZB_4xK7LLJvie0WdZJ32s8T8AOO-ua-66aw_x0JE'
        },

      
       
    ];
</script>

<link href="https://fonts.googleapis.com/css2?family=Anton&display=swap" rel="stylesheet">
<div class="w-full h-[50px] bg-[#17194a] text-white flex items-center overflow-hidden">
  <!-- Static "News Updates" -->
  <div class="w-[20%] flex items-center justify-center text-[#f6d287] font-semibold">
    News Updates
  </div>

  <!-- Scrolling Marquee -->
  <div class="w-[80%] marquee-container overflow-hidden relative">
    <div class="marquee-content flex gap-6 animate-marquee whitespace-nowrap">
      <span class="news-span">Student Startups Raised $5M+ This Quarter</span>
      <span class="news-span">New Startups launching soon!</span>
      <span class="news-span">Student Startups Raised $5M+ This Quarter</span>
      <span class="news-span">New Startups launching soon!</span>
      <span class="news-span">Student Startups</span>
      <span class="news-span">Scholarships available for meritorious students</span>
      <span class="news-span">New Startups launching soon!</span>
      <span class="news-span">Student Startups</span>
      <span class="news-span">Scholarships available for meritorious students</span>
      <span class="news-span">New Startups launching soon!</span>
      <span class="news-span">Student Startups Raised $5M+ This Quarter</span>
      <span class="news-span">New Startups launching soon!</span>
      <span class="news-span">Student Startups Raised $5M+ This Quarter</span>
     
    </div>
  </div>
</div>


<div class="relative bg-white">
    <!-- Hero Section with Animated Background -->
    <section class="relative  pt-0 pb-20">
        <div class="absolute inset-0 -z-10">
            <div class="absolute inset-0 bg-[linear-gradient(to_right,#80808012_1px,transparent_1px),linear-gradient(to_bottom,#80808012_1px,transparent_1px)] bg-[size:24px_24px]"></div>
            <div class="absolute left-0 top-24 h-72 w-72 rounded-full bg-blue-200 opacity-20 blur-[100px]"></div>
            <div class="absolute right-0 top-96 h-72 w-72 rounded-full bg-cyan-200 opacity-20 blur-[100px]"></div>
        </div>

        <div class="container relative mx-5 px-4 ">

            <div class="grid items-center gap-10 lg:grid-cols-2">
                <div>
                    <div class="inline-flex items-center rounded-full border border-blue-100 bg-blue-50/50 pt-9 py-1">
                        <span class="text-sm font-medium text-blue-800"></span>
                    </div>
                    <h1 class="mt-10 text-2xl font-bold tracking-tight text-slate-900 lg:text-2xl xl:text-2xl ">
                        Shaping the Future 
                        <span class="relative whitespace-nowrap">
                           
                            <span class="relative text-blue-400">   Through Innovation</span>
                  
                 
                         
                        </span>
                    </h1>
                    <p class="mt-10 text-m leading-relaxed text-slate-600 ">
                        Where groundbreaking ideas meet world-class expertise. <br>Join us in shaping tomorrow's technology and innovations.
                    </p>
                    <div class="mt-14 flex flex-wrap gap-6">
                        <button class="group relative overflow-hidden rounded-lg bg-slate-800 px-2 py-2 transition-all hover:ring-2 hover:ring-blue-400 hover:ring-offset-2">
                            <span class="relative z-10 font-8xs text-white">Explore Programs</span>
                            <div class="absolute inset-0 -z-10 bg-gradient-to-r from-blue-600 to-cyan-600 opacity-0 transition-opacity group-hover:opacity-100"></div>
                        </button>
                        <button on:click={() => goTo('/listoffaculty')} class="group rounded-lg border-1 border-slate-200 px-2 py-1 font-medium text-slate-600 transition-all hover:border-blue-400 hover:bg-blue-50">
                             Meet Our Faculty
                        </button>
                        
                    </div>
                </div>
                <div class="relative grid grid-cols-4 gap-4 lg:mt-0 top-10 mb-10">
                  {#each stats as stat}
                      <div class="group rounded-xl border border-white bg-white p-4 shadow-sm backdrop-blur-sm transition-all duration-300 ease-in-out hover:-translate-y-1  hover:bg-yellow-100">
                          <div class="mb-3 inline-block rounded-lg bg-white-500 p-3 transition-colors duration-300 group-hover:bg-white-500">
                              <span class="text-5xl">{stat.icon}</span> <!-- Increased icon size -->
                          </div>
                          <p class="text-sm font-bold text-slate-800">{stat.value}</p>
                          <p class="mt-2 text-sm text-slate-500">{stat.label}</p>
                      </div>
                  {/each}
              </div>
              
                
                
            </div>
        </div>
    </section>

<!-- Wrapper -->
<div class="w-full h-[280px] bg-gray-100 flex items-center overflow-hidden relative">

    <!-- Fixed Text -->
    <div class="w-[20%] flex justify-center items-center text-2xl bg-grey-400 text-black-600 font-semibold px-4 z-10">
       <h1 class='red'>Student Startups</h1> 
      </div>
      
      
  
      <div class="w-[80%] overflow-hidden">
        <div class="whitespace-nowrap animate-scroll-marquee flex items-center space-x-16">
          <img src="static/lib/logos/11.png" alt="Logo 1" class="h-47 rounded-lg" />
          <img src="/lib/logos/22.png" alt="Logo 2" class="h-47 rounded-lg" />
          <img src="/lib/logos/33.png" alt="Logo 3" class="h-47 rounded-lg" />
          <img src="/lib/logos/44.png" alt="Logo 4" class="h-47 rounded-lg" />
          <img src="/lib/logos/55.png" alt="Logo 5" class="h-47 rounded-lg" />
          <img src="/lib/logos/66.png" alt="Logo 6" class="h-47 rounded-lg" />
          <!-- Duplicates -->
          <img src="/lib/logos/11.png" alt="Logo 1" class="h-47 rounded-lg" />
          <img src="/lib/logos/22.png" alt="Logo 2" class="h-47 rounded-lg" />
          <img src="/lib/logos/33.png" alt="Logo 3" class="h-47 rounded-lg" />
          <img src="/lib/logos/44.png" alt="Logo 4" class="h-47 rounded-lg" />
          <img src="/lib/logos/55.png" alt="Logo 5" class="h-47 rounded-lg" />
          <img src="/lib/logos/66.png" alt="Logo 6" class="h-47 rounded-lg" />
        </div>
      </div>
      
    
  </div>
  
      
      
   <!-- Faculty Section -->
   <section class="relative py-2 bg-gradient-to-b from-transparent via-blue-50/50 to-transparent">
    <div class="container mx-auto px-4">
      <div class="mt-6 mb-10 text-left">
        <h2 class=" font-bold tracking-tight text-slate-900 lg:text-2xl xl:text-2xl ">
            Meet Our Industry <span class="relative bg-blue-400"></span>Experts
        </h2>
        <div class="flex items-center gap-2 mt-2">
            <!-- Two dots -->
            <span class="w-3 h-3 bg-blue-900 rounded-full"></span>
            <span class="w-3 h-3 bg-blue-900 rounded-full"></span>
            <!-- Line -->
            <div class="w-[100px] h-1 bg-blue-900 ml-2"></div>
        </div>
    </div>
    
        <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-4 mb-10">
            {#each facultyAchievements as faculty}
                <div class="group relative rounded-xl border border-slate-100 bg-white p-4 shadow-sm transition-all hover:-translate-y-1 hover:shadow-lg duration-300 ease-in-out">

                    <!-- 🔽 Add your PNG here -->
                    <img 
                        src="\lib\logos\istockphoto-1075374570-612x612.jpg" 
                        alt="Top Left PNG"
                        class="absolute top-8 left-7 h-20 w-20 mr-10 border-2 border-black rounded object-cover"
                    />

                    

                    <!-- Image + Industry text -->
                   

                    <!-- Name and Title -->
                 

                    <!-- Achievements -->
                    <div class="space-y-2 mt-30">
                        {#each faculty.achievements as achievement}
                            <div class="flex items-center gap-2 rounded-lg bg-slate-50 px-3 py-2 text-sm text-slate-600">
                                <svg class="h-4 w-4 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                          d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                </svg>
                                {achievement}
                            </div>
                        {/each}
                    </div>
                </div>
            {/each}
        </div>
    </div>
</section>


 
     <!-- <section class="relative py-12">
        <div class="container mx-auto px-6">
            <div class="mb-16">
                <span class="mb-4 inline-block rounded-full bg-blue-100 px-3 py-1 text-sm font-medium text-blue-800">
                    Success Stories
                </span>
                <h2 class="text-4xl font-bold text-slate-900">Student Startups</h2>
            </div>
            <div class="grid gap-6 lg:grid-cols-2">
                {#each studentStartups as startup}
                    <div class="group relative overflow-hidden rounded-2xl border border-slate-100 bg-white p-8 shadow-sm transition-all hover:-translate-y-1 hover:shadow-lg">
                        <div class="flex items-start justify-between">
                            <div>
                                <h3 class="text-xl font-semibold text-slate-900">{startup.name}</h3>
                                <p class="mt-2 text-slate-600">{startup.description}</p>
                            </div>
                            <div class="flex flex-col items-end gap-2">
                                <span class="inline-flex items-center rounded-full bg-blue-50 px-3 py-1 text-sm font-medium text-blue-700">
                                    {startup.status}
                                </span>
                                <span class="text-sm text-slate-500">{startup.year}</span>
                            </div>
                        </div>
                        <div class="absolute bottom-0 left-0 h-1 w-0 bg-gradient-to-r from-blue-500 to-cyan-500 transition-all duration-300 group-hover:w-full"></div>
                    </div>
                {/each}
            </div>
        </div>
    </section>


-->
</div>




<style>
@keyframes marquee {
  0% { transform: translateX(100%); }
  100% { transform: translateX(-100%); }
}

.news-span {
  min-width: max-content;
  display: inline-block;
  letter-spacing: 1px;
  white-space: nowrap;
  padding-right: 3rem;
}

.marquee-content {
  animation: marquee 70s linear infinite;
}


.marquee {
    width: 100%;
    overflow: hidden;
    position: relative;
  }

  .marquee-content {
    display: inline-flex;
    white-space: nowrap;
  }

  .logo {
    height: 80px;
    margin: 0 2rem;
  }
  @keyframes scroll-marquee {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(-100%);
  }
}

.animate-scroll-marquee {
  animation: scroll-marquee 50s linear infinite;
}


  .animate-slow-marquee {
    animation: scroll-marquee 50s linear infinite;
  }

  @media (max-width: 768px) {
    .logo {
      height: 60px;
      margin: 0 1rem;
    }
  }

.marquee-container {
  position: relative;
  overflow: hidden;
  height: 100%;
  display: flex;
  align-items: center;
}



@keyframes scroll-marquee {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(-100%);
  }
}

@keyframes slow-marquee {
  0%   { transform: translateX(0%); }
  100% { transform: translateX(-50%); }
}

.animate-slow-marquee {
  animation: slow-marquee 30s linear infinite;
}


h1,h2{
  font-size: 1.6rem;
    font-weight: 700;
    letter-spacing: 2px;
    font-family: 'source sans pro';
    color: #000A30;
    max-width: 1200px;
    line-height: 1;
    margin-bottom: 1.5rem;



}
    p {
		position: relative;
	    top:12px;
		font-size: 17px;
		word-spacing: 6px;
		line-height: 28px;
        font-family: 'source sans pro';
	}

    
	

  .red{
    font-size: 1.2rem; /* Big font */
    font-weight: 500; /* Extra bold */
    color: #000A30; /* Deep blue */
    text-align: center;
   
    text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
    font-family: 'Poppins', Tahoma, Geneva, Verdana, sans-serif;
  }

  

  @media (max-width: 768px) {
    h1 {
      font-size: 2.6rem;
    }
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
		width: 100px;
		position: relative;

		top:20PX;
		
		transition: background-color 0.5s ease;
	}

	button:hover {
		background-color: #1c3faa; /* slightly darker on hover */
	}

    </style>
    