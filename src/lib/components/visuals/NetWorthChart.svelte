<div class="w-full h-full flex items-center justify-center">
  <div class="w-full max-w-2xl px-8">
    <!-- Simple line chart visualization -->
    <div class="relative h-48">
      <!-- Y-axis labels -->
      <div class="absolute left-0 top-0 bottom-0 flex flex-col justify-between text-xs text-gray-600">
        <span>$3M</span>
        <span>$2M</span>
        <span>$1M</span>
        <span>$0</span>
      </div>
      
      <!-- Chart area -->
      <div class="ml-12 h-full relative">
        <!-- Grid lines -->
        {#each Array(4) as _, i}
          <div class="absolute left-0 right-0 border-t border-white/5" style="top: {i * 33.33}%"></div>
        {/each}
        
        <!-- Line chart path -->
        <svg class="absolute inset-0 w-full h-full" viewBox="0 0 400 200" preserveAspectRatio="none">
          <defs>
            <linearGradient id="chartGradient" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" style="stop-color:rgb(139, 92, 246);stop-opacity:0.3" />
              <stop offset="100%" style="stop-color:rgb(139, 92, 246);stop-opacity:0" />
            </linearGradient>
          </defs>
          
          <!-- Area under the line -->
          <path
            d="M 0 180 L 0 120 Q 100 100, 200 80 T 400 40 L 400 180 Z"
            fill="url(#chartGradient)"
          />
          
          <!-- Line -->
          <path
            d="M 0 120 Q 100 100, 200 80 T 400 40"
            stroke="rgb(139, 92, 246)"
            stroke-width="2"
            fill="none"
          />
          
          <!-- Data points -->
          {#each [
            { x: 0, y: 120 },
            { x: 100, y: 100 },
            { x: 200, y: 80 },
            { x: 300, y: 60 },
            { x: 400, y: 40 }
          ] as point}
            <circle cx={point.x} cy={point.y} r="4" fill="white" />
          {/each}
        </svg>
        
        <!-- X-axis labels -->
        <div class="absolute -bottom-6 left-0 right-0 flex justify-between text-xs text-gray-600">
          <span>Jan</span>
          <span>Mar</span>
          <span>May</span>
          <span>Jul</span>
          <span>Sep</span>
        </div>
      </div>
    </div>
  </div>
</div>
