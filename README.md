# Scaffolding `frontend` and `backend` monorepo in TypeScript

## Why?

### The history behind motivation

The term "vibe-coding" had never made any sense to me because I could not trust writing a prompt and letting code be written without (double) checking, essentially reviewing all the code generated in each step. 

Nevertheless, it seems this is the new reality: write prompts and let the AI code. Otherwise, people wouldn't be talking about multi-agents if it's hard for me to babysit one agent, how could I do it for multi-agents?

This is where my friend [fabricioviapiana](https://github.com/fabricioviapiana) introduces me to the "AI for Devs" course from [rodrigobranas](https://github.com/rodrigobranas). It was a hands-on course about creating good prompts and, beyond that, a workflow from Product Requirement Document (PRD) through the effective generation and execution of tasks. How to manage the context window that sometimes is compacted or even already too cluttered to perform nicely.

### Finally the curiosity as fuel to start

They started the course with a "base" monorepo with `frontend` and `backend`.

I wondered how they created this "base" and then I decided to follow the hand-crafted prompts taught in the course, which mix `tags` and `markdown`: one prompt to bootstrap the backend and another for the frontend.

## So was AI used to create the monorepo?

Yes, I started with the creation of the `backend` prompt and let the LLM generate the code. After each try I asked the LLM to fix the codebase due to something unexpected and also adjust the prompt to avoid the issue in the future.

When the result was satisfactory, i.e., the LLM could write the code as I expected, I created the `frontend` prompt based on the `backend` once it was sufficiently refined.

## Tech details

### Prompts

The initial prompts that I used to bootstrap the repo are under the [`./prompts`](./prompts/) folder.

### Only prompts at this moment?

Yes, I wanted to start this way, so I'll create `rules` and `skills` at another time, for instance, to build some functionality using this scaffolding monorepo as the base project.

The course introduced prompts, templates, and commands in Portuguese, although I'd prefer to have them in English. This is a good opportunity to review the main ideas and nuances, which I can apply in future projects.
