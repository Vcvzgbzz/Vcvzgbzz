# Hello, I'm Jadeyn Fincher 👋

Front-end developer by trade, systems tinkerer by hobby. Most of my professional
work is React and TypeScript inside a private work org, so what's public here is
personal projects, which is also where I get to build the parts of the stack I
don't touch at work.

## What I do professionally

- 💻 Front-end development: TypeScript, React, and the tooling around them.
- 🎨 Interfaces that hold up. State that stays honest, components that compose,
  and UI that doesn't fall apart the moment the data gets messy.
- 💼 More detail on [LinkedIn](https://www.linkedin.com/in/jadeyn-fincher).

## What I build for myself

### 🖼️ [Vechy's Room](https://ai.vechkabaz.com)

A self hosted image and video generation app, live and open to sign ups. React,
Hono and SQLite on the front, a GPU doing diffusion work on the back. Multi user
with per account isolation, a content safety pipeline built on local LLM
sidecars, a community feed, and an API key surface that other clients build
against.

### Everything underneath it

All of this runs on a homelab I maintain and keep online.

- 🤖 A Discord bot driving the app through that same public API surface,
  deliberately a thin client with no privileged access.
- ⚡ GPU inference tuning on Intel Arc: quantised diffusion models, PyTorch XPU,
  and a fair amount of carefully measuring things that turned out not to help.
- 🛠️ The infrastructure itself. Proxmox, LXC, ZFS, Cloudflare Tunnel, CrowdSec,
  monitoring, and backups I actually restore test.

The source for these is private for now. Some of it may open up.

## Tools I reach for

`TypeScript` · `React` · `Node` · `Hono` · `Python` · `Java` · `SQLite` ·
`Linux` · `Proxmox` · `ZFS` · `LXC`

## Public repositories

- [CatScript Compiler](https://github.com/Vcvzgbzz/CatScript-Compilers-Project):
  my capstone, a compiler for a small language.
- [Redis Mini](https://github.com/Vcvzgbzz/RedisMini-Project): a from scratch
  reimplementation of a slice of the Redis command set.
- [Tic Tac Toe with AI](https://github.com/Vcvzgbzz/ticTacToeWithComputerAI):
  an early one, built for fun.
