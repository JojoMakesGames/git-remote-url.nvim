# Git Remote URL:
This simple plugin adds the user commands: CopyGithubLink and CopyGithubLinkWithBranchName to fetch the remote URL for main and your current branch respectively.

It also exposes 2 functions for use however you like.

```lua
-- defined functions:
require('git-remote-url').git_url_to_clipboard(optional_branch, optional_path, optional_line_start, optional_line_end)
require('git-remote-url').get_git_remote_url(optional_branch, optional_path, optional_line_start, optional_line_end)
```

The functions can optionally be given a different branch or path as an argument,
but it will default to the current branch and the current path of the current buffer.

If supplied a branch as argument, it will include the line selection only if it matches the current branch.

If given a path as argument, it will not include the line selection.

## Installation
Lazy:
```lua
return {
  'JojoMakesGames/git-remote-url.nvim',
  opts = {},
  keys = {
    {
      '<leader>yg', ':CopyGithubLink "main"<CR>'
      mode = '', desc = 'Git Remote Url main branch',
    },
    {
      '<leader>yG', ':CopyGithubLink<CR>'
      mode = '', desc = 'Git Remote Url',
    },
  },
}
```

### Notes:
This is a very simple plugin that will be receiving updates, just wanted to see real quick how easy it was to create a plugin!
