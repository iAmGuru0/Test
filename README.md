# THE CINEMATIC DIMENSION

A cinematic, single-page portfolio concept for an independent video editor / filmmaker. Built with React, TypeScript, Vite, React Three Fiber, Three.js, Drei and Lenis.

## Run locally

```bash
npm install
npm run dev
```

Build for production:

```bash
npm run build
npm run preview
```

## First customisations

1. Open `src/data/projects.ts` and replace the six sample project records. Each record supports title, category, client, year, description, editing approach, credits, thumbnail, video URL, tools and accent colour.
2. Replace `hello@yourname.com`, `YOUR NAME`, social links and location in `src/App.tsx`.
3. Replace the portrait placeholder in the About chapter with your own portrait.
4. Replace sample video URLs with your own MP4 or approved video embed URLs. The player uses `preload="none"` and only loads when a project is opened.

## Experience architecture

- `src/scene/World.tsx` — persistent WebGL environment, camera interpolation, sculpture, project monoliths, process objects, lighting and reflective floor.
- `src/hooks/useExperience.ts` — Lenis scroll smoothing and normalized scroll progress.
- `src/components/ProjectExperience.tsx` — editable project gallery, accessible project modal, HTML5 video controls and previous / next navigation.
- `src/components/Navigation.tsx` — minimal desktop and mobile navigation.
- `src/data/projects.ts` — all editable portfolio project data.
- `src/styles/global.css` — responsive visual system and reduced-motion styles.

## Notes

- The six scene camera waypoints are interpolated from normalized page scroll. Adjust the `points` array in `CameraRig` to retime or reshape the journey.
- The current sample media are replaceable demo assets, not the portfolio owner's real work.
- The environment uses procedural Three.js geometry; it does not rely on a static background image.
- The experience degrades gracefully when reduced motion is preferred, but the app still requires WebGL for its full 3D environment.
- For production, self-host and compress project media, add a poster/thumbnail for every video, verify rights to all media, and run `npm run build` on the deployment environment.
