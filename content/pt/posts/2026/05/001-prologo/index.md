+++
title = "Prólogo: 12 Horas, 3 Sistemas de Comentários e um Blog (Quase) Funcional"
date = 2026-05-06
draft = false
slug = "prologo-blog-quase-funcional"
tags = ["hugo", "linux", "blog", "open-source", "github-pages"]

[cover]
    image = "images/Prologo-Aperture.webp"
    alt = "Old School Monitor"
    relative = true
+++


Eu tinha um objetivo simples: iniciar um blog para compartilhar minhas aventuras e desventuras técnicas envolvendo Linux, software livre e assuntos correlatos. Bolei uma estrutura legal, um layout honesto, fiz alguma pesquisa sobre plataformas e pronto — decidi hospedar tudo no GitHub. Parecia um caminho lógico e natural, já que um blog sobre Open Source *precisa* ficar no GitHub, certo?

Parecia certo.

Dizem que configurar um blog estático com Hugo é *"vapt-vupt"*. É o que os tutoriais no YouTube, gravados por pessoas que provavelmente não têm um FX-6300 e uma inclinação genética para a teimosia, tentam te vender. A realidade? É uma guerra de trincheiras contra arquivos `.toml` e hierarquias de pastas que parecem ter sido desenhadas por um arquiteto sádico.


---

## O Plano Original

A ideia era simples: colocar o **Teimoso do Linux** no ar.

- **Motor:** Hugo
- **Tema:** PaperMod
- **Objetivo:** ter um lugar para documentar minhas peripécias técnicas sem as distrações das redes sociais

Tudo corria razoavelmente bem, até eu pensar:

> *"Mas seria bom ter uma área de comentários no rodapé. Afinal, todo Blog tem isso."*

Mal sabia eu que o "ato final" — configurar uma simples caixa de comentários — se tornaria o meu **final boss**.

<p align="center">
  <img src="images/Git-King.webp" width="80%" alt="GitHub o início">
  <br><em>Criar uma conta no GitHub foi a parte fácil.</em>
</p>


---

## A Odisséia das Ferramentas

### 1. Disqus — *A Via Tradicional*

*"Se o mestre Fabio Akita usa, eu uso"*, pensei. Vamos de Disqus. Configurei o shortname, ajustei o arquivo de configuração e... nada. O rodapé continuava um deserto de pixels cinzas.

O Disqus é como aquele driver proprietário que você sabe que deveria funcionar, mas que decide entrar em greve sem emitir um único log de erro.

### 2. Giscus — *A Via Nerd*

Apelei para o Giscus. *"Vamos usar as Discussions do GitHub!"*, gritei para as paredes. O resultado? O blog, em um ato de rebeldia pura, decidiu **renderizar o código-fonte do script na tela** em vez de executar a ferramenta.

Ver o seu próprio código HTML impresso como se fosse um poema concretista é uma experiência transcendental, mas pouco funcional.

### 3. Cactus.chat — *A Via da Privacidade*

Tentei ser ético. Tentei ser minimalista. O Cactus.chat prometia comentários via Matrix, sem rastreio e com visual limpo.

O Hugo respondeu exibindo apenas o título *"Comentários"*, seguido de um vácuo existencial.

---

## O "Berro" do Goldmark

No meio do caminho, descobri que o Hugo tem um sistema de segurança chamado **Goldmark** que, por padrão, trata qualquer HTML "estranho" como uma ameaça biológica.

Tentei desativar a trava com o famoso:

```toml
unsafe = true
```

O Hugo não apenas ignorou o comando, como *berrou* erros de sintaxe que me fizeram questionar se eu ainda sabia ler um arquivo de configuração.

<p align="center">
  <img src="images/Crisis-Finalis.webp" width="80%" alt="Desgraça pouca é bobagem">
  <br><em>Nada como um dia exasperante de combate contra o terminal.</em>
</p>

---

## Lições de um Dia de Combate

Após horas editando parciais, criando overrides de layouts e reiniciando o servidor (`hugo server -D`) mais vezes do que reiniciei meu primeiro Slackware, cheguei a uma conclusão importante:

> **O "feito" é melhor que o "perfeito", mas o "postado" é melhor que o "esgotado".**

O blog está no ar. As tags estão lá. A busca *(que também deu luta!)* está operacional. O design está limpo.

O fato de não haver comentários agora talvez seja um aviso do universo: antes de ouvir a opinião dos outros, eu precisava primeiro terminar de configurar o meu próprio espaço.

---

## Próximos Passos

Se você está lendo isso e quer comentar — sinto muito: você não pode. Pelo menos não hoje. A caixa de comentários ainda é um mito urbano neste domínio. Certamente esqueci alguma vírgula fora de lugar em arquivos de configuração ocultos, ou apaguei algo que não deveria.

Mas fiquem tranquilos: **a teimosia não morreu**. Ela só foi dormir para não jogar o notebook pela janela.

---

*Veredito:* **Hugo 1 × 0 Sanidade Mental.** *(Mas haverá volta.)*
