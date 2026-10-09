# GVOID for Claude

Create images, video clips, cinematic voices, songs, sound effects and 3D models
in your [GVOID](https://gvoidstudio.com) account without leaving Claude. Ask in
plain words — "a 10-second shot of a fox running through snow at dawn", "a
voice line saying this with anger", "turn this image into a 3D model" — and
Claude picks the model, tells you the price in voids, generates it and hands you
the result. Everything you create is saved in your GVOID library, so you can
keep editing it on the web canvas.

## What you need

- A GVOID account: https://gvoidstudio.com
- An API key: GVOID → Profile → **API & MCP** → **New key** (starts with `gv_`).

## Install (Claude Code)

```
/plugin marketplace add x-jim/gvoid-claude-plugin
/plugin install gvoid@gvoid
```

Claude Code asks for your API key once and keeps it in your system's secure
store. Generations are charged in voids at catalogue price.

## What's inside

- **MCP server** `https://gvoidstudio.com/mcp` with the GVOID tools: balance,
  model catalogue with prices, image, video, voice, music, sound effects, 3D,
  character animation, run status, your assets and uploads.
- **Skill** `gvoid-studio`: how to choose a model, check the price first, follow
  a generation to the end and chain your own files as references.

## Privacy and terms

- Privacy: https://gvoidstudio.com/p/privacidad
- Terms: https://gvoidstudio.com/p/terminos

## License

MIT
