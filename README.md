# Projeto Cardápio

Projeto de cardápio digital desenvolvido do zero, com base no canal **Sujeito Programador**.

Qualquer dúvida, abra uma *issue*.

## Tecnologias utilizadas

O projeto foi desenvolvido com: **HTML, CSS, Node, Tailwind e JavaScript**.

## Horário de funcionamento

O projeto possui um controle de horário de funcionamento implementado em JavaScript. Fora do horário definido no script, a opção de finalizar o pedido no carrinho é desabilitada.

> Recomendo alterar ou remover essa regra, já que não há como saber em qual horário o professor (ou avaliador) irá acessar o site.

## Alterando a imagem de fundo

Para trocar a imagem de fundo, edite o arquivo `tailwind.config.js`.

## Alterando a aparência

Para mudar qualquer elemento visual, edite diretamente o HTML. Use `Ctrl+F` no seu editor de código para localizar o trecho desejado.

> **Atenção:** não altere os `id`s já declarados no HTML — isso pode gerar conflitos com o backend.

Você pode trocar todas as imagens do site e adicionar quantos itens/produtos quiser.

### Adicionando imagens

Ao adicionar uma imagem, lembre-se de apontar o diretório correto na tag `<img />` do item correspondente:

```html
<img
  src="./assets/nome_imagem.png"  <!-- caminho da nova imagem -->
  alt="NOME-DO-ITEM"              <!-- nome/descrição da imagem -->
  class="w-28 h-28 rounded-md hover:scale-110 hover:-rotate-2 duration-300"  <!-- estilização -->
/>
```

### Adicionando novos itens ao cardápio

Para adicionar um novo item, copie e adapte o código abaixo, colando-o dentro da seção `<!-- INICIO MENU -->`:

```html
<!-- PRODUTO ITEM -->
<div class="flex gap-2">
  <img
    src="./assets/hamb-1.png"
    alt="NOME-DO-ITEM"
    class="w-28 h-28 rounded-md hover:scale-110 hover:-rotate-2 duration-300"
  />
  <div>
    <p class="font-bold">NOME-DO-ITEM</p>
    <p class="text-sm">Descrição aqui Descrição aqui Descrição aqui Descrição aqui</p>
    <div class="flex items-center gap-2 justify-between mt-3">
      <p class="font-bold text-lg">R$99,99</p>
      <button class="bg-gray-900 px-5 rounded add-to-cart-btn"
        data-name="ID-DO-ITEM"
        data-price="99.99"
      >
        <i class="fa fa-cart-plus text-lg text-white"></i>
      </button>
    </div>
  </div>
</div>
<!-- FIM ITEM -->
```

> **Lembrete:** sempre que adicionar um novo item, configure também o `data-name` e o `data-price`, para que o backend consiga capturar os dados corretamente.

### Adicionando itens à seção de bebidas

Para adicionar um item à seção de bebidas, copie e adapte o código abaixo, colando-o dentro da seção `<!-- GRID BEBIDAS -->`:

```html
<!-- BEBIDA ITEM -->
<div class="flex gap-2 w-full">
  <img src="./assets/refri-1.png" alt="Coca Lata" class="w-28 h-28 rounded-md hover:scale-110 hover:-rotate-2 duration-300"/>
  <div class="w-full">
    <p class="font-bold">NOME-BEBIDA-DISPLAY</p>
    <div class="flex items-center gap-2 justify-between mt-3">
      <p class="font-bold text-lg">R$6,00</p>
      <button class="bg-gray-900 px-5 rounded add-to-cart-btn"
        data-name="NOME-BEBIDA"
        data-price="6"
      >
        <i class="fa fa-cart-plus text-lg text-white"></i>
      </button>
    </div>
  </div>
</div>
<!-- FIM BEBIDA ITEM -->
```

## Configurações pessoais

Lembre-se de editar os dados pessoais, como o número de WhatsApp para envio dos pedidos, diretamente no JavaScript.

## Hospedagem

Recomendo hospedar o projeto na **Netlify** ou **Vercel**. O processo é simples: basta dar *fork* e vincular o repositório do GitHub, ou baixar o projeto compactado (.zip) e enviar (*commit*) diretamente.
