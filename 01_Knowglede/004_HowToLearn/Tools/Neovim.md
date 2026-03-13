Tags: #SecondBrain 
Status: #open, #unprocessed
Related: 

---
# Neovim



### NvChad
https://github.com/NvChad/NvChad
What is it?
- NvChad is a neovim config written in lua aiming to provide a base configuration with very beautiful UI and blazing fast startuptime (around 0.02 secs ~ 0.07 secs). We tweak UI plugins such as telescope, nvim-tree etc well to provide an aesthetic UI experience.
- NvChad is supposed to be used with its [starter config](https://github.com/nvchad/starter), so nvchad main repo (this repo) can be imported as a plugin via lazy's import feature and then you can easily use this repo's modules like autocmds etc.


### Example:
https://vineeth.io/posts/neovim-setup
[https://github.com/ThePrimeagen/init.lua](https://github.com/ThePrimeagen/init.lua)

[https://blog.nikfp.com/how-to-install-and-set-up-neovim-on-windows](https://blog.nikfp.com/how-to-install-and-set-up-neovim-on-windows)

### Package manager:
[https://github.com/LazyVim](https://github.com/LazyVim)

### Plugin:
[https://github.com/nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim) (Fuzzy file finder using ripgrep)
[https://github.com/folke/which-key.nvim](https://github.com/folke/which-key.nvim) (Shows keybindings)
[https://github.com/simrat39/symbols-outline.nvim](https://github.com/simrat39/symbols-outline.nvim) (Simple outline)
[https://github.com/RRethy/vim-illuminate](https://github.com/RRethy/vim-illuminate) (Highlight word under cursor)

### Init.lua help:
[https://github.com/nvim-lua/kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)
[The Only Video You Need to Get Started with Neovim](https://www.youtube.com/watch?v=m8C0Cq9Uv9o&list=PL-_3ytZuZ-Hgyacbgo0UcRsFodBmcN8u9&index=120)
![](https://www.youtube.com/watch?v=m8C0Cq9Uv9o&list=PL-_3ytZuZ-Hgyacbgo0UcRsFodBmcN8u9&index=121)

### Windows:
Tree sitter require "CC", "cc", "gcc", "clang", "cl", "zig"
Can be download [https://ziglang.org/learn/getting-started/](https://ziglang.org/learn/getting-started/) to use "zig" command.

Install command `:TSInstallSync cpp`


---
# References
Official website: https://neovim.io/
Wikipedia: https://github.com/neovim
Youtube: