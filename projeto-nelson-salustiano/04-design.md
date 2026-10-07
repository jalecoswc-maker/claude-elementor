# Design

O chaveiro usa preto, amarelo `#FFFF00`, verde WhatsApp e Roboto (visual de urgência). **Não reutilizar**: o site do Nelson deve ser calmo e acolhedor. Mantém-se a estrutura e a grade, troca-se a identidade.

## Paleta aprovada pelo usuário (contraste de texto verificado)
| Uso | Cor |
|---|---|
| Principal (títulos, rodapé, hero) | Azul-acinzentado `#3E5260` |
| Fundo claro | Areia `#F4EFE8` |
| Botões e destaques | Terracota `#9C5638` (texto branco: contraste ~5,5:1) |
| Apoio | Verde-sálvia `#8A9A87` |
| Texto | `#2B2F33` |

Evitar terracota mais claro (`#B5694A`) com texto branco: contraste ~4,1:1, abaixo do mínimo.

## Tipografia
Lora (títulos) + Inter (texto). Gravar como Global Fonts do Kit do Elementor.

## Como o chaveiro guarda o design (para replicar o mecanismo)
Kit ativo: `elementor_active_kit` → meta `_elementor_page_settings` com `system_colors`, `custom_colors`, `system_typography`.
Home: meta `_elementor_data` da página inicial (`page_on_front`).

## Pendente do usuário
Logo, foto do Nelson, link do Google Maps do Instituto Laar. Usar espaços reservados até chegarem.
