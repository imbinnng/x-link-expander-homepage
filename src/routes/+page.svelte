<script lang="ts">
  import Navbar from '$lib/components/Navbar.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import Demo from '$lib/components/Demo.svelte';
  import Features from '$lib/components/Features.svelte';
  import Installation from '$lib/components/Installation.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  <title>X-Link Expander - Expand Your Links</title>
  <meta name="description" content="A powerful tool to expand and analyze shortened URLs" />
</svelte:head>

<div class="min-h-screen bg-black text-white">
  <Navbar />
  <main>
    <Hero />
    <Demo />
    <Features />
    <Installation />
  </main>
  <Footer />
</div>