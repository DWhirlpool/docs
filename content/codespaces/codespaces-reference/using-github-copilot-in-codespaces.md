---
title: Using GitHub Copilot in Codespaces
intro: You can use Copilot in Codespaces by adding the extension.
versions:
  fpt: '*'
  ghec: '*'
type: reference
topics:
  - Codespaces
  - Copilot
  - Visual Studio Code
product: '{% data reusables.gated-features.codespaces %}'
shortTitle: Copilot in Codespaces
redirect_from:
  - /codespaces/codespaces-reference/using-copilot-in-codespaces
---

## Using {% data variables.product.prodname_copilot %}

[{% data variables.product.prodname_copilot %}](https://copilot.github.com/), an AI pair programmer, can be used in any codespace. To start using {% data variables.product.prodname_copilot_short %} in {% data variables.product.prodname_codespaces %}, install the [{% data variables.product.prodname_copilot_short %} extension from the {% data variables.product.prodname_vscode_marketplace %}](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot).

To include {% data variables.product.prodname_copilot_short %}, or other extensions, in all of your codespaces, enable Settings Sync. For more information, see "[Personalizing {% data variables.product.prodname_codespaces %} for your account](/codespaces/customizing-your-codespace/personalizing-codespaces-for-your-account#settings-sync)." Additionally, to include {% data variables.product.prodname_copilot_short %} in a given project for all users, you can specify `GitHub.copilot` as an extension in your `devcontainer.json` file like this:
```json
// For format details, see https://aka.ms/devcontainer.json. For config options, see the README at:
// https://github.com/microsoft/vscode-dev-containers/tree/v0.236.0/containers/javascript-node
{
	"name": "Node.js",
	"build": {
		"dockerfile": "Dockerfile",
		// Update 'VARIANT' to pick a Node version: 18, 16, 14.
		// Append -bullseye or -buster to pin to an OS version.
		// Use -bullseye variants on local arm64/Apple Silicon.
		"args": { "VARIANT": "16-bullseye" }
	},

	// Configure tool-specific properties.
	"customizations": {
		// Configure properties specific to VS Code.
		"vscode": {
			// Add the IDs of extensions you want installed when the container is created.
			"extensions": [
				"GitHub.copilot"
			]
		}
	},

	// Use 'forwardPorts' to make a list of ports inside the container available locally.
	// "forwardPorts": [],

	// Use 'postCreateCommand' to run commands after the container is created.
	// "postCreateCommand": "yarn install",

	// Comment out to connect as root instead. More info: https://aka.ms/vscode-remote/containers/non-root.
	"remoteUser": "node",
	"features": {
		"docker-in-docker": "latest",
		"docker-from-docker": "latest",
		"kubectl-helm-minikube": "latest",
		"terraform": "latest",
		"git": "latest",
		"git-lfs": "latest",
		"github-cli": "latest",
		"aws-cli": "latest",
		"azure-cli": "latest",
		"sshd": "latest",
		"desktop-lite": "latest",
		"homebrew": "latest",
		"fish": "latest",
		"python": "latest",
		"golang": "latest",
		"java": "lts",
		"maven": "latest",
		"gradle": "latest",
		"ruby": "latest",
		"rust": "latest",
		"powershell": "latest",
		"dotnet": "latest"
	}
}
```
. For information about configuring a `devcontainer.json` file, see "[Introduction to dev containers](/codespaces/customizing-your-codespace/configuring-codespaces-for-your-project#creating-a-custom-dev-container-configuration)."

