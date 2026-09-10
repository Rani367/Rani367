<p align="center">
  <strong>Rust, Next.js, and TypeScript developer</strong>
</p>

<p align="center">
  <a href="https://rani.is-a.dev">Portfolio</a> ·
  <a href="mailto:rani2011367@gmail.com">Email</a>
</p>

---

### Open Source Contributions

Mostly editor and compiler internals, with a focus on performance and correctness.

#### [Zed](https://github.com/zed-industries/zed)

* [**Skip multi-cursor selection broadcast when unshared**](https://github.com/zed-industries/zed/pull/60605): removed an O(selections) per-keystroke remap that ran with zero collaborators.
* [**Speed up multi-cursor editing**](https://github.com/zed-industries/zed/pull/58510): fast paths in the display map and selection resolution, ~2x faster typing, 700+ lines.
* [**Add upsell banners for integrated extensions**](https://github.com/zed-industries/zed/pull/43872): tells users searching for Basedpyright, Ruff, or Ty that they're now built in.

#### [Rust](https://github.com/rust-lang/rust)

* [**Fix escaping bound regions in nested `for<...>` binders of E0308 notes**](https://github.com/rust-lang/rust/pull/159232): rustc printed invalid types like `for<'a> fn(for<'a> fn(&'a ()))` in type mismatch errors.

#### [Next.js](https://github.com/vercel/next.js)

* [**Support TypeScript `noUncheckedSideEffectImports` for CSS imports**](https://github.com/vercel/next.js/pull/88199): missing module declarations for `.css`, `.sass`, and `.scss`.

#### Other

* [**magic-portfolio**](https://github.com/once-ui-system/magic-portfolio/pull/146): upgraded to Next.js 16 and React 19.2.

### Projects

* [**Hativon**](https://hativon.vercel.app): my school's newspaper website. `Next.js`
* [**Skarn**](https://github.com/Rani367/Skarn): OS-sandboxed MCP gateway in one binary. `Rust`
* [**affected**](https://github.com/Rani367/affected): finds which monorepo packages a Git change affects. `Rust`
* [**ferro**](https://github.com/Rani367/ferro): hobby AArch64 OS with a desktop, browser engine, and DOOM. `Rust`
* [**lo-agent**](https://github.com/Rani367/lo-agent): offline coding agent for Apple Silicon. `Rust`
* [**Armadillo**](https://github.com/Rani367/Armadillo): macOS antivirus with zero system dependencies. `Rust`
* [**singularity**](https://github.com/Rani367/singularity): gravitational-lensing black-hole game for the Playdate. `C`
