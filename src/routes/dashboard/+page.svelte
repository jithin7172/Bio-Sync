<script>
    const stats = [
      { title: 'FFM', value: '55' },
      { title: 'BMR', value: '1260.5' },
      { title: 'TBW', value: '1260.5' }
    ];
  </script>
  
  <div class="min-h-screen bg-gray-50">
    <div class="p-4 md:p-6 lg:p-8">
      <nav class="flex flex-wrap gap-4 mb-12">
        <button class="px-8 py-3 rounded-full text-lg font-medium shadow-sm bg-[#0a0f15] text-white hover:opacity-90 transition-opacity w-full sm:w-auto">
          Dashboard
        </button>
        <button class="px-8 py-3 rounded-full text-lg font-medium shadow-sm bg-white text-gray-600 hover:bg-gray-50 transition-colors w-full sm:w-auto">
          Diet Plan
        </button>
      </nav>
  
      <header class="mb-12">
        <h1 class="text-4xl text-[#4867AA] font-medium mb-2">Overview</h1>
        <h2 class="text-4xl text-[#9096A3] font-normal">Patient Health</h2>
      </header>
  
      <div class="md:relative h-[70vh] flex flex-col md:flex-row gap-8">
        <div class="flex justify-center items-center w-full md:w-1/3 max-w-[500px] min-w-[200px] mx-auto">
          <img 
            src="/images/char.png" 
            alt="Character" 
            class="md:absolute md:w-[580px] md:-b-[80px] w-full h-auto object-contain animate-float filter drop-shadow-lg transition-all duration-300 hover:scale-105"
          >
        </div>
  
        <main class="grid grid-cols-1 w-full md:grid-cols-2 lg:grid-cols-2 gap-8 flex-grow max-w-[1200px]">
          <!-- BMI Card -->
          <div class="bg-[#0a0f15] text-white p-8 rounded-3xl shadow-lg hover:shadow-xl transition-shadow">
            <p class="text-xl opacity-90 mb-8 leading-relaxed">
              Your current BMI is very good, and you seem to be having a healthy body
            </p>
            <div class="text-6xl font-medium text-green-400">23.6</div>
          </div>
  
          <!-- Fat Percentage Card -->
          <div class="bg-white p-8 rounded-3xl shadow-lg hover:shadow-xl transition-shadow">
            <p class="text-xl text-gray-500 mb-4">Total Fat %</p>
            <div class="text-6xl font-medium text-gray-900">16%</div>
          </div>
  
          <!-- Stats Grid -->
         <div class="flex flex-col md:flex-row gap-4 w-full col-span-full">
            {#each stats as stat}
              <div class="flex-1 bg-white p-7 rounded-3xl shadow-lg hover:shadow-xl transition-shadow">
                <h3 class="text-2xl text-gray-900 font-medium mb-2">{stat.title}</h3>
                <p class="text-gray-400 mb-3">your {stat.title} is</p>
                <div class="text-4xl font-medium text-gray-900">{stat.value}</div>
              </div>
            {/each}
          </div>
        </main>
      </div>
    </div>
  </div>
  
  <style>
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
    }
  
    .animate-float {
      animation: float 6s ease-in-out infinite;
    }
  </style>