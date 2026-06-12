# PowerDigital Lab

A lean agent operation for producing Meta creatives and programmatic ad banners, one brand at a time.

The first brand is **Katapult**, used as the pilot for the operation. Once the model is proven, the same structure is replicated for other brands, each in its own folder under `brands/`.

## Pilot scope

- **Meta creatives** (Instagram / Facebook)
- **Google Ads programmatic** banners (Display / DV360)

## How the operation works

Work enters through a front that receives the demand and the brand, then distributes briefs to the execution agents.

```
Demand + Branding
        │
        ▼
  Brand Guardian  ──holds the brand, enforces consistency──┐
        │                                                   │
        ▼                                                   │
  Studio Producer ──translates the demand into briefs───────┤
        │                                                   │
        ├──► Content Creator ───────► Meta creatives (copy)  │
        ├──► Instagram Curator ─────► Meta creatives (visual)│
        ├──► Ad Creative Strategist ► banners (copy)         │ brand
        ├──► Image Prompt Engineer ─► banners (visual)       │ consistency
        ├──► Programmatic Buyer ────► GDN delivery           │
        └──► Tracking Specialist ───► measurement            │
                                                             │
        all consume the brand defined by ◄───────────────────┘
```

## Operation agents

In [.claude/agents/](.claude/agents/).

### Front
- **Brand Guardian** (`design-brand-guardian.md`): brand custody. Receives the branding elements and enforces consistency across everything produced.
- **Studio Producer** (`project-management-studio-producer.md`): receives the demand and distributes briefs to the execution agents.

### Meta creatives
- **Content Creator** (`marketing-content-creator.md`): copy and editorial calendar.
- **Instagram Curator** (`marketing-instagram-curator.md`): aesthetic, grid, and formats.

### Banners (Google Ads programmatic)
- **Ad Creative Strategist** (`paid-media-creative-strategist.md`): creative copy and variations, testing.
- **Image Prompt Engineer** (`design-image-prompt-engineer.md`): banner visuals via AI.
- **Programmatic & Display Buyer** (`paid-media-programmatic-buyer.md`): delivery on Google Display Network / DV360.
- **Tracking & Measurement Specialist** (`paid-media-tracking-specialist.md`): conversion tracking.

## Per-brand structure

```
brands/
  katapult/
    branding/    brand elements (identity, voice, palette, guidelines)
    briefings/   demands translated by the Studio Producer
    outputs/
      social/    Meta creatives produced
      banners/   banner creatives produced
```

## Next step

Populate `brands/katapult/branding/` with Katapult's brand elements. From there the Brand Guardian becomes the source of consistency and the Studio Producer starts opening briefs.
