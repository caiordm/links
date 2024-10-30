<script>
  import {
    IconLayout,
    IconBrush,
    IconDeviceMobile,
    IconBolt,
  } from "@tabler/icons-svelte";
  import Form from "../lib/Form.svelte";

  const features = [
    {
      icon: "Layout",
      title: "Editor Intuitivo",
      description:
        "Arrange facilmente os itens da sua página com nosso editor intuitivo.",
    },
    {
      icon: "Brush",
      title: "Design Customizável",
      description:
        "Personalize cada parte da sua página da forma que achar melhor.",
    },
    {
      icon: "DeviceMobile",
      title: "Responsivo para dispositivos móveis",
      description:
        "Sua página funciona bem em qualquer dispositivo, seja num computador um smartphone",
    },
    {
      icon: "Bolt",
      title: "Lançamento Rápido",
      description: "Veja sua página no ar após pouco tempo.",
    },
  ];

  const steps = [
    {
      step: 1,
      title: "Escolha um template",
      description: "Comece com o nosso template para poupar seu esforço.",
    },
    {
      step: 2,
      title: "Customize sua página",
      description:
        "Adicione seu conteúdo, ajuste da forma que preferir e estilize de acordo com a sua marca",
    },
    {
      step: 3,
      title: "Publique",
      description:
        "Após revisar todos os detalhes, publique sua página com um simples clique!",
    },
  ];
</script>

<section id="home" class="pt-16 lg:pt-32 pb-20 px-4">
  <div class="container mx-auto text-center">
    <h1
      class="text-4xl lg:text-5xl font-bold mb-6 bg-clip-text text-transparent bg-gradient-to-r from-purple-950 to-purple-500"
    >
      Crie um site profissional e personalizado sem complicações. É fácil,
      É rápido!
    </h1>
    <p class="text-xl text-gray-600 mb-8 max-w-2xl mx-auto">
      Tenha um site profissional e moderno em minutos, sem precisar de
      conhecimentos técnicos, com nossa plataforma, você tem o controle total
      sobre o seu site.
    </p>
    <a href="#antecipado" class="bg-purple-800 p-4 rounded-md text-lg text-white animate-bounce">
      Tenha acesso antecipado
    </a>
  </div>
</section>

<section id="features" class="py-20 bg-gray-50">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl text-zinc-700 font-bold text-center mb-12">
      Nossas funcionalidades
    </h2>
    <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
      {#each features as feature, index}
        <div
          class="border rounded-lg text-center hover:shadow-lg transition-shadow"
        >
          <div class="p-6">
            {#if feature.icon === "Layout"}
              <IconLayout class="h-10 w-10 text-primary mb-4 inline-block" />
            {/if}
            {#if feature.icon === "Brush"}
              <IconBrush class="h-10 w-10 text-primary mb-4 inline-block" />
            {/if}
            {#if feature.icon === "DeviceMobile"}
              <IconDeviceMobile
                class="h-10 w-10 text-primary mb-4 inline-block"
              />
            {/if}
            {#if feature.icon === "Bolt"}
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
          <div
            class="flex-shrink-0 w-12 h-12 rounded-full { item.step == 1 ? 'bg-purple-600' : ''} { item.step == 2 ? 'bg-purple-800' : ''} { item.step == 3 ? 'bg-purple-950' : ''} text-white flex items-center justify-center text-xl font-bold mr-4"
          >
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

<section id="antecipado" class="pb-14 container mx-auto px-4 flex flex-col items-center justify-center">
  <h2 class="text-3xl font-bold text-center mb-12">Acesso antecipado</h2>
  <div data-tf-live="01JBDNDVCFRKEP8X6JFN6M7F6M"></div><script src="//embed.typeform.com/next/embed.js"></script>
</section>
