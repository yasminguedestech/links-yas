# 💜 Yasmin Guedes · Link in Bio

Página pessoal estilo *link-in-bio* (Linktree) da **Yasmin Guedes — Data Analyst**.
Reúne os principais links (portfólio, LinkedIn, GitHub e e-mail) em uma página única, leve e responsiva, com uma esfera 3D animada de fundo.

🔗 **Links da página**
- Portfólio: https://yasminguedes.vercel.app
- LinkedIn: https://linkedin.com/in/yasmin-guedes-0101
- GitHub: https://github.com/yasminguedestech
- E-mail: yasminguedestech@gmail.com
- 📍 São Paulo, SP

---

## ✨ Features

- **Esfera 3D animada** no fundo (Three.js) com gradiente que muda de cor sozinho (rosa → lilás → roxo).
- **Foto de perfil** embutida no próprio HTML (base64) — não depende de arquivo externo.
- **Botões em vidro fosco** (glassmorphism) com animação de entrada e micro-interações no hover.
- **100% responsivo** — a esfera reescala e se reposiciona em telas pequenas.
- **Acessibilidade**: respeita `prefers-reduced-motion` (reduz a animação pra quem prefere menos movimento).
- **Arquivo único**: tudo (HTML, CSS, JS e a foto) vive em um só `index.html`.

---

## 🛠️ Tecnologias

- HTML5, CSS3 e JavaScript puro (sem build, sem framework)
- [Three.js](https://threejs.org/) (carregado via CDN) para a esfera 3D
- Fontes [Fraunces](https://fonts.google.com/specimen/Fraunces) e [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) (Google Fonts)

---

## 📁 Estrutura

```
.
├── index.html   # a página inteira (HTML + CSS + JS + foto em base64)
└── README.md
```

---

## ▶️ Rodando localmente

Como é um arquivo estático, basta abrir o `index.html` no navegador.
Pra ver a animação 3D, é preciso estar **conectado à internet** (o Three.js vem de CDN).

Opcional — servidor local:

```bash
# Python
python3 -m http.server 5500
# depois acesse http://localhost:5500
```

---

## 🚀 Deploy na Vercel

1. Suba este repositório no GitHub.
2. Em [vercel.com](https://vercel.com), clique em **Add New → Project** e importe o repositório.
3. Não precisa configurar build (é estático) — deixe os campos no padrão e clique em **Deploy**.
4. Pronto: a Vercel gera o link público automaticamente. 🎉

> Dica: também dá pra arrastar a pasta direto na Vercel CLI com `vercel`.

---

## 🎨 Como personalizar

Tudo está no `index.html`:

| O que mudar | Onde |
|---|---|
| **Nome / cargo / textos** | dentro de `<main class="wrap">` |
| **Links** | nos `<a class="link" href="...">` |
| **Trocar a foto** | substitua o `src="data:image/jpeg;base64,..."` da `<img>` por uma nova imagem em base64 (ou por um caminho/URL de arquivo) |
| **Cores da esfera** | variável `hue` no `fragmentShader` (dentro da `<script>`) |
| **Velocidade / intensidade da animação** | `u_intensity` e os incrementos em `mesh.rotation` |
| **Paleta geral** | bloco `:root { ... }` no CSS |

### Trocar a foto por um arquivo externo
Se preferir não usar base64, salve a imagem (ex.: `perfil.jpg`) na raiz do projeto e troque:

```html
<img src="perfil.jpg" alt="Yasmin Guedes" />
```

---

## 📬 Contato

**Yasmin Guedes** — Data Analyst
📧 yasminguedestech@gmail.com · 📍 São Paulo, SP

> Obrigada por fazer parte desta etapa da minha trajetória. 💜
