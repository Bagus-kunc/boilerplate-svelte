<script lang="ts">
  import { onMount } from 'svelte';
  import Button from './Button.svelte';
  
  let isScrolled = $state(false);

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 50;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<nav class="fixed top-0 left-0 right-0 z-50 transition-all duration-500 {isScrolled ? 'py-4 glass shadow-lg' : 'py-8 bg-transparent'}">
  <div class="container mx-auto px-6 flex items-center justify-between">
    <div class="flex items-center gap-2 group cursor-pointer">
      <div class="w-10 h-10 premium-gradient rounded-xl flex items-center justify-center text-white font-bold text-xl group-hover:scale-110 transition-transform duration-300">
        S
      </div>
      <span class="text-2xl font-display font-extrabold tracking-tight {isScrolled ? 'text-brand-dark' : 'text-white'}">
        SVELTE<span class="text-brand-primary">CORE</span>
      </span>
    </div>

    <div class="hidden md:flex items-center gap-8 font-medium {isScrolled ? 'text-brand-dark/80' : 'text-white/80'}">
      <a href="#features" class="hover:text-brand-primary transition-colors">Features</a>
      <a href="#about" class="hover:text-brand-primary transition-colors">About</a>
      <a href="#pricing" class="hover:text-brand-primary transition-colors">Pricing</a>
      <a href="#contact" class="hover:text-brand-primary transition-colors">Contact</a>
    </div>

    <div class="flex items-center gap-4">
      <Button variant="ghost" class="hidden sm:block font-semibold {isScrolled ? 'text-brand-dark' : 'text-white'}">
        Log in
      </Button>
      <Button class="premium-gradient text-white px-6 py-2 font-bold hover:brightness-110">
        Get Started
      </Button>
    </div>
  </div>
</nav>
