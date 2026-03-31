<script lang="ts">
  let { 
    children, 
    variant = "primary", 
    class: className = "", 
    ...props 
  }: { 
    children: any, 
    variant?: "primary" | "secondary" | "outline" | "ghost" | "invert", 
    class?: string,
    [key: string]: any
  } = $props();

  const variants = {
    primary: "bg-brand-primary text-white hover:bg-brand-primary/90 shadow-lg shadow-brand-primary/20",
    secondary: "bg-brand-secondary text-white hover:bg-brand-secondary/90 shadow-lg shadow-brand-secondary/20",
    outline: "border-2 border-brand-primary text-brand-primary hover:bg-brand-primary/10",
    ghost: "text-brand-dark hover:bg-brand-dark/5",
    invert: "bg-white text-brand-dark hover:bg-brand-light shadow-lg shadow-white/10"
  };
</script>

<button
  class="px-6 py-3 rounded-full font-semibold transition-all duration-300 active:scale-95 disabled:opacity-50 disabled:pointer-events-none {variants[variant]} {className}"
  {...props}
>
  {@render children()}
</button>
