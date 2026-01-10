<script>
    import Navbar from './Navbar.svelte';
</script>

<section class="relative min-h-screen flex flex-col items-center pt-32 overflow-hidden bg-[#050505]">
    <!-- Gradient overlay with brand colors -->
    <div class="absolute inset-0 bg-[radial-gradient(circle_at_top,_var(--tw-gradient-stops))] from-primary-900/30 via-[#1a202c] to-[#050505] pointer-events-none opacity-60"></div>
    
    <Navbar transparent={true} />
    
    <div class="text-center z-10 px-4 max-w-4xl mx-auto mt-10">
        <div class="mb-6 text-white/80 text-sm font-medium tracking-wide">Built by a fintech CTO.</div>
        <h1 class="text-5xl md:text-7xl font-medium text-white tracking-tight mb-8 leading-[1.1]">
            Quiet clarity for<br />
            everything you own and owe.
        </h1>
        
        <div class="flex items-center justify-center gap-6 mb-20">
            <a href="#get-started" class="bg-white text-black px-6 py-3 rounded-full font-semibold hover:bg-gray-100 transition-colors">Start tracking</a>
            <span class="text-white/70 text-sm font-medium">Simple. Calm. Complete.</span>
        </div>
    </div>

    <!-- Hero Dashboard Mockup -->
    <div class="relative w-full max-w-7xl mx-auto perspective-2000 z-10">
        <div class="transform rotate-x-20 rotate-y-minus-10 rotate-z-10 scale-90 translate-y-20 origin-top">
            <!-- Dashboard Card -->
            <div class="bg-[#1a1a1a] rounded-xl shadow-2xl overflow-hidden border border-white/10 relative">
                <!-- Header -->
                <div class="h-12 bg-[#1a1a1a] border-b border-white/5 flex items-center px-6 gap-4">
                    <div class="flex gap-2">
                        <div class="w-3 h-3 rounded-full bg-[#ff5f57]"></div>
                        <div class="w-3 h-3 rounded-full bg-[#febc2e]"></div>
                        <div class="w-3 h-3 rounded-full bg-[#28c840]"></div>
                    </div>
                    <div class="flex-1"></div>
                    <div class="text-xs text-gray-500">Net Worth</div>
                </div>
                
                <!-- Dashboard Content -->
                <div class="bg-[#0f0f0f] p-8">
                    <!-- Net Worth Display -->
                    <div class="mb-8 text-center py-6">
                        <div class="text-xs text-gray-500 uppercase tracking-wider mb-2">Total Net Worth</div>
                        <div class="text-5xl font-bold text-white mb-1">$2,847,392</div>
                        <div class="text-sm text-green-400">+$47,392 this month</div>
                    </div>
                    
                    <!-- Account List -->
                    <div class="space-y-3">
                        {#each [
                            { name: 'Chase Checking', amount: '$12,847', type: 'cash' },
                            { name: 'Vanguard 401(k)', amount: '$847,392', type: 'investment' },
                            { name: 'Fidelity Brokerage', amount: '$1,247,392', type: 'investment' },
                            { name: 'Home (Estimated)', amount: '$950,000', type: 'property' },
                            { name: 'Mortgage', amount: '-$347,239', type: 'debt' },
                            { name: 'Tesla Model 3', amount: '$42,000', type: 'vehicle' },
                            { name: 'Amex Platinum', amount: '-$4,847', type: 'debt' },
                            { name: 'Emergency Fund', amount: '$50,000', type: 'cash' }
                        ] as account}
                            <div class="flex items-center justify-between px-4 py-3 bg-[#1a1a1a] rounded-lg border border-white/5 hover:bg-white/5 transition-colors group">
                                <div class="flex items-center gap-3">
                                    <div class="w-8 h-8 rounded-full bg-gradient-to-br from-gray-700 to-gray-800 flex-shrink-0"></div>
                                    <div class="text-sm text-gray-300">{account.name}</div>
                                </div>
                                <div class="text-sm font-semibold {account.amount.startsWith('-') ? 'text-red-400' : 'text-white'}">{account.amount}</div>
                            </div>
                        {/each}
                    </div>
                </div>
                
                <!-- Fade out at bottom of card -->
                <div class="absolute bottom-0 left-0 right-0 h-32 bg-gradient-to-t from-[#050505] to-transparent"></div>
            </div>
        </div>
    </div>
</section>

<style>
    .perspective-2000 {
        perspective: 2000px;
    }
    .rotate-x-20 {
        transform: rotateX(20deg) rotateY(-10deg) rotateZ(5deg);
    }
</style>
