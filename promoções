<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Páscoa Feliz</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gradient-to-br from-pink-100 via-yellow-50 to-white min-h-screen text-black font-sans p-4">
  <div class="text-center mb-6">
    <h1 class="text-5xl font-extrabold text-pink-600 drop-shadow-lg">Páscoa Feliz</h1>
    <p class="text-sm mt-2 text-gray-600">Surpreenda com os melhores presentes da Páscoa</p>
  </div>
  <div class="max-w-xl mx-auto bg-white border border-yellow-300 p-6 rounded-xl shadow-xl text-center">
    <h2 class="text-3xl font-extrabold mb-4 text-green-700">Fazer Pedido</h2>
    <p class="mb-4 text-gray-700">Preencha as informações abaixo para confirmar seu pedido. O atendimento será finalizado diretamente no WhatsApp.</p>
    <form id="formPix" class="text-left space-y-4">
      <div>
        <label class="block font-semibold">Nome Completo</label>
        <input type="text" id="nome" required class="w-full border p-2 rounded" />
      </div>
      <div>
        <label class="block font-semibold">Endereço Completo</label>
        <input type="text" id="endereco" required class="w-full border p-2 rounded" />
      </div>
      <div>
        <label class="block font-semibold">Produto Desejado</label>
        <select id="produto" class="w-full border p-2 rounded">
          <option value="Kit 3 Ovos - R$129,40">Kit 3 Ovos - R$129,40</option>
          <option value="Ovo Chef Pistache - R$49,90">Ovo Chef Pistache - R$49,90</option>
          <option value="Coelho Cacau Magia - R$19,90">Coelho Cacau Magia - R$19,90</option>
        </select>
      </div>
      <div>
        <label class="block font-semibold">Forma de Pagamento</label>
        <input type="text" disabled value="PIX" class="w-full border p-2 rounded bg-gray-100" />
      </div>
      <button type="submit" class="w-full bg-green-600 text-white font-semibold py-2 rounded hover:bg-green-700">
        Enviar Pedido no WhatsApp
      </button>
    </form>
  </div>
  <script>
    document.getElementById("formPix").addEventListener("submit", function (e) {
      e.preventDefault();
      const nome = document.getElementById("nome").value;
      const endereco = document.getElementById("endereco").value;
      const produto = document.getElementById("produto").value;
      const mensagem = `Olá! Quero finalizar meu pedido:\n\n*Nome:* ${nome}\n*Endereço:* ${endereco}\n*Produto:* ${produto}\n*Pagamento:* PIX`;
      const url = `https://wa.me/5583996745627?text=${encodeURIComponent(mensagem)}`;
      window.location.href = url;
    });
  </script>
</body>
</html>
