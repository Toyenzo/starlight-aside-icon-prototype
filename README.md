# Repro: Starlight asides accept `Object.prototype` names as custom icons

Uses `@astrojs/starlight@0.42.11` and `astro@7.4.11` (Node >= 22.23.4).

```sh
npm install
npm run build
grep -o 'starlight-aside__icon">[^<]*<' dist/index.html
```

**Actual:** `:::note{icon="constructor"}` and `:::tip{icon="toString"}` build without an error, and the asides' `<svg>` icons contain the text `function Object() { [native code] }` and `function toString() { [native code] }`.

**Expected:** like any other unknown icon name (for example `icon="not-an-icon"`), the build fails with "Invalid aside icon".
