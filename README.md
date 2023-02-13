# emmet-language-server

Emmet Language Server, with support for CSS within `styled` (`.ts` files).

## Install

```
npm install -g emmet-language-server
```

## Configuration 

### Example Configuration

With [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig):

```lua
local capabilities = require 'cmp_nvim_lsp'.default_capabilities();

capabilities.textDocument.completion.completionItem.snippetSupport = true

require 'lspconfig'.emmet_ls.setup {
  cmd = { "emmet-language-server", "--stdio" },
  capabilities = capabilities,
  -- on_attach = on_attach,
  filetypes = {
    'html', 'typescript', 'typescriptreact', 'javascriptreact', 'css', 'sass', 
    'scss', 'less'
  },
}
```
