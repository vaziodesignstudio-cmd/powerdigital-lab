# Katapult branding

Brand source of truth and per-agent briefs, fed from the Katapult Brand Guidelines (v1.3, June 2022).

## Files

- `brand-guidelines.md` — master digest of the full guidelines. The Brand Guardian owns it.
- `agents/` — one focused brief per operation agent, containing only the slice that agent needs.

## How the briefs map to the agents

| Agent (in `.claude/agents/`) | Brief |
| --- | --- |
| Brand Guardian | `agents/brand-guardian.md` |
| Studio Producer | `agents/studio-producer.md` |
| Content Creator | `agents/content-creator.md` |
| Instagram Curator | `agents/instagram-curator.md` |
| Ad Creative Strategist | `agents/ad-creative-strategist.md` |
| Image Prompt Engineer | `agents/image-prompt-engineer.md` |
| Programmatic & Display Buyer | `agents/programmatic-display-buyer.md` |
| Tracking & Measurement Specialist | `agents/tracking-measurement-specialist.md` |

The agent definitions in `.claude/agents/` stay brand-agnostic so they can be reused for future brands. Brand knowledge lives here, under the brand folder. When the Studio Producer opens a brief, it hands each agent its matching file; the Brand Guardian checks returned work against the master.

## What each agent was fed

- Brand Guardian: everything (the master is its reference).
- Studio Producer: brand essentials, audience framing, routing rules.
- Content Creator: voice modes, writing style, message and proof points, audiences.
- Instagram Curator: palette, typography, photography style, the Bounce, logo-on-grid rules.
- Ad Creative Strategist: voice, approved ad references, CTA, angles, testing notes.
- Image Prompt Engineer: palette hex, photography style with negative prompts, the Bounce, typography spirit.
- Programmatic & Display Buyer: audience, positioning, brand-safety posture.
- Tracking & Measurement Specialist: business model, conversion actions, audiences.

The `brand-guidelines.md` digest is the operation's working source. To keep the original on hand, drop the source PDF (Katapult Brand Guidelines v1.3, June 2022) into a `source/` folder here when available.
