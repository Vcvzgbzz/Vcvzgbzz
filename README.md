# Jadeyn Fincher

I build things I want to understand by running them myself.

Day job is React and TypeScript: customer-facing analytics and reporting over
real-time data. Everything below is what I do with the rest of my time.

[jadeynfincher.com](https://jadeynfincher.com) · [LinkedIn](https://www.linkedin.com/in/jadeyn-fincher)

## [Vechy's Room](https://ai.vechkabaz.com)

My AI platform: chat, image, and video generation from models running on my own
GPUs, open to anyone who signs up. It's a real multi-user app, not a demo, so
it has the parts that come with that: accounts, an API other tools build
against, a content policy and moderation, and separate dev and prod
environments on Kubernetes.

Most of what I've learned about running software comes from keeping this
thing up. Uptime is public at [status.vechkabaz.com](https://status.vechkabaz.com).

## [hearth](https://github.com/Vcvzgbzz/hearth)

One GPU fits one model at a time. Two clients asking for different models make
it thrash, each one evicting the other's weights. hearth sits in front of the
inference server and decides who goes next. It has priority lanes, it ages
waiting jobs so nothing starves, and it prefers whatever model is already
loaded. If a friend has spare capacity, it can send work to their box instead.

It speaks the OpenAI API, so switching to it is a URL change. It started as a
hack inside Vechy's Room and is now on npm as
[`@vcvzgbzz/hearth`](https://www.npmjs.com/package/@vcvzgbzz/hearth).

## [Running a 27B model on an Arc Pro B70](https://github.com/Vcvzgbzz/b70-cookbook)

The coding model behind Vechy's Room is Qwen3.8-27B on a single B70, served by
vLLM on Intel XPU with MTP speculative decoding. The cookbook has the patches,
launch flags, and eval scripts.

- **~142 tok/s on edits and ~106 on code**, single stream. The other public B70
  numbers I found for this model were in the mid 80s.
- Trimming the draft head's vocabulary to the tokens that actually show up in
  code got +5% for free. Acceptance didn't move.
- Profiling showed the GEMMs running at about 89% of the card's memory
  bandwidth. There isn't much left there.
- EvalPlus scored every 4-bit quant I tried as a tie. Comparing them token by
  token against Q8_0 showed G128 drifting 1.7 to 1.9x more than G32, for about
  11% more speed.

## Also

- [pi-vechkabaz](https://github.com/Vcvzgbzz/pi-vechkabaz) and
  [dsh-vechkabaz](https://github.com/Vcvzgbzz/dsh-vechkabaz): one-command setup
  so anyone with a key can point the pi and DeepSeek Harness coding agents at my API.
- Infrastructure: Proxmox, ZFS, Cloudflare Tunnel with CrowdSec at the edge,
  Grafana metrics, and centralized logging.

`TypeScript` · `React` · `MobX` · `Node` · `Python` · `Kubernetes` · `vLLM` · `Proxmox` · `ZFS`
