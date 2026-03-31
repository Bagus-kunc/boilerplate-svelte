<script lang="ts">
  let { title, description, icon: Icon, delay = 0 }: { 
    title: string, 
    description: string, 
    icon: any,
    delay?: number
  } = $props();
</script>

<div 
  class="premium-card group hover:-translate-y-2 transition-all duration-300"
  style="animation-delay: {delay}ms"
>
  <div class="w-14 h-14 rounded-2xl premium-gradient flex items-center justify-center text-white mb-6 group-hover:scale-110 transition-transform duration-500 shadow-lg shadow-brand-primary/20">
    <Icon size={32} />
  </div>
  <h3 class="text-2xl font-display font-bold text-brand-dark mb-3 tracking-tight">{title}</h3>
  <p class="text-brand-dark/60 leading-relaxed font-medium">
    {description}
  </p>
</div>
