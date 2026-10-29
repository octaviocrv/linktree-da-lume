# Linktree da Lume

Página de links da **Lume | Soluções Digitais**: um linktree próprio, feito à mão, que leva o visitante direto para uma conversa no WhatsApp e para os serviços da Lume.

> Sites, automações e sistemas que resolvem problemas reais e geram resultado.

## O que tem na página

- **Foto do fundador + marca** no topo, para o contato começar com um rosto, não com um logo.
- **Card do WhatsApp em destaque**, com o status "Online agora" e um botão laranja como ação principal.
- **Serviços e contato** em uma lista única: site oficial, sites de alta conversão, automações e sistemas, e e-mail.
- **Botão flutuante do WhatsApp**, que aparece só depois que o card principal sai da tela.
- **Animações discretas**: uma cortina laranja na entrada e os blocos surgindo conforme o visitante rola.

## Visual

| | |
|---|---|
| Fundo | Off-white `#FAF8F5` com textura de grão e pontilhado |
| Destaque | Laranja Lume `#E8611A` |
| Texto | `#0A0A0A` |
| Fonte | [Satoshi](https://www.fontshare.com/fonts/satoshi), servida localmente |

A página foi pensada primeiro para o celular. Tamanhos e espaçamentos se ajustam à largura da tela, e o botão flutuante respeita a área segura do iPhone. Quem ativa "reduzir movimento" no sistema vê tudo sem animação.

## Tecnologia

HTML, CSS e um pouco de JavaScript puro. Sem framework, sem build e sem dependências.

```
.
├── index.html
└── assets/
    ├── css/styles.css
    ├── fonts/           # Satoshi (400, 500, 700)
    └── images/          # foto, símbolo e logo em webp
```

## Rodando localmente

Basta abrir o `index.html` no navegador. Para testar no celular, suba um servidor estático:

```bash
python -m http.server 5500
```

Depois acesse `http://localhost:5500`, ou `http://<IP-do-seu-PC>:5500` pelo celular no mesmo Wi-Fi.

## Editando

- **Links e textos:** direto no `index.html`.
- **Número do WhatsApp:** aparece em dois lugares no `index.html` (card principal e botão flutuante). Procure por `wa.me/`.
- **Cores e espaçamentos:** nas variáveis do `:root`, no início do `assets/css/styles.css`.
- **Foto:** use um retrato de no mínimo 1260 × 1323 px, porque o card exibe a imagem com até 420 × 441 px em telas de alta densidade. Converta para `.webp` e use um nome de arquivo novo a cada troca, para o celular não mostrar a versão antiga guardada.

---

Feito pela [Lume](https://www.lumewebsites.com.br/) · [@lume.mov](https://www.instagram.com/lume.mov/)
