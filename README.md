# Cardápio digital do Bello

Cardápio em tela cheia (um produto por tela, foto e vídeo passando para o lado) da **Bebidas Bello Conveniência**, Sorriso/MT.

Site: https://bello-cardapio.vercel.app
Painel para editar: https://bello-cardapio.vercel.app/admin/

## Como editar (sem mexer em código)

1. Abra o **Painel** (`/admin/`).
2. Na aba **Conexão GitHub**, cole um token de acesso (uma vez só):
   - Crie em <https://github.com/settings/personal-access-tokens/new>
   - Escolha só este repositório e, em *Permissions*, marque **Contents: Read and write**.
3. Em **Produtos**: `+ Produto`, `+ Lista de itens` (vários itens numa tela, ex.: sabores de pastel) ou `+ Tela de foto`.
   Adicione fotos e vídeos por **link** ou **enviando o arquivo**.
4. Toque em **Salvar no GitHub**. O site se atualiza sozinho em cerca de 1 minuto.

Na aba **Dados da loja** ficam WhatsApp, frase da entrada, fotos da entrada, endereço e as categorias (bolinhas do topo).

## Como o projeto é organizado

```
index.html          o cardápio que o cliente vê
admin/index.html    o painel de edição
data/cardapio.js    TODOS os produtos, preços e mídias (é o arquivo que o painel altera)
img/                fotos e vídeos (img/uploads/ recebe os enviados pelo painel)
```

Para editar à mão, abra `data/cardapio.js`. Cada produto tem `categoria`, `nome`, `descricao`, `preco` e `midia` (lista de fotos e vídeos; a primeira aparece primeiro).

Modo da foto (opcional, por foto): `"cover"` (tela cheia), `"pk"` (garrafa/lata com fundo branco, ganha fundo amarelo e verde) ou `"contain"` (inteira, sem cortar).

## Observações

- Os preços vieram do cardápio impresso do Bello. Confira antes de divulgar.
- Muitas fotos e vídeos de bebidas e comidas são **de exemplo, tiradas da internet** (Pexels e buscas na web). Troque pelas fotos próprias do Bello antes de usar de verdade.
- As métricas simples (visualizações, curtidas) ficam só no navegador de cada pessoa; não somam entre clientes.
