# PowerDigital Lab

Operação enxuta de agents para executar conteúdo de redes sociais e banners de ad programmatic, marca a marca.

A primeira marca é a **Katapult**, usada como piloto para validar a operação com os líderes. Se funcionar, a mesma estrutura é replicada para outras marcas, cada uma na sua pasta dentro de `brands/`.

## Escopo do piloto

- Posts orgânicos de **Instagram**
- Banners de **Google Ads programmatic** (Display / DV360)

## Como a operação funciona

O fluxo entra por um front que recebe a demanda e a marca, e distribui briefs para os agents de execução.

```
Demanda + Branding
        │
        ▼
  Brand Guardian  ──guarda a marca, impõe consistência──┐
        │                                                │
        ▼                                                │
  Studio Producer ──traduz a demanda em briefs──────────┤
        │                                                │
        ├──► Content Creator ───────► posts (copy)       │
        ├──► Instagram Curator ─────► posts (estética)   │
        ├──► Ad Creative Strategist ► banners (copy)     │ consistência
        ├──► Image Prompt Engineer ─► banners (visual)   │ de marca
        ├──► Programmatic Buyer ────► veiculação GDN     │
        └──► Tracking Specialist ───► medição            │
                                                         │
        todos consomem a marca definida pelo ◄───────────┘
```

## Agents da operação

Em [.claude/agents/](.claude/agents/). Seleção feita a partir de [agency-agents](https://github.com/msitarzewski/agency-agents).

### Front
- **Brand Guardian** (`design-brand-guardian.md`): custódia da marca. Recebe os branding elements e garante consistência em tudo que é produzido.
- **Studio Producer** (`project-management-studio-producer.md`): recebe a demanda e distribui briefs para os agents de execução.

### Posts (Instagram)
- **Content Creator** (`marketing-content-creator.md`): copy e calendário editorial.
- **Instagram Curator** (`marketing-instagram-curator.md`): estética, grid e formatos.

### Banners (Google Ads programmatic)
- **Ad Creative Strategist** (`paid-media-creative-strategist.md`): copy e variações de criativo, testes.
- **Image Prompt Engineer** (`design-image-prompt-engineer.md`): visuais dos banners via IA.
- **Programmatic & Display Buyer** (`paid-media-programmatic-buyer.md`): veiculação no Google Display Network / DV360.
- **Tracking & Measurement Specialist** (`paid-media-tracking-specialist.md`): rastreamento de conversão.

## Estrutura por marca

```
brands/
  katapult/
    branding/    elementos de marca (identidade, voz, paleta, guidelines)
    briefings/   demandas traduzidas pelo Studio Producer
    outputs/
      social/    posts produzidos
      banners/   criativos de banner produzidos
```

## Próximo passo

Alimentar `brands/katapult/branding/` com os elementos de marca da Katapult. A partir daí o Brand Guardian passa a ser a fonte de consistência e o Studio Producer começa a abrir briefs.
