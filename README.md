# @astrojs/react strips the component's own `<link>` tags from island HTML

1. `npm install`
2. `npm run build`
3. In `dist/index.html` the island is `<div id="widget">Widget</div>`, without the two `<link>` tags that `src/components/Widget.jsx` renders.
4. `npm run preview` and open the page: `#widget` is black until it hydrates, and hydration logs React errors #418 (twice) and #423.

With React 19 (`npm install react@19.3.1 react-dom@19.3.1`) the links are gone too, and hydration logs #418.
