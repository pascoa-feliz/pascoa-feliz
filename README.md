<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Páscoa</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-white text-black font-sans p-4">
  <div class="grid grid-cols-1 md:grid-cols-3 gap-4">

    <!-- Produto 1 -->
    <div class="border border-green-700 p-4 rounded-xl">
      <span class="bg-purple-100 text-purple-800 text-xs font-bold px-2 py-1 rounded">TOP 1 MAIS VENDIDO</span>
      <h2 class="font-bold mt-2">Kit Exclusivo 3x Ovos de Páscoa</h2>
      <p class="text-sm text-gray-600">Entrega Grátis via Motoboy</p>
      <p class="line-through text-sm text-gray-400">R$ 109,90</p>
      <p class="text-green-600 text-2xl font-bold">R$ 89,40</p>
      <img src="https://via.placeholder.com/150" class="mx-auto my-3" alt="Produto">
      <div class="flex flex-col gap-2 mt-4">
        <button onclick="abrirGateway('Kit 3 Ovos - R$129,40')" class="bg-red-600 text-white text-center py-2 rounded-xl hover:bg-red-700">Finalizar Pedido</button>
      </div>
    </div>

    <!-- Produto 2 -->
    <div class="border border-green-700 p-4 rounded-xl">
      <span class="bg-purple-100 text-purple-800 text-xs font-bold px-2 py-1 rounded">TOP 2 MAIS VENDIDO</span>
      <h2 class="font-bold mt-2">Ovo de Páscoa do Chef Pistache 600g</h2>
      <p class="text-sm text-gray-600">Entrega Grátis via Motoboy</p>
      <p class="line-through text-sm text-gray-400">R$ 119,90</p>
      <p class="text-green-600 text-2xl font-bold">R$ 49,90</p>
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQaSYzQRY6OTrbtC_pq9ibppr9a9CXP41up6TUQ1__Rr-qXYWgMvqhLsKo&s=10" class="mx-auto my-3" alt="Produto">
      <div class="flex flex-col gap-2 mt-4">
        <button onclick="abrirGateway('Ovo Chef Pistache - R$49,90')" class="bg-red-600 text-white text-center py-2 rounded-xl hover:bg-red-700">Finalizar Pedido</button>
      </div>
    </div>

    <!-- Produto 3 -->
    <div class="border border-green-700 p-4 rounded-xl">
      <span class="bg-purple-100 text-purple-800 text-xs font-bold px-2 py-1 rounded">TOP 6 MAIS VENDIDO</span>
      <h2 class="font-bold mt-2">Coelho Cacau Magia ao Leite 400g</h2>
      <p class="text-sm text-gray-600">Entrega Grátis via Motoboy</p>
      <p class="line-through text-sm text-gray-400">R$ 39,90</p>
      <p class="text-green-600 text-2xl font-bold">R$ 19,90</p>
      <img src="https://via.placeholder.com/150" class="mx-auto my-3" alt="Produto">
      <div class="flex flex-col gap-2 mt-4">
        <button onclick="abrirGateway('Coelho Cacau Magia - R$19,90')" class="bg-red-600 text-white text-center py-2 rounded-xl hover:bg-red-700">Finalizar Pedido</button>
      </div>
    </div>

  </div>

  <!-- FORMULÁRIO CLONADO -->
  <div id="form-clone" class="fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center z-50 hidden">
    <div class="max-w-xl mx-auto bg-white border border-yellow-300 p-6 rounded-xl shadow-xl text-center">
      <h1 class="text-2xl font-bold mb-2 text-green-700">Finalizar Pedido</h1>
      <p class="mb-4 text-gray-700 text-sm">Preencha as informações abaixo para confirmar seu pedido via WhatsApp.</p>
      <form id="formPix" class="text-left space-y-4">
        <div>
          <label class="block font-semibold text-sm">Nome Completo</label>
          <input type="text" id="nome" required class="w-full border p-2 rounded text-sm">
        </div>
        <div>
          <label class="block font-semibold text-sm">Endereço Completo</label>
          <input type="text" id="endereco" required class="w-full border p-2 rounded text-sm">
        </div>
        <div>
          <label class="block font-semibold text-sm">Produto Desejado</label>
          <input type="text" id="produto" readonly class="w-full border p-2 rounded text-sm bg-gray-100">
        </div>
        <div>
          <label class="block font-semibold text-sm">Forma de Pagamento</label>
          <input type="text" disabled value="PIX" class="w-full border p-2 rounded text-sm bg-gray-100">
        </div>
        <button type="submit" class="w-full bg-green-600 text-white font-semibold py-2 rounded hover:bg-green-700">Enviar Pedido no WhatsApp</button>
        <button type="button" onclick="fecharGateway()" class="w-full text-gray-600 text-sm underline mt-2">Cancelar</button>
      </form>
    </div>
  </div>

  <script>
    function abrirGateway(produto) {
      document.getElementById("form-clone").classList.remove("hidden");
      document.getElementById("produto").value = produto;
    }

    function fecharGateway() {
      document.getElementById("form-clone").classList.add("hidden");
    }

    document.getElementById("formPix").addEventListener("submit", function(e) {
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
