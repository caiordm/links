<script>
    import { IconBrandInstagram, IconBrandLinkedin} from '@tabler/icons-svelte';
</script>

<div id="about" class="container mx-auto px-4">
    <div class="grid md:grid-cols-3 gap-8">
    <div>
        <h3 class="text-lg font-semibold mb-4">Links</h3>
        <p class="text-gray-400">Crie seu próprio site em minutos com nosso construtor intuitivo.</p>
    </div>
    <div>
        <h3 class="text-lg font-semibold mb-4">Acesso rápido</h3>
        <ul class="space-y-2">
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors">Funcionalidades</a></li>
        <li><a href="#how" class="text-gray-400 hover:text-white transition-colors">Como funciona</a></li>
        </ul>
    </div>
    <div>
        <h3 class="text-lg font-semibold mb-4">Contate-nos</h3>
        <a href="https://www.instagram.com/sprintech.net_/" class="mb-4 flex gap-1 items-center text-gray-400"><IconBrandInstagram/>Nosso Instagram</a>
        <a href="https://www.linkedin.com/company/sprintech-software" class="flex gap-1 items-center text-gray-400"><IconBrandLinkedin/>Nosso Linkedin</a>
    </div>
    </div>
    <div class="mt-8 pt-8 border-t border-gray-700 text-center text-gray-400">
    <p>&copy; 2024 Sprintech. All rights reserved.</p>
    </div>
</div>