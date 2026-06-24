# 2. Set up your tools & Adobe account

This page gets your computer and your Adobe account ready. You only do this
once. Allow about 20–30 minutes the first time.

## What you need before you start

- **An Adobe ID** with access to an Adobe organization. This is the account you
  use to sign in to Fusion. If you can sign in to Fusion, you have this.
- **Developer access to App Builder.** Your organization administrator may need
  to grant you the **Developer** role and add you to a **Product Profile** that
  includes App Builder. If commands later fail with "you are not a developer" or
  you cannot see your organization, ask your Adobe org admin to add you.
- **A System Administrator** (possibly someone else on your team) for the final
  release step. Creating and deploying needs only the Developer role, but
  **submitting an extension for approval/publishing requires the System
  Administrator role**. See Adobe's
  [How to Get Access](https://developer.adobe.com/uix/docs/guides/get-access/).
- **A computer where you can install software** and run terminal commands
  (macOS, Windows, or Linux).

## Step 1 — Install Node.js

The Adobe tooling runs on **Node.js**. Install the **LTS** version (18 or 20).

1. Go to <https://nodejs.org> and download the **LTS** installer.
2. Run the installer and accept the defaults.
3. Confirm it worked by opening a terminal and running:

   ```sh
   node --version
   npm --version
   ```

   You should see version numbers (for example `v20.17.0` and `10.x`). If
   `node` is not found, close and reopen your terminal, or restart your
   computer.

> **Tip:** If you work with multiple Node versions, a version manager such as
> `nvm` is convenient, but it is optional. The Adobe CLI requires Node 18 or
> newer; very new, non-LTS versions can occasionally cause issues, so stick to
> LTS.

## Step 2 — Install the Adobe I/O CLI (`aio`)

`aio` is the command-line tool you use to create, build, and publish your
extension. Install it globally with npm:

```sh
npm install -g @adobe/aio-cli
```

Confirm it installed:

```sh
aio --version
```

You should see something like `@adobe/aio-cli/11.x.x`.

> If you see a permissions error on macOS/Linux, do **not** use `sudo`. Instead
> fix npm's global folder permissions, or use a Node version manager that
> installs into your home directory.

## Step 3 — Sign in to Adobe

Connect the CLI to your Adobe account:

```sh
aio login
```

This opens a browser window. Sign in with your Adobe ID and approve access. When
it succeeds you can close the browser tab and return to the terminal.

To sign out later (for example to switch accounts): `aio logout`.

## Step 4 — Understand the Developer Console (and let `aio` set it up for you)

The **Adobe Developer Console** (<https://developer.adobe.com/console>) is the
web dashboard where your project officially lives. You do not have to click
through it manually — the `aio` command can create everything for you in the
next page — but it helps to know the vocabulary:

| Term | What it means |
|------|---------------|
| **Organization** | Your company's Adobe org. The same org you use in Fusion. |
| **Project** | A container for one app/extension. You will create one project for your extension. |
| **Workspace** | A copy of the project's configuration for a stage of work. Every project has a **Production** workspace, and you typically also use a **Stage** workspace for testing. Think of workspaces like "environments." |
| **Credentials / Services** | Permissions your app is allowed to use. The defaults created for you are enough to start. |

You have two ways to create the project:

- **Recommended (automatic):** let `aio app init` create the project and
  workspaces for you while generating the code. This is what the next page does.
- **Manual:** create the project yourself in the Developer Console first
  (**Create new project → Add App Builder**), then point `aio` at it. Only do
  this if your organization requires projects to be created centrally.

> **Which workspace should I use?** Start in **Stage**. Fusion discovers
> Stage-published extensions during development and testing. You promote to
> **Production** later. See [Publish your extension](./07-publish.md).

## Step 5 — Confirm your active org (optional but recommended)

Check which organization the CLI is pointed at:

```sh
aio console org list      # see organizations you can use
aio console where         # see your currently selected org/project/workspace
```

If you belong to several organizations, select the correct one:

```sh
aio console org select
```

You are now ready to create the project.

Next: [Create the project →](./03-create-project.md)