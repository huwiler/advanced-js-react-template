
# Scripts
This folder is for build and deployment scripts that support your project.

You are encouraged to use an AI coding assistant (e.g. Codex, Gemini Code Assist, Claude Code, Cursor, or GitHub Copilot) to help generate scripts tailored to your operating system, your shell, and your deployment environment.

Important: Protect your SSH private key and never put it inside this repo. Store it in your user profile and reference it by path. Common locations:

- Windows: `C:\Users\<username>\.ssh\starfruit-key.pem`
- Linux: `/home/<username>/.ssh/starfruit-key.pem` or `~/.ssh/starfruit-key.pem`

Keep private keys out of version control and do not share them.

Example 1: Creating an SSH script

Once you have your key downloaded locally, you can make signing in via ssh easy with a simple ssh wrapper that AI can generate for you. Here's a prompt:

"Create a wrapper script for the command ssh -i ~/.ssh/starfruit-key.pem \<username>@starfruit.champlain.edu so I don't have to type this in every time I want to ssh.  Place the script here: scripts/ssh-starfruit"

---

Example 2: Creating a Website Publish Script

Once you have your Vite website running locally, you can create a script to build and deploy it. Here’s an example prompt you might provide to your AI assistant:

"Create a website publish script scripts/publish-website that does the following: (a) builds Vite site by running npm run build in website/, (b) deploys to \<username>@starfruit.champlain.edu:/home/\<username>/public_html/ using the ssh key located at ~/.ssh/starfruit-key.pem".

Feel free to adapt this prompt to your environment (Windows, macOS, or Linux) and your preferred scripting language (Bash, PowerShell, or others).
