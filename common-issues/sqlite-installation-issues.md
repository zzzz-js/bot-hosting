---
description: Are you having issues with your Sqlite database dependency installing?
---

# SQLite Installation Issues

This is normally caused by the build uploaded to your server not being correct for it's operating system. This is a simple issue to resolve on `Node.js`, simply deleted the `node_modules` folder in your server's files and restart to force Sqlite to reinstall and download the correct build.
