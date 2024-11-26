<script>
	import { onMount, onDestroy } from 'svelte';
	import '../app.css';
	import Header from '../lib/Header.svelte';
	import Footer from '../lib/Footer.svelte';
	let { children } = $props();
	
  let isScrolled = $state(false);

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };

    window.addEventListener('scroll', handleScroll);

    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });
</script>

<div class="absolute inset-0 -z-10 h-full w-full bg-white bg-[linear-gradient(to_right,#8080800a_1px,transparent_1px),linear-gradient(to_bottom,#8080800a_1px,transparent_1px)] bg-[size:14px_24px]"><div class="absolute left-0 right-0 top-0 -z-10 m-auto h-[310px] w-[310px] rounded-full bg-amber-400 opacity-50 blur-[100px]"></div></div>

<main class="min-h-screen">
	<header class="{isScrolled ? 'bg-gray-50 shadow-md fixed top-0 left-0 right-0 z-50 transition-all duration-300' : ''}"><Header></Header></header>
	{@render children()}
	<footer class="bg-zinc-800 text-white py-12"><Footer></Footer></footer>
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&display=swap');

	:global(html) {
		scroll-behavior: smooth;
		font-family: "DM Sans", sans-serif;	
	}
</style>