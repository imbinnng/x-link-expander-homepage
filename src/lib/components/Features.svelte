<script lang="ts">
  import { fly, slide } from 'svelte/transition';

  const features = [
    {
      title: 'Automatic Expansion',
      description: 'Automatically expands all t.co links on X.com pages in real-time as you scroll and new content loads.',
      icon: '⚡'
    },
    {
      title: 'Manual Control',
      description: 'Access popup interface to manually trigger expansion and clear history when needed.',
      icon: '🎮'
    },
    {
      title: 'Hover Information',
      description: 'Shows both original and expanded URLs when you hover over links for quick reference.',
      icon: '👁️'
    },
    {
      title: 'Privacy First',
      description: 'Only operates on X.com pages. No data collection, no external servers, complete local processing.',
      icon: '🔒'
    }
  ];
</script>

<section id="features" class="section">
  <div class="container">
    <div class="text-center mb-8">
      <h2 class="hero-title mb-4">
        Powerful Features
      </h2>
      <p class="hero-description mx-auto">
        Powerful features for enhanced X.com browsing experience
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
      {#each features as feature, i}
        <div 
          class="feature-card"
          in:fly={{ y: 20, delay: i * 100, duration: 600 }}
        >
          <div class="text-3xl mb-4">{feature.icon}</div>
          <h3 class="feature-title">{feature.title}</h3>
          <p class="feature-description">{feature.description}</p>
        </div>
      {/each}
    </div>
  </div>
</section>