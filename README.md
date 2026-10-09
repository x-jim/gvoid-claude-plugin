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

## Install (Claude Code)

```
/plugin marketplace add x-jim/gvoid-claude-plugin
/plugin install gvoid@gvoid
```

The first time Claude uses GVOID it opens a GVOID page in your browser: sign in
and press **Allow**. In Claude Code you can also start it with `/mcp`. You can
disconnect it anytime in GVOID → Profile → **API & MCP**. Generations are paid with your voids and keep your plan perks, just like on the web.

## What's inside

- **MCP server** `https://www.gvoidstudio.com/mcp` with the GVOID tools: balance,
  model catalogue with prices, image, video, voice, music, sound effects, 3D,
  character animation, run status, your assets and uploads.
- **Skill** `gvoid-studio`: how to choose a model, check the price first, follow
  a generation to the end and chain your own files as references.

## Privacy and terms

- Privacy: https://gvoidstudio.com/p/privacidad
- Terms: https://gvoidstudio.com/p/terminos

## License

MIT
