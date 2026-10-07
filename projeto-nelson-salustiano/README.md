# Projeto: site do Nelson Salustiano (Psicanalista em Indaiatuba)

Pasta de contexto para continuar o trabalho em outra conversa. Leia este arquivo primeiro.

## Objetivo
Construir, em Elementor, o site do psicanalista Nelson Salustiano em um **subdomínio novo**,
replicando a estrutura (roteiro) da home do site Chaveiro Central, com visual calmo e acolhedor.

## Arquivos
- `01-briefing-nelson.md`: textos e dados do profissional (conteúdo base, NAP, horários)
- `02-palavras-chave.md`: lista oficial de palavras-chave (só estes termos)
- `03-estrutura-do-site.md`: páginas, mega menu e roteiro da home
- `04-design.md`: paleta, fontes e regras visuais
- `05-regras-e-pendencias.md`: cuidados éticos, decisões tomadas e o que falta

## Status
- Briefing, palavras-chave, estrutura e paleta aprovados pelo usuário.
- **Pendente:** conectar o site do Nelson via Novamira (servidor `novamira-psicanalistanels` não apareceu na sessão anterior; conectores só carregam no início da sessão, então abrir uma sessão nova depois de adicionar o conector).
- Nada foi gravado no site novo ainda.

## Como começar na nova conversa
1. Confirmar que o servidor Novamira do Nelson está conectado (ToolSearch pelo nome).
2. Ler o estado do site (tema, plugins, se o PRO Elements tem mega menu). Só leitura.
3. Gravar o Kit global (cores e fontes), depois a home, depois as demais páginas, mostrando ao usuário antes de seguir.
4. Manter `blog_public = 0` (bloqueado para buscadores) até o lançamento.

## Referência: site do chaveiro (somente leitura)
Servidor `novamira-chaveirocentral`. Home = página 11. Estrutura lida em 99 elementos (ver `03-estrutura-do-site.md`).
Lição aprendida lá: site criado em subdomínio com indexação desligada. Ao migrar, conferir `blog_public`, `home`/`siteurl` em https e limpar o cache do sitemap do Yoast.
