# cs2-rcon-action

Execute RCON commands on a CS2 server. Based on https://github.com/gorcon/rcon-cli.

## Example usage

```yaml
name: Execute RCON command

on:
  workflow_dispatch:

jobs:
  execute:
    runs-on: ubuntu-latest
    steps:
      - name: Execute command
        uses: milesizzo/cs2-rcon-action@v1
        with:
          host: ${{ secrets.CS2_RCON_HOST }}
          port: ${{ secrets.CS2_RCON_PORT }}
          password: ${{ secrets.CS2_RCON_PASSWORD }}
          command: "status"
```

## Input parameters

Note: all parameters are required.

Input | Description
--- | ---
`host` | RCON server host
`port` | RCON server port
`password` | RCON password
`command` | Command to execute

