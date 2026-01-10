<script lang="ts">
  import { fly } from 'svelte/transition';
</script>

<section class="section">
  <div class="container">
    <div class="text-center" in:fly={{ y: -20, duration: 800 }}>
      <h1 class="hero-title mb-4">
        X.com Link Expander
      </h1>
      <p class="hero-description mx-auto mb-8">
        A Chrome browser extension that automatically expands t.co links on X.com (Twitter) pages, 
        showing the actual destination URLs instead of shortened links.
      </p>
      <div class="flex gap-4 justify-center">
        <a href="#install" class="cta-button">
          Install Extension
        </a>
        <a href="https://github.com/imbinnng/x-link-expander" target="_blank" rel="noopener" class="cta-button secondary">
          View on GitHub
        </a>
      </div>
    </div>
    
    <div class="mt-16 text-center" in:fly={{ y: 20, delay: 400, duration: 800 }}>
      <div class="code-block max-w-2xl mx-auto">
        <pre>{`Chrome Extension Usage:
1. Install the extension from Chrome Web Store
2. Navigate to any X.com page
3. t.co links automatically expand
4. Hover to see original/expanded URLs

Manual Control:
• Click extension icon for stats
• "Expand Links Now" for manual trigger
• "Clear History" to reset statistics`}</pre>
      </div>
    </div>
  </div>
</section>