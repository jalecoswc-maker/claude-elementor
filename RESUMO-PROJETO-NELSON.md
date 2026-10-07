# Resumo do projeto: site do Nelson Salustiano

## Objetivo
Site em Elementor do psicanalista Nelson Salustiano (Indaiatuba), em subdominio novo, replicando o layout do site Chaveiro Central, com visual calmo e acolhedor.

## Acessos
- Site do Nelson: https://psicanalistanelsonsalustiano.meunegocioo.com.br (servidor MCP `novamira-psicanalistanels`)
- Referencia somente leitura: servidor `novamira-chaveirocentral` (home = pagina 11, cabecalho = template 18, rodape = template 19, pagina de servico exemplo = 59)
- Stack do site: WordPress 7.1.3, Hello Elementor, Elementor 4.3.4, PRO Elements 4.1.0 (tem widget de mega menu)
- `blog_public = 0` (bloqueado para buscadores ate o lancamento)

## Identidade (aprovada)
- Design salvo e ativo no Novamira: "Escuta Serena" (slug `nelson-salustiano`)
- Cores atuais ("Escuta Viva"): turquesa #007C89, turquesa escuro #00525C (rodape), vermelho-coral #D63E24 (botoes, texto branco), amarelo-sol #FFD166 (detalhes), creme #FFF8EC, aqua claro #D6F3EF, texto #12333A
- Fontes: Lora (titulos) e Inter (texto), gravadas no Kit global (kit 5)

## Dados do profissional
- Nelson Salustiano, Psicanalista Clinico e Psicoterapeuta, especializacao em Trauma e Tanatologia, registro ANTPC-RP 842/22
- Instituto Laar, R. Ademar de Barros, 475, Sala 6, Centro, Indaiatuba - SP, CEP 13330-130
- WhatsApp/telefone: (19) 98157-0264
- Horarios: segunda a sexta, 09h as 18h. Sabado e domingo fechado
- Atendimento individual, adultos, presencial e online. NAO atende casais

## O que ja esta no site
| Item | ID / endereco |
|---|---|
| Home (pagina inicial) | ID 10, `/` |
| Servicos (indice) | ID 11, `/servicos/` |
| 7 categorias (uma secao H2 por palavra-chave, 76 secoes) | IDs 12 a 18, `/servicos/<slug>/`: trauma-e-tanatologia, ansiedade-e-sobrecarga, autoestima-e-autoconhecimento, relacionamentos, luto-tristeza-e-mudancas, trabalho-e-desenvolvimento-emocional, modalidades |
| Psicanalista em Indaiatuba | ID 20 |
| Sobre | ID 21 |
| Atendimento | ID 22 |
| Blog | ID 23 |
| FAQ | ID 24 |
| Contato (formulario) | ID 25 |
| Cabecalho com mega menu (7 colunas) | template 26 |
| Rodape | template 27 |
| Modelo de artigo do blog | template 28 |
| Modelo de lista de artigos | template 29 |

## Estado da home (ID 10)
Refeita para seguir a home do chaveiro: hero azul com cartoes brancos flutuantes e divisor curvo; faixa de 4 icones; "Nossos Servicos" com 6 cards em grade; secao azul "Por que buscar a analise" com divisor inclinado; faixa de 3 passos (no lugar das avaliacoes); Sobre em 3 colunas (imagem, texto, lista); Atendimento com etiquetas; FAQ em caixas com + e -; blog em 3 colunas.
Caixas de imagem estao em branco (placeholder do Elementor) ate o Nelson enviar as fotos.

## Regras de conteudo
- Usar somente as palavras-chave oficiais (arquivo 02 do projeto)
- Sem promessa de cura, sem urgencia, 24 horas ou orcamento
- Sem depoimentos sem autorizacao (secao de avaliacoes omitida)
- Registro ANTPC-RP 842/22 sempre visivel
- Nao incluir "terapia de casal"

## Pendencias
1. Conferir visualmente a home e as paginas internas (nao foi possivel abrir o site a partir da sessao em nuvem: o ambiente bloqueia o dominio; liberar em Network access > Custom > Allowed domains, ou enviar prints)
2. Aproximar as paginas internas do layout do chaveiro (topo com foto, faixa de confianca, passos)
3. Fotos do Nelson, logo, e conferir o e-mail de destino do formulario de contato
4. Escrever os primeiros artigos do blog (a lista esta vazia)
5. Publicar a politica de privacidade (pagina 3, em rascunho)
6. Revisao de SEO (titulo e descricao de cada pagina) e leitura dos textos pelo Nelson antes do lancamento
7. No lancamento: ativar indexacao, conferir `home`/`siteurl` em https e reenviar o sitemap

## Observacoes tecnicas
- Cache da Hostinger pode mostrar versao antiga: limpar cache apos alteracoes
- Se abrir uma sessao nova, conferir se o servidor `novamira-psicanalistanels` aparece (conectores so carregam no inicio da sessao)
- O servidor `novamira-visual-mcp` (npx) tem no JSON enviado os erros `comando` (deve ser `command`) e `-e` (deve ser `-y`)
