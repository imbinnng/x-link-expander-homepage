<script lang="ts">
  import { fly } from 'svelte/transition';
  
  let isHovering = false;
  const githubUrl = 'https://github.com/imbinnng/x-link-expander';
  const shortUrl = 'https://t.co/abcdef890';
</script>

<section class="section">
  <div class="container">
    <div class="text-center mb-8">
      <p class="hero-description mx-auto">
        Hover over the t.co link to see how X-Link Expander reveals the actual destination
      </p>
    </div>

    <div class="max-w-2xl mx-auto" in:fly={{ y: 20, duration: 800 }}>
      <div class="feature-card">
        <div class="mb-4">
          <h3 class="text-white font-semibold mb-4">Try hovering over this X.com link:</h3>
          
          <div 
            class="relative inline-block"
            on:mouseenter={() => isHovering = true}
            on:mouseleave={() => isHovering = false}
          >
            <!-- Original t.co link -->
            <a 
              href={githubUrl} 
              target="_blank" 
              rel="noopener"
              class="link"
            >
              {shortUrl}
            </a>
            
            <!-- Expanded popover -->
            {#if isHovering}
              <div 
                class="popover"
                style="margin-top: -5em;" 
                in:fly={{ y: -10, duration: 200 }}
              >
                <div class="popover-arrow"></div>
                <div class="text-xs text-gray-400 mb-2">Link expanded:</div>
                <a 
                  href={githubUrl} 
                  target="_blank" 
                  rel="noopener"
                  class="text-green-400 hover:text-green-300 text-sm font-mono break-all"
                >
                  {githubUrl}
                </a>
              </div>
            {/if}
          </div>
        </div>

        <div class="border-t border-gray-800 pt-4">
          <div class="flex items-center gap-2 mb-2">
            <div class="w-3 h-3 bg-green-400 rounded-full animate-pulse"></div>
            <span class="text-green-400 text-sm font-medium">Link expansion active</span>
          </div>
          <p class="text-gray-400 text-sm">
            X-Link Expander automatically detects and expands t.co links on X.com pages, 
            showing you the actual destination before you click.
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .link {
    color: #1e40af;
    text-decoration: underline;
    transition: color 0.2s ease;
  }

  .link:hover {
    color: #1d4ed8;
    text-decoration: none;
  }

  .popover {
    position: absolute;
    left: 0;
    top: calc(100% + 4px);
    padding: 16px;
    background: rgba(17, 24, 39, 0.95);
    backdrop-filter: blur(8px);
    border: 1px solid rgba(75, 85, 99, 0.5);
    border-radius: 12px;
    box-shadow: 
      0 4px 6px -1px rgba(0, 0, 0, 0.1),
      0 2px 4px -1px rgba(0, 0, 0, 0.06),
      0 0 0 1px rgba(255, 255, 255, 0.05);
    z-index: 50;
    min-width: 300px;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  }

  .popover-arrow {
    position: absolute;
    top: -7px;
    left: 16px;
    width: 14px;
    height: 14px;
    background: rgba(17, 24, 39, 0.95);
    border: 1px solid rgba(75, 85, 99, 0.5);
    border-right: none;
    border-bottom: none;
    transform: rotate(45deg);
  }

  .animate-pulse {
    animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
  }

  @keyframes pulse {
    0%, 100% {
      opacity: 1;
    }
    50% {
      opacity: 0.5;
    }
  }
</style>