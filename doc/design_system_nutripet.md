t# Design System — NutriPet

## Objetivo
Padronizar a interface do site institucional da NutriPet, preservando a identidade visual da marca e garantindo consistência, acessibilidade e responsividade.

## 1. Paleta de cores

| Token | Cor | HEX | Aplicação |
|---|---|---|---|
| Primária | Azul-marinho | `#123B68` | Títulos, links e botões principais |
| Secundária | Amarelo | `#FFC928` | Promoções e destaques |
| Complementar | Turquesa | `#20A6A6` | Botões secundários e ícones |
| Complementar | Azul-claro | `#78BDF2` | Fundos e elementos de apoio |
| Destaque | Coral | `#F27A42` | Chamadas pontuais |
| Fundo | Creme | `#FFF9EF` | Fundos de seções |
| Neutra | Branco | `#FFFFFF` | Cards e campos |
| Texto | Grafite | `#263445` | Textos e títulos |

## 2. Tipografia

- **Títulos e botões:** Poppins — pesos 600 e 700.
- **Textos e descrições:** Nunito Sans — pesos 400 e 500.

| Elemento | Desktop | Mobile | Peso |
|---|---:|---:|---:|
| H1 | 40 px | 30 px | 700 |
| H2 | 32 px | 26 px | 700 |
| H3 | 24 px | 22 px | 600 |
| H4 | 20 px | 18 px | 600 |
| Parágrafo | 16 px | 16 px | 400 |
| Texto pequeno | 14 px | 14 px | 400 |
| Botão | 16 px | 15 px | 600 |

Usar entrelinha confortável, hierarquia clara e negrito apenas para informações importantes.

## 3. Botões

- **Primário:** fundo `#123B68`, texto branco.
- **Secundário:** fundo `#20A6A6`, texto branco.
- **Destaque:** fundo `#FFC928`, texto `#123B68`.
- Fonte Poppins SemiBold; altura de 48 px; padding horizontal de 24 px; raio de 12 px.

Estados: normal, hover (mudança sutil de tonalidade), pressionado, foco visível por teclado, desabilitado (opacidade reduzida) e carregando (indicador visual e interação bloqueada).

## 4. Formulários

- Campos brancos, borda cinza-claro, raio de 10 px e altura de 48 px.
- Padding interno de 14 px; fonte Nunito Sans; rótulos acima dos campos.
- Estados: normal, foco (borda azul-marinho), erro (borda coral e mensagem), sucesso (confirmação) e desabilitado (fundo cinza-claro).
- Campos previstos: nome, e-mail, telefone, assunto e mensagem.
- Ação principal: **Enviar mensagem**.

## 5. Cards e componentes

**Card de produto:** imagem, nome, descrição ou preço e botão de consulta. Fundo branco, raio de 16 px, padding de 16 px e sombra leve.

**Card de oferta:** imagem, identificação da promoção, preço, condições e botão de consulta.

**Card de categoria:** ícone ou imagem, nome e fundo creme ou azul-claro.

Outros componentes reutilizáveis: banner promocional, card de contato, menu, barra de pesquisa, botão de WhatsApp, breadcrumb, avisos e rodapé.

## 6. Bordas, sombras e espaçamentos

| Elemento | Raio |
|---|---:|
| Botões | 12 px |
| Campos | 10 px |
| Cards | 16 px |
| Banners | 20 px |
| Tags | 20 px |

Sombras discretas: padrão `0 2px 8px rgba(38,52,69,.08)`; hover `0 6px 16px rgba(38,52,69,.12)`.

Escala de espaçamento: 4, 8, 16, 24, 32, 48 e 64 px.

## 7. Responsividade

| Dispositivo | Largura | Organização |
|---|---|---|
| Mobile | Até 767 px | Uma coluna e menu compacto |
| Tablet | 768–1023 px | Duas colunas e menu adaptado |
| Desktop | A partir de 1024 px | Três ou quatro colunas e menu horizontal |

Imagens devem manter proporção; cards e textos devem se ajustar à largura; botões precisam de área de toque confortável; navegação deve funcionar por toque e teclado; evitar rolagem horizontal.

## 8. Componentes por página

| Componente | Início | Sobre | Produtos | Ofertas | Contato |
|---|:---:|:---:|:---:|:---:|:---:|
| Cabeçalho e menu | ✓ | ✓ | ✓ | ✓ | ✓ |
| Banner | ✓ | — | — | ✓ | — |
| Card de produto | ✓ | — | ✓ | ✓ | — |
| Card de categoria | ✓ | — | ✓ | — | — |
| Botão WhatsApp | ✓ | ✓ | ✓ | ✓ | ✓ |
| Formulário | — | — | — | — | ✓ |
| Mapa | — | — | — | — | ✓ |
| Rodapé | ✓ | ✓ | ✓ | ✓ | ✓ |

**Cabeçalho:** logomarca, navegação e acesso ao contato; no mobile, menu hambúrguer.

**Rodapé:** logomarca, links, redes sociais, WhatsApp, endereço e horário de funcionamento.

## 9. Tokens para CSS

```css
:root {
  --color-primary: #123B68;
  --color-secondary: #FFC928;
  --color-turquoise: #20A6A6;
  --color-light-blue: #78BDF2;
  --color-coral: #F27A42;
  --color-cream: #FFF9EF;
  --color-white: #FFFFFF;
  --color-text: #263445;

  --font-heading: "Poppins", sans-serif;
  --font-body: "Nunito Sans", sans-serif;

  --radius-button: 12px;
  --radius-input: 10px;
  --radius-card: 16px;
  --radius-banner: 20px;

  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  --shadow-card: 0 2px 8px rgba(38,52,69,.08);
  --shadow-hover: 0 6px 16px rgba(38,52,69,.12);
}
```

## 10. Diretrizes finais

Aplicar os mesmos padrões em todas as páginas. Reutilizar componentes sempre que possível, manter contraste e legibilidade, oferecer foco visível para teclado e não alterar as cores, fontes ou características visuais originais da NutriPet.

Este documento serve como referência para implementação em CSS ou Tailwind CSS.
