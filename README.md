# Serverless Issue #9565 Repro

https://github.com/serverless/serverless/issues/9565

## How to reproduce the issue:

Checkout the repo

```bash
$ yarn install
# You might need to run this a few times since it is a race condition
# and might not happen _every_ time
$ yarn build-all
```

### Expected

It always works

### Actual

```
➤ YN0000:  Error ---------------------------------------------------
➤ YN0000:
➤ YN0000:   Error: dest already exists.
➤ YN0000:       at /var/home/seandawson/Development/work/ai-media/serverless-issue-9565-repro/node_modules/fs-extra/lib/move/move.js:41:31
➤ YN0000:       at /var/home/seandawson/Development/work/ai-media/serverless-issue-9565-repro/node_modules/universalify/index.js:22:54
➤ YN0000:
➤ YN0000:      For debugging logs, run again after setting the "SLS_DEBUG=*" environment variable.
➤ YN0000:
➤ YN0000:   Get Support --------------------------------------------
➤ YN0000:      Docs:          docs.serverless.com
➤ YN0000:      Bugs:          github.com/serverless/serverless/issues
➤ YN0000:      Issues:        forum.serverless.com
➤ YN0000:
➤ YN0000:   Your Environment Information ---------------------------
➤ YN0000:      Operating System:          linux
➤ YN0000:      Node Version:              12.20.1
➤ YN0000:      Framework Version:         2.44.0 (local)
➤ YN0000:      Plugin Version:            5.2.0
➤ YN0000:      SDK Version:               4.2.3
➤ YN0000:      Components Version:        3.11.0
```
