<div class="w-full h-full flex items-center justify-center p-8">
  <div class="w-full max-w-md space-y-4">
    <!-- Main net worth card -->
    <div class="bg-[#1a1a1a] rounded-lg p-6 border border-white/10">
      <div class="text-xs text-gray-500 uppercase tracking-wider mb-2">Net Worth</div>
      <div class="text-3xl font-bold text-white">$2,847,392</div>
      <div class="text-sm text-green-400 mt-1">↑ 12.4% this year</div>
    </div>
    
    <!-- Quick stats grid -->
    <div class="grid grid-cols-2 gap-4">
      <div class="bg-[#1a1a1a] rounded-lg p-4 border border-white/5">
        <div class="text-xs text-gray-500 mb-1">Assets</div>
        <div class="text-xl font-semibold text-white">$3.2M</div>
      </div>
      <div class="bg-[#1a1a1a] rounded-lg p-4 border border-white/5">
        <div class="text-xs text-gray-500 mb-1">Liabilities</div>
        <div class="text-xl font-semibold text-red-400">$352K</div>
      </div>
    </div>
    
    <!-- Mini account list -->
    <div class="space-y-2">
      {#each [
        { name: 'Vanguard', amount: '$847K', color: 'from-purple-600 to-purple-800' },
        { name: 'Fidelity', amount: '$1.2M', color: 'from-green-600 to-green-800' },
        { name: 'Chase', amount: '$13K', color: 'from-blue-600 to-blue-800' }
      ] as account}
        <div class="flex items-center justify-between bg-[#1a1a1a] rounded-lg p-3 border border-white/5">
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-full bg-gradient-to-br {account.color}"></div>
            <div class="text-sm text-gray-300">{account.name}</div>
          </div>
          <div class="text-sm font-semibold text-white">{account.amount}</div>
        </div>
      {/each}
    </div>
  </div>
</div>
