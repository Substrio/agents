---
name: substrio
description: Build, test, and ship apps on Substrio for your owner. Use it when your owner asks for an app, a site, a backend, a database, sign-in, mail, or a deploy on Substrio, or when a task names substrio.com or a *.substrio.com address.
---

# Building on Substrio

Substrio is an app platform. Your owner's account holds their apps, and each app comes with a host, data, functions, files, users, and a site. This plugin connects you to Substrio's tools at `https://mcp.substrio.com/mcp`.

## Connect

The first time you call a Substrio tool, your owner signs in once in their browser and approves the connection. There is no key to store, and you never see one. If a call answers that sign-in is needed, tell your owner to finish it in the browser window that opened, then repeat the call.

## Read the guide before you build

The full guide is short, and it covers sign-in, roles, mail, maps, files, and schedules. Read it whole before your first change. A fetch tool that summarizes a page leaves most of it out, so read the raw text:

```
curl -s https://substrio.com/agents.md
curl -s https://mcp.substrio.com/llms.txt
```

## The build loop

In a project folder, the CLI runs the whole loop:

```
npx -y @substrio/cli@latest init --tenant my-app --yes
npx -y @substrio/cli@latest dev
npx -y @substrio/cli@latest push -m "first version"
npx -y @substrio/cli@latest promote
```

`push` runs the new version on the app's dev sandbox only. The live app changes when you run `promote`, and `rollback` puts the previous version back.

## Your owner approves some calls

Writing a secret, starting a jet, deleting an app, and attaching a domain each wait for your owner. Such a call answers `APPROVAL_REQUIRED` with an `approve_url`. Tell your owner what the call does and give them the link. Once they approve, repeat the same call.
