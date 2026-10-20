# My AI stack

Building a list of my favorite skills I have found or written myself, AI automations, AI tools & how I use them.

I use AI for coding, design, making content, and things like researching events or sending outreach emails. I've also set up automations for the repetitive stuff, like sending people project links from my Instagram reels.

The tools I use are below, along with the skills and repos I've been collecting. Steal them for yourself.

## Frontend & design

A lot of the skills I've collected are for frontend work. Getting an agent to build something that works is one thing, getting the design and interactions right takes more direction.

[awesome-design-md](https://github.com/VoltAgent/awesome-design-md) is a collection of DESIGN.md files based on popular brands' design systems. Copy one into your project root and ask your agent to read it before building. It gives it specific typography, spacing, colors and component rules to follow. You can keep the structure of a reference and change the palette and type.

These are my favorite skills from others:

- [Impeccable](https://github.com/pbakaus/impeccable): frontend design and UI review. Useful for asking what needs changing in the typography, spacing and hierarchy of a page.
- [Emil Kowalski's skills](https://github.com/emilkowalski/skill): UI polish and animation taste, especially when the interface works but the interactions feel off.
- [Frontend Design by Anthropic](https://github.com/anthropics/skills/tree/main/skills/frontend-design): avoids the generic AI look. Give it a reference and a clear direction before asking it to build.
- [Motion AI Kit](https://motion.dev/docs/ai-kit): the official skill and MCP for animations with the Motion library.
- [shadcn/ui](https://ui.shadcn.com/docs/skills): guidance for working with shadcn components, themes and registries.
- [React Best Practices by Vercel](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices): React and Next.js performance guidelines for reviewing rendering, data fetching and bundle size.
- [Supabase](https://github.com/supabase/agent-skills): Supabase and Postgres best practices for database work.

Skills are instructions your coding agent can load for a task. Here are the install commands; some install a collection, so check what the installer selects:

```bash
npx impeccable install
npx skills@latest add emilkowalski/skills
npx motion-ai
pnpm dlx skills add shadcn/ui
npx skills add vercel-labs/agent-skills
npx skills add supabase/agent-skills
```

Anthropic's skill uses the [Claude Code plugin setup](https://github.com/anthropics/skills). Once installed, ask your agent to use the relevant skill on the page or component you're working on.

### React composition

The React composition skill is based on Fernando Rojo’s [Composition Is All You Need](https://www.youtube.com/watch?v=4KvbVq3Eg5w) talk. It covers compound components over boolean props, JSX over config arrays, and lifting providers above the components that need their state.

You can find it in the [skills folder](skills/react-composition.md). Have your agent read it before writing or reviewing React components.

## Tools I use

**[Aside](https://aside.com)** is an AI browser. I can't say enough good things about this tool. Feels like the missing step to what AI is capable of doing for you. I use it for research, outreach emails, event RSVPs and job applications. Give it the task, your constraints and the sites to use. It works in your logged-in accounts, so you can ask it to fill a form and stop before submitting, or research something and bring back the links.

**[Gamma](https://gamma.app)** is an AI presentation builder, my last semester of university depended on this tool. Give it your notes or an outline and tell it who the presentation is for. Edit the slides it generates, then share the deck or export it to PowerPoint or PDF.

**[Reve](https://app.reve.com)** is for images & graphics that don't look like AI slop. As an artist, I usually think these are slop, but the output of this one is great. Describe the image, layout and any text you need, then edit the parts you want changed.

**[Google AI Studio](https://aistudio.google.com)** is a bit janky sometimes, but being able to have so much control over the specs for image and video generation is great. Choose a generation model, add your prompt and references, then set the options it supports, like aspect ratio and resolution.

**[Motion.so](https://motion.so)** is for motion graphics. Tried this on launch, initially thought it was a scam, but now it's better than Hyperframes or Remotion (a bit pricey tho). Give it an idea, footage or a reference and ask for edits in chat. This is a different product from the Motion animation library above.

**[Remotion](https://www.remotion.dev/docs/ai/skills)** lets you make videos in React. Use this if you want to work on the video in code, preview the composition and render it. Install its skills with `npx skills add remotion-dev/skills`, then give your agent the script, assets and timing.

**[Monid](https://monid.ai)**: one API key for literally everything you could want an agent to do. Connect it to your agent to discover and call tools for search, scraping, media generation and more. Usage comes out of one balance instead of setting up each provider separately. You still pay for the calls.

**[OpenRouter](https://openrouter.ai)** gives you access to models from different providers through one API. Useful for trying different models for coding or connecting them to your own apps without setting up each provider separately. You can use it through [Cline](https://docs.cline.bot/provider-config/openrouter): choose OpenRouter as your provider, paste in your API key and pick a model.

## An automation I've set up

If you've seen my "comment project and I'll send you the links" reels, this is how I set up the DMs.

An Aside routine checks the comments every 20 minutes, finds people who commented the keyword and sends them the links. It tracks who has already received a message so it doesn't send duplicates on the next check.

To set up your own, give Aside the reel URLs, keyword, exact message and check interval. Tell it to skip anyone already messaged, and specify whether you want to approve sends. You need to give it those rules as well as the message.

## Other cool repos

[REA](https://github.com/morluto/rea) helps you figure out how an app's features work and rebuild them. Run `npx rea-agents setup`, then ask your agent to investigate a specific feature in an app you're authorized to analyze.

[Caveman](https://github.com/JuliusBrussee/caveman) makes your coding agent talk like a caveman to save tokens. Install just the skill with `npx skills add JuliusBrussee/caveman -g`, then use `/caveman` in a supported agent.

[AI Job Search](https://github.com/MadsLorentzen/ai-job-search) is a Claude Code workflow for evaluating jobs, tailoring your CV and preparing for interviews. Fork it, follow the setup and fill in your profile before giving it a job posting.

For video automation, there's [MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo), [OpenMontage](https://github.com/calesthio/OpenMontage) and [YouTube Automation Agent](https://github.com/darkzOGx/youtube-automation-agent). Each has its own setup and API requirements, so check the running costs before starting a pipeline.

### Free open-source alternatives

[Mann Bellani](https://github.com/Blueturboguy07) clones paid apps and open-sources them for free. Some of his:

- [cue](https://github.com/Blueturboguy07/cue): free Cluely, an AI meeting copilot.
- [WhimprFlow](https://github.com/Blueturboguy07/WhimprFlow): free Wispr Flow, local voice dictation.
- [publikclip](https://github.com/Blueturboguy07/publikclip): free OpusClip, turns long videos into short clips.
- [NitroAI](https://github.com/Blueturboguy07/NitroAI): turns lectures, PDFs and videos into notes, flashcards and quizzes.
- [lunara](https://github.com/Blueturboguy07/lunara): free Flo, a private cycle and fertility tracker.

His startup [Publik](https://publikhq.com) puts these alternatives in one place. Follow each app's install instructions and check whether it needs paid APIs or hosting.
