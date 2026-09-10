<p align="center">
  <strong>Rust, Next.js, and TypeScript developer</strong>
</p>

<p align="center">
  <a href="https://rani.is-a.dev">Portfolio</a> ·
  <a href="mailto:rani2011367@gmail.com">Email</a>
</p>

---

### Open Source Contributions

I contribute to the tools I use every day. Most of my work is in editor and compiler internals, with a focus on performance and correctness.

#### [Zed](https://github.com/zed-industries/zed)

* **[Skip multi-cursor selection broadcast when unshared](https://github.com/zed-industries/zed/pull/60605)** · Merged
  Profiling showed the per-keystroke selection broadcast doing an O(selections) anchor remap even with zero collaborators (0.9ms per call at 1k cursors, 8.4ms at 10k). Added `CollaborationHub::should_broadcast_selections`, gated the broadcast on it, and re-publish selections when a project becomes shared so peers joining later still see the host's cursor. `Rust`

* **[Speed up multi-cursor editing](https://github.com/zed-industries/zed/pull/58510)** · Merged
  Multi-cursor typing was O(N) per keystroke and effectively hung at high cursor counts. Profiled each phase of `handle_input`, then added fast paths in `InlayMap::sync` and `WrapMap::interpolate`, batched anchor-to-offset resolution to skip the per-selection display round-trip, and made render and autoscroll resolve only the selections they need. Roughly 2x faster typing across a 14-file, 700+ line change. `Rust`

* **[Add upsell banners for integrated extensions](https://github.com/zed-industries/zed/pull/43872)** · Merged
  Banners on the extensions page that tell users searching for Basedpyright, Ruff, or Ty that the functionality is now built into Zed. `Rust`

#### [Rust](https://github.com/rust-lang/rust)

* **[Don't list escaping bound regions in nested `for<...>` binders of E0308 notes](https://github.com/rust-lang/rust/pull/159232)** · Merged
  "One type is more general than the other" errors printed invalid types like `for<'a> fn(for<'a> fn(&'a ()))`. Traced it to `RegionFolder` folding regions bound by enclosing binders into the map that `cmp_fn_sig` uses to build its `for<...>` prefixes, and fixed the region collection so nested binders only list what they actually bind. `Rust` `rustc`

#### [Next.js](https://github.com/vercel/next.js)

* **[Support TypeScript `noUncheckedSideEffectImports` for CSS imports](https://github.com/vercel/next.js/pull/88199)** · Merged
  Plain `.css`, `.sass`, and `.scss` side-effect imports errored under TypeScript 5.6's `noUncheckedSideEffectImports`. Added the missing module declarations and extended the test suite to cover them. `TypeScript`

#### Other

* **[magic-portfolio](https://github.com/once-ui-system/magic-portfolio/pull/146)**: Upgraded the template to Next.js 16 and React 19.2. · Merged

### Projects

* **[Hativon](https://hativon.vercel.app)**: My school's newspaper website, used by students and staff. `Next.js` `TypeScript` `Postgres`
* **[Skarn](https://github.com/Rani367/Skarn)**: OS-sandboxed MCP gateway in a single Rust binary. `Rust`
* **[affected](https://github.com/Rani367/affected)**: Language-agnostic CLI that finds which monorepo packages a Git change affects. `Rust`
* **[ferro](https://github.com/Rani367/ferro)**: Hobby AArch64 OS with a graphical desktop, its own browser engine, and DOOM. `Rust`
* **[lo-agent](https://github.com/Rani367/lo-agent)**: Local-first, fully offline coding agent for Apple Silicon. `Rust`
* **[Armadillo](https://github.com/Rani367/Armadillo)**: macOS antivirus with five detection engines and zero system dependencies. `Rust`
* **[singularity](https://github.com/Rani367/singularity)**: Real-time gravitational-lensing black-hole game for the Playdate. `C`
