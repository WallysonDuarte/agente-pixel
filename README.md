<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=e91e63&height=220&section=header&text=PIXEL&fontColor=ffffff&fontSize=72&fontAlignY=38&desc=UI/UX%20Designer&descSize=22&descAlignY=60" width="100%" />

<img src="./assets/portrait.png" width="200" alt="Pixel" />

# 🎨 Pixel · UI/UX Designer

**Desenha e implementa interface com sistema de design consistente, responsiva de verdade e acessivel por padrao — nao por correcao posterior.**

![Skills](https://img.shields.io/badge/skills-5-e91e63?style=for-the-badge)
![CLIs](https://img.shields.io/badge/CLIs-8-2980b9?style=for-the-badge)
![Idioma](https://img.shields.io/badge/pt--BR-nativo-1abc9c?style=for-the-badge)

</div>

---

## Por que usar este agente

- **Consistencia que escala.** Simbolos de design unicos para aplicacao, painel e site — uma mudanca de marca e uma mudanca de arquivo.
- **Acessivel desde o primeiro commit.** Contraste, foco, nome acessivel e navegacao por teclado conferidos na entrega.
- **Responsivo verificado.** Varredura automatizada em tres larguras pega estouro horizontal e botao deformado antes do usuario.
- **Cinco estados por tela.** Nada de tela branca, carregamento sem aviso ou erro mudo.
- **Reaproveita em vez de reinventar.** Menos codigo de estilo, menos regressao visual.

---

## Skills

| Skill | Titulo | O que resolve |
|---|---|---|
| [`sistema-de-design`](skills/sistema-de-design/SKILL.md) | Sistema de design e simbolos | Definir e aplicar simbolos de cor, espaco, tipografia e elevacao, com tema claro e escuro consistentes. |
| [`componentes-e-estados`](skills/componentes-e-estados/SKILL.md) | Componentes e estados | Construir biblioteca de componentes com variantes, todos os estados de interacao e estados de tela desenhados. |
| [`layout-responsivo`](skills/layout-responsivo/SKILL.md) | Layout responsivo | Construir layout que funciona de 320 px a telas largas, sem estouro horizontal, com verificacao automatizada. |
| [`acessibilidade`](skills/acessibilidade/SKILL.md) | Acessibilidade | Garantir conformidade pratica com as diretrizes de acessibilidade: contraste, semantica, teclado, leitor de tela e formulario. |
| [`revisao-de-interface`](skills/revisao-de-interface/SKILL.md) | Revisao de interface | Roteiro de revisao visual e de experiencia antes de aprovar uma tela, incluindo propagacao da correcao para telas irmas. |

Cada skill e um arquivo markdown autocontido (`skills/<slug>/SKILL.md`): pode ser instalada
isolada, sem o resto do repositorio.

---

## Instalacao rapida

```bash
git clone https://github.com/WallysonDuarte/agente-pixel.git
cd agente-pixel

# Claude Code — skills nativas
cp -r skills/* ~/.claude/skills/

# Qualquer outra CLI — arquivo unico de instrucao
cat AGENT.md skills/*/SKILL.md > AGENTS.md
```

| CLI | Instalacao (Windows / PowerShell) | Onde colocar as skills | Rodar |
|---|---|---|---|
| **Claude Code** | `irm https://claude.ai/install.ps1 \| iex` | `~/.claude/skills/` | `claude -p "<pedido>"` |
| **Codex** | `irm https://chatgpt.com/codex/install.ps1 \| iex` | `AGENTS.md na raiz do projeto` | `codex exec --skip-git-repo-check "<pedido>"` |
| **Grok** | `irm https://x.ai/cli/install.ps1 \| iex` | `passado no prompt` | `grok -p "<pedido>"` |
| **Antigravity** | `irm https://antigravity.google/cli/install.ps1 \| iex` | `passado no prompt` | `agy -p "<pedido>"` |
| **Hermes** | `iex (irm https://hermes-agent.nousresearch.com/install.ps1)` | `passado no prompt` | `hermes` |
| **OpenClaw** | `& ([scriptblock]::Create((iwr -useb https://openclaw.ai/install.ps1))) -NoOnboard` | `~/.openclaw/skills/` | `openclaw agent --local -m "<pedido>"` |
| **OpenCode** | `irm https://opencode.ai/install \| iex` | `AGENTS.md na raiz do projeto` | `opencode` |
| **Kimi Code** | `irm https://code.kimi.com/kimi-code/install.ps1 \| iex` | `passado no prompt` | `kimi -p "<pedido>"` |

Passo a passo por CLI, incluindo macOS/Linux: **[install/README.md](install/README.md)**

---

## Estrutura

```
agente-pixel/
├── AGENT.md                 definicao canonica do agente
├── .agent/agent.json        metadados legiveis por maquina
├── skills/
│   ├── sistema-de-design/SKILL.md
│   ├── componentes-e-estados/SKILL.md
│   ├── layout-responsivo/SKILL.md
│   ├── acessibilidade/SKILL.md
│   └── revisao-de-interface/SKILL.md
├── install/README.md        instalacao nas 8 CLIs
└── assets/portrait.png
```

---

## Ecossistema

Este agente faz parte de um time de 9 agentes especializados:

[![Master](https://img.shields.io/badge/Master-00ff41?style=flat-square)](https://github.com/WallysonDuarte/agente-master) [![Nova](https://img.shields.io/badge/Nova-9b59b6?style=flat-square)](https://github.com/WallysonDuarte/agente-nova) [![Atlas](https://img.shields.io/badge/Atlas-1abc9c?style=flat-square)](https://github.com/WallysonDuarte/agente-atlas) [![Pixel](https://img.shields.io/badge/Pixel-e91e63?style=flat-square)](https://github.com/WallysonDuarte/agente-pixel) [![Forge](https://img.shields.io/badge/Forge-e67e22?style=flat-square)](https://github.com/WallysonDuarte/agente-forge) [![Cipher](https://img.shields.io/badge/Cipher-c0392b?style=flat-square)](https://github.com/WallysonDuarte/agente-cipher) [![Luna](https://img.shields.io/badge/Luna-f39c12?style=flat-square)](https://github.com/WallysonDuarte/agente-luna) [![Lira](https://img.shields.io/badge/Lira-f0932b?style=flat-square)](https://github.com/WallysonDuarte/agente-lira) [![Rank](https://img.shields.io/badge/Rank-2980b9?style=flat-square)](https://github.com/WallysonDuarte/agente-rank)

[![Hub](https://img.shields.io/badge/ver%20o%20time%20completo-e91e63?style=for-the-badge)](https://github.com/WallysonDuarte/softwarehub-agentes)

---

<div align="center">

## Apoie este trabalho

Os 9 agentes sao mantidos de forma independente e publicados abertamente.
Se este material te poupou tempo, voce pode retribuir com um cafe:

<a href="https://buy.stripe.com/bJefZi3wJ4JH18WeuEgA800">
<img src="https://img.shields.io/badge/Apoie--me-R$%2010-e91e63?style=for-the-badge&logo=stripe&logoColor=white" alt="Apoie-me com R$ 10" />
</a>

## Links

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/dududev/)
[![Do Zero ao Junior](https://img.shields.io/badge/Do%20Zero%20ao%20Junior-1abc9c?style=for-the-badge)](https://dozeroaojunior.com.br/)
[![Curitiba Software](https://img.shields.io/badge/Curitiba%20Software-2980b9?style=for-the-badge)](https://curitibasoftware.com.br/)
[![SoftwareHub](https://img.shields.io/badge/SoftwareHub-00ff41?style=for-the-badge)](https://softwarehub.com.br/)


</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=e91e63&height=100&section=footer" width="100%" />
