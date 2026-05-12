+++
title = "What Does a Nerd Do on a Saturday Night?"
date = 2026-05-09
draft = false
slug = "what-does-a-nerd-do"
tags = ["blog", "configuration", "hugo", "papermod", "social media", "Batman"]

[cover]
    image = "images/header-1200x630.webp"
    alt = "Saturday night"
    relative = true
+++

He certainly doesn't go out dressed as a bat, hunting clown-costumed criminals to beat up.

He polishes bits. Obviously.

While the outside world was doing outside world things, I was here in my home office — between the computer desk, the laptop desk and the drawing board — wrapping up the last configuration loose ends on the blog. An anorexic social life, as the true nerd manual dictates.

But it was a productive night. And productivity deserves documentation.

---

## Exorcising the "About" Ghost

The first bug hunted down that night was subtle. Using the blog's search function and typing "A" or "About" returned a result pointing to an *About* page — that didn't exist. Ghost page. Haunting from a previous configuration.

The culprit: a forgotten `content/about.md` file lurking in a corner, leftover from an earlier attempt. The menu entry had been removed, but the file stayed behind. Hugo indexed the content in search results even without a navigation link. One surgical `rm` and a `hugo --gc` later, the ghost was exorcised.

First lesson of the night: in Hugo, deleting from the menu is not the same as deleting the content.

---

## Bio Updated, Identity Consolidated

I took the opportunity to update the blog bio to mirror exactly what's on social media:

> *"Analog dinosaur from the DOS era, getting beaten by Open Source since 2002 and losing sanity from excessive Xterm usage."*

<br>
<p align="center">
  <img src="images/Subgenius_Celus_512x512.webp" width="80%" alt="SubGenius Nerd">
  <br><em>Quite the character.</em>
</p>

---

## The Favicon and the Wrong Browser Saga

Every self-respecting blog needs a favicon — that tiny icon that appears in the browser tab and that 90% of people ignore, but whose absence bothers anyone who knows it should be there.

I tried PNG. Didn't work. Tried SVG. Nothing. Converted to the ancient `.ico` format using an online converter — and it worked on the first try.

The legacy format wins again. The modern option isn't always better; sometimes it's just more annoying.

The tragicomic detail of the night: I spent several minutes frantically hitting reload to see if the icon would appear, with zero results. When I finally realized what was happening, I'd been pressing F5 on the GitHub Pages address — not the local server. The blog had been running at `localhost:1313` the whole time.

Who hasn't been there.

---

## Social Icons in the Theme

PaperMod, the Hugo theme used here on the blog, has native support for social icons, and the theme already knows about X (formerly Twitter) and Instagram. All it took was adding the entries to `hugo.toml`:

```toml
[[params.socialIcons]]
  name = "x"
  url = "https://x.com/teimosodolinux"

[[params.socialIcons]]
  name = "instagram"
  url = "https://instagram.com/teimosodolinux"
```

Worked on the first try. I'm getting good at this.

<br>
<p align="center">
  <img src="images/social-900x600.webp" width="80%" alt="X logo">
  <br><em>Elon Musk, my buddy.</em>
</p>

---

## Social Media Exists. I Have Proof.

**Teimoso do Linux** already has a confirmed presence on X and Instagram, both with the handle `@teimosodolinux`. And to prove this isn't just talk, here's the project's first official social media post:

{{< x user="TeimosoDoLinux" id="2053190666323169552" >}}

"I don't use Linux because it's good. I use Linux because I'm stubborn."

Philosophy summarized in 140 characters.

---

## Period. (For Today)

Blog with favicon, consolidated bio, ghosts removed, social media live and icons working. The heavy configuration work is done — officially, or at least unofficially.

The next post will be the formal introduction of the blog and the project. That is, if nothing else breaks along the way. But that's for another day.

For today, the Stubborn One is going to sleep. The bits are sufficiently polished.

---

## Epilogue: I Celebrated Too Soon

I said I was getting good at this. I celebrated too soon.

The blog collapsed faster than a house of cards during attempts to embed a Twitter snippet. The server crashed, the log spat out errors in series, and the root cause was simple and humiliating: Hugo evolved, Elon Musk renamed Twitter to X, and the entire world had to update their configs as a result.

The `{{</* tweet */>}}` shortcode was removed in Hugo v0.156.0. The correct one now is `{{</* x */>}}`. And the privacy block in `hugo.toml` that used to be `[privacy.twitter]` is now `[privacy.x]`. Two details. Two crashes. One mental curse at Elon Musk. And one at Bill Gates too, just to keep the tradition alive.

Mental note: seriously reconsider this habit of embedding things in the blog.

---

*Written on a Saturday night, with Hugo server open in one tab and GitHub in another — sometimes in the wrong tab. Cláudio delivered the draft in YAML. The blog uses TOML. Cláudio suggested `privacy.twitter`, already deprecated. The Stubborn One pasted the log. Balance restored, twice.*

*Who on earth is "Cláudio"? Just one of my AI virtual assistants. Claude was too formal for me, Jarvis was already taken. A "rebrand" to Cláudio was the only logical solution, obviously.*