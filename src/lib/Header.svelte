<script>
    import { Hamburger } from "svelte-hamburgers";
    import Menu from "./Menu.svelte";
    import logo from "../images/logol.png"
    let open = $state(false);
</script>

<div id="header-component" class="w-full flex items-center justify-between p-4 pl-8 pr-8 lg:pl-16 lg:pr-16 text-zinc-700 {open ? 'bg-zinc-50' : ''}">
    <img src={logo} alt="Sprintech Logo" title="Sprintech Logo" class="max-w-12" />
    <ul class="flex items-center gap-2 lg:gap-4 text-base lg:text-xl font-normal">
        <li><a href="#features">Funcionalidades</a></li>
        <li><a href="#how">Como funciona</a></li>
        <li><a href="#about">Sobre</a></li>
        <li class="list-none"><a href="#antecipado" class="text-xl p-6 pt-3 pb-3 bg-amber-700 rounded-lg text-white flex items-center justify-center font-medium animate-pulse">Acesso antecipado</a></li>
    </ul>
    <div class="hamburguer-icon">
        <Hamburger class="hamburguer-icon" title="Toggle nav links" ariaControls="nav" type="spring" --layer-spacing="8px" --layer-height="2px" --border-radius="10px" --color="black" bind:open  />
    </div>
</div>
<Menu class="hamburguer-menu" bind:open />

<style>
    .hamburguer-menu {
        display: none;
        position: fixed;
        top: 0;
        left: 0;
        width: 80%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.9);
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 999;
        transition: 0.3s ease;
    } 


    .hamburguer-icon {
        display: none;
        z-index: 1000;
        cursor: pointer;
        color: wheat;
    }

    .hamburguer-menu a {
        color: white;
        font-size: 24px;
        margin: 1rem 0;
    }

    /* Esconde o menu normal em telas menores */
    @media (max-width: 1000px) {
        ul {
            display: none;
        }

        .hamburguer-icon {
            display: block;
        }
    }
</style>

