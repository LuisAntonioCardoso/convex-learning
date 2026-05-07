This is a Portfolio/Dairy of my journey learning convex

It consist of a Astro app with Svelte islands as a documentation page.

The backend is a convex instance where I do all the implementation, exploration and learning.

-- Diary tracking --

- in the root folder, initd bun
- cleared the unnecessary files (in this case just the index.ts that is pointed in the package.json as the 'entry point' of the app with 'module:"index.ts"')
- created to folder for the backend to init convex project
- update package.json (clean up default stuff and add workspace definitions)
- init bun inside backend folder, add convex and init convex
- clean up package.json and default folders
- not adding convex-helpers to create shareable/exportable API folder, because its a team of 1, but do it if extra decoupling is needed/wanted (likely needed when deploying, not sure though)
- 'bun create astro' a new astro project, docs style
- add scripts to run the convex and astro servers (with bunx --bun to use the bun runtime)
- defined the scripts locally to each project, and then I have script with the same name at the root directory with the --workspaces flag to run the scripts in parallel in all workspaces. current scripts:
	- "dev": run dev
	- "clean": clear cache
	- "nuke": clear node modules
	- "typecheck": run typecheck
	- other project specific ones in the respective package.json
- astro repo is using starlight for the doc style site and started with the starlight template
- Convex - Astro integration:
	- created convex.ts file that imports api based on the current env and exports it 
	- tsconfigs defines @convex as path to convex.ts, frontend files 'import {api} form "@convex"
	- convex.ts has logic to choose where the import comes from (diff dev from prod)
- CI/deployment
	- defined a 'build' command in the frontend that goes to the backend, deploys, uses convex-helper ts-api-spec to gen the frontend API directly to <UI>/src/lib/convexApi.ts and finish with astro build
	- this build command should only run in the host (vercel)
	- Convex dash > settings > general > deploy keys > create (gen prod/preview API key) that needs to be passed to the host (needed because of convex deploy)
- added .env for local, prod.local, and .env.example
- I will add the DX of preview deployments later