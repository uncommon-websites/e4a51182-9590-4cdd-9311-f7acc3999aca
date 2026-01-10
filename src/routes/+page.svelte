<script lang="ts">
	import Hero from "$lib/components/Hero.svelte";
	import FeatureSection from "$lib/components/FeatureSection.svelte";
	import Footer from "$lib/components/Footer.svelte";
	
	import NetWorthChart from "$lib/components/visuals/NetWorthChart.svelte";
	import AccountConnections from "$lib/components/visuals/AccountConnections.svelte";
	import SimpleDashboard from "$lib/components/visuals/SimpleDashboard.svelte";
	import RealTimeSync from "$lib/components/visuals/RealTimeSync.svelte";
	import Security from "$lib/components/visuals/Security.svelte";
	import Design from "$lib/components/visuals/Design.svelte";
</script>

<main class="bg-[#050505] min-h-screen text-white selection:bg-white/20">
	<Hero />
	
	<div class="mt-20 md:mt-40">
        <!-- Intro Section -->
        <div class="px-4 max-w-6xl mx-auto mb-32 relative">
             <div class="aspect-video bg-[#0A0A0A] rounded-lg border border-white/5 flex flex-col justify-center items-center p-6 md:p-10 relative overflow-hidden">
                 <div class="absolute inset-0 bg-gradient-to-b from-transparent to-black/50"></div>
                 <div class="relative z-10 text-center max-w-2xl">
                     <div class="flex items-center justify-center gap-3 text-white font-semibold mb-4">
                         <svg class="w-8 h-8" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M15.7321 18.4096C15.464 19.0054 15.1307 19.5889 14.7312 20.0937C18.0462 18.9764 20.4865 15.9576 20.7551 12.3344H19.5751C18.135 12.3344 16.9782 13.4839 16.7442 14.9048C16.5284 16.2146 16.1832 17.4073 15.7321 18.4096Z" fill="currentColor"/>
                            <path d="M13.122 12.3344C14.6297 12.3344 15.8632 13.5922 15.5862 15.0743C14.9847 18.2935 13.5564 20.5574 11.8901 20.5574C9.78166 20.5574 8.05421 16.9326 7.90082 12.3344H13.122Z" fill="currentColor"/>
                            <path d="M16.7748 8.62303C16.9953 10.0573 18.1574 11.2232 19.6085 11.2232H20.7689C20.5856 7.50155 18.1137 4.38174 14.7312 3.24164C15.1307 3.74646 15.464 4.32993 15.7321 4.9257C16.2052 5.97693 16.5618 7.23753 16.7748 8.62303Z" fill="currentColor"/>
                            <path d="M15.6307 8.5099C15.8829 9.98453 14.6549 11.2232 13.1588 11.2232H7.89462C7.99881 6.52003 9.74782 2.77795 11.8901 2.77795C13.599 2.77795 15.0576 5.15916 15.6307 8.5099Z" fill="currentColor"/>
                            <path d="M6.78316 11.2232C6.83365 8.81927 7.29225 6.60525 8.04807 4.9257C8.31614 4.32993 8.64941 3.74646 9.04901 3.24164C5.66642 4.38174 3.19455 7.50155 3.01129 11.2232H6.78316Z" fill="currentColor"/>
                            <path d="M3.02502 12.3344C3.29367 15.9576 5.73401 18.9764 9.04903 20.0937C8.64944 19.5889 8.31616 19.0054 8.0481 18.4096C7.31563 16.7819 6.86229 14.6523 6.78903 12.3344H3.02502Z" fill="currentColor"/>
                         </svg>
                         <span class="text-xl">Brand Foundation</span>
                     </div>
                     <p class="text-gray-400 text-lg">A single, purpose-built view of everything you own and owe.</p>
                 </div>
             </div>
             <div class="text-center mt-10 text-gray-500 text-sm flex flex-col items-center gap-2">
                 <span class="transform rotate-90">›</span>
                 See how we bring clarity to your finances.
             </div>
        </div>

		<FeatureSection 
			label="NET WORTH TRACKING"
			title="See your complete financial picture."
			description="Track your net worth across all accounts, investments, properties, and debts in one calm, beautiful view."
		>
			<SimpleDashboard />
		</FeatureSection>

		<FeatureSection 
			label="GROWTH OVER TIME"
			title="Watch your wealth grow."
			description="Visualize your financial progress with clear charts that show how your net worth changes over time."
		>
			<NetWorthChart />
		</FeatureSection>

		<FeatureSection 
			label="CONNECT EVERYTHING"
			title="All your accounts in one place."
			description="Banks, investments, credit cards, loans, real estate, and more. Connect everything you own and owe."
		>
			<AccountConnections />
		</FeatureSection>

		<FeatureSection 
			label="REAL-TIME UPDATES"
			title="Always up to date."
			description="Your balances sync automatically, so you always have an accurate view of your financial position."
		>
			<RealTimeSync />
		</FeatureSection>

		<FeatureSection 
			label="SIMPLE INTERFACE"
			title="Calm clarity, not chaos."
			description="A premium, distraction-free experience designed to reduce spreadsheet fatigue and financial anxiety."
		>
			<Design />
		</FeatureSection>

		<FeatureSection 
			label="SECURITY & PRIVACY"
			title="Bank-level security."
			description="Your financial data is encrypted and protected with the same security standards used by major banks."
		>
			<Security />
		</FeatureSection>
        
        <FeatureSection 
			label="BUILT BY EXPERTS"
			title="Founded by a fintech CTO."
			description="Created by Jon Adair, CTO of multiple fintech companies, with deep expertise in financial technology."
		>
			<div class="w-full h-full flex items-center justify-center">
				<div class="text-center">
					<div class="w-24 h-24 rounded-full bg-gradient-to-br from-gray-700 to-gray-800 mx-auto mb-4"></div>
					<div class="text-white font-semibold text-lg">Jon Adair</div>
					<div class="text-gray-400 text-sm">Founder & CTO</div>
				</div>
			</div>
		</FeatureSection>
	</div>

	<Footer />
</main>

