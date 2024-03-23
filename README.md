# Git Remote Url:
This _very_ simple plugin simply contains function to fetch the remote url a git repository.

```lua
-- defined functions:
require('git-remote-url').git_url_to_clipboard(optional_branch, optional_path)
require('git-remote-url').get_git_remote_url(optional_branch, optional_path)
```

The function can optionally be given a different branch or path as an argument,
but it will default to the current branch and the current path of the current buffer.

If supplied a different path as argument, it will not include the line selection

There is a function that will return the link, but also one to directly add it to your `+` register!

## Installation
Lazy:
```lua
return {
  'JojoMakesGames/git-remote-url.nvim',
  config = function()
    vim.keymap.set('', '<leader>yg', function()
      require('git-remote-url').git_url_to_clipboard("main")
    end, { desc = 'Git Remote Url main branch' })
    vim.keymap.set('', '<leader>yG', function()
      require('git-remote-url').git_url_to_clipboard()
    end, { desc = 'Git Remote Url' })
  end
}
```

### Notes:
This is a very simple plugin that will be recieving updates to follow plugin standards, just wanted to see real quick how easy it was to create a plugin!
