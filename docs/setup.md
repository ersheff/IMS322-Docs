# Setup

The sections on this page will lead you through the process of setting up the applications and accounts needed to complete IMS322 coursework. It is recommended that you follow the steps below in the order listed.

1. Install [Git](#git).
2. Create a [GitHub](#github) account (if neeeded).
3. Login to [CodePen](#codepen).
4. Install additional [browsers](#browsers) (if needed).
5. Install [VS Code](#vs-code) and configure with extensions and settings.
6. Review assignment [procedures](#procedures).

---

## Git

[Git](https://git-scm.com) is a "version control system" that helps track and manage changes in files. While Git itself is very powerful, we will primarily be using it through the Source Control panel in VS Code.

### Mac

Mac users should follow the [Homebrew installation option](https://git-scm.com/download/mac):

1. Install [Homebrew](https://brew.sh/).
2. Run the `brew install git` in Terminal. If prompted, install the "command line developer tools." This will likely take a while...

### Windows

Windows users should use the 64-bit Git for Windows Setup under [Standalone Installer](https://git-scm.com/download/win).

### Linux

If you're using Linux, you probably don't need help installing Git! Follow the instructions [here](https://git-scm.com/download/linux).

---

## GitHub

[GitHub](https://github.com) is a platform for creating, storing, and managing code. It relies on Git to commit and sync changes between files stored locally on your computer (the ones that you'll be editing in VS Code) and online repositories. In this class, we will be using GitHub to manage all major assignments.

1. Create a [GitHub](https://github.com) account.
2. Register for GitHub [Student Benefits](https://github.com/education/students) (this will give you access to the GitHub Copilot AI assistant).

---

## CodePen - XXX

[CodePen](https://codepen.io/) is a popular online code editor focused on creating and sharing snippets of HTML, CSS, and JavaScript

Pros
Can login with GitHub account
Can embed
No setup

Limitations
No free file hosting
Clutters up the inspector
No fullscreen preview
No HTML head

Sign-in to CodePen using your GitHub account.

---

## Browsers - XXX

Although there are many different modern web browsers, there are essentially only 3 different [browser engines](https://en.wikipedia.org/wiki/Browser_engine) that currently run them all. A browser engine is essentially the software component "under the hood" of the application that handles document layout, rendering, and security.

- **WebKit** is maintained by Apple and used for the desktop and mobile versions of [Safari](https://www.apple.com/safari/).
- **Blink** is maintained by Google and powers all Chromium-based browsers, which includes [Google Chrome](https://www.google.com/chrome/), [Microsoft Edge](https://www.microsoft.com/en-us/edge), [Brave](https://brave.com/), [Opera GX](https://www.opera.com/gx), and others.
- **Gecko** is maintained by Mozilla and used for [Firefox](https://www.mozilla.org/en-US/firefox/).

---

## VS Code - XXX

[Visual Studio Code](https://code.visualstudio.com) (aka VS Code) is the code editor that we will be using for all major assignments in this class. After installing the VS Code application, follow the instructions below to configure the necessary extensions and settings.

### Extensions

We will be using a small collection of VS Code extensions to assist with formatting and development. Search for the following extensions in the Extensions panel to install:

- GitHub Copilot and Copilot Chat (AI code assistant, requires GitHub Student Benefits)
- JS-Beautify for VS Code (for HTML formatting)
- Prettier (for CSS and JavaScript formatting)
- Live Server (for easy browser preview)
- Live Share (for collaborative coding)

### Git and GitHub

1. Click the Accounts icon in the lower-left corner and sign-in using your GitHub account.
2. Click on the Terminal menu and choose "New Terminal."
3. In the Terminal panel, run the following 2 commands, inserting your own username and email where indicated (you will not see a confirmation message):  
   `git config --global user.name "your username"`  
   `git config --global user.email your@email.com`

### Editor Settings

The following VS Code editor settings are primarily

#### Copy-Paste Configuration

Alternatively, you can copy-paste settings in the settings.json file:

1. Go to the View menu and choose Command Palette...
2. Use the search field to find and run the "Preferences: Open User Settings (JSON)" command.
3. Copy-paste the text below into the open settings.json file.
4. Save and close the file.

_You will still need to manually hide Run and Debug in the Activity Bar and choose your Live Server Custom Browser in the Settings GUI._

```json
{
  "editor.minimap.enabled": false,
  "breadcrumbs.enabled": false,
  "editor.tabSize": 2,
  "editor.formatOnSave": true,
  "prettier.trailingComma": "none",
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[html]": {
    "editor.defaultFormatter": "vsce-toolroom.vscode-beautify"
  },
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}
```

#### Manual Configuration

In the left Activity Bar:

1. Right-click the Activity Bar.
2. Uncheck Run and Debug.
3. Ensure that Explorer, Search, Source Control, Extensions, Chat, and Accounts are all checked.

From the View menu:

1. Under Appearance, uncheck Minimap.
2. Under Apperance, uncheck Toggle Breadcrumbs.

In Settings:

1. Set Editor: Tab Size to 2.
2. Enable Format on Save.
3. Set Prettier: Trailing Comma to None.
4. Choose a Custom Browser for Live Server.

To choose JS-Beautify as the default HTML formatter:

1. Open any HTML file.
2. Right-click within the file and choose Format Document With...
3. You will be offered a dropdown menu - choose Configure Default Formatter...
4. Select JS-Beautify for VS Code.

To select Prettier as the default CSS and JavaScript formatter:

1. Open any CSS file.
2. Right-click within the file and choose Format Document With...
3. You will be offered a dropdown menu - choose Configure Default Formatter...
4. Select Prettier.
5. Repeat the previous steps within an open JavaScript file.

---

## Procedures - XXX

### Accepting Assignments

Click the link in the corresponding Canvas Assignment. This will prompt you to accept the assignment on GitHub Classroom.

The first time you accept a GitHub Classroom assignment, you will be asked to link your GitHub account to your name.

After a few moments, GitHub Classroom will report that you are ready to go and provide a url to a new fork of the repository.

To find this repository in the future, it should be visible in Top Repositories when you first land on the GitHub site. You can also find it by visiting the IMS322-Sheffield-F24 organization

Make sure that you are working with the repository called "assignment-username" as you will also see the original "Assignment" repository that was used as the starting template.

Open VS Code and make sure that you do not have any folders open - go to the File menu and choose "Close Folder."
Open the Source Control panel and click the Clone Repository button. Copy-paste the url from your repository into the text field. You will be prompted for a location on your computer to save this folder.
To open this folder in the future, go to the File menu and choose "Open Folder…"

### Committing and Submitting Assignments

It is recommended that you Stage, Commit, and Sync often (steps 1 & 2 below) as that will essentially act as a backup for your files.

Make sure that your code is formatted using the built-in formatting tools

The IMS322 VS Code profile has "Format on Save" enabled by default, but you can also right-click in a file and choose "Format Document."

You should see a blue indicator on the Source Control icon. Open the Source Control panel and do the following:

Stage all changes by clicking the + next to Changes.
Enter a commit message and click the Commit button (use "finished" for your final commit).
The Commit button should change to a Sync Changes button. Click this to finish syncing the latest changes to your GitHub Repository.

Return to your assignment repository on GitHub.
Go to Settings and navigate to the Pages section.
Under Branch, choose "main" and click Save.
After a few moments, if you refresh this page, there should now be a URL near the top next to a Visit Site button. If you click this button, you should see your site open in a new window.

Copy the URL generated by GitHub Pages, paste it in the Website URL field of the corresponding Canvas Assignment, and click Submit Assignment.

### Accepting Assignments

Depending on the assignment instructions, do one of the following:

Create a new empty Pen by clicking on "Pen" in the left sidebar or choosing "New Pen" from the menu under your user icon, or...

Fork the example Pen (if provided) by clicking the Fork button in the lower-right corner of the editor window. You may need to click Edit on CodePen first if you are looking at an embedded example from the documentation.

Change the Pen name to the name provided in the Canvas assignment and click Save. If you need to find this Pen again later, it will be in Your Work.

### Submitting Assignments

Click the Save button in the upper-right corner of the CodePen window.
Click Share in the bottom-right corner and select Copy Link.
Paste the copied link in the Website URL field of the corresponding Canvas Assignment and click Submit Assignment.

Feedback
Feedback will be provided in comments on Canvas.
Occasionally, I may fork your Pen and share a link in the comments to an updated version with some revisions.
