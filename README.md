# Vinheria Agnello

## Descrição do caso

A **Vinheria Agnello** é uma empresa fictícia do ramo de vinhos, utilizada como estudo de caso para o desenvolvimento de um site institucional em HTML e CSS. O objetivo é apresentar a marca, a história, os produtos, sugestões de harmonização e um canal de contato, com layout organizado, acessível e alinhado à identidade visual da vinharia.

## Estrutura do projeto

| Arquivo / pasta | Função |
|-----------------|--------|
| **index.html** | Página inicial: apresentação da vinharia, destaques e acesso rápido às demais seções. |
| **src/pages/historia.html** | História da empresa e sua trajetória. |
| **src/pages/produtos.html** | Catálogo de vinhos com tabela de informações. |
| **src/pages/harmonizacao.html** | Sugestões de harmonização entre vinhos e alimentos. |
| **src/pages/contato.html** | Formulário de contato e confirmação após o envio. |
| **src/css/style.css** | Estilos globais, layout, formulário, tabelas e componentes. |
| **src/css/efeitos.css** | Animações e transições reutilizadas (importado por `style.css`). |

Os arquivos HTML da raiz e de `src/pages/` compartilham o mesmo cabeçalho, rodapé e folha de estilo principal (`src/css/style.css`).

## Integrantes

- Luiz Soares  
- Gustavo Noleto  
- Lucas Gaspar  

## Link do site (GitHub Pages)

https://luizademario.github.io/Vinheria_Agnello/

---

## Efeitos visuais

No CSS foram aplicadas **pseudo-classes**, **pseudo-elementos**, **transições** e **animações** para feedback visual, hierarquia e consistência com a paleta do site.

### Pseudo-classes

- **`:hover`** — Links do menu (cor e leve deslocamento em `efeitos.css`); imagem do banner (escala e rotação suave); linhas da tabela de produtos (fundo destacado); links “ver produto” (cor e sublinhado); cards da grade (escala e sombra); botões do formulário e do modal (cor e sombra); barra de rolagem customizada (`::-webkit-scrollbar-thumb:hover`).
- **`:focus`** — Links do menu e de produto (contorno visível para teclado); campos nome, e-mail e mensagem (contorno, fundo e borda); botões de enviar e fechar modal (contorno).
- **`:active`** — Links do menu e de produto (estado ao clicar: fundo/cores contrastantes).

### Pseudo-elementos

- **`h2::after`** — Barra decorativa abaixo dos subtítulos (`content`, largura fixa, cor da marca).
- **`::selection`** — Cor de fundo e texto ao selecionar conteúdo na página (identidade visual).
- **`::-webkit-scrollbar`**, **`::-webkit-scrollbar-track`**, **`::-webkit-scrollbar-thumb`** — Estilização da barra de rolagem (navegadores WebKit), alinhada às cores do projeto.

*(No formulário, `*::before` e `*::after` entram na regra de `box-sizing` para padronizar dimensões; não alteram aparência diretamente.)*

### Animações e `@keyframes`

- **`pulsarSuave`** — Aplicada ao título principal (`main h1`): leve variação de escala e opacidade em loop, chamando atenção sem poluir a leitura.
- **`fadeIn`** — Aplicada aos `h2`: entrada com opacidade e deslocamento vertical (`translateY`), deixando os títulos de seção mais suaves ao carregar.

As animações estão definidas em `src/css/efeitos.css` e o `style.css` importa esse arquivo no início.

### Transições (`transition`)

Transições em cores, `transform` e `box-shadow` nos links do menu, banner, cards, botões e links de produto tornam as mudanças de estado menos bruscas e melhoram a percepção de qualidade da interface.
