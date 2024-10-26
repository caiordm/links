<script>
    let { open = $bindable() } = $props()
</script>


{#if open}
    <ul id="nav" class="absolute z-50 bg-white w-full pb-8 border-b border-zinc-200 text-zinc-700 flex flex-col items-center gap-4 lg:gap-8 text-lg lg:text-xl font-regular">
        <li><a href="#features">Funcionalidades</a></li>
        <li><a href="#how">Como funciona</a></li>
        <li><a href="#about">Sobre</a></li>
        <li class="list-none"><a href="#iniciar" class="text-xl p-6 pt-3 pb-3 bg-zinc-800 rounded-lg text-white flex items-center justify-center font-medium">Em Breve...</a></li>
    </ul>
{/if}