# Hi-Flow

Live: https://hi-flow.hi-flow.workers.dev/

A never-ending generative music stream that drifts between house, techno, breakbeat and EDM, with gentle in-key controls, a step sequencer, a sequence bank and a rearrangeable module board.

Everything is in `public/index.html` (plain HTML, CSS and JavaScript, no build step). All sound is synthesized live with the Web Audio API.

## Deploying on Cloudflare Workers
`wrangler.jsonc` tells Cloudflare to serve the `public` folder as static files.

Workers Builds settings:
- Production branch: `main`
- Build command: (leave empty)
- Deploy command: `npx wrangler deploy`

Every push to `main` deploys automatically to the `hi-flow` Worker.

## Note
On claude.ai the Bank saves to your account. On any other host it keeps saves only until the page is closed.
