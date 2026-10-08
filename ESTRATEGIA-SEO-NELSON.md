# Estratégia de SEO e arquitetura de conteúdo: Nelson Salustiano

Gerado com a skill `seo-arquiteto-conteudo`. Contém apenas estratégia e esqueleto. Não contém o texto final das páginas.

## 1. Entidades e dados de NAP (usar em todas as páginas)

| Campo | Valor |
|---|---|
| Nome | Nelson Salustiano, Psicanalista Clínico e Psicoterapeuta |
| Registro | ANTPC-RP 842/22 |
| Especialização | Trauma e Tanatologia |
| Local | Instituto Laar, R. Ademar de Barros, 475, Sala 6, Centro, Indaiatuba - SP, CEP 13330-130 |
| Telefone / WhatsApp | (19) 98157-0264 |
| Horário | Segunda a sexta, 09h às 18h (sábado e domingo fechado), mediante agendamento |
| Modalidades | Presencial (Indaiatuba) e online por videoconferência |
| Público | Adultos, atendimento individual. Não atende casais |
| Segmento | Psicanálise clínica e psicoterapia |

**Variações geográficas para os termos LSI:** Indaiatuba, Indaiatuba - SP, Centro de Indaiatuba, Instituto Laar, interior de São Paulo, região de Campinas (para o online: "de qualquer cidade ou estado").

## 2. Classificação das palavras-chave por intenção

### Transacionais (76 termos oficiais, todos "em Indaiatuba")
Vão para páginas de serviço. Foco em conversão.
- **Atendimento e modalidades (8):** Psicanálise, Atendimento psicanalítico, Consulta com psicanalista, Psicoterapia, Terapia individual, presencial, online, para adultos.
- **Ansiedade e sobrecarga (11):** ansiedade, preocupações excessivas, estresse, esgotamento emocional, sobrecarga emocional, autocobrança, perfeccionismo, medo de errar, medo de fracassar, dificuldade de relaxar, pensamentos repetitivos.
- **Autoestima e autoconhecimento (15), Relacionamentos (15), Luto, tristeza e mudanças (13), Trabalho e desenvolvimento emocional (13), Trauma (1).**

### Informacionais (vieram do autocompletar do Google)
Vão para o blog. Foco em educar e levar à página transacional.
- "quem pode ser psicanalista", "psicanalista precisa ser psicólogo", "psicanalista é formado em quê"
- "por que fazer psicanálise", "psicanálise o que faz", "psicanálise funciona", "por que psicanálise não é ciência"
- "qual terapia para ansiedade", "quem tem ansiedade precisa fazer terapia", "terapia ajuda na ansiedade"
- "terapia online é seguro", "terapia online é eficaz", "é melhor terapia online ou presencial"
- "o que causa traumas psicológicos", "como superar traumas", "o que são traumas psicológicos"
- "o que é crise existencial", "o que fazer numa crise existencial", "por que temos crise existencial"
- "por que o autoconhecimento é importante"

## 3. Arquitetura hierárquica (Pillar → Clusters)

### Páginas transacionais

| Tipo | Página | Slug | Palavra-chave foco | Linka para |
|---|---|---|---|---|
| Transacional | Home | `/` | psicanalista em Indaiatuba | pilares e `/atendimento/` |
| Transacional | Pilar principal | `/psicanalista-em-indaiatuba/` | psicanálise em Indaiatuba | pilares de tema |
| Transacional | Índice de serviços | `/servicos/` | atendimento psicanalítico em Indaiatuba | 7 pilares |
| Transacional | Pilar Trauma e tanatologia | `/servicos/trauma-e-tanatologia/` | terapia para traumas em Indaiatuba | `/contato/` |
| Transacional | Pilar Ansiedade e sobrecarga | `/servicos/ansiedade-e-sobrecarga/` | terapia para ansiedade em Indaiatuba | `/contato/` |
| Transacional | Pilar Autoestima e autoconhecimento | `/servicos/autoestima-e-autoconhecimento/` | terapia para autoconhecimento em Indaiatuba | `/contato/` |
| Transacional | Pilar Relacionamentos | `/servicos/relacionamentos/` | terapia para conflitos nos relacionamentos em Indaiatuba | `/contato/` |
| Transacional | Pilar Luto, tristeza e mudanças | `/servicos/luto-tristeza-e-mudancas/` | acompanhamento para luto em Indaiatuba | `/contato/` |
| Transacional | Pilar Trabalho e desenvolvimento | `/servicos/trabalho-e-desenvolvimento-emocional/` | terapia para estresse no trabalho em Indaiatuba | `/contato/` |
| Transacional | Pilar Modalidades | `/servicos/modalidades/` | terapia online em Indaiatuba | `/atendimento/` |
| Transacional | Atendimento | `/atendimento/` | consulta com psicanalista em Indaiatuba | `/contato/` |
| Transacional | Sobre (E-E-A-T) | `/sobre/` | Nelson Salustiano psicanalista | `/atendimento/` |
| Transacional | Contato | `/contato/` | agendar psicanálise Indaiatuba | WhatsApp |

### Clusters informacionais (blog) e para onde linkam

Taxonomia sugerida: `/blog/<categoria>/<titulo>/`. Os 6 artigos já publicados estão marcados como existente.

| Tipo | Cluster | Slug sugerido | Palavra-chave foco | Linka para (pilar) |
|---|---|---|---|---|
| Informacional | Psicanalista, psicólogo e psiquiatra (existente) | `/blog/psicanalise/psicanalista-psicologo-psiquiatra/` | diferença psicanalista psicólogo | `/psicanalista-em-indaiatuba/` |
| Informacional | O que é psicanálise (existente) | `/blog/psicanalise/o-que-e-psicanalise/` | o que é psicanálise | `/psicanalista-em-indaiatuba/` |
| Informacional | Quanto tempo dura a análise | `/blog/psicanalise/quanto-tempo-dura-a-analise/` | quanto tempo dura psicanálise | `/servicos/modalidades/` |
| Informacional | Primeira sessão de psicanálise | `/blog/psicanalise/primeira-sessao-de-psicanalise/` | primeira sessão de psicanálise | `/atendimento/` |
| Informacional | Psicanálise funciona? críticas e evidências | `/blog/psicanalise/psicanalise-funciona/` | psicanálise funciona | `/psicanalista-em-indaiatuba/` |
| Informacional | Terapia para ansiedade (existente) | `/blog/ansiedade/terapia-para-ansiedade/` | qual terapia para ansiedade | `/servicos/ansiedade-e-sobrecarga/` |
| Informacional | Sintomas de ansiedade: quando buscar ajuda | `/blog/ansiedade/sintomas-de-ansiedade/` | sintomas de ansiedade | `/servicos/ansiedade-e-sobrecarga/` |
| Informacional | Autocobrança e perfeccionismo | `/blog/ansiedade/autocobranca-e-perfeccionismo/` | autocobrança excessiva | `/servicos/ansiedade-e-sobrecarga/` |
| Informacional | Estresse, burnout e ansiedade | `/blog/ansiedade/estresse-burnout-ansiedade/` | diferença estresse burnout ansiedade | `/servicos/ansiedade-e-sobrecarga/` |
| Informacional | Pensamentos repetitivos | `/blog/ansiedade/pensamentos-repetitivos/` | pensamentos repetitivos | `/servicos/ansiedade-e-sobrecarga/` |
| Informacional | Por que o autoconhecimento é importante | `/blog/autoconhecimento/por-que-autoconhecimento-importa/` | por que o autoconhecimento é importante | `/servicos/autoestima-e-autoconhecimento/` |
| Informacional | Síndrome do impostor | `/blog/autoconhecimento/sindrome-do-impostor/` | síndrome do impostor | `/servicos/autoestima-e-autoconhecimento/` |
| Informacional | Dificuldade de impor limites | `/blog/autoconhecimento/dificuldade-de-impor-limites/` | dificuldade de dizer não | `/servicos/autoestima-e-autoconhecimento/` |
| Informacional | Crise existencial (existente) | `/blog/autoconhecimento/crise-existencial/` | o que é crise existencial | `/servicos/luto-tristeza-e-mudancas/` |
| Informacional | Ciúmes: de onde vêm | `/blog/relacionamentos/ciumes/` | por que sinto ciúmes | `/servicos/relacionamentos/` |
| Informacional | Dependência emocional: sinais | `/blog/relacionamentos/dependencia-emocional/` | dependência emocional sinais | `/servicos/relacionamentos/` |
| Informacional | Como lidar com o fim de um relacionamento | `/blog/relacionamentos/fim-de-relacionamento/` | como lidar com término | `/servicos/relacionamentos/` |
| Informacional | Fases do luto: existe tempo certo | `/blog/luto/fases-do-luto/` | fases do luto | `/servicos/luto-tristeza-e-mudancas/` |
| Informacional | Luto antecipatório | `/blog/luto/luto-antecipatorio/` | luto antecipatório | `/servicos/luto-tristeza-e-mudancas/` |
| Informacional | Como apoiar alguém em luto | `/blog/luto/como-apoiar-alguem-em-luto/` | como ajudar quem está de luto | `/servicos/luto-tristeza-e-mudancas/` |
| Informacional | Traumas psicológicos (existente) | `/blog/trauma/traumas-psicologicos/` | o que são traumas psicológicos | `/servicos/trauma-e-tanatologia/` |
| Informacional | O que é tanatologia | `/blog/trauma/o-que-e-tanatologia/` | o que é tanatologia | `/servicos/trauma-e-tanatologia/` |
| Informacional | Trauma de infância na vida adulta | `/blog/trauma/trauma-de-infancia/` | trauma de infância adulto | `/servicos/trauma-e-tanatologia/` |
| Informacional | Estresse no trabalho: sinais | `/blog/trabalho/estresse-no-trabalho/` | estresse no trabalho sinais | `/servicos/trabalho-e-desenvolvimento-emocional/` |
| Informacional | Assédio moral e efeitos emocionais | `/blog/trabalho/assedio-moral-efeitos-emocionais/` | assédio moral consequências emocionais | `/servicos/trabalho-e-desenvolvimento-emocional/` |
| Informacional | Procrastinação: por que adiamos | `/blog/trabalho/procrastinacao/` | por que procrastino | `/servicos/trabalho-e-desenvolvimento-emocional/` |
| Informacional | Terapia online (existente) | `/blog/atendimento-online/terapia-online/` | terapia online é segura | `/servicos/modalidades/` |
| Informacional | Como se preparar para a terapia online | `/blog/atendimento-online/como-se-preparar-terapia-online/` | como se preparar terapia online | `/servicos/modalidades/` |

## 4. Briefing por página

Formato: Tipo, Slug, Palavra-chave foco, Termos LSI, Briefing. Em todos, usar o NAP quando indicado e o tom de acolhimento, sem promessa de cura.

### Páginas transacionais

**Home** (Transacional, `/`)
- Foco: psicanalista em Indaiatuba
- LSI: psicanalista clínico Indaiatuba, psicoterapia Indaiatuba, atendimento psicanalítico Centro, consulta com psicanalista, Instituto Laar, trauma e tanatologia
- Briefing: converter para agendamento pelo WhatsApp. Mostrar credenciais (ANTPC-RP 842/22), 6 temas, modalidades, perguntas frequentes. NAP completo no topo, no corpo e no rodapé.

**Pilar principal** (Transacional, `/psicanalista-em-indaiatuba/`)
- Foco: psicanálise em Indaiatuba
- LSI: atendimento psicanalítico, terapia individual, terapia presencial, terapia online, psicoterapia, terapia para adultos, escuta psicanalítica
- Briefing: página de entrada para quem busca o serviço. Explicar o atendimento em linguagem simples e distribuir para os temas. Evitar disputa com a home: aqui o foco é o serviço "psicanálise", a home foca a profissional.

**Índice de serviços** (Transacional, `/servicos/`)
- Foco: atendimento psicanalítico em Indaiatuba
- LSI: temas de atendimento, sofrimento emocional, terapia para adultos
- Briefing: distribuir para os 7 pilares, sem conteúdo educativo longo.

**Pilares de tema** (Transacionais, `/servicos/<tema>/`)
Cada pilar tem uma seção H2 por palavra-chave oficial do grupo. Foco = palavra-chave principal do grupo (tabela da seção 3).
- LSI geral: "em Indaiatuba", Centro, Instituto Laar, escuta psicanalítica, sigilo, atendimento individual, presencial ou online.
- LSI por tema:
  - Trauma e tanatologia: elaboração, finitude, perda, morte, sentido de vida.
  - Ansiedade e sobrecarga: preocupação, estresse, esgotamento, autocobrança, medo de errar.
  - Autoestima e autoconhecimento: insegurança, autocrítica, limites, culpa, vergonha, impostor.
  - Relacionamentos: ciúmes, dependência emocional, término, separação, comunicação, confiança.
  - Luto, tristeza e mudanças: perdas, solidão, vazio, crise existencial, propósito, decisões.
  - Trabalho e desenvolvimento: carreira, rotina, procrastinação, raiva, pertencimento.
  - Modalidades: videoconferência, agendamento, adultos, individual.
- Briefing: converter. Cada seção responde "isso é para mim?" e leva ao contato. Linkar para os clusters do tema. Não aprofundar explicações educativas: isso é função do blog.
- NAP: telefone e endereço no corpo, horário na faixa de atendimento.

**Atendimento** (Transacional, `/atendimento/`)
- Foco: consulta com psicanalista em Indaiatuba
- LSI: endereço Instituto Laar, como chegar, horário, agendamento, atendimento online
- Briefing: logística completa. NAP completo, mapa, tabela de horários, passo a passo de agendamento.

**Sobre** (Transacional de confiança, `/sobre/`)
- Foco: Nelson Salustiano psicanalista
- LSI: formação, registro ANTPC-RP 842/22, especialização trauma e tanatologia, abordagem, ética
- Briefing: E-E-A-T. Credenciais, abordagem, postura ética. Foto real do Nelson.

**Contato** (Transacional, `/contato/`)
- Foco: agendar psicanálise Indaiatuba
- Briefing: formulário, WhatsApp, NAP completo, aviso de que não é canal de emergência (CVV 188, SAMU 192).

### Clusters informacionais

Para todos: tom educativo e acolhedor, responder a pergunta em até 150 palavras no início, subtítulos em forma de pergunta, trecho final com link para o pilar indicado na seção 3 e chamada suave ao agendamento com o NAP resumido. Sem promessa de cura.

| Cluster | Termos LSI sugeridos |
|---|---|
| Psicanalista, psicólogo e psiquiatra (existente) | formação do psicanalista, CRP, psiquiatra receita medicação, ANTPC, análise pessoal |
| O que é psicanálise (existente) | associação livre, sessão de análise, inconsciente, Freud, escuta |
| Quanto tempo dura a análise | frequência das sessões, processo analítico, tempo de cada pessoa, Indaiatuba |
| Primeira sessão de psicanálise | como funciona, o que falar, sigilo, agendamento, Indaiatuba |
| Psicanálise funciona? críticas e evidências | ciência, pesquisa, críticas, abordagem, limites, avaliação médica |
| Terapia para ansiedade (existente) | sintomas, tipos de terapia, avaliação médica, psicoterapia, Indaiatuba |
| Sintomas de ansiedade | coração acelerado, insônia, preocupação, quando procurar ajuda |
| Autocobrança e perfeccionismo | exigência, medo de falhar, cobrança interna, origem |
| Estresse, burnout e ansiedade | esgotamento, trabalho, sobrecarga, diferenças |
| Pensamentos repetitivos | ruminação, preocupação, sono, repetição |
| Por que o autoconhecimento é importante | escolhas, relações, história pessoal, escuta |
| Síndrome do impostor | autoestima, conquistas, trabalho, culpa |
| Dificuldade de impor limites | dizer não, culpa, agradar, relações |
| Crise existencial (existente) | sentido, identidade, mudança, finitude |
| Ciúmes | insegurança, comparação, medo de perder, vínculo |
| Dependência emocional | apego, medo de abandono, relações, autonomia |
| Fim de relacionamento | luto amoroso, separação, divórcio, recomeço |
| Fases do luto | perda, tristeza, tempo, elaboração, tanatologia |
| Luto antecipatório | doença, despedida, finitude, familiares |
| Como apoiar alguém em luto | o que dizer, escuta, presença, rede de apoio |
| Traumas psicológicos (existente) | experiência traumática, elaboração, lembranças, violência, perda |
| O que é tanatologia | morte, morrer, perda, finitude, especialização |
| Trauma de infância | vínculos, memória, repetição, vida adulta |
| Estresse no trabalho | prazos, cobrança, sinais, limites |
| Assédio moral e efeitos emocionais | humilhação, medo, orientação jurídica, acolhimento |
| Procrastinação | medo, exigência, adiamento, rotina |
| Terapia online (existente) | videoconferência, sigilo, privacidade, presencial |
| Como se preparar para a terapia online | local reservado, fones, internet, plataforma |

## 5. Regras de linkagem e governança

1. Todo cluster linka para o pilar indicado e, no fim, para `/atendimento/` ou `/contato/`.
2. Cada pilar linka para os 3 a 5 clusters do seu tema, numa seção "Leia também" ao fim, mantendo o conteúdo principal transacional.
3. Nenhum pilar recebe texto educativo longo. Conteúdo explicativo vai para o blog.
4. Uma palavra-chave foco por página, sem repetir entre páginas (evitar canibalização entre home e `/psicanalista-em-indaiatuba/`).
5. NAP idêntico (nome, endereço, telefone) em todo o site, no rodapé e nos dados estruturados.
6. Dados estruturados: um conjunto único para o consultório (local), Service nos pilares, Article e FAQ nos artigos.

## 6. Pontos de decisão (comparação com o que já existe no site)

- **URLs do blog:** hoje os artigos estão na raiz (`/nome-do-artigo/`). A taxonomia proposta usa `/blog/<categoria>/<titulo>/`. Mudar antes do lançamento é seguro, depois exige redirecionamentos.
- **Home e `/psicanalista-em-indaiatuba/`:** hoje a home foca "psicanalista em Indaiatuba" e a página "psicanálise em Indaiatuba". Manter assim, com textos diferentes.
- **Pilares de tema:** concentram 76 seções. Numa segunda fase, promover os temas de maior busca (ansiedade, luto, trauma, autoconhecimento) a páginas próprias, mantendo o pilar como índice.
- **Publicação:** hoje existem 6 de 28 clusters. Ordem sugerida: psicanálise, ansiedade, luto e trauma primeiro.
- **Validação:** conferir volume e dificuldade das palavras-chave informacionais antes de escrever (Ubersuggest ou Semrush).
