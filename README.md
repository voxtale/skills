# VoxTale skills

Skills for creating and refining YouTube titles and thumbnails through the [VoxTale MCP server](https://voxtale.so/docs/mcp).

## Create YouTube thumbnails

The [thumbnail skill](skills/create-youtube-thumbnails/SKILL.md) guides this flow:

1. Ask for the full video transcript, or as much detail about the video as possible. Reuse material the creator already supplied or saved in VoxTale.
2. Ask whether to use a particular face photo: upload a new one, choose one stored in VoxTale, or continue without a face photo.
3. Generate rendered thumbnails by default, using **Balanced** (`style: clean`). Style-reference thumbnails and other generation settings are optional.
4. Follow the same run to completion, then show its titles, hooks, angles and thumbnails. Edit or restore a chosen option when requested.

An explicit request for text-only concepts uses concept mode instead. Both full and concept runs use the connected account's generation allowance. Project lookups and status checks do not start new runs.

## Use

Install the `skills/create-youtube-thumbnails` folder in a host that supports `SKILL.md` skills and remote MCP. The skill declares its dependency in `agents/openai.yaml`:

- Server: `https://mcp.voxtale.so/mcp`
- Transport: Streamable HTTP
- Sign-in: VoxTale OAuth

Connect your VoxTale account through the host's normal OAuth flow. Do not put passwords, API keys or tokens in the skill or this repository. Image uploads need a host that can send HTTP PUT requests; otherwise upload through VoxTale first.

VoxTale does not publish to YouTube or change billing. Generated options are a test set, not a promise of views or click-through rate.
