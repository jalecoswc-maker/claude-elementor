# Playbook: replicar este site em outro cliente (barato e rapido)

Base: site do psicanalista Nelson Salustiano (Elementor + PRO, Hello Elementor, Novamira MCP).
Objetivo: criar um site novo igual em estrutura, trocando so dados, textos, cores e imagens.

## 0. Antes de comecar (peca tudo de uma vez ao cliente)
- Nome, profissao, registro profissional, NAP (endereco e telefone), horarios, redes sociais.
- Lista oficial de palavras-chave (nao inventar outras), cidade/regiao.
- O que NAO atende, regras de conteudo (sem promessa de cura, sem urgencia, sem depoimento sem autorizacao).
- Cores/estilo (ou escolher uma paleta viva logo na primeira vez: o cliente rejeitou paleta apagada).
- Fotos: ou usar as do cliente, ou gerar com IA (prompts por pagina, versao desktop e versao mobile vertical).
- Dados para paginas legais: razao social/CNPJ ou CPF, e-mail de privacidade, prazos de guarda.
- Servidor MCP do WordPress novo conectado (Novamira) e `blog_public = 0` ate o lancamento.

## 1. Ordem de construcao (nao refazer)
1. Design tokens no kit global (cores, fontes) e salvar com `novamira/save-design`.
2. Cabecalho com mega menu (PRO) + rodape (templates de tema, condicao "todo o site").
3. Home (hero com foto de fundo, faixa de icones, cards de servico, "por que", passos, sobre, atendimento, FAQ em sanfona, blog).
4. Uma pagina-categoria por grupo de palavras-chave (uma secao H2 por palavra-chave, ancora `id` = slug).
5. Paginas: sobre, atendimento, FAQ, contato (formulario), landing da cidade.
6. Blog: modelo de artigo (single), modelo de lista (archive), modelo de categoria, cartao do loop-grid.
7. Artigos (6 a 10) com CTA e FAQ em sanfona (`<details>` + FAQPage).
8. SEO (Yoast), dados estruturados, paginas legais, banner de cookies, favicon, credito no rodape.
9. Limpar caches, verificar no celular, so entao liberar indexacao.

## 2. Estrutura que funcionou (copiar tal qual)
- Home: hero com foto de fundo (container com background_image, overlay em gradiente, `custom_css` com media queries) + 3 chips de confianca; 6 cards (image + h3 + texto + botao); secao colorida com divisor; faixa de 3 passos; sobre em 3 colunas; FAQ em `nested-accordion`; 3 posts.
- Categoria: hero + indice de temas (botoes-ancora) + uma secao por tema + "Como comecar" + FAQ + CTA + "Leia no blog" + "Outros temas".
- Artigo: titulo, post-info, imagem de capa, `theme-post-content` (CSS de `.nelson-cta`, `.nelson-faq`, `.nelson-related`, H2 30/27/24 px), compartilhar, caixa do autor, CTA final.
- Mobile do hero: foto de fundo VERTICAL propria (imagem mobile separada), texto por cima, overlay mais leve, botoes grandes, sem divisor.

## 3. Regras de design aprendidas
- Paleta viva: turquesa #007C89, escuro #00525C, amarelo #FFD166, creme #FFF8EC, aqua #D6F3EF, tinta #12333A. Coral so em detalhes pequenos.
- Botao de WhatsApp SEMPRE verde oficial #25D366 (texto #0B3B2E, hover #1EBE57), inclusive o flutuante.
- Nunca texto vermelho/turquesa sobre fundo vermelho. Cartao de destaque: fundo escuro + titulo amarelo + texto creme.
- Titulos de artigo e paginas legais menores (H2 24 a 30 px).
- Imagens em widget Image: o controle e `object-fit` (com hifen). `object_fit` e ignorado e a foto estica.

## 4. Armadilhas tecnicas (economizam tokens)
- Editar `_elementor_data` direto via `novamira/execute-php`; sempre `wp_slash(wp_json_encode($d))`.
- Closures que alteram por referencia: `function(&$els)` e `foreach($els as &$e)`; regex com delimitador `~`.
- Limpar cache depois de TODA mudanca: `\Elementor\Plugin::$instance->files_manager->clear_cache()`, `wp_cache_flush()` e chamar o callback da rota `/hostinger-tools-plugin/v1/clear-cache` direto (a REST via `rest_do_request` da 403).
- O cache da Hostinger (hCDN) serve versao velha por navegador/celular: testar sempre com aba anonima e com `wp_remote_get` usando User-Agent mobile.
- URLs `data:` sao removidas: placeholders de imagem como arquivo SVG em `uploads/`.
- Editar pelo editor do Elementor pode gravar versao antiga por cima (a home perdeu imagens e cores uma vez). Depois de mexer pelo editor, conferir o `_elementor_data`.
- O sandbox da nuvem nao acessa o dominio do site (politica de rede). Verificar por loopback no servidor (`wp_remote_get`) e pedir prints ao cliente.
- Site de terceiros (concorrente) tambem so e acessivel via `wp_remote_get` do servidor WordPress.
- Condicoes do Theme Builder: `...get_conditions_manager()->save_conditions($id, [[...]])`; para o blog usar `page_for_posts`.
- Yoast: titulo/descricao por pagina em `_yoast_wpseo_title` e `_yoast_wpseo_metadesc`; imagem social padrao em `wpseo_social`; foto de capa com `set_post_thumbnail`.

## 5. Dados estruturados (mu-plugin `nelson-schema.php`)
- Um unico filtro `wpseo_schema_graph` injeta no grafo do Yoast: ProfessionalService (NAP, horarios, area atendida, identificador do registro), Person (profissional), Service por pagina de servico, AboutPage/ContactPage, publisher/author nos artigos, `sameAs` (Instagram).
- Remover JSON-LD solto de widgets HTML para nao duplicar. FAQPage: ligar `faq_schema` nos `nested-accordion` e manter o JSON-LD no conteudo dos artigos.

## 6. Paginas legais e LGPD
- Politica de Privacidade, Politica de Cookies, Termos de Uso (curtos), com campos `[PREENCHER: ...]` em amarelo ate o cliente informar CNPJ/CPF, e-mail e prazos.
- Banner de cookies leve (HTML widget no rodape): Aceitar/Recusar, grava `localStorage`, dispara evento `...Consent` para liberar Analytics/Pixel so depois do aceite.
- Formulario: campo `acceptance` obrigatorio com link da politica; aviso para nao enviar dados sensiveis.
- Site de saude (psicologia): dado sensivel (art. 11), texto de sigilo e aviso de emergencia (CVV 188, SAMU 192). Site comum (chaveiro): versao mais simples, sem a parte de saude.

## 7. Interligacao (link juice)
- Cada artigo: caixa "Conheca o atendimento" (3 links para temas de servico, com ancora) + "Continue lendo" (2 artigos).
- Cada pagina de servico: bloco "Leia no blog sobre este tema".
- Logo do cabecalho e do rodape linka para a home.

## 8. SEO e conteudo (skill seo-arquiteto-conteudo)
- Transacional (servicos) separado de Informacional (blog). Pillar + clusters; clusters linkam de volta ao servico.
- Perguntas para artigos: Google autocomplete (psicanalista/terapia + cidade) e "as pessoas tambem perguntam".
- Meta: titulo ate 60 caracteres, descricao 140 a 160; 1 H1 por pagina.
- Benchmark: conteudo longo vence. Home 1.500 a 2.000 palavras, artigos 1.000 a 1.400, depoimentos reais autorizados ou Google Meu Negocio.

## 9. Extras no rodape/geral
- Favicon: gerado com Imagick a partir do icone SVG do Font Awesome (pena) e `update_option('site_icon', $id)`.
- Credito: "Site criado por Meu Negocioo" (pilula com borda) linkando para https://meunegocioo.com.br/.
- Instagram em `social-icons` do rodape e em `sameAs`.

## 10. Checklist final antes do lancamento
- [ ] Campos amarelos das paginas legais preenchidos
- [ ] E-mail de destino do formulario conferido
- [ ] Fotos reais ou geradas aplicadas (desktop e mobile) sem esticar
- [ ] Teste em celular real: home, uma categoria, um artigo, formulario, botoes
- [ ] Yoast: titulo/descricao de todas as paginas, sitemap ok
- [ ] Teste de Resultados Relacionados do Google (home, servico, artigo)
- [ ] `blog_public = 1`, home/siteurl em https, enviar sitemap no Search Console, limpar cache

## Como pedir ao Claude para replicar (prompt curto)
"Replique o site do Nelson para <CLIENTE> seguindo o PLAYBOOK-REPLICAR-SITE.md e o ESTRATEGIA-SEO-NELSON.md. Dados do cliente: <...>. Servidor MCP: <nome>. Use as mesmas estruturas e a paleta <...>."
