<script>
  // No script needed
</script>

<div class="space-y-32 pb-32">
  <!-- Arkade Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Arkade</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Bitcoin capital markets infrastructure.</strong> Native platform for programmable transactions, custody-free liquidity, and scalable DeFi protocols built on Bitcoin's security.
      </p>
      <div class="flex flex-col gap-2">
        <a href="https://docs.arkadeos.com" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="https://docs.arkadeos.com" class="text-sm text-gray-400 hover:text-black transition-colors">View docs</a>
      </div>
    </div>
    <div class="bg-gray-50 rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Arkade Visualization -->
      <div class="relative w-full max-w-md">
        <div class="flex justify-between items-center">
          <!-- Central Hub -->
          <div class="w-16 h-16 bg-black rounded-lg flex items-center justify-center relative z-10">
            <svg width="32" height="32" viewBox="0 0 152 125" fill="white" xmlns="http://www.w3.org/2000/svg">
              <path d="M143.58 84.2131H151.874L141.028 72.9422C125.504 56.7801 104.026 47.6357 81.4839 47.6357H78.9319H73.4028H70.6382C48.309 47.6357 26.8304 56.7801 11.0937 72.9422L0.248047 84.2131H8.54176C30.871 84.2131 52.3495 75.0688 68.0863 58.9067L76.1674 50.613C71.4889 79.1093 30.871 124.193 30.871 124.193H76.38H121.889C121.889 124.193 81.6965 79.7473 76.5927 51.2509L84.0358 59.1193C99.5599 75.0688 121.038 84.2131 143.58 84.2131Z" fill="white"/>
            </svg>
          </div>
          
          <!-- Endpoints -->
          <div class="flex flex-col gap-3">
            {#each ['Liquidity', 'Trading', 'DeFi', 'Custody-free', 'Stablecoins', 'Derivatives', 'Programmable'] as item, i}
              <div class="flex items-center gap-4">
                <div class="w-24 h-[1px] bg-gradient-to-r from-primary-500/30 to-transparent transform rotate-180 origin-left"></div>
                <div class="flex items-center gap-2">
                  <div class="w-3 h-3 rounded-full bg-primary-500" style="opacity: {1 - i * 0.1}"></div>
                  <span class="text-xs font-medium text-gray-600">{item}</span>
                </div>
              </div>
            {/each}
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Ark Protocol Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Ark Protocol</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Custody-free liquidity.</strong> Revolutionary protocol enabling non-custodial liquidity pools on Bitcoin. Users maintain full control while accessing programmable finance infrastructure.
      </p>
      <div class="flex flex-col gap-2">
        <a href="https://docs.arklabs.xyz/ark.pdf" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Read whitepaper 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="https://docs.arkadeos.com" class="text-sm text-gray-400 hover:text-black transition-colors">View docs</a>
      </div>
    </div>
    <div class="bg-gradient-to-br from-primary-50 to-primary-100 rounded-3xl overflow-hidden min-h-[400px] relative">
      <div class="absolute inset-0 p-8 font-mono text-xs leading-none text-primary-600 opacity-40 break-all overflow-hidden select-none">
        {Array(2000).fill(0).map(() => Math.random().toString(36).substring(2, 3)).join('')}
      </div>
      <div class="absolute inset-0 bg-gradient-to-b from-transparent to-primary-100"></div>
    </div>
  </section>

  <!-- Developer Infrastructure Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Developer Infrastructure</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Built for Bitcoin developers.</strong> Comprehensive APIs, SDKs, and documentation to build scalable fintech apps with programmable Bitcoin transactions and non-custodial liquidity.
      </p>
      <div class="flex flex-col gap-2">
        <a href="https://docs.arkadeos.com" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Start building 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="https://blog.arklabs.xyz" class="text-sm text-gray-400 hover:text-black transition-colors">Read blog</a>
      </div>
    </div>
    <div class="bg-black rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Developer Interface Mockup -->
      <div class="relative w-full max-w-md">
        <div class="bg-gray-900 rounded-2xl border border-gray-800 shadow-2xl overflow-hidden">
          <!-- Terminal Header -->
          <div class="bg-gray-800 px-4 py-2 flex items-center gap-2 border-b border-gray-700">
            <div class="flex gap-1.5">
              <div class="w-3 h-3 rounded-full bg-red-500"></div>
              <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
              <div class="w-3 h-3 rounded-full bg-green-500"></div>
            </div>
            <span class="text-xs text-gray-400 ml-2">arkade-cli</span>
          </div>
          <!-- Terminal Content -->
          <div class="p-4 font-mono text-xs text-green-400 space-y-2">
            <div><span class="text-gray-500">$</span> arkade init</div>
            <div class="text-gray-400">✓ Connected to Bitcoin network</div>
            <div class="text-gray-400">✓ Liquidity pools active</div>
            <div><span class="text-gray-500">$</span> arkade deploy --protocol=defi</div>
            <div class="text-primary-400">→ Deploying to mainnet...</div>
            <div class="text-green-400">✓ Contract deployed</div>
            <div class="text-gray-400">Address: bc1q...</div>
            <div><span class="text-gray-500">$</span> <span class="animate-pulse">_</span></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>
