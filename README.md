# Slack local docker bot
Based on https://github.com/rockymadden/slack-cli

The idea is to:

* isolate the Slack bot in a Docker container (can run anywhere and is somewhat sandboxed from your dev environments)
* be able to run multiple instances for different Slack bots / accounts / spaces
* have simple local aliases like `slack dev-update "Doing the deploy"`

## Installation

1. Choose a name for the Docker image, say 'dev'
1. Build the image with this name: `./slack-cli.sh init dev`
1. Add an alias to your .bashrc / .zshrc etc:

   ```
   # Say something in the #dev channel
   alias slack-say-dev "docker run slack-say-dev:latest slack chat send --channel '#dev'"
   ```

