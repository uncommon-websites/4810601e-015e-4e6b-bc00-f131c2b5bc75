<script>
  let activeTab = 'Trading';
  const tabs = ['Trading', 'Liquidity', 'DeFi', 'Custody-free', 'Derivatives', 'Stablecoins', 'Programmable', 'Capital Markets'];
</script>

<section class="pt-32 pb-20 px-6 max-w-7xl mx-auto">
  <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-16">
    <div>
      <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-black leading-[1.1] mb-8">
        Programmable Bitcoin <br /> capital markets
      </h1>
    </div>
    <div class="flex flex-col justify-end items-start lg:pl-12">
      <p class="text-xl text-gray-600 mb-6 max-w-md leading-relaxed">
        Native infrastructure for custody-free liquidity protocols. Build programmable finance on Bitcoin's security.
      </p>
      <a href="https://docs.arkadeos.com" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
        Explore Arkade 
        <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
      </a>
    </div>
  </div>

  <!-- Interactive Visual Section -->
  <div class="rounded-3xl overflow-hidden bg-gray-50 border border-gray-200 shadow-sm">
    <!-- Tabs -->
    <div class="flex overflow-x-auto scrollbar-hide border-b border-gray-200 bg-white/50 backdrop-blur-sm">
      {#each tabs as tab}
        <button 
          class="px-5 py-4 text-sm font-medium whitespace-nowrap transition-colors relative {activeTab === tab ? 'text-black' : 'text-gray-500 hover:text-gray-800'}"
          on:click={() => activeTab = tab}
        >
          {tab}
          {#if activeTab === tab}
            <div class="absolute bottom-0 left-0 right-0 h-0.5 bg-black"></div>
          {/if}
        </button>
      {/each}
    </div>

    <!-- Content Area -->
    <div class="relative h-[500px] bg-gradient-to-br from-gray-900 via-gray-800 to-black overflow-hidden group">
      <!-- Bitcoin Network Visualization -->
      <div class="absolute inset-0 opacity-20">
        <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, rgba(99, 179, 237, 0.15) 1px, transparent 0); background-size: 40px 40px;"></div>
      </div>
      
      <!-- Floating UI Card - Trading Interface -->
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-80 bg-white/10 backdrop-blur-md border border-white/20 rounded-2xl p-5 text-white shadow-2xl">
        <div class="flex justify-between items-center mb-6">
          <span class="text-xs font-medium text-white/80">Bitcoin Capital Markets</span>
          <div class="px-2 py-1 rounded bg-primary-500/20 text-primary-300 text-[10px] font-medium">LIVE</div>
        </div>
        
        <!-- Liquidity Pool -->
        <div class="flex items-center gap-3 mb-4">
          <div class="w-10 h-10 rounded-full bg-orange-500 flex items-center justify-center text-white shrink-0 font-bold text-sm">
            ₿
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline">
              <h3 class="text-sm font-medium truncate">BTC Liquidity Pool</h3>
              <span class="text-sm font-medium text-primary-300">Active</span>
            </div>
            <div class="flex justify-between items-baseline">
              <p class="text-xs text-white/60">Non-custodial</p>
              <p class="text-xs text-white/60">$2.4M TVL</p>
            </div>
          </div>
        </div>

        <!-- Trading Activity -->
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-full bg-primary-500 flex items-center justify-center text-white shrink-0">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"></polyline></svg>
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline">
              <h3 class="text-sm font-medium truncate">Programmable Trade</h3>
              <span class="text-sm font-medium">0.125 BTC</span>
            </div>
            <div class="flex justify-between items-baseline">
              <p class="text-xs text-white/60">Just executed</p>
              <div class="px-1.5 py-0.5 rounded bg-primary-500/20 text-[10px] font-medium text-primary-300">Arkade</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Code Block -->
    <div class="bg-gray-50 p-6 border-t border-gray-200 overflow-x-auto">
      <pre class="font-mono text-xs leading-relaxed text-gray-600">
<span class="text-gray-400 select-none">1</span>  <span class="text-gray-400"># Execute programmable Bitcoin transaction with Arkade</span>
<span class="text-gray-400 select-none">2</span>
<span class="text-gray-400 select-none">3</span>  <span class="text-purple-600">curl</span> <span class="text-blue-600">-X POST</span> <span class="text-green-600">'https://api.arkadeos.com/v1/transactions'</span> \
<span class="text-gray-400 select-none">4</span>    <span class="text-blue-600">-H</span> <span class="text-green-600">'Authorization: Bearer YOUR_API_KEY'</span> \
<span class="text-gray-400 select-none">5</span>    <span class="text-blue-600">-H</span> <span class="text-green-600">'Content-Type: application/json'</span> \
<span class="text-gray-400 select-none">6</span>    <span class="text-blue-600">-d</span> '&#123;
<span class="text-gray-400 select-none">7</span>      <span class="text-blue-800">"type"</span>: <span class="text-green-600">"liquidity_pool"</span>,
<span class="text-gray-400 select-none">8</span>      <span class="text-blue-800">"amount"</span>: <span class="text-green-600">"0.125"</span>,
<span class="text-gray-400 select-none">9</span>      <span class="text-blue-800">"custody"</span>: <span class="text-green-600">"non_custodial"</span>,
<span class="text-gray-400 select-none">10</span>     <span class="text-blue-800">"protocol"</span>: &#123;
<span class="text-gray-400 select-none">11</span>       <span class="text-blue-800">"network"</span>: <span class="text-green-600">"bitcoin"</span>,
<span class="text-gray-400 select-none">12</span>       <span class="text-blue-800">"programmable"</span>: <span class="text-orange-600">true</span></pre>
    </div>
  </div>
</section>
