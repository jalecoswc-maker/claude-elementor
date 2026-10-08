---
name: design-site-servicos-locais
description: Guia de design (designer) para sites Elementor de profissionais e servicos locais (saude, psicologia, consultorios, servicos). Use ao definir paleta, tipografia, hero, cards, botoes de WhatsApp, mobile, contraste e imagens de um site novo, ou ao corrigir um visual que ficou apagado, esticado ou ilegivel.
---

# Design de sites de servicos locais (Elementor)

Base: aprendizados do site do psicanalista Nelson Salustiano. Leia tambem `PLAYBOOK-REPLICAR-SITE.md`.

## Paleta (viva, nunca apagada)
- Primaria forte + escura (rodape/hero) + clara (secoes) + creme (fundo) + 1 cor de destaque quente (amarelo) + 1 cor de detalhe (coral, so em detalhes).
- Exemplo aprovado: #007C89 / #00525C / #D6F3EF / #FFF8EC / #FFD166 / coral #D63E24 so em detalhes, texto #12333A.
- Botao de WhatsApp: sempre verde oficial #25D366 (texto #0B3B2E, hover #1EBE57), inclusive o botao flutuante.
- Contraste: nunca texto de cor parecida sobre fundo vermelho/turquesa. Cartao de destaque: fundo escuro, titulo amarelo, texto creme.

## Tipografia
- Titulos em serifada (ex.: Lora), texto em sans (ex.: Inter). Tamanhos: H1 hero 40 a 52 px; H2 de pagina 30 a 40; H2 dentro de artigo 30/27/24 (desktop/tablet/mobile); H3 22/19.
- Titulos nao devem dominar a tela no celular. Paginas legais: H1 28 a 34 px, H2 24 px.

## Hero
- Foto de fundo (container com background_image) + overlay em gradiente escuro (esquerda forte, direita leve) para o texto ficar legivel.
- Mobile: usar imagem VERTICAL propria (`background_image_mobile`), texto por cima, overlay mais leve, botoes grandes de largura total, sem divisor.
- Divisores de forma so no desktop.

## Imagens
- Controle correto no widget Image: `object-fit` (com hifen). `object_fit` e ignorado e a foto estica. Em cards usar `custom_css` com `selector img{width:100%;object-fit:cover}` e altura fixa.
- Fotos de pessoa: proporcao original (ex.: 1:1) com `aspect-ratio` e `object-position` no rosto.
- Gerar prompts por pagina, com versao desktop e versao mobile vertical, nomes de arquivo com a palavra-chave e comprimidas (webp).

## Componentes que funcionam
- Cards de servico (imagem + icone + H3 + texto + botao), faixa de 3 passos, FAQ em sanfona (`nested-accordion` ou `<details>`), caixa de CTA com botao verde, caixa "Conheca o atendimento / Continue lendo", credito no rodape em pilula.
- Sempre CTA para WhatsApp no topo, no meio e no fim das paginas e artigos.

## Checklist antes de entregar
- [ ] Teste em celular real (aba anonima por causa do cache)
- [ ] Nenhuma imagem esticada, nenhum texto ilegivel
- [ ] Botoes de WhatsApp verdes e flutuante verde
- [ ] Titulos em tamanho confortavel no celular
- [ ] Logo e nome linkam para a home
