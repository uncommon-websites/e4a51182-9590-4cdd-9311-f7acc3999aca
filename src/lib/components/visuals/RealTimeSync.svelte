<script>
  import { onMount } from 'svelte';
  
  let pulseIndex = 0;
  
  onMount(() => {
    const interval = setInterval(() => {
      pulseIndex = (pulseIndex + 1) % 3;
    }, 1000);
    
    return () => clearInterval(interval);
  });
</script>

<div class="w-full h-full flex items-center justify-center">
  <div class="relative">
    <!-- Center node -->
    <div class="w-16 h-16 rounded-full bg-white flex items-center justify-center shadow-lg">
      <svg class="w-8 h-8 text-black" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M15.7321 18.4096C15.464 19.0054 15.1307 19.5889 14.7312 20.0937C18.0462 18.9764 20.4865 15.9576 20.7551 12.3344H19.5751C18.135 12.3344 16.9782 13.4839 16.7442 14.9048C16.5284 16.2146 16.1832 17.4073 15.7321 18.4096Z"
          fill="currentColor"
        />
        <path
          d="M13.122 12.3344C14.6297 12.3344 15.8632 13.5922 15.5862 15.0743C14.9847 18.2935 13.5564 20.5574 11.8901 20.5574C9.78166 20.5574 8.05421 16.9326 7.90082 12.3344H13.122Z"
          fill="currentColor"
        />
        <path
          d="M16.7748 8.62303C16.9953 10.0573 18.1574 11.2232 19.6085 11.2232H20.7689C20.5856 7.50155 18.1137 4.38174 14.7312 3.24164C15.1307 3.74646 15.464 4.32993 15.7321 4.9257C16.2052 5.97693 16.5618 7.23753 16.7748 8.62303Z"
          fill="currentColor"
        />
        <path
          d="M15.6307 8.5099C15.8829 9.98453 14.6549 11.2232 13.1588 11.2232H7.89462C7.99881 6.52003 9.74782 2.77795 11.8901 2.77795C13.599 2.77795 15.0576 5.15916 15.6307 8.5099Z"
          fill="currentColor"
        />
        <path
          d="M6.78316 11.2232C6.83365 8.81927 7.29225 6.60525 8.04807 4.9257C8.31614 4.32993 8.64941 3.74646 9.04901 3.24164C5.66642 4.38174 3.19455 7.50155 3.01129 11.2232H6.78316Z"
          fill="currentColor"
        />
        <path
          d="M3.02502 12.3344C3.29367 15.9576 5.73401 18.9764 9.04903 20.0937C8.64944 19.5889 8.31616 19.0054 8.0481 18.4096C7.31563 16.7819 6.86229 14.6523 6.78903 12.3344H3.02502Z"
          fill="currentColor"
        />
      </svg>
    </div>
    
    <!-- Orbiting nodes -->
    {#each Array(3) as _, i}
      <div 
        class="absolute w-10 h-10 rounded-full bg-[#1a1a1a] border-2 flex items-center justify-center transition-all duration-500"
        class:border-white={pulseIndex === i}
        class:border-white/20={pulseIndex !== i}
        class:scale-110={pulseIndex === i}
        style="
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%) rotate({i * 120}deg) translateY(-80px) rotate(-{i * 120}deg);
        "
      >
        <div class="w-2 h-2 rounded-full bg-white/50"></div>
      </div>
    {/each}
    
    <!-- Connection lines -->
    {#each Array(3) as _, i}
      <div 
        class="absolute h-px bg-gradient-to-r from-white/0 via-white/20 to-white/0 transition-opacity duration-500"
        class:opacity-100={pulseIndex === i}
        class:opacity-20={pulseIndex !== i}
        style="
          width: 80px;
          top: 50%;
          left: 50%;
          transform-origin: left center;
          transform: translateY(-50%) rotate({i * 120}deg);
        "
      ></div>
    {/each}
  </div>
</div>
