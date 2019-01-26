# VS Code - Trello Viewer
<a href="https://marketplace.visualstudio.com/items?itemName=Ho-Wan.vscode-trello-viewer" style="text-decoration : none" title="Go to VS marketplace">
  <img src="https://vsmarketplacebadge.apphb.com/version-short/ho-wan.vscode-trello-viewer.svg">
  <img src="https://vsmarketplacebadge.apphb.com/installs/ho-wan.vscode-trello-viewer.svg">
</a>
<a href="https://dev.azure.com/hw-vscode/vscode-trello-viewer/_build/latest?definitionId=3?branchName=master">
  <img src="https://dev.azure.com/hw-vscode/vscode-trello-viewer/_apis/build/status/Ho-Wan.vscode-trello-viewer?branchName=master">
</a>

Welcome to Trello Viewer for VS Code! This extension provides the following features:

- Browse Trello boards, lists and cards.
- View selected card using the markdown previewer and open to the side.
- See formatted checklists and cover image for the card.
- Assign a favourite list to easily access cards.
- Saves credentials to use between sessions.
- Shows only starred boards as default.

## Authenication

- Activate extension by clicking on the icon in the left Activity Bar.
- Login to trello at https://trello.com/login
- Get API key at https://trello.com/app-key
- Set credentials by clicking the key icon in the left Side Bar or running command "Trello Viewer: Authenticate".
- After entering API key, a new page should open in browser to get a readonly API token.
- Alternatively, use the command "Trello Viewer: Set Credentials" and follow instructions from Trello to manually generate a token.

## Tree View

<img src="https://raw.githubusercontent.com/Ho-Wan/vscode-trello-viewer/master/images/readme/main-tree-view-markup.png" alt="Trello Viewer tree view markup">

## Usage

- Trello boards, lists, and cards appears in left Side Bar.
- Clicking a board or list expands or collapses object.
- Clicking a card opens the markdown file as well as the previewer, opening this to the right side (editor column 2 by default).
- Clicking on the star to the right of a list assigns this as your "favourite list", shown in the lower part of the side bar.
- Clicking on the icons in the side bar runs various commands, such as setting credentials, removing credentials, showing saved info, and refreshing views.

## Trello Card Markdown Preview

<img src="https://raw.githubusercontent.com/Ho-Wan/vscode-trello-viewer/master/images/readme/screenshot2-markdown-preview.png" alt="Trello Viewer markdown preview">

## Useful Commands

Main functionality is provided using the VS code interface in the left Side Bar. Running commands to use this extension is optional.

Command | Description
--- | ---
```Trello Viewer: Authenticate``` | Set user Trello API key and token.
```Trello Viewer: Refresh``` | Refresh the main Trello tree view.
```Trello Viewer: Reset Credentials``` | Removes saved credentials.

## Extension Settings

Name of Setting | Default | Description
--- | --- | ---
```trelloViewer.starredBoardsOnly``` | ```true``` | Controls whether to display starred boards only or all boards.
```trelloViewer.viewColumn``` | ```2``` | Specifies which editor column markdown previewer opens at.

## Advanced

- This extension creates a temporary file named `~vscodeTrello.md` in the user's [VS Code Settings folder](https://code.visualstudio.com/docs/getstarted/settings#_settings-file-locations).
- The markdown file contains parsed content of the Trello card and can be saved locally.
- Hover over any board, list or card to see the Trello ID.
- The API token is stored using AES 256 encryption with IV.
- The setting "markdown.preview.breaks" is automatically set to true in only to see new lines correctly formatted.

## Unsupported Features

- Adding or editing Trello items.

If you wish to see additional functionality such as being able to create cards or add comments, leave a feature request in the repository!
