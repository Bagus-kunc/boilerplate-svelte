<script lang="ts">
  import Navbar from '$lib/components/Navbar.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import Button from '$lib/components/Button.svelte';
  import FeatureCard from '$lib/components/FeatureCard.svelte';
  import { 
    Zap, 
    Shield, 
    Globe, 
    Cpu, 
    Layers, 
    MessageSquare,
    ChevronRight,
    Mail,
    Share2,
    Link
  } from 'lucide-svelte';

  const features = [
    {
      title: "Svelte 5 Runes",
      description: "Harness the power of fine-grained reactivity with the latest Svelte 5 engine.",
      icon: Zap
    },
    {
      title: "Tailwind 4 CSS",
      description: "Direct-to-CSS engine providing unmatched performance and modern styling.",
      icon: Cpu
    },
    {
      title: "TypeScript Core",
      description: "Full type safety integrated throughout the entire application lifecycle.",
      icon: Shield
    },
    {
      title: "Global Reach",
      description: "Built-in SEO and accessibility best practices for a worldwide audience.",
      icon: Globe
    },
    {
      title: "Component Driven",
      description: "Highly modular and reusable component architecture for scale.",
      icon: Layers
    },
    {
      title: "Modern Tooling",
      description: "Equipped with Vite, Vitest, and Playwright for professional dev cycles.",
      icon: MessageSquare
    }
  ];
</script>

<svelte:head>
  <title>SvelteCore | Premium Svelte 5 Boilerplate</title>
  <meta name="description" content="The ultimate premium starting point for modern Svelte 5 applications with Tailwind CSS 4." />
</svelte:head>

<main class="bg-brand-light">
  <Navbar />
  <Hero />

  <!-- Features Section -->
  <section id="features" class="py-32 px-6 bg-white overflow-hidden">
    <div class="container mx-auto">
      <div class="max-w-4xl mx-auto text-center mb-20 animate-fade-in">
        <h2 class="text-4xl lg:text-6xl font-display font-extrabold text-brand-dark mb-6 tracking-tight">
          Every tool you need to <span class="text-brand-primary">Ship Faster</span>.
        </h2>
        <p class="text-xl text-brand-dark/60 max-w-2xl mx-auto font-medium">
          Stop worrying about configuration and start building features with our carefully curated stack.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-7xl mx-auto">
        {#each features as feature, i}
          <FeatureCard {...feature} delay={i * 100} />
        {/each}
      </div>
    </div>
  </section>

  <!-- CTA Section -->
  <section class="py-32 px-6 premium-gradient">
    <div class="container mx-auto max-w-5xl text-center text-white">
      <h2 class="text-5xl lg:text-7xl font-display font-black mb-8 leading-tight animate-pulse-slow">
        Ready to build? <br /> Your future starts here.
      </h2>
      <p class="text-2xl text-white/80 max-w-3xl mx-auto mb-12 font-medium">
        Join 1,000+ developers building premium web experiences with SvelteCore.
      </p>
      <Button variant="invert" class="px-12 py-6 text-2xl font-black flex items-center justify-center gap-4 mx-auto">
        Join the Waitlist <ChevronRight size={32} />
      </Button>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-brand-dark py-20 px-6 border-t border-white/5">
    <div class="container mx-auto grid grid-cols-1 md:grid-cols-4 gap-12 text-white/60 mb-20">
      <div class="md:col-span-2">
        <div class="flex items-center gap-2 mb-8">
          <div class="w-8 h-8 premium-gradient rounded-lg flex items-center justify-center text-white font-bold text-lg">
            S
          </div>
          <span class="text-2xl font-display font-extrabold text-white">
            SVELTE<span class="text-brand-primary">CORE</span>
          </span>
        </div>
        <p class="max-w-md text-lg leading-relaxed mb-8">
          Crafting the next generation of web development tools for creators who want to make an impact.
        </p>
        <div class="flex gap-4">
          <a href="/" class="w-12 h-12 rounded-xl bg-white/5 hover:bg-white/10 flex items-center justify-center transition-all">
            <Mail size={24} />
          </a>
          <a href="/" class="w-12 h-12 rounded-xl bg-white/5 hover:bg-white/10 flex items-center justify-center transition-all">
            <Share2 size={24} />
          </a>
          <a href="/" class="w-12 h-12 rounded-xl bg-white/5 hover:bg-white/10 flex items-center justify-center transition-all">
            <Link size={24} />
          </a>
        </div>
      </div>
      
      <div>
        <h4 class="text-white font-display font-bold text-xl mb-8">Resource</h4>
        <ul class="space-y-4 text-lg">
          <li><a href="/" class="hover:text-brand-primary transition-all">Documentation</a></li>
          <li><a href="/" class="hover:text-brand-primary transition-all">Components</a></li>
          <li><a href="/" class="hover:text-brand-primary transition-all">Templates</a></li>
          <li><a href="/" class="hover:text-brand-primary transition-all">Changelog</a></li>
        </ul>
      </div>

      <div>
        <h4 class="text-white font-display font-bold text-xl mb-8">Company</h4>
        <ul class="space-y-4 text-lg">
          <li><a href="/" class="hover:text-brand-primary transition-all">About Us</a></li>
          <li><a href="/" class="hover:text-brand-primary transition-all">Careers</a></li>
          <li><a href="/" class="hover:text-brand-primary transition-all">Blog</a></li>
          <li><a href="/" class="hover:text-brand-primary transition-all">Contact</a></li>
        </ul>
      </div>
    </div>
    
    <div class="container mx-auto pt-10 border-t border-white/5 text-center text-white/20 font-medium">
      © 2026 SvelteCore. All rights reserved. Built with ❤️ for you.
    </div>
  </footer>
</main>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }
</style>
