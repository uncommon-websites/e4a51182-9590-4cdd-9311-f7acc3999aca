<div class="w-full h-full flex items-center justify-center">
  <div class="grid grid-cols-3 gap-6">
    {#each [
      { name: 'Banks', connected: true },
      { name: 'Investments', connected: true },
      { name: 'Credit Cards', connected: true },
      { name: 'Loans', connected: true },
      { name: 'Real Estate', connected: true },
      { name: 'Crypto', connected: false }
    ] as account}
      <div class="flex flex-col items-center gap-3 p-4 rounded-lg bg-[#1a1a1a] border border-white/5 hover:border-white/10 transition-all">
        <div class="w-12 h-12 rounded-full bg-gradient-to-br from-gray-700 to-gray-800 flex items-center justify-center">
          {#if account.connected}
            <svg class="w-6 h-6 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
            </svg>
          {:else}
            <div class="w-2 h-2 rounded-full bg-gray-600"></div>
          {/if}
        </div>
        <div class="text-xs text-gray-400 text-center">{account.name}</div>
      </div>
    {/each}
  </div>
</div>
