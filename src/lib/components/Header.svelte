<script lang="ts">
  import Home from '@lucide/svelte/icons/home';
  import User from '@lucide/svelte/icons/user';
  import Lightbulb from '@lucide/svelte/icons/lightbulb';
  import Briefcase from '@lucide/svelte/icons/briefcase';
  import Mail from '@lucide/svelte/icons/mail';

  const navItems = [
    { name: 'Inicio', href: '/', icon: Home },
    { name: 'Acerca de Mí', href: '/about', icon: User },
    { name: 'Servicios', href: '/services', icon: Lightbulb },
    { name: 'Proyectos', href: '/work', icon: Briefcase },
    { name: 'Contacto', href: '/contact', icon: Mail },
  ];
</script>

<header>
  <a href="/" class="logo">
    <img src="/marca/logo_circle.png" alt="Marco Gómez Logo" class="logo-img" />
  </a>
  <nav>
    {#each navItems as item}
      <a href={item.href}>
        <item.icon size={18} />
        {item.name}
      </a>
    {/each}
  </nav>
</header>
