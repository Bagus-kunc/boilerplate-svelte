<script lang="ts">
  import Button from './Button.svelte';
</script>

<section class="relative min-h-screen flex items-center justify-center overflow-hidden bg-brand-dark pt-20">
  <!-- Hero Background Image with Overlay -->
  <div class="absolute inset-0 z-0">
    <img 
      src="/hero-bg.png" 
      alt="Abstract Background" 
      class="w-full h-full object-cover opacity-60 scale-105 animate-pulse-slow"
    />
    <div class="absolute inset-0 bg-gradient-to-t from-brand-dark via-brand-dark/40 to-transparent"></div>
    <div class="absolute inset-0 bg-gradient-to-r from-brand-dark/80 via-transparent to-brand-dark/80"></div>
  </div>

  <div class="container mx-auto px-6 relative z-10 text-center">
    <!-- Badge -->
    <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full glass mb-8 animate-float">
      <span class="w-2 h-2 rounded-full bg-brand-primary animate-ping"></span>
      <span class="text-brand-primary font-bold text-sm tracking-widest uppercase">New Svelte 5 Boilerplate</span>
    </div>

    <!-- Title -->
    <h1 class="text-6xl lg:text-8xl font-display font-extrabold text-white mb-6 leading-tight tracking-tighter">
      Build the <span class="text-transparent bg-clip-text premium-gradient">Future</span> <br /> 
      of the Web
    </h1>

    <!-- Subtitle -->
    <p class="text-xl text-white/70 max-w-2xl mx-auto mb-10 leading-relaxed font-medium">
      A premium starting point for your next Svelte 5 project. 
      Experience the power of Runes, Tailwind 4, and high-performance tooling out of the box.
    </p>

    <!-- CTAs -->
    <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
      <Button variant="invert" class="px-10 py-5 text-lg">
        Start Building Now
      </Button>
      <Button variant="outline" class="border-white/20 text-white hover:bg-white/10 px-10 py-5 text-lg">
        View Components
      </Button>
    </div>

    <!-- Stats -->
    <div class="mt-20 grid grid-cols-2 md:grid-cols-4 gap-8 border-t border-white/10 pt-10 max-w-4xl mx-auto">
      <div>
        <div class="text-3xl font-display font-bold text-white">99%</div>
        <div class="text-white/40 text-sm">LightHouse Score</div>
      </div>
      <div>
        <div class="text-3xl font-display font-bold text-white">0.5ms</div>
        <div class="text-white/40 text-sm">Bundle Size</div>
      </div>
      <div>
        <div class="text-3xl font-display font-bold text-white">100+</div>
        <div class="text-white/40 text-sm">Premium Icons</div>
      </div>
      <div>
        <div class="text-3xl font-display font-bold text-white">24/7</div>
        <div class="text-white/40 text-sm">Fast Support</div>
      </div>
    </div>
  </div>
</section>
