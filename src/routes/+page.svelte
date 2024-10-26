<script>
    import { IconLayout, IconBrush, IconDeviceMobile , IconBolt} from '@tabler/icons-svelte';

    const features = [
        { icon: 'Layout', title: 'Editor Intuitivo', description: 'Arrange facilmente os itens da sua página com nosso editor intuitivo.' },
        { icon: 'Brush', title: 'Design Customizável', description: 'Personalize cada parte da sua página da forma que achar melhor.' },
        { icon: 'DeviceMobile', title: 'Responsivo para dispositivos móveis', description: 'Sua página funciona bem em qualquer dispositivo, seja num computador um smartphone' },
        { icon: 'Bolt', title: 'Lançamento Rápido', description: 'Veja sua página no ar após pouco tempo.' },
    ];


    const steps = [
          { step: 1, title: "Escolha um template", description: "Comece com o nosso template para poupar seu esforço." },
          { step: 2, title: "Customize sua página", description: "Adicione seu conteúdo, ajuste da forma que preferir e estilize de acordo com a sua marca" },
          { step: 3, title: "Publique", description: "Após revisar todos os detalhes, publique sua página com um simples clique!" },
        ]
</script>

<section id="home" class="pt-32 pb-20 px-4">
    <div class="container mx-auto text-center">
        <h1
            class="text-5xl font-bold mb-6 bg-clip-text text-transparent bg-gradient-to-r from-zinc-700 to-purple-600"
        >
            Crie seu próprio site em minutos!
        </h1>
        <p class="text-xl text-gray-600 mb-8 max-w-2xl mx-auto">
            Construa o seu próprio site, da forma que você quer, sem precisar
            saber sobre códigos.
        </p>
        <button class="bg-zinc-900 p-3 rounded-md text-white animate-pulse"> Em Breve... </button>
    </div>
</section>

<section id="features" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4">
        <h2 class="text-3xl text-zinc-700 font-bold text-center mb-12">Nossas funcionalidades</h2>
        <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
          {#each features as feature, index}
            <div class="border rounded-lg text-center hover:shadow-lg transition-shadow">
              <div class="p-6">
                {#if feature.icon === 'Layout'}
                  <IconLayout class="h-10 w-10 text-primary mb-4 inline-block" />
                {/if}
                {#if feature.icon === 'Brush'}
                  <IconBrush class="h-10 w-10 text-primary mb-4 inline-block" />
                {/if}
                {#if feature.icon === 'DeviceMobile'}
                  <IconDeviceMobile class="h-10 w-10 text-primary mb-4 inline-block" />
                {/if}
                {#if feature.icon === 'Bolt'}
                  <IconBolt class="h-10 w-10 text-primary mb-4 inline-block" />
                {/if}
                <h3 class="text-xl font-medium mb-2">{feature.title}</h3>
                <p class="text-gray-600">{feature.description}</p>
              </div>
            </div>
          {/each}
        </div>
      </div>
</section>

<section id="how" class="py-20">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">Como funciona</h2>
      <div class="max-w-3xl mx-auto">
          {#each steps as item}
          <div class="flex items-start mb-8">
            <div class="flex-shrink-0 w-12 h-12 rounded-full bg-zinc-800 text-white flex items-center justify-center text-xl font-bold mr-4">
                {item.step}
            </div>
            <div>
                <h3 class="text-xl font-semibold mb-2">{item.title}</h3>
                <p class="text-gray-600">{item.description}</p>
            </div>
        </div>
        {/each}
      </div>
    </div>
  </section>
