<script>
    import send from '@sendgrid/mail';

    let name = $state("");
    let email = $state("");

    const sendEmail = async () => {
        try {
            await send({
                to: "sprintechsoftware@gmail.com", // Replace with your email
                from: "sprintechsoftware@gmail.com",
                subject: "New Contact Form Submission",
                text: `Name: ${name}\nEmail: ${email}`,
                html: `<strong>Name:</strong> ${name}<br><strong>Email:</strong> ${email}`,
            });
            alert(
                `Obrigado pelo interesse! logo entraremos em contato. ${name}`,
            );
        } catch (error) {
            console.error("Error sending:", error);
            alert("Houve um erro ao enviar, tente novamente!");
        }
    };
</script>

<form
    class="border rounded-lg text-center items-center justify-center shadow-lg w-11/12 lg:w-1/3 p-4 flex flex-col gap-3"
>
    <h1 class="text-zinc-600">
        Preencha suas informações e entraremos em contato!
    </h1>
    <div class="flex flex-col items-start gap-1">
        <label for="name" class="text-zinc-600">Nome: </label>
        <input
            name="name"
            type="text"
            required
            bind:value={name}
            class="p-2 bg-zinc-100 border border-zinc-300 rounded-2xl"
            placeholder="Coloque seu nome aqui"
        />
    </div>
    <div class="flex flex-col items-start gap-1">
        <label for="name" class="text-zinc-600">Email: </label>
        <input
            name="name"
            type="text"
            required
            bind:value={email}
            class="p-2 bg-zinc-100 border border-zinc-300 rounded-2xl"
            placeholder="Coloque seu email aqui"
        />
    </div>
    <button
        class="p-2 bg-purple-800 text-white w-1/3 rounded-lg mt-2"
        onclick={sendEmail}>Enviar</button
    >
</form>
