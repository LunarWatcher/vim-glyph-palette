# 🎨 glyph-palette

This is an AI slop-free fork of vim-glyph-palette. This fork is primarily intended for compatibility with [LunarWatcher/fern.vim](https://github.com/LunarWatcher/fern.vim?tab=readme-ov-file#plugins-and-compatibility) via [LunarWatcher/vim-fern-renderer-nerdfont](https://github.com/LunarWatcher/vim-fern-renderer-nerdfont).

As of 2026-03-08, this plugin is no longer maintained. Due to [AI slop in vim](https://hachyderm.io/@AndrewRadev/116175986749599825), I have moved to emacs with evil mode.

## Requirements

For the glyphs to render at all, you'll need a [Nerd Font](https://github.com/ryanoasis/nerd-fonts). Without it, the glyphs will not render.

## Usage

If you're using a plugin using this plugin, you do not need to read this section. If you're writing a plugin or want to use this plugin directly, keep reading.

Call `glyph_palette#apply()` function on a target buffer like:

```vim
augroup my-glyph-palette
  autocmd! *
  autocmd FileType fern call glyph_palette#apply()
  autocmd FileType fall-list call glyph_palette#apply()
  autocmd FileType nerdtree,startify call glyph_palette#apply()
augroup END
```

Then glyphs in `g:glyph_palette#palette` on the buffer will be highlighted by predefined highlight groups.

See `:help glyph-palette-usage` for more details
