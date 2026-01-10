<script lang="ts">
  import { fly } from 'svelte/transition';
  
  const installSteps = [
    {
      title: 'Download Extension',
      description: 'Download or clone this repository to get the extension files.'
    },
    {
      title: 'Open Chrome Extensions',
      description: 'Navigate to chrome://extensions/ in your Chrome browser.'
    },
    {
      title: 'Enable Developer Mode',
      description: 'Click the "Developer mode" toggle in the top right corner.'
    },
    {
      title: 'Load Extension',
      description: 'Click "Load unpacked" and select the extension directory.'
    }
  ];

  const permissions = [
    'storage: For saving statistics and history',
    'activeTab: For accessing current tab content', 
    'Host permissions for x.com, twitter.com, and t.co'
  ];
</script>

<section id="install" class="section">
  <div class="container">
    <div class="text-center mb-8">
      <h2 class="hero-title mb-4">
        Installation Guide
      </h2>
      <p class="hero-description mx-auto">
        Get X-Link Expander running in your Chrome browser in minutes
      </p>
    </div>

      <div class="max-w-4xl mx-auto" in:fly={{ y: 20, duration: 800 }}>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-12">
          {#each installSteps as step, i}
            <div 
              class="feature-card"
              in:fly={{ y: 20, delay: i * 100, duration: 600 }}
            >
              <div class="flex items-start gap-4">
                <div class="bg-gray-800 text-white rounded-full w-8 h-8 flex items-center justify-center flex-shrink-0 font-semibold">
                  {i + 1}
                </div>
                <div style="flex: 1; display: flex; align-items: center; justify-content: space-between;">
                  <div>
                    <h3 class="feature-title mb-2">{step.title}</h3>
                    <p class="feature-description">{step.description}</p>
                  </div>
                  {#if i === 0}
                    <a href="https://github.com/imbinnng/x-link-expander" target="_blank" rel="noopener" class="cta-button">
                      Download Now
                    </a>
                  {/if}
                </div>
              </div>
            </div>
          {/each}
        </div>

      <div class="feature-card mb-8">
        <h3 class="feature-title mb-4">Usage Instructions</h3>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div>
            <h4 class="text-white font-semibold mb-2">Automatic Mode</h4>
            <ul class="text-gray-400 space-y-1">
              <li>Navigate to any X.com page</li>
              <li>t.co links automatically expand</li>
              <li>Links highlighted with light blue background</li>
              <li>Continues working as you scroll</li>
            </ul>
          </div>
          <div>
            <h4 class="text-white font-semibold mb-2">Manual Control</h4>
            <ul class="text-gray-400 space-y-1">
              <li>Click extension icon in toolbar</li>
              <li>View status and statistics</li>
              <li>"Expand Links Now" for manual trigger</li>
              <li>"Clear History" to reset stats</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="feature-card">
        <h3 class="feature-title mb-4">Permissions Required</h3>
        <div class="code-block">
          <pre>{permissions.join('\n')}</pre>
        </div>
        <p class="text-gray-400 text-sm mt-4">
          The extension only operates on X.com/Twitter pages and does not collect personal data.
        </p>
      </div>

      <div class="mt-8 text-center">
        <a href="https://github.com/imbinnng/x-link-expander" target="_blank" rel="noopener" class="cta-button">
          Download from GitHub
        </a>
      </div>
    </div>
  </div>
</section>