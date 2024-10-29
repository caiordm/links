<script>
    let { open = $bindable() } = $props()
</script>


{#if open}
    <ul id="nav" class="absolute z-50 bg-zinc-50 w-full pt-4 pb-8 border-b-2 border-zinc-200 text-zinc-700 flex flex-col items-center gap-4 lg:gap-8 text-lg lg:text-xl font-regular">
        <li><a href="#features">Funcionalidades</a></li>
        <li><a href="#how">Como funciona</a></li>
        <li><a href="#about">Sobre</a></li>
        <li class="list-none"><a href="#antecipado" class="text-xl p-6 pt-3 pb-3 bg-zinc-800 rounded-lg text-white flex items-center justify-center font-medium">Acesso antecipado</a></li>
    </ul>
{/if}