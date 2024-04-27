React + Next
- React Server Components + Suspense Boundaries used for partial prerendering and streaming
  - Out of order streaming - components streamed parallely.
    - for sibling components
  - In order streaming - components streamed in sequence.
    - for nested components

- React api calls via `fetch` api are cached in memory so that it could be shared across components.
- Pages router
  - Data fetching - `getStaticProps` & `getServerSideProps`
  - `next/head` api for head element updates like metatags, links...
- App router
  - Data fetching - enhanced `fetch` api
  - new metadata api using metadata object / `generateMetadata` funtion for dynamic values

- Caching
  - local dev server and production build works differently for caching. With local server, data is always fetched/re-rendered.
  - static vs dynamic rendering, use `cookies(), headers(), noStore()` from `next/headers` to enforce dynamic rendering.
  - fetching, caching, revalidating, static-dynamic rendering, streaming, prerendering

CSS
- `clsx`, `cva (Class Variance Authority)` - to conditionally add classNames on React components.
