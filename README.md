# Description
`counterparty-classic-xcp-proxy` is a websockets proxy for all the Counterparty Classic subsystems.

# Installation
For a simple Docker-based install of the Counterparty Classic software stack, see [this guide](https://github.com/jdogresorg/counterparty-classic-fednode).

Manual installation can be done by:

```bash
git clone https://github.com/jdogresorg/counterparty-classic-xcp-proxy
cd counterparty-classic-xcp-proxy
npm install
npm start
```

The server expects several environment variables to point at the respective backend servers.

The available environment variables along with their defaults are:

```bash
SECRETS_PATH=./
HTTP_PORT=8097
ADDRINDEXRS_URL=tcp://localhost:8432
COUNTERPARTY_URL=http://rpc:rpc@localhost:4000
BITCOIN_ZMQ_URL=tcp://localhost:28832
REDIS_URL=redis://localhost:6379/8
SESSION_SECRET=configure this!
INTERVAL_CHECK_COUNTERPARTY_PARSED=1000
```

You can include them in a `secrets` file and point it by setting the SECRETS_PATH
environment variable to it.

# License
Read LICENSE
